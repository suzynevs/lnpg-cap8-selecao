//C
int j = -3;
int i = 0;

while (i < 3 && j <= 0) {
    int val = j + 2;

    if (val == 3 || val == 2) {
        j--;
    } else if (val == 0) {
        j += 2;
    } else {
        j = 0;
    }

    if (j <= 0) {
        j = 3 - i;
        i++;
    }
}

//PYTHON
j = -3
i = 0

while i < 3 and j <= 0:
    val = j + 2

    if val in (2, 3):
        j -= 1
    elif val == 0:
        j += 2
    else:
        j = 0

    if j <= 0:
        j = 3 - i
        i += 1

//ERLANG
loop(I, J) when I >= 3; J > 0 ->
    J;

loop(I, J) ->
    Val = J + 2,
    J1 =
        case Val of
            3 -> J - 1;
            2 -> J - 1;
            0 -> J + 2;
            _ -> 0
        end,
    case J1 > 0 of
        true -> J1;
        false -> loop(I + 1, 3 - I)
    end.
