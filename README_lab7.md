# Домашнее задание к работе 7

## Условие задачи

Создать программу с использованием оператора выбора `switch`: определение типа введенного символа (цифра, латинская буква или иной символ), простой калькулятор четырех арифметических действий, а также индивидуальное задание (вывод порядкового номера заглавной буквы латинского алфавита).

## Алгоритм и блок-схема

### Алгоритм

1. Начало
2. Функция `task_one`:
   - Ввод символа `c`.
   - Проверка с помощью оператора `switch` на принадлежность к цифрам ('0'-'9'), буквам ('A'-'Z', 'a'-'z') или неизвестным символам.
   - Вывод соответствующего сообщения.
3. Функция `task_two`:
   - Ввод операндов `x`, `y` и математического знака операции `c` ('+', '-', '*', '/').
   - Выполнение арифметической операции через `switch`.
   - Вывод полного математического выражения и результата.
4. Функция `homework_or_individual_assignment`:
   - Ввод заглавной латинской буквы.
   - Определение ее порядкового номера (от 1 до 26) с использованием `switch`.
   - Вывод номера буквы.
5. Функция `main`: вызов всех задач.
6. Конец

### Блок-схема

<img width="1024" height="733" alt="image" src="https://github.com/user-attachments/assets/b3f8a9ec-d3c2-496b-9c96-8c9b909ad1dd" />


## Реализация программы

```c
#include <stdio.h>
#include <stdlib.h>
#include <locale.h>
#include <math.h>
#define _USE_MATH_DEFINES
task_one();
task_two();
homework_or_individual_assignment();
int main() {
    task_one();
    task_two();
    homework_or_individual_assignment();
}
int task_one() {
    puts("TASK ONE----------------------------------------------------------------------------------------------------------------");
    char c;
    printf("Enter the number or symbol:\n");
    scanf_s("%c", &c, 1);
    switch (c) {
    case '0': case '1': case '2': case '3': case '4':
    case '5': case '6': case '7': case '8': case '9':
        printf("This number\n");
        break;
    case 'A': case 'B': case 'C': case 'D': case 'E': case 'F': case 'G': case 'H': case 'I': case 'J': case 'K': case 'L': case 'M':
    case 'N': case 'O': case 'P': case 'Q': case 'R': case 'S': case 'T': case 'U': case 'V': case 'W': case 'X': case 'Y': case 'Z':
    case 'a': case 'b': case 'c': case 'd': case 'e': case 'f': case 'g': case 'h': case 'i': case 'j': case 'k': case 'l': case 'm':
    case 'n': case 'o': case 'p': case 'q': case 'r': case 's': case 't': case 'u': case 'v': case 'w': case 'x': case 'y': case 'z':
        printf("This symbol\n");
        break;
    default:
        printf("Unknown symbol (Not number and not symbol)\n");
        break;
    }
    return 0;
}
int task_two() {
    puts("TASK TWO----------------------------------------------------------------------------------------------------------------");
    double x, y, z = 0;
    char c;
    printf("Enter the numbers and operation:");
    scanf_s("%lf %c %lf", &x, &c, 1, &y);
    switch (c) {
    case '+': z = x + y; break;
    case '-': z = x - y; break;
    case '*': z = x * y; break;
    case '/': z = x / y; break;
    default: printf("Please enter mathematical symbol, not another\n");
    }
    printf("%lf %c %lf = %lf\n", x, c, y, z);
}
int homework_or_individual_assignment() {
    puts("HOMEWORK----------------------------------------------------------------------------------------------------------------");
    char c = 0;
    puts("Enter letter:");
    scanf_s(" %c", &c);
    switch (c) {
    case 'A': printf("This is letter 1\n"); break;
    case 'B': printf("This is letter 2\n"); break;
    case 'C': printf("This is letter 3\n"); break;
    case 'D': printf("This is letter 4\n"); break;
    case 'E': printf("This is letter 5\n"); break;
    case 'F': printf("This is letter 6\n"); break;
    case 'G': printf("This is letter 7\n"); break;
    case 'H': printf("This is letter 8\n"); break;
    case 'I': printf("This is letter 9\n"); break;
    case 'J': printf("This is letter 10\n"); break;
    case 'K': printf("This is letter 11\n"); break;
    case 'L': printf("This is letter 12\n"); break;
    case 'M': printf("This is letter 13\n"); break;
    case 'N': printf("This is letter 14\n"); break;
    case 'O': printf("This is letter 15\n"); break;
    case 'P': printf("This is letter 16\n"); break;
    case 'Q': printf("This is letter 17\n"); break;
    case 'R': printf("This is letter 18\n"); break;
    case 'S': printf("This is letter 19\n"); break;
    case 'T': printf("This is letter 20\n"); break;
    case 'U': printf("This is letter 21\n"); break;
    case 'V': printf("This is letter 22\n"); break;
    case 'W': printf("This is letter 23\n"); break;
    case 'X': printf("This is letter 24\n"); break;
    case 'Y': printf("This is letter 25\n"); break;
    case 'Z': printf("This is letter 26\n"); break;
    default: printf("Incorrect symbol\n");
    }
}
```

## Результаты работы программы

```text
TASK ONE----------------------------------------------------------------------------------------------------------------
Enter the number or symbol:
7
This number
TASK TWO----------------------------------------------------------------------------------------------------------------
Enter the numbers and operation:10 + 5
10.000000 + 5.000000 = 15.000000
HOMEWORK----------------------------------------------------------------------------------------------------------------
Enter letter:
A
This is letter 1
```

## Информация о разработчике

Панарин Егор БИД-261
