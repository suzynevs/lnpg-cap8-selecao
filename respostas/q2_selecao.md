//C
switch (k) {
    case 1:
    case 2:
        j = 2 * k - 1;
        break;

    case 3:
    case 5:
        j = 3 * k + 1;
        break;

    case 4:
        j = 4 * k - 1;
        break;

    case 6:
    case 7:
    case 8:
        j = k - 2;
        break;
}

//RUBY
case k
when 1, 2
  j = 2 * k - 1
when 3, 5
  j = 3 * k + 1
when 4
  j = 4 * k - 1
when 6, 7, 8
  j = k - 2
end

//ERLANG
j =
  case k of
    1 -> 2 * k - 1;
    2 -> 2 * k - 1;
    3 -> 3 * k + 1;
    5 -> 3 * k + 1;
    4 -> 4 * k - 1;
    6 -> k - 2;
    7 -> k - 2;
    8 -> k - 2
  end.

  
