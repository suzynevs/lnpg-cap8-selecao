j = -3;
int continuar = 1;

for (i = 0; i < 3 && continuar; i++) {
    switch (j + 2) {
        case 3:
        case 2:
            j--;
            break;
        case 0:
            j += 2;
            break;
        default:
            j = 0;
    }

    if (j > 0) {
        continuar = 0;
    } else {
        j = 3 - i;
    }
}
