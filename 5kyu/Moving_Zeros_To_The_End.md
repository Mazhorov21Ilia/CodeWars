# Задача:
Write an algorithm that takes an array and moves all of the zeros to the end, preserving the order of the other elements.

## Пример
```
move_zeros([1, 0, 1, 2, 0, 1, 3]) # returns [1, 1, 2, 1, 3, 0, 0]
```
# Решение:

```
lst = [1, 0, 1, 2, 0, 1, 3]
def move(lst):
    q = lst.count(0)
    for i in range(q):
        lst.remove(0)
        lst.append(0)
    return lst
```