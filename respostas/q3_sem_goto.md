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

//ASSEMBLY
; j = -3
MOV j, -3

; i = 0
MOV i, 0

LOOP_START:
    ; if (i >= 3 || j > 0) -> sair
    CMP i, 3
    JGE LOOP_END

    CMP j, 0
    JG LOOP_END

    ; val = j + 2
    MOV val, j
    ADD val, 2

    ; if (val == 2 || val == 3)
    CMP val, 2
    JE CASE_DEC
    CMP val, 3
    JE CASE_DEC

    ; else if (val == 0)
    CMP val, 0
    JE CASE_ADD

    ; default: j = 0
    MOV j, 0
    JMP AFTER_SWITCH

CASE_DEC:
    ; j--
    SUB j, 1
    JMP AFTER_SWITCH

CASE_ADD:
    ; j += 2
    ADD j, 2

AFTER_SWITCH:
    ; if (j > 0) sair
    CMP j, 0
    JG LOOP_END

    ; j = 3 - i
    MOV j, 3
    SUB j, i

    ; i++
    ADD i, 1

    JMP LOOP_START

LOOP_END:
