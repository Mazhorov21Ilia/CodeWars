# Задача:
Define a regular expression which tests if a given string representing a binary number is divisible by 5.

## Пример:

```
# 5 divisible by 5
PATTERN.match('101') == true

# 135 divisible by 5
PATTERN.match('10000111') == true

# 666 not divisible by 5
PATTERN.match('0000001010011010') == false
```

# Решение:
[Статья](https://stackoverflow.com/questions/34476333/regular-expression-for-binary-numbers-divisible-by-5) на хабре

```
# Выражение моделирует состояния конечного автомата (Finite State Machine), для делимости на 5
PATTERN = r'^(0|1(10)*(0|11)(01*0(1|(01)*(00|1)))*1)+$'
```