# Тема 8. Основы объектно-ориентированного программирования
Отчет по Теме #8 выполнил:
- Кайгородов Олег Юрьевич
- ПИЭ-22-1

| Задание | Лаб_раб | Сам_раб |
| ------ |---------|---------|
| Задание 1 | +       | +       |
| Задание 2 | +       | +       |
| Задание 3 | +       | +       |
| Задание 4 | +       | +       |
| Задание 5 | +       | +       |

знак "+" - задание выполнено; знак "-" - задание не выполнено;

Работу проверили:
- к.э.н., доцент Панов М.А.

## Лабораторная работа №1
### Создайте класс “Car” с атрибутами производитель и модель. Создайте
### объект этого класса. Напишите комментарии для кода, объясняющие
### его работу. Результатом выполнения задания будет листинг кода с
### комментариями.

```python
class Car:
    def __init__(self, make, model):
        self.make = make
        self.model = model

my_car = Car("Toyota", "Corolla")
```
### Результат.

![Меню](https://github.com/pipsowich/SoftwareEngineering/blob/Tema_8/Imagies/8_1.png)

### Выводы

Создали класс “Car” с атрибутами производитель и модель.

## Лабораторная работа №2
### Дополните код из первого задания, добавив в него атрибуты и методы
### класса, заставьте машину “поехать”. Напишите комментарии для кода, объясняющие его работу. Результатом выполнения задания будет
### листинг кода с комментариями и получившийся вывод в консоль.

```python
class Car:
    def __init__(self, make, model):
        self.make = make
        self.model = model

    def drive(self):
        print(f"Driving the {self.make} {self.model}")

my_car = Car("Toyota", "Corolla")
my_car.drive()
```
### Результат.

![Меню](https://github.com/pipsowich/SoftwareEngineering/blob/Tema_8/Imagies/8_2.png)

### Выводы

добавили метод drive

## Лабораторная работа №3
### Создайте новый класс “ElectricCar” с методом “charge” и атрибутом
### емкость батареи. Реализуйте его наследование от класса, созданного в
### первом задании. Заставьте машину поехать, а потом заряжаться.
### Результатом выполнения задания будет листинг кода с комментариями
### и получившийся вывод в консоль.

```python
class Car:
    def __init__(self, make, model):
        self.make = make
        self.model = model

    def drive(self):
        print(f"Driving the {self.make} {self.model}")
my_car = Car("Toyota", "Corolla")
my_car.drive()
class ElectricCar(Car):
    def __init__(self, make, model, battery_capacity):
        super().__init__(make, model)
        self.battery_capacity = battery_capacity

    def charge(self):
        print(f"Charging the {self.make} {self.model} with {self.battery_capacity} kWh")

my_electric_car = ElectricCar("Tesla", "Model S", 75)
my_electric_car.drive()
my_electric_car.charge()
```
### Результат.

![Меню](https://github.com/pipsowich/SoftwareEngineering/blob/Tema_8/Imagies/8_3.png)

### Выводы

Создали новый класс “ElectricCar” с методом “charge” и атрибутом емкость батареи
  
## Лабораторная работа №4
### Реализуйте инкапсуляцию для класса, созданного в первом задании.
### Создайте защищенный атрибут производителя и приватный атрибут
### модели. Вызовите защищенный атрибут и заставьте машину поехать.
### Напишите комментарии для кода, объясняющие его работу.
### Результатом выполнения задания будет листинг кода с комментариями
### и получившийся вывод в консоль.


```python
class Car:
    def __init__(self, make, model):
        self._make = make
        self.__model = model

    def drive(self):
        print(f"Driving the {self._make} {self.__model}")

my_car = Car("Toyota", "Corolla")

print(my_car._make)
my_car.drive()
```
### Результат.

![Меню](https://github.com/pipsowich/SoftwareEngineering/blob/Tema_8/Imagies/8_4.png)

### Выводы

добавили инкапсуляцию, сделав атрибуты приватными

## Лабораторная работа №5
### Реализуйте полиморфизм создав основной (общий) класс “Shape”, а
### также еще два класса “Rectangle” и “Circle”. Внутри последних двух
### классов реализуйте методы для подсчета площади фигуры. После этого
### создайте массив с фигурами, поместите туда круг и прямоугольник, затем при помощи цикла выведите их площади. Напишите
### комментарии для кода, объясняющие его работу. Результатом
### выполнения задания будет листинг кода с комментариями и
### получившийся вывод в консоль.



```python
class Shape:
    def area(self):
        pass

class Rectangle(Shape):
    def __init__(self, width, height):
        self.width = width
        self.height = height

    def area(self):
        return self.width * self.height

class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return 3.14 * self.radius * self.radius

my_rectangle = Rectangle(3, 4)
my_circle = Circle(3)

print(my_rectangle.area())
print(my_circle.area())
```
### Результат.

![Меню](https://github.com/pipsowich/SoftwareEngineering/blob/Tema_8/Imagies/8_5.png)

### Выводы

добавили два класса наследника, где переопределили метод area, таким образом применив полиморфизм

## Самостоятельная работа №1
### Самостоятельно создайте класс и его объект. Они должны
### отличаться, от тех, что указаны в теоретическом материале
### (методичке) и лабораторных заданиях. Результатом выполнения
### задания будет листинг кода и получившийся вывод консоли.

```python
class Hero:
    def __init__(self, dmg):
        self.dmg = dmg

    def Damage(self):
        return self.dmg

hero = Hero(500)
print(hero.Damage())
```
### Результат.

![Меню](https://github.com/pipsowich/SoftwareEngineering/blob/Tema_8/Imagies/8_6.png)

### Выводы

1. `class Hero:` создаем класс Hero
2. `def __init__(self, dmg):` конструктор класса
3. `hero = Hero(500)` создаем объект класса
  
## Самостоятельная работа №2
### Самостоятельно создайте атрибуты и методы для ранее созданного
### класса. Они должны отличаться, от тех, что указаны в
### теоретическом материале (методичке) и лабораторных заданиях.
### Результатом выполнения задания будет листинг кода и
### получившийся вывод консоли.

```python
class Hero:
    def __init__(self, dmg, golos):
        self.dmg = dmg
        self.golos = golos

    def Damage(self):
        return self.dmg

    def Golos(self):
        return self.golos

hero = Hero(500, "Hero Never die")
print(hero.Damage())
print(hero.Golos())
```
### Результат.

![Меню](https://github.com/pipsowich/SoftwareEngineering/blob/Tema_8/Imagies/8_7.png)

### Выводы

1. `def __init__(self, dmg, golos):` добавил атрибут golos
2. `def Golos(self):` добавил метод Golos, который возвращает golos
  
## Самостоятельная работа №3
### Самостоятельно реализуйте наследование, продолжая работать с
### ранее созданным классом. Оно должно отличаться, от того, что
### указано в теоретическом материале (методичке) и лабораторных
### заданиях. Результатом выполнения задания будет листинг кода и
### получившийся вывод консоли.


```python
class Hero:
    def __init__(self, dmg):
        self.dmg = dmg
        self.golos = "Hero Never die"

    def Damage(self):
        return self.dmg

    def Golos(self):
        return self.golos

class Skopos(Hero):
    def __init__(self, dmg):
        super().__init__(dmg)
        self.golos = "Oh my god!"
hero = Hero(500)
skopos = Skopos(12)
print(hero.Golos())
print(skopos.Golos())
```
### Результат.

![Меню](https://github.com/pipsowich/SoftwareEngineering/blob/Tema_8/Imagies/8_8.png)

### Выводы

1. `class Skopos(Hero):` создаем класс Skopos у наследуемый от класса Hero
2. `super().__init__(dmg)` передаем аргумент в конструктор родительского класса
3. `self.golos = "Oh my god!"` переопределяем golos 
4. `skopos = Skopos(12)` создаем объект класса Skopos
  
## Самостоятельная работа №4
### Самостоятельно реализуйте инкапсуляцию, продолжая работать с
### ранее созданным классом. Она должна отличаться, от того, что
### указана в теоретическом материале (методичке) и лабораторных
### заданиях. Результатом выполнения задания будет листинг кода и
### получившийся вывод консоли.

```python
class Hero:
    def __init__(self, dmg):
        self.__dmg = dmg
        self.golos = "Hero Never die"

    def Damage(self):
        return self.__dmg

    def Golos(self):
        return self.golos

    def set_damage(self, new_dmg):
        if new_dmg >= 50:
            self.__dmg = new_dmg
        else:
            print("Слабенький")

class Skopos(Hero):
    def __init__(self, dmg):
        super().__init__(dmg)
        self.golos = "Oh my god!"
hero = Hero(500)
skopos = Skopos(12)
print(hero.Golos())
print(skopos.Golos())

print(hero.Damage())
hero.set_damage(100)
print(hero.Damage())
hero.set_damage(42)
```
### Результат.

![Меню](https://github.com/pipsowich/SoftwareEngineering/blob/Tema_8/Imagies/8_9.png)

### Выводы

1. `self.__dmg = dmg` делаем dmg приватным
2. `def Damage(self)` добавляем геттер
3. `def set_damage(self, new_dmg):` добавляем сеттер
  
## Самостоятельная работа №5
### Самостоятельно реализуйте полиморфизм. Он должен отличаться, от того, что указан в теоретическом материале (методичке) и
### лабораторных заданиях. Результатом выполнения задания будет
### листинг кода и получившийся вывод консоли.

```python
class Hero:
    def __init__(self, dmg):
        self.__dmg = dmg

    def Damage(self):
        return self.__dmg

    def Golos(self):
        return "Hero Never die"

    def set_damage(self, new_dmg):
        if new_dmg >= 50:
            self.__dmg = new_dmg
        else:
            print("Слабенький")

class Skopos(Hero):
    def __init__(self, dmg):
        super().__init__(dmg)
    def Golos(self):
        return "Oh my god!"
class Bandit (Hero):
    def __init__(self,dmg):
        super().__init__(dmg)

    def Golos(self):
        return "Privet"
heroes = [Hero(100), Skopos(34), Bandit(211)]

for hero in heroes:
    print(hero.Golos()) 
```

### Результат.

![Меню](https://github.com/pipsowich/SoftwareEngineering/blob/Tema_8/Imagies/8_10.png)

### Выводы

переопределяем метод Golos в Skopos и Bandit, таким образом получаем полиморфизм

## Общие выводы по теме
Базово освоил работу в ооп стиле на python. А если точнее познакомился с классами, их конструкторами, полиморфизмом и инкапсуляцией, а также наследованием
