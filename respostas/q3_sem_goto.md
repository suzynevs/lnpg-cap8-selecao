//PYTHON
j = -3
i = 0
continuar = True

while i < 3 and continuar:
    if j + 2 == 3 or j + 2 == 2:
        j -= 1
    elif j + 2 == 0:
        j += 2
    else:
        j = 0

    if j > 0:
        continuar = False
    else:
        j = 3 - i

    i += 1

//JAVA
int j = -3;
boolean continuar = true;

for (int i = 0; i < 3 && continuar; i++) {
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
        continuar = false;
    } else {
        j = 3 - i;
    }
}

//JAVASCRIPT
let j = -3;
let continuar = true;

for (let i = 0; i < 3 && continuar; i++) {
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
        continuar = false;
    } else {
        j = 3 - i;
    }
}
