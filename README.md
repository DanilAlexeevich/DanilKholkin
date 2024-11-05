# Тема 9. Концепции и принципы ООП
Отчет по Теме #9 выполнил(а):
- Холкин Данил Алексеевич
- ПИЭ-22-1

| Задание | Лаб_раб | Сам_раб |
| ------ | ------ | ------ |
| Задание 1 | + | + |
| Задание 2 | + | 
| Задание 3 | + | 
| Задание 4 | + | 
| Задание 5 | + | 


знак "+" - задание выполнено; знак "-" - задание не выполнено;

Работу проверили:
- к.э.н., доцент Панов М.А.

## Лабораторная работа №1
### Допустим, что вы решили оригинально и немного странно познакомится с человеком. Для этого у вас должен быть написан свой класс на Python, который будет проверять угадал ваше имя человек или нет. Для этого создайте класс, указав в свойствах только имя. Дальше создайте функцию init (), а в ней сделайте проверку на то угадал человек ваше имя или нет. Также можете проверить что будет, если в этой функции указав атрибут, который не указан в вашем классе, например, попробуйте вызвать фамилию.

```python
class Danil:
        __slots__ = ['name']

        def __init__(self, name):
            if name == 'Данил':
                self.name = f"Да, я {name}"
            else:
                self.name = f"Я не {name}, а Данил"


person1 = Danil('Алексей')
person2 = Danil('Данил')
print(person1.name)
print(person2.name)

person2.surname = 'Холкин'
```

### Результат
![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/img/1t9.png)

## Выводы
Создание класса с одним свойством. Создание функции init(). Проверка, что будет если указать несществующий атрибут класса.

## Лабораторная работа №2
### Вам дали важное задание, написать продавцу мороженого программу, которая будет писать добавили ли топпинг в мороженое и цену после возможного изменения. Для этого вам нужно написать класс, в которой будет определяться изменили ли состав мороженого или нет. В этом классе реализуйте метод, выводящий на печать «Мороженое с {ТОППИНГ}» в случае наличия добавки, а иначе отобразится следующая фраза: «Обычное мороженое». При этом программа должна воспринимать как топпинг только атрибуты типа string.

```python
class Icecream:
        def __init__(self, ingredient=None):
            if isinstance(ingredient, str):
                self.ingredient = ingredient
            else:
                self.ingredient = None

        def composition(self):
            if self.ingredient:
                print(f"Мороженое с {self.ingredient}")
            else:
                print('Обычное мороженое')


icecream = Icecream()
icecream.composition()
icecream = Icecream('шоколадом')
icecream.composition()
icecream = Icecream(5)
icecream.composition()
```
### Результат
![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/img/2t9.png)

## Выводы
Создание класса Icecream с методом, который выводит на печать «Мороженое с {ТОППИНГ}» в случае наличия добавки, а иначе отобразится следующая фраза: «Обычное мороженое». Программа воспринимает только атрибуты типа string.

## Лабораторная работа №3
### Петя – начинающий программист и на занятиях ему сказали реализовать икапсу…что-то. А вы хороший друг Пети и ко всему прочему прекрасно знаете, что икапсу…что-то – это инкапсуляция, поэтому решаете помочь вашему другу с написанием класса с инкапсуляцией. Ваш класс будет не просто инкапсуляцией, а классом с сеттером, геттером и деструктором. После написания класса вам необходимо продемонстрировать что все написанные вами функции работают. Также вас необходимо объяснить Пете почему на скриншоте ниже в консоли выводится ошибка.

```python
class MyClass:
        def __init__(self, value):
            self._value = value

        def set_value(self, value):
            self._value = value

        def get_value(self):
            return self._value

        def del_value(self):
            del self._value

        value = property(get_value, set_value, del_value, "Свойство value")

obj = MyClass(42)
print(obj.get_value())
obj.set_value(45)
print(obj.get_value())
obj.set_value(100)
print(obj.get_value())
obj.del_value()
print(obj.get_value())

```

### Результат
![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/img/3t9.png)

## Выводы
Этот код создает класс MyClass с атрибутом _value и свойством value, которое управляет доступом к этому атрибуту через методы get_value, set_value и del_value. Это свойство позволяет получать, устанавливать и удалять значение _value с помощью property. Ошибка возникает в последней строке print(obj.get_value()), потому что после вызова obj.del_value() атрибут _value был удален. Попытка его чтения приводит к ошибке AttributeError, так как атрибут больше не существует.
  
## Лабораторная работа №4
### Вам прекрасно известно, что кошки и собаки являются млекопитающими, но компьютер этого не понимает, поэтому вам нужно написать три класса: Кошки, Собаки, Млекопитающие. И при помощи “наследования” объяснить компьютеру что кошки и собаки – это млекопитающие. Также добавьте какой-нибудь свой атрибут для кошек и собак, чтобы показать, что они чем-то отличаются друг от друга.

```python
class Mammal:
    className = 'Mammal'


class Dog(Mammal):
    species = 'canine'
    sounds = 'wow'

class Cat(Mammal):
    species = 'feline'
    sounds = 'meow'

dog = Dog()
print(f"Dog is {dog.className}, but they say {dog.sounds}")
cat = Cat()
print(f"Cat is {cat.className}, but they say {cat.sounds}")

```

### Результат

![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/img/4t9.png)
## Выводы
Этот код создает базовый класс Mammal и два подкласса Dog и Cat, которые наследуют от Mammal. Этот код выводит информацию о каждом из объектов dog и cat, используя их свойства.
## Лабораторная работа №5
### На разных языках здороваются по-разному, но суть остается одинаковой, люди друг с другом здороваются. Давайте вместе с вами реализуем программу с полиморфизмом, которая будет описывать всю суть первого предложения задачи. Для этого мы можем выбрать два языка, например, русский и английский и написать для них отдельные классы, в которых будет в виде атрибута слово, которым здороваются на этих языках. А также напишем функцию, которая будет выводить информацию о том, как на этих языках здороваются. Заметьте, что для решения поставленной задачи мы использовали декоратор @staticmethod, поскольку нам не нужны обязательные параметры-ссылки вроде self.

```python
class Russian:

    @staticmethod
    def greeting():
        print("Привет")

class English:

    @staticmethod
    def greeting():
        print("Hello")

def greet(language):
    language.greeting()

ivan = Russian()
greet(ivan)
john = English()
greet(john)

```

### Результат
![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/img/5t9.png)

## Выводы
Этот код создает два класса Russian и English, каждый из которых имеет статический метод greeting, выводящий приветствие на соответствующем языке.

## Самостоятельная работа №1
### Задание Садовник и помидоры.
```python
# Класс Tomato (Помидор)
class Tomato:
    # Статическое свойство states, содержащее стадии созревания
    states = ["отсутствует", "цветение", "зеленый", "красный"]

    def __init__(self, index):
        # Динамическое свойство _index — уникальный идентификатор томата
        self._index = index
        # Динамическое свойство _state — начальная стадия созревания (первое значение из states)
        self._state = Tomato.states[0]

    # Метод для роста томата, переход на следующую стадию созревания
    def grow(self):
        current_state_index = Tomato.states.index(self._state)
        if current_state_index < len(Tomato.states) - 1:
            self._state = Tomato.states[current_state_index + 1]

    # Метод для проверки, что томат созрел (стал красным)
    def is_ripe(self):
        return self._state == Tomato.states[-1]


# Класс TomatoBush (Куст помидоров)
class TomatoBush:
    def __init__(self, num_tomatoes):
        # Динамическое свойство tomatoes — список объектов Tomato
        self.tomatoes = [Tomato(index) for index in range(num_tomatoes)]

    # Метод для роста всех томатов на кусте
    def grow_all(self):
        for tomato in self.tomatoes:
            tomato.grow()

    # Метод для проверки, что все томаты на кусте созрели
    def all_are_ripe(self):
        return all(tomato.is_ripe() for tomato in self.tomatoes)

    # Метод для сбора урожая (очищает список томатов после сбора)
    def give_away_all(self):
        self.tomatoes = []


# Класс Gardener (Садовник)
class Gardener:
    def __init__(self, name, plant):
        # Публичное свойство name — имя садовника
        self.name = name
        # Динамическое свойство _plant — куст томатов, за которым ухаживает садовник
        self._plant = plant

    # Метод работы садовника (растит куст с томатами)
    def work(self):
        self._plant.grow_all()

    # Метод сбора урожая
    def harvest(self):
        if self._plant.all_are_ripe():
            self._plant.give_away_all()
            print("Урожай собран!")
        else:
            print("Не все томаты созрели, нельзя собирать урожай.")

    # Статический метод справки по садоводству
    @staticmethod
    def knowledge_base():
        print("Справка по садоводству: поливайте растения, ухаживайте за ними, соберите урожай, когда они созреют.")


# Тесты
# Вызов справки по садоводству
Gardener.knowledge_base()

# Создание объектов TomatoBush и Gardener
bush = TomatoBush(num_tomatoes=5)
gardener = Gardener(name="Иван", plant=bush)

# Уход за кустом с помидорами
gardener.work()
gardener.harvest()  # Попытка собрать урожай, когда томаты еще не дозрели

# Продолжение ухода за кустом, пока все томаты не созреют
for _ in range(3):  # Дополнительные циклы для полного созревания
    gardener.work()
    gardener.harvest()  # Проверка созревания и сбор урожая, если созрели

```

### Результат.
![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/img/6t9.png)
## Выводы
Этот код моделирует садоводческий процесс с помощью трех классов: Tomato, TomatoBush и Gardener. Tomato представляет один помидор, который проходит через четыре стадии созревания. Он может расти, переходя на следующую стадию, и проверять, достиг ли стадии зрелости. TomatoBush — это куст с множеством помидоров. Он управляет ростом всех помидоров одновременно, проверяет их зрелость и предоставляет урожай (очищает список помидоров после сбора). Gardener ухаживает за кустом, ускоряя рост помидоров, и может собрать урожай только когда все помидоры полностью созрели. Также садовник имеет метод для вывода справки по садоводству. Садовник многократно "работает" над кустом, что постепенно переводит все помидоры через стадии созревания. Когда все плоды созрели, садовник может собрать урожай, удаляя созревшие помидоры из куста.

## Общий вывод 
Концепции и принципы объектно-ориентированного программирования (ООП) играют ключевую роль в современном программировании, обеспечивая модульность, гибкость и повторное использование кода. В Python объектно-ориентированное программирование (ООП) реализовано гибко и просто, что позволяет эффективно применять его основные принципы: инкапсуляцию, наследование, полиморфизм и абстракцию.
