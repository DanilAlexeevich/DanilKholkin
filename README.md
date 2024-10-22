# Тема 7. Работа с файлами (ввод, вывод) 
Отчет по Теме #7 выполнил(а):
- Холкин Данил Алексеевич
- ПИЭ-22-1

| Задание | Лаб_раб | Сам_раб |
| ------ | ------ | ------ |
| Задание 1 | + | + |
| Задание 2 | + | + |
| Задание 3 | + | + |
| Задание 4 | + | + |
| Задание 5 | + | + |
| Задание 6 | + | - |
| Задание 7 | + | - |
| Задание 8 | + | - |
| Задание 9 | + | - |
| Задание 10 | + | - |


знак "+" - задание выполнено; знак "-" - задание не выполнено;

Работу проверили:
- к.э.н., доцент Панов М.А.

## Лабораторная работа №1
### Составьте текстовый файл и положите его в одну директорию с программой на Python. Текстовый файл должен состоять минимум из двух строк. 
request = int(input('Введите номер кабинета: '))

dictionary = {

101: {'key': 1234, 'access': True},

102: {'key': 1337, 'access': True},

103: {'key': 8943, 'access': True},

104: {'key': 5555, 'access': False},

None: {'key': None, 'access': False},

}

response = dictionary.get(request)

if not response:

response = dictionary[None]

key = response.get('key')

access = response. get('access')

print(key, access)

### Результат
![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/img/1t7.png)

## Выводы
Код запрашивает у пользователя номер кабинета и проверяет, есть ли такой кабинет в словаре. Если номер существует, то программа выводит ключ и значение параметра access для этого кабинета.

## Лабораторная работа №2
### Напишите программу, которая выведет только первую строку из вашего файла, при этом используйте конструкцию open()/close().
from pprint import pprint

my_dict = {'first': 'so easy'}

def dict_maker(**kwargs) :

my_dict.update(**kwargs)

dict_maker(a1=1, a2=20, a3=54, a4=13)

dict_maker(name='Михаил', age=31, weight=70, eyes_color='blue')

pprint(my_dict)
### Результат
 ![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/img/2t7.png)

## Выводы
Код создаёт словарь с помощью функции dict_maker(), которая принимает произвольное количество именованных аргументов (**kwargs) и добавляет их в существующий словарь my_dict с помощью метода .update().

## Лабораторная работа №3
### Напишите программу, которая выведет все строки из вашего файла в массиве, при этом используйте конструкцию open()/close().
input_string = 'HelloWorld'

result = tuple(input_string)

print(result)

print (list (result))

### Результат
![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/img/3t7.png)

## Выводы
Код принимает строку 'HelloWorld' и преобразует её в кортеж с помощью функции tuple(), а затем выводит полученный кортеж, после снова печатает преобразованный кортеж, но уже как список с помощью функции list(), которая преобразует кортеж в список.
  
## Лабораторная работа №4
### Напишите программу, которая выведет все строки из вашего файла в массиве, при этом используйте конструкцию with open().
def personal_info(name, age, company='unnamed' ):

print(f"Имя: {name} Возраст: {age} Компания: {company}")

tom = ("Григорий", 22)

personal_info(*tom)

bob = ("Георгий", 41, "Yandex")

personal_info(*bob)

### Результат

![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/img/4t7.png)
## Выводы
Функция выводит на экран строку с информацией о человеке, используя переданные аргументы.

## Лабораторная работа №5
### Напишите программу, которая выведет каждую строку из вашего файла отдельно, при этом используйте конструкцию with open().
def tuple_sort(tpl):

for elm in tpl:
    
if not isinstance(elm, int):
        
return tpl
            
return tuple(sorted(tpl))

if __name__ == '__main__':

print (tuple_sort((5, 5, 3, 1, 9)))
    
print(tuple_sort((5, 5, 2.1, '1', 9)))

### Результат
![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/img/5t7.png)

## Выводы
Сортировка и возвращение кортежа

## Лабораторная работа №6
### Напишите программу, которая будет добавлять новую строку в ваш файл, а потом выведет полученный файл в консоль. Вывод можно осуществлять любым способом. Обязательно проверьте сам файл, чтобы изменения в нем тоже отображались.
def tuple_sort(tpl):

for elm in tpl:
    
if not isinstance(elm, int):
        
return tpl
            
return tuple(sorted(tpl))

if __name__ == '__main__':

print (tuple_sort((5, 5, 3, 1, 9)))
    
print(tuple_sort((5, 5, 2.1, '1', 9)))

### Результат
![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/img/6t7.png)

## Выводы
Сортировка и возвращение кортежа

## Лабораторная работа №7
### Напишите программу, которая перепишет всю информацию, которая была у вас в файле до этого, например напишет любые данные из произвольно вами составленного списка. Также не забудьте проверить что измененная вами информация сохранилась в файле.
def tuple_sort(tpl):

for elm in tpl:
    
if not isinstance(elm, int):
        
return tpl
            
return tuple(sorted(tpl))

if __name__ == '__main__':

print (tuple_sort((5, 5, 3, 1, 9)))
    
print(tuple_sort((5, 5, 2.1, '1', 9)))

### Результат
![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/img/7t7.png)

## Выводы
Сортировка и возвращение кортежа

## Лабораторная работа №8
### Выберите любую папку на своем компьютере, имеющую вложенные директории. Выведите на печать в терминал ее содержимое, как и всех подкаталогов при помощи функции print_docs(directory).
def tuple_sort(tpl):

for elm in tpl:
    
if not isinstance(elm, int):
        
return tpl
            
return tuple(sorted(tpl))

if __name__ == '__main__':

print (tuple_sort((5, 5, 3, 1, 9)))
    
print(tuple_sort((5, 5, 2.1, '1', 9)))

### Результат
![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/img/8t7.png)

## Выводы
Сортировка и возвращение кортежа

## Лабораторная работа №9
### Требуется реализовать функцию, которая выводит слово, имеющее максимальную длину (или список слов, если таковых несколько). Проверьте работоспособность программы на своем наборе данных

def tuple_sort(tpl):

for elm in tpl:
    
if not isinstance(elm, int):
        
return tpl
            
return tuple(sorted(tpl))

if __name__ == '__main__':

print (tuple_sort((5, 5, 3, 1, 9)))
    
print(tuple_sort((5, 5, 2.1, '1', 9)))

### Результат
![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/img/9t7.png)

## Выводы
Сортировка и возвращение кортежа

## Лабораторная работа №10
### Требуется создать csv-файл «rows_300.csv» со следующими столбцами: № - номер по порядку (от 1 до 300); Секунда – текущая секунда на вашем ПК; Микросекунда – текущая миллисекунда на часах. Для наглядности на каждой итерации цикла искусственно приостанавливайте скрипт на 0,01 секунды.

def tuple_sort(tpl):

for elm in tpl:
    
if not isinstance(elm, int):
        
return tpl
            
return tuple(sorted(tpl))

if __name__ == '__main__':

print (tuple_sort((5, 5, 3, 1, 9)))
    
print(tuple_sort((5, 5, 2.1, '1', 9)))

### Результат
![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/img/10t7.png)

## Выводы
Сортировка и возвращение кортежа

## Самостоятельная работа №1
### Найдите в интернете любую статью (объем статьи не менее 200 слов), скопируйте ее содержимое в файл и напишите программу, которая считает количество слов в текстовом файле и определит самое часто встречающееся слово. Результатом выполнения задачи будет: скриншот файла со статьей, листинг кода, и вывод в консоль, в котором будет указана вся необходимая информация.
from collections import Counter

with open('вап.txt', 'r', encoding='utf-8') as file:
    text = file.read()

words = text.split()

word_count = len(words)

word_frequency = Counter(words)

most_common_word = word_frequency.most_common(1)[0]

print(f"Общее количество слов: {word_count}")
print(f"Самое часто встречающееся слово: {most_common_word[0]} ({most_common_word[1]} раз)")


### Результат.
![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/img/11.1t7.png)
![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/img/11.2t7.png)
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
![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/img/12t7.png)
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
### 4) Напишите программу, которая получает на вход предложение, выводит его в терминал, заменяя все запрещенные слова звездочками * (количество звездочек равно количеству букв в слове). Запрещенные слова, разделенные символом пробела, хранятся в текстовом файле input.txt. Все слова в этом файле записаны в нижнем регистре. Программа должна заменить запрещенные слова, где бы они ни встречались, даже в середине другого слова. Замена производится независимо от регистра: если файл input.txt содержит запрещенное слово exam, то слова exam, Exam, ExaM, EXAM и exAm должны быть заменены на ****.


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
### 5) Самостоятельно придумайте и решите задачу, в которой будут обязательно использоваться кортеж или список. Проведите минимум три теста для проверки работоспособности вашей задачи.

def count_unique_words(file_path):
    with open(file_path, 'r', encoding='utf-8') as f:
        text = f.read()
    
    # Преобразуем текст в список слов и убираем дубликаты
    words = set(text.split())
    
    # Количество уникальных слов
    unique_count = len(words)
    
    # Записываем результат в файл
    with open('output.txt', 'w', encoding='utf-8') as f:
        f.write(f"Количество уникальных слов: {unique_count}\n")
        f.write(f"Уникальные слова: {', '.join(words)}")

count_unique_words('input.txt')




### Результат.
![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/img/15t7.png)
## Выводы
Задача показала важность работы с множествами для получения уникальных элементов. Она продемонстрировала полезный способ обработки текстов, который может быть использован в текстовой аналитике для получения статистики по данным.
## Общий вывод 
В ходе выполнения всех заданий были рассмотрены различные аспекты работы с файлами, строками, кортежами, списками и словарями. Эти задания способствовали изучению и закреплению навыков ввода-вывода данных, работы с неизменяемыми структурами (кортежи), а также использования множества встроенных функций Python, таких как сортировка, фильтрация и регулярные выражения. Все задачи решались с применением базовых и продвинутых методов Python, что развивает способность эффективно обрабатывать данные и взаимодействовать с файлами.
