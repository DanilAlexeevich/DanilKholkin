# Тема 8. Введение в ООП 
Отчет по Теме #8 выполнил(а):
- Холкин Данил Алексеевич
- ПИЭ-22-1

| Задание | Лаб_раб | Сам_раб |
| ------ | ------ | ------ |
| Задание 1 | + | + |
| Задание 2 | + | + |
| Задание 3 | + | + |
| Задание 4 | + | + |
| Задание 5 | + | + |


знак "+" - задание выполнено; знак "-" - задание не выполнено;

Работу проверили:
- к.э.н., доцент Панов М.А.

## Лабораторная работа №1
### Создайте класс “Car” с атрибутами производитель и модель. Создайте объект этого класса. Напишите комментарии для кода, объясняющие его работу. Результатом выполнения задания будет листинг кода с комментариями.
```python
class Car:
    # Конструктор класса, инициализирующий атрибуты make и model
    def __init__(self, make, model):
        self.make = make  # Устанавливаем марку автомобиля
        self.model = model  # Устанавливаем модель автомобиля

# Создаем объект my_car класса Car с маркой "Toyota" и моделью "Corolla"
my_car = Car("Toyota", "Corolla")
```

### Результат
![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/img/1t8.png)

## Выводы
Создание класса Car с конструктором инициализирующим атрибуты make и model. Создание объекта my_car класса Car с маркой "Toyota" и моделью "Corolla".

## Лабораторная работа №2
### Дополните код из первого задания, добавив в него атрибуты и методы класса, заставьте машину “поехать”. Напишите комментарии для кода, объясняющие его работу. Результатом выполнения задания будет листинг кода с комментариями и получившийся вывод в консоль.
```python
class Car:
    # Конструктор класса, который инициализирует атрибуты make и model
    def __init__(self, make, model):
        self.make = make  # Устанавливаем марку автомобиля
        self.model = model  # Устанавливаем модель автомобиля

    # Метод для запуска действия "водить" автомобиля
    def drive(self):
        # Выводит сообщение о вождении автомобиля с указанием марки и модели
        print(f"Driving the {self.make} {self.model}")

# Создаем объект my_car класса Car с маркой "Toyota" и моделью "Corolla"
my_car = Car("Toyota", "Corolla")
# Вызываем метод drive для my_car, что выведет сообщение о вождении
my_car.drive()

```
### Результат
![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/img/2t8.png)

## Выводы
Создание класса Car с конструктором инициализирующим атрибуты make и model. Создание метода drive, который выводит сообщение в консоль. Создаем объект my_car класса Car. Вызываем метод drive для my_car.

## Лабораторная работа №3
### Создайте новый класс “ElectricCar” с методом “charge” и атрибутом емкость батареи. Реализуйте его наследование от класса, созданного в первом задании. Заставьте машину поехать, а потом заряжаться. Напишите комментарии для кода, объясняющие его работу. Результатом выполнения задания будет листинг кода с комментариями и получившийся вывод в консоль.

```python
class Car:
    # Конструктор класса, который инициализирует атрибуты make и model
    def __init__(self, make, model):
        self.make = make  # Устанавливаем марку автомобиля
        self.model = model  # Устанавливаем модель автомобиля

    # Метод для запуска действия "водить" автомобиля
    def drive(self):
        # Выводит сообщение о вождении автомобиля с указанием марки и модели
        print(f"Driving the {self.make} {self.model}")


# Создаем объект my_car класса Car с маркой "Toyota" и моделью "Corolla"
my_car = Car("Toyota", "Corolla")
# Вызываем метод drive для my_car, что выведет сообщение о вождении
my_car.drive()


class ElectricCar(Car):
    # Конструктор класса ElectricCar, наследуемого от Car, и инициализация атрибута батареи
    def __init__(self, make, model, battery_capacity):
        # Вызов конструктора базового класса Car для установки make и model
        super().__init__(make, model)
        self.battery_capacity = battery_capacity  # Устанавливаем емкость батареи

    # Метод для запуска действия "зарядки" электромобиля
    def charge(self):
        # Выводит сообщение о зарядке автомобиля с указанием емкости батареи
        print(f"Charging the {self.make} {self.model} with {self.battery_capacity} kWh")


# Создаем объект my_electric_car класса ElectricCar с маркой "Tesla", моделью "Model S" и емкостью батареи 75 кВт⋅ч
my_electric_car = ElectricCar('Tesla', 'Model S', 75)
# Вызываем метод drive для my_electric_car, что выведет сообщение о вождении
my_electric_car.drive()
# Вызываем метод charge для my_electric_car, что выведет сообщение о зарядке
my_electric_car.charge()

```

### Результат
![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/img/3t8.png)

## Выводы
Создаем класс ElectricCar, наследуемого от Car, и инициализация атрибута батареи. Создаем метод charge для зарядки батареи. Создаем объект my_electric_car класса ElectricCar с маркой "Tesla", моделью "Model S" и емкостью батареи 75 кВт⋅ч. Вызываем метод drive для my_electric_car, что выведет сообщение о вождении. Вызываем метод charge для my_electric_car, что выведет сообщение о зарядке.
  
## Лабораторная работа №4
### Реализуйте инкапсуляцию для класса, созданного в первом задании. Создайте защищенный атрибут производителя и приватный атрибут модели. Вызовите защищенный атрибут и заставьте машину поехать. Напишите комментарии для кода, объясняющие его работу. Результатом выполнения задания будет листинг кода с комментариями и получившийся вывод в консоль.
```python
class Car:
    # Конструктор класса, который инициализирует атрибуты _make и __model
    def __init__(self, make, model):
        self._make = make  # Полузакрытый атрибут _make (может использоваться вне класса, но рекомендуется использовать внутри)
        self.__model = model  # Закрытый атрибут __model (может использоваться только внутри класса)

    # Метод для запуска действия "водить" автомобиля
    def drive(self):
        # Выводит сообщение о вождении автомобиля с указанием марки и модели
        print(f"Driving the {self._make} {self.__model}")


# Создаем объект my_car класса Car с маркой "Toyota" и моделью "Corolla"
my_car = Car("Toyota", "Corolla")
# Выводим значение полузакрытого атрибута _make объекта my_car
print(my_car._make)
# Вызываем метод drive для my_car, что выведет сообщение о вождении
my_car.drive()

```

### Результат

![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/img/4t8.png)
## Выводы
self._make: полузакрытый атрибут, к которому можно обратиться извне, хотя предпочтительно использовать его только внутри класса.
self.__model: закрытый атрибут, доступ к которому возможен только внутри класса, благодаря двойному подчеркиванию.

## Лабораторная работа №5
### Реализуйте полиморфизм создав основной (общий) класс “Shape”, а также еще два класса “Rectangle” и “Circle”. Внутри последних двух классов реализуйте методы для подсчета площади фигуры. После этого создайте массив с фигурами, поместите туда круг и прямоугольник, затем при помощи цикла выведите их площади. Напишите комментарии для кода, объясняющие его работу. Результатом выполнения задания будет листинг кода с комментариями и получившийся вывод в консоль.
```python
# Определяем базовый класс "Shape" с методом area, который будет переопределяться в дочерних классах
class Shape:
    # Метод для расчета площади фигуры; базовый метод не выполняет действий
    def area(self):
        pass


# Определяем класс "Rectangle", наследуемый от "Shape", для представления прямоугольника
class Rectangle(Shape):
    # Конструктор класса, инициализирующий ширину и высоту прямоугольника
    def __init__(self, width, height):
        self.width = width  # Устанавливаем ширину
        self.height = height  # Устанавливаем высоту

    # Переопределенный метод для расчета площади прямоугольника
    def area(self):
        return self.width * self.height  # Площадь прямоугольника = ширина * высота


# Определяем класс "Circle", наследуемый от "Shape", для представления круга
class Circle(Shape):
    # Конструктор класса, инициализирующий радиус круга
    def __init__(self, radius):
        self.radius = radius  # Устанавливаем радиус

    # Переопределенный метод для расчета площади круга
    def area(self):
        return 3.14 * self.radius * self.radius  # Площадь круга = π * радиус^2


# Создаем массив (список) с экземплярами фигур: круг и прямоугольник
shapes = [
    Rectangle(4, 5),  # Прямоугольник с шириной 4 и высотой 5
    Circle(3)         # Круг с радиусом 3
]

# Проходим циклом по массиву фигур и выводим площади для каждой фигуры
for shape in shapes:
    print(shape.area())  # Вызываем метод area для каждого объекта в списке

```

### Результат
![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/img/5t8.png)

## Выводы
Ищем площади фигур

## Самостоятельная работа №1
### Найдите в интернете любую статью (объем статьи не менее 200 слов), скопируйте ее содержимое в файл и напишите программу, которая считает количество слов в текстовом файле и определит самое часто встречающееся слово. Результатом выполнения задачи будет: скриншот файла со статьей, листинг кода, и вывод в консоль, в котором будет указана вся необходимая информация.
from collections import Counter

with open('input.txt', 'r', encoding='utf-8') as file:
    text = file.read()

words = text.split()

word_count = len(words)

word_frequency = Counter(words)

most_common_word = word_frequency.most_common(1)[0]

print(f"Общее количество слов: {word_count}")
print(f"Самое часто встречающееся слово: {most_common_word[0]} ({most_common_word[1]} раз)")


### Результат.
![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/img/6t7.png)
## Выводы

Данная задача продемонстрировала базовые операции с вводом данных в Python, а также показала, как преобразовать строку чисел в другие структуры данных, такие как список и кортеж. Это полезно для получения и дальнейшей обработки данных от пользователя в различных форматах.

## Самостоятельная работа №2
### У вас появилась потребность в ведении книги расходов, посмотрев все существующие варианты вы пришли к выводу что вас ничего не устраивает и нужно все делать самому. Напишите программу для учета расходов. Программа должна позволять вводить информацию о расходах, сохранять ее в файл и выводить существующие данные в консоль. Ввод информации происходит через консоль. Результатом выполнения задачи будет: скриншот файла с учетом расходов, листинг кода, и вывод в консоль, с демонстрацией работоспособности программы.

def add_expense():
    expense = input("Введите описание расхода: ")
    amount = input("Введите сумму расхода: ")

    with open('expenses.txt', 'a', encoding='utf-8') as file:
        file.write(f"{expense}: {amount}\n")


def read_expenses():
    with open('expenses.txt', 'r', encoding='utf-8') as file:
        data = file.read()
        if data:
            print("Существующие расходы:")
            print(data)
        else:
            print("Расходы отсутствуют")


while True:
    choice = input("Введите 1 для добавления расхода, 2 для просмотра расходов, 0 для выхода: ")
    if choice == '1':
        add_expense()
    elif choice == '2':
        read_expenses()
    elif choice == '0':
        break
    else:
        print("Неверный выбор, попробуйте еще раз.")


### Результат.
![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/img/7t7.png)
## Выводы

Данная задача показала, что несмотря на неизменяемость кортежей, их можно "модифицировать" через создание новых кортежей. Это позволило понять, как можно реализовать логику изменений кортежей с сохранением их неизменяемости.



## Самостоятельная работа №3
### Имеется файл input.txt с текстом на латинице. Напишите программу, которая выводит следующую статистику по тексту: количество букв латинского алфавита; число слов; число строк.

import string

def analyze_text(file_path):
    with open(file_path, 'r', encoding='utf-8') as file:
        text = file.read()

    # Подсчет букв латинского алфавита
    letter_count = sum(1 for char in text if char in string.ascii_letters)

    # Подсчет слов
    word_count = len(text.split())

    # Подсчет строк
    line_count = len(text.splitlines())

    # Вывод результатов
    print(f"Количество букв: {letter_count}")
    print(f"Количество слов: {word_count}")
    print(f"Количество строк: {line_count}")

analyze_text('input.txt')


### Результат.
![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/img/13t7.png)
## Выводы

Задача помогает закрепить навыки работы со строками и словарями. Также она показывает, как эффективно работать с частотными подсчетами и сортировкой данных в Python, что является важным аспектом обработки данных.


## Самостоятельная работа №4
### Напишите программу, которая получает на вход предложение, выводит его в терминал, заменяя все запрещенные слова звездочками * (количество звездочек равно количеству букв в слове). Запрещенные слова, разделенные символом пробела, хранятся в текстовом файле input.txt. Все слова в этом файле записаны в нижнем регистре. Программа должна заменить запрещенные слова, где бы они ни встречались, даже в середине другого слова. Замена производится независимо от регистра: если файл input.txt содержит запрещенное слово exam, то слова exam, Exam, ExaM, EXAM и exAm должны быть заменены на ****.


import re

def replace_forbidden_words(text, forbidden_words):
    # Проходим по каждому слову из списка запрещенных
    for word in forbidden_words:
        # Создаем регулярное выражение для поиска слова без учета регистра
        pattern = re.compile(re.escape(word), re.IGNORECASE)
        # Заменяем все вхождения слова на звездочки
        text = pattern.sub('*' * len(word), text)
    return text

with open('input.txt', 'r', encoding='utf-8') as f:
    forbidden_words = f.read().split()

text = "Hello, world! Python IS the programming language of thE future. My EMAIL is.... PYTHON is awesome!!!!"

result = replace_forbidden_words(text, forbidden_words)

print(result)



### Результат.
![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/img/14t7.png)

## Выводы

Задача продемонстрировала работу с файлами, строками и регулярными выражениями. Это полезный навык при создании программ для фильтрации текста, что может применяться, например, в системах модерации контента.

## Самостоятельная работа №5
### Самостоятельно придумайте и решите задачу, которая будет взаимодействовать с текстовым файлом. Задача последнее посещение
import os

from datetime import datetime, timedelta

def record_visit():

with open('input.txt', 'a', encoding='utf-8') as f:

f.write(f"{datetime.now().strftime('%Y-%m-%d %H:%M:%S')}\n")

def get_last_visit():

last_visit = None

if os.path.exists('input.txt'):

with open('input.txt', 'r', encoding='utf-8') as f:

for line in f:

last_visit = line.strip()

return last_visit

record_visit()

print(f"Последнее посещение: {get_last_visit()}")

### Результат.
![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/img/15.1.png)
![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/img/15.2.png)
## Выводы
Эта программа фиксирует посещение, записывая текущее время в файл, а также выводит последнее время посещения. Каждый раз при запуске записывает текущие дату и время посещения в файл input.txt.
Читает файл и выводит время последнего посещения, которое может быть как последним записанным временем, так и временем из предыдущих посещений. Если запустить программу несколько раз, в файл будет добавляться несколько строк с разными временными отметками, и программа всегда будет возвращать последнюю из них.
## Общий вывод 
В ходе выполнения всех заданий были рассмотрены различные аспекты работы с файлами, строками, кортежами, списками и словарями. Эти задания способствовали изучению и закреплению навыков ввода-вывода данных, работы с неизменяемыми структурами (кортежи), а также использования множества встроенных функций Python, таких как сортировка, фильтрация и регулярные выражения. Все задачи решались с применением базовых и продвинутых методов Python, что развивает способность эффективно обрабатывать данные и взаимодействовать с файлами.
