
# Тема 4. Функции и модули
Отчет по Теме #4 выполнил:
- Кайгородов Олег Юрьевич
- ПИЭ-22-1

| Задание | Лаб_раб | Сам_раб |
| ------ |---------|---------|
| Задание 1 | +       | +       |
| Задание 2 | +       | +       |
| Задание 3 | +       | +       |
| Задание 4 | +       | +       |
| Задание 5 | +       | +       |
| Задание 6 | +       | -       |
| Задание 7 | +       | -       |
| Задание 8 | +       | -       |
| Задание 9 | +       | -       |
| Задание 10 | +       | -       |

знак "+" - задание выполнено; знак "-" - задание не выполнено;

Работу проверили:
- к.э.н., доцент Панов М.А.

## Лабораторная работа №1
### Напишите функцию, которая выполняет любые арифметические действия и выводит результат в консоль. Вызовите функцию используя “точку входа”.

```python
def main():
    print(2*9)

if __name__ == '__main__':
    main()
```
### Результат.

![Меню](https://github.com/pipsowich/SoftwareEngineering/blob/Tema_4/Imagies/%D0%BB4_1.png)

### Выводы
`if __name__ == '__main__':` точка входа
## Лабораторная работа №2
### Напишите функцию, которая выполняет любые арифметические действия, возвращает при помощи return значение в место, откуда вызывали функцию. Выведите результат в консоль. Вызовите функцию используя “точку входа”.

```python
def main():
    return 3*9

if __name__ == ('__main__'):
    print(main())
```
### Результат.

![Меню](https://github.com/pipsowich/SoftwareEngineering/blob/Tema_4/Imagies/%D0%BB4_2.png)

### Выводы
`if __name__ == '__main__':` точка входа
## Лабораторная работа №3
### Напишите функцию, в которую передаются два аргумента, над ними производится арифметическое действие, результат возвращается туда, откуда эту функцию вызывали. Выведите результат в консоль. Вызовите функцию в любом небольшом цикле.

```python
def main(one, two):
    result = one + two
    return result

for i in range(5):
    x=1
    y=10
    answer = main(x,y)
    print(answer)
```
### Результат.

![Меню](https://github.com/pipsowich/SoftwareEngineering/blob/Tema_4/Imagies/%D0%BB4_3.png)

### Выводы
`def main(one, two):` функция с двумя аргументами  
## Лабораторная работа №4
### Напишите функцию, на вход которой подается какое-то изначальное неизвестное количество аргументов, над которыми будет производится арифметические действия. Для выполнения задания необходимо использовать кортеж “*args”. 

```python
def main(x, *args):
    one = x
    two = sum(args)
    three = float(len(args))

    print(f"one={one}\ntwo={two}\nthree={three}")

    return x+sum(args) / float(len(args))


if __name__ == '__main__':
    result = main(10,0,1,2,-1,0,-1,1,2)
print(f"\nresult={result}")
```
### Результат.

![Меню](https://github.com/pipsowich/SoftwareEngineering/blob/Tema_4/Imagies/%D0%BB4_4.png)

### Выводы
`def main(x, *args):` функция с двумя аргументами, второй аргумент массив 

## Лабораторная работа №5
### Напишите функцию, которая на вход получает кортеж “**kwargs” и при помощи цикла выводит значения, поступившие в функцию. На скриншоте ниже указаны два варианта вызова функции с “**kwargs” и два варианта работы с данными, поступившими в эту функцию. Комментарии в коде и теоретическая часть помогут вам разобраться в этом нелегком аспекте. Вызовите функцию используя “точку входа”.

```python
def main(**kwargs):
    for i in kwargs.items():
        print(i[0], i[1])
    print()

    for key in kwargs:
        print(f"{key} = {kwargs[key]}")

if __name__ == '__main__':
    main(x=[1,2,3], y=[3,3,0], z=[2,3,0], q=[3,3,0], w=[3,3,0])
    print()

    main(**{'x': [1,2,3], 'y':[3,3,0]})
```
### Результат.

![Меню](https://github.com/pipsowich/SoftwareEngineering/blob/Tema_4/Imagies/%D0%BB4_5.png)

### Выводы
1. `def main(**kwargs):` функция с картежом в качестве аргумента
2. `for i in kwargs.items():` проходимся по предметам
3. `for key in kwargs:` проходимся по ключам

## Лабораторная работа №6
### Напишите две функции. Первая – получает в виде параметра “**kwargs”. Вторая считает среднее арифметическое из значений первой функции. Вызовите первую функцию используя “точку входа” и минимум 4 аргумента.

```python
def main(**kwargs):
    for i,j in kwargs.items():
        print(f"{i}. Mean = {mean(j)}")

def mean(data):

    return sum(data)/ float(len(data))

if __name__ == '__main__':
    main(x=[1,2,3], y=[3,3,0])
```
### Результат.

![Меню](https://github.com/pipsowich/SoftwareEngineering/blob/Tema_4/Imagies/%D0%BB4_6.png)

### Выводы
`def main(**kwargs):` функция с картежом в качестве аргумента
## Лабораторная работа №7
### Создайте дополнительный файл .py. Напишите в нем любую функцию, которая будет что угодно выводить в консоль, но не вызывайте ее в нем. Откройте файл main.py, импортируйте в него функцию из нового файла и при помощи “точки входа” вызовите эту функцию.

```python
from for_import import say_hello

if __name__ == '__main__':
    say_hello()
```
### Результат.

![Меню](https://github.com/pipsowich/SoftwareEngineering/blob/Tema_4/Imagies/%D0%BB4_7.png)

### Выводы
`from for_import import say_hello` импортируем наш файл и метод
## Лабораторная работа №8
### Напишите программу, которая будет выводить корень, синус, косинус полученного от пользователя числа.

```python
import math
def main():
    value = int(input())
    print(math.sqrt(value))
    print(math.sin(value))
    print(math.cos(value))
if __name__ == '__main__':
    main()
```
### Результат.

![Меню](https://github.com/pipsowich/SoftwareEngineering/blob/Tema_4/Imagies/%D0%BB4_8.png)

### Выводы
`import math` импортируем math
## Лабораторная работа №9
### Напишите программу, которая будет рассчитывать какой день недели будет через n-нное количество дней, которые укажет пользователь.

```python
from datetime import datetime as dt
from datetime import timedelta as td

def main():
    print(
        f"Сегодня{dt.today().date()}. "
        f"День недели - {dt.today().isoweekday()}"
    )
    n = int(input())
    today = dt.today()
    result = today + td(days=n)
    print(
        f"Через {n} дней будет {result.date()}"
        f"День недели - {result.isoweekday()}"
    )
if __name__ == '__main__':
    main()
```
### Результат.

![Меню](https://github.com/pipsowich/SoftwareEngineering/blob/Tema_4/Imagies/%D0%BB4_9.png)

### Выводы
производим импорт datetime и timedelta и даем им псевдонимы
## Лабораторная работа №10
### Напишите программу с использованием глобальных переменных, которая будет считать площадь треугольника или прямоугольника в зависимости от того, что выберет пользователь. Получение всей необходимой информации реализовать через input(), а подсчет площадей выполнить при помощи функций. Результатом программы будет число, равное площади, необходимой фигуры.

```python
global result
def rectangle():
    a = float(input("Ширина: "))
    b = float(input("Высота: "))
    global result
    result = a*b
def triangle():
    a = float(input("Основание: "))
    h = float(input("Высота: "))
    global result
    result = 0.5*a*h
figure = input("1 - Прямоугольник, 2 - треугольник:")
if figure == '1':
    rectangle()
elif figure == '2':
    triangle()
print(f"Площадь: {result}")
```
### Результат.

![Меню](https://github.com/pipsowich/SoftwareEngineering/blob/Tema_4/Imagies/%D0%BB4_10.png)

### Выводы
пишим две функции и вызываем их
## Самостоятельная работа №1
### Дайте подробный комментарий для кода, написанного ниже. Комментарий нужен для каждой строчки кода, нужно описать что она делает. Не забудьте, что функции комментируются по-особенному.

```python
from datetime import datetime
from math import sqrt

def main(**kwargs):
    for key in kwargs.items():
        result = sqrt(key[1][0] ** 2 + key[1][1] ** 2)
        print(result)

if __name__ == '__main__':
    start_time = datetime.now()
    main(
        one=[10, 3],
        two=[5, 4],
        three=[15, 13],
        four=[93, 53],
        five=[133, 15]
    )
    time_costs = datetime.now() - start_time
    print(f"Время выполнения программы - {time_costs}")
```
### Результат.

![Меню](https://github.com/pipsowich/SoftwareEngineering/blob/Tema_4/Imagies/%D0%BB4_11.png)

### Выводы
1.`from datetime import datetime` импорт
2.`from math import sqrt` импорт
3.`def main(**kwargs):` функция с картежом в качестве параметра
4.`for key in kwargs.items():` проходимся по предметам
5.`if __name__ == '__main__':` точка входа
6.`start_time = datetime.now()` узнаем настоящее время
7.`time_costs = datetime.now() - start_time` узнаем затраты времени вычитая из настоящего времени время старта

## Самостоятельная работа №2
### Напишите программу, которая будет заменять игральную кость с 6 гранями. Если значение равно 5 или 6, то в консоль выводится «Вы победили», если значения 3 или 4, то вы рекурсивно должны вызвать эту же функцию, если значение 1 или 2, то в консоль выводится «Вы проиграли». При этом каждый вызов функции необходимо выводить в консоль значение “кубика”. Для выполнения задания необходимо использовать стандартную библиотеку random. Программу нужно написать, используя одну функцию и “точку входа”

```python
import random
def roll_dice():
    dice_roll = random.randint(1, 6)
    print(f"Выпало число: {dice_roll}")

    if dice_roll in [5, 6]:
        print("Вы победили!")
    elif dice_roll in [3, 4]:
        roll_dice()
    else:
        print("Вы проиграли.")
if __name__ == "__main__":
    roll_dice()
```
### Результат.

![Меню](https://github.com/pipsowich/SoftwareEngineering/blob/Tema_4/Imagies/%D0%BB4_12.png)

### Выводы
`import random` импортируем random
`dice_roll = random.randint(1, 6)` получаем рандомное число от 1 до 6м
`if __name__ == '__main__':` точка входа

## Самостоятельная работа №3
### Напишите программу, которая будет выводить текущее время, с точностью до секунд на протяжении 5 секунд. Программу нужно написать с использованием цикла. Подсказка: необходимо использовать модуль datetime и time, а также вам необходимо как-то “усыплять” программу на 1 секунду.

```python
import datetime
import time

for i in range(5):
    current_time = datetime.datetime.now().strftime('%H:%M:%S')
    print(f'Current time: {current_time}')
    time.sleep(1)
```
### Результат.

![Меню](https://github.com/pipsowich/SoftwareEngineering/blob/Tema_4/Imagies/%D0%BB4_13.png)

### Выводы
`import datetime` импорт datetime
`import time` импорт time
`time.sleep(1)` усыпляем программу на 1 секунду  
## Самостоятельная работа №4
### Напишите программу, которая считает среднее арифметическое от аргументов вызываемое функции, с условием того, что изначальное количество этих аргументов неизвестно. Программу необходимо реализовать используя одну функцию и “точку входа”.

```python
def main():
    print("Введите любое количество чисел (разделяйте пробелом):")
    numbers = [float(x) for x in input().split()]
    result = sum(numbers)/len(numbers)
    print(f"Среднее арифметическое: {result:.2f}")

if __name__ == "__main__":
    main()
```
### Результат.

![Меню](https://github.com/pipsowich/SoftwareEngineering/blob/Tema_4/Imagies/%D0%BB4_14.png)

### Выводы
`*args:` - Любое количество числовых аргументов.
`def main():` - Точка входа в программу. 
## Самостоятельная работа №5
### Создайте два Python файла, в одном будет выполняться вычисление площади треугольника при помощи формулы Герона (необходимо реализовать через функцию), а во втором будет происходить взаимодействие с пользователем (получение всей необходимой информации и вывод результатов). Напишите эту программу и выведите в консоль полученную площадь.

```python
from square import square

if __name__ == '__main__':
    a = int(input())
    b = int(input())
    c = int(input())

    print(square(a, b, c))
```

```python
from math import sqrt

def square(a, b, c):
    p = (a + b + c) / 2
    return sqrt(p * (p - a) * (p - b) * (p - c))
```
### Результат.

![Меню](https://github.com/pipsowich/SoftwareEngineering/blob/Tema_4/Imagies/%D0%BB4_15.png)

### Выводы
`from square import square` импортируем наш файл и метод
## Общие выводы по теме
Научился работать в datetime, time, date, math. Научился писать свои методы, ставить точку входа.
