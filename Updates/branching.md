The break statement terminates only the loop in which it is currently located. If this loop is performed inside another loop, the outer loop won't be stopped.
The following code prints a ladder of numbers:

for (int i = 0; i < 10; i++) {
    for (int j = 0; j < 10; j++) {
        System.out.print(j + " ");
        if (i == j) {
            break;
        }
    }
    System.out.println();
}


To stop the outer loop we'd like to declare a Boolean variable stopped and use it as a special Boolean flag.

boolean stopped = false;
for (int i = 0; (i < 10) && !stopped; i++) {
    for (int j = 0; j < 10; j++) {
        System.out.print(j + " ");
        if (i == j) {
            stopped = true;
            break;
        }
     }
    System.out.println();
}

It causes a loop to skip the current iteration and go to the next one.

This statement can be used inside any kind of loops.

int n = 10;
for (int i = 0; i < n; i++) {
    if (i % 2 != 0) {
        continue;
    }
    System.out.print(i + " ");
}

int n = 10;
for (int i = 0; i < n; i++) { 
    if (i % 2 == 0) {
        System.out.print(i + " ");
    } 
}
