# Coding Challenges :: Patterns

## Square Patterns

**Pattern - 1: Square Pattern (r=4)**

```text
* * * *
* * * *
* * * *
* * * *
```

```java
public class Test {

    public static void printPattern(int rows) {
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < rows; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }

    public static void main(String[] args) {
        printPattern(4);
    }
}
```

**Pattern - 2: Rectangle Pattern (r=5, c=7)**

```text
* * * * * * *
* * * * * * *
* * * * * * *
* * * * * * *
* * * * * * *
```

```java
public class Test {

    public static void printPattern(int rows, int cols) {
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }

    public static void main(String[] args) {
        printPattern(5, 7);
    }
}
```

**Pattern - 3: Hollow Square (r=5)**

```text
* * * * *
*       *
*       *
*       *
* * * * *
```

```java
public class Test {

    public static void printPattern(int rows) {
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < rows; j++) {
                if (i == 0 || i == rows - 1) {
                    System.out.print("* ");
                } else if (j == 0 || j == rows - 1) {
                    System.out.print("* ");
                } else {
                    System.out.print("  ");
                }
            }
            System.out.println();
        }
    }

    public static void main(String[] args) {
        printPattern(5);
    }
}
```

**Pattern - 4 (r=7)**

```text
* * * * * * *
*     *     *
*     *     *
* * * * * * *
*     *     *
*     *     *
* * * * * * *
```

```java
public class Test {

    public static void printPattern(int rows) {
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < rows; j++) {
                if (i == 0 || i == rows - 1) {
                    System.out.print("* ");
                } else if (j == 0 || j == rows - 1) {
                    System.out.print("* ");
                } else if (i == rows / 2) {
                    System.out.print("* ");
                } else if (j == rows / 2) {
                    System.out.print("* ");
                } else {
                    System.out.print("  ");
                }
            }
            System.out.println();
        }
    }

    public static void main(String[] args) {
        printPattern(7);
    }
}
```

## Triangle Patterns

**Pattern - 1 (r=5)**

```text
*
* *
* * *
* * * *
* * * * *
```

```java
public class Test {

    // [Algorithm-1]
    public static void printPattern1(int rows) {
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j <= i; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }

    // [Algorithm-2]
    public static void printPattern2(int rows) {
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < rows; j++) {
                if (i >= j) {
                    System.out.print("* ");
                }
            }
            System.out.println();
        }
    }

    public static void main(String[] args) {
        System.out.println("[Algorithm-1]");
        printPattern1(5);
        System.out.println("\n[Algorithm-2]");
        printPattern2(5);
    }
}
```

**Pattern - 2 (r=5)**

```text
        *
      * *
    * * *
  * * * *
* * * * *
```

```java
public class Test {

    // [Algorithm-1]
    public static void printPattern1(int rows) {
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < rows - i - 1; j++) {
                System.out.print("  ");
            }

            for (int j = 0; j <= i; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }

    // [Algorithm-2]
    public static void printPattern2(int rows) {
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < rows; j++) {
                if (i + j >= rows - 1) {
                    System.out.print("* ");
                } else {
                    System.out.print("  ");
                }
            }
            System.out.println();
        }
    }

    // [Algorithm-3]
    public static void printPattern3(int rows) {
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < rows; j++) {
                if (j >= rows - i - 1) {
                    System.out.print("* ");
                } else {
                    System.out.print("  ");
                }
            }
            System.out.println();
        }
    }

    public static void main(String[] args) {
        System.out.println("[Algorithm-1]");
        printPattern1(5);

        System.out.println("\n[Algorithm-2]");
        printPattern2(5);

        System.out.println("\n[Algorithm-3]");
        printPattern3(5);
    }
}
```

**Pattern - 3 (r=5)**

```text
* * * * *
* * * *
* * *
* *
*
```

```java
public class Test {

    // [Algorithm-1]
    public static void printPattern1(int rows) {
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < rows - i; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }

    // [Algorithm-2]
    public static void printPattern2(int rows) {
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < rows; j++) {
                if (i <= j) {
                    System.out.print("* ");
                }
            }
            System.out.println();
        }
    }

    // [Algorithm-3]
    public static void printPattern3(int rows) {
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < rows; j++) {
                if (i + j <= rows - 1) {
                    System.out.print("* ");
                } else {
                    System.out.print("  ");
                }
            }
            System.out.println();
        }
    }

    public static void main(String[] args) {
        System.out.println("[Algorithm-1]");
        printPattern1(5);

        System.out.println("\n[Algorithm-2]");
        printPattern2(5);

        System.out.println("\n[Algorithm-3]");
        printPattern3(5);
    }
}
```

**Pattern - 4 (r=5)**

```text
* * * * *
  * * * *
    * * *
      * *
        *
```

```java
public class Test {

    // [Algorithm-1]
    public static void printPattern1(int rows) {
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < i; j++) {
                System.out.print("  ");
            }

            for (int j = 0; j < rows - i; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }

    // [Algorithm-2]
    public static void printPattern2(int rows) {
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < rows; j++) {
                if (i <= j) {
                    System.out.print("* ");
                } else {
                    System.out.print("  ");
                }
            }
            System.out.println();
        }
    }

    public static void main(String[] args) {
        System.out.println("[Algorithm-1]");
        printPattern1(5);

        System.out.println("\n[Algorithm-2]");
        printPattern2(5);
    }
}
```
