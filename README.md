# Тема 1. Работа с Git
Отчет по Теме #1 выполнил(а):
- Холкин Данил Алексеевич
- ПИЭ-22-1

| Задание | Лаб_раб | Сам_раб |
| ------ | ------ | ------ |
| Задание 1 | + | - |
| Задание 2 | + | - |
| Задание 3 | + | - |
| Задание 4 | + | - |
| Задание 5 | + | - |
| Задание 6 | + | - |
| Задание 7 | + | - |
| Задание 8 | + | - |
| Задание 9 | + | - |
| Задание 10 | + | - |
| Задание 11 | + | - |
| Задание 12 | + | - |
| Задание 13 | + | - |
| Задание 14 | + | - |
| Задание 15 | + | - |

знак "+" - задание выполнено; знак "-" - задание не выполнено;

Работу проверили:
- к.э.н., доцент Панов М.А.

## Задание №1
### Установка

### Результат.
![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/git1.png)

## Выводы

Git был успешно установлен, также был создан этот репозиторий и ветка Tema_1

## Задание №2
### Настройка
$ git config --global user.name "Danil"

$ git config --global user.email "mr.danil.kholkin@mail.ru"


### Результат.
![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/git2.png)

## Выводы

Установлено имя пользователя и почта

## Задание №3
### Создание нового репозитория
cd /c/Users/user/Software

git init

### Результат.
![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/git3.png)

## Выводы

Был инициализирован пустой репозиторий

## Задание №4
### Подготовка файлов
git add proba.txt

git status
### Результат.
![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/git4.png)

## Выводы

Файл proba.txt подготовлен к коммиту

## Задание №5
### Фиксация изменений
git commit -m "Первый коммит: начальная версия проекта" - создание коммита с описанием

git log - просмотр списка коммитов

git log --oneline - просмотр коммитов в компактном виде

git log --graph - графическое древо коммитов

### Результат.
![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/git5.png)

## Выводы

Был создан коммит, просмотрена история добавления коммитов

## Задание №6
### Подключение к удаленному репозиторию
git remote add origin [ссылка_удаленного_репозитория] - связывание локального репозитория с удаленным

git push origin main - загрузка изменений

git pull origin main - извлечение изменений 

git pull --rebase origin main - указание метода слияния

git stash - добавление изменений в стеш

git stash save "Описание изменений" - добавление изменений в стеш с названием

git stash apply - возврат к сохраненным изменениям

git stash pop - применение стеш и удаление его из стеша
### Результат.
![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/git6.png)

## Выводы

Успешное подключение к удаленному репозиторию, а также загрузка и извлечение изменений

## Задание №7
### Ветвление
git branch wetka - создание новой ветки

git checkout/switch wetka - переключение на ветку

git merge/feature - слияние веток

### Результат.
![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/git7.png)

## Выводы

Созданы и объединены две ветки 

## Задание №8
### Особенности применения «Фетч»
git fetch [удаленный_репозиторий] - команда для выполнения фетча

### Результат.
![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/git8.png)

## Выводы

После выполнения фетча можно посмотреть изменения и если нужно выполнить слияние

## Задание №9
### Удаление файлов, веток, локальных и удалённых репозиториев
git rm [имя файла] - удаление файла

git rm --cached [имя файла] - удаление файла только из индекса

git branch -d [имя ветки] - удаление ветки

git push -delete [имя ветки] - удаление удаленной ветки
### Результат.
![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/git9.png)

## Выводы

Удалены ветки и файлы

## Задание №10
### Отслеживание изменений в коммитах
git log - просмотр истории коммитов 

git diff - посмотреть изменения между последним и текущим коммитом

git diff [коммит1][коммит2] - изменения между двумя коммитами
### Результат.
![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/git10.png)

## Выводы

Просмотр изменений

## Задание №11
### Возвращение файла к предыдущему (определенному) состоянию
git checkout 9019ef71aad7cca1103df075c5bd979ac0b85c2a -- /c/Users/user/Software/proba.txt 

git commit -m "Восстановление файла к предыдущему состоянию"

### Результат.
![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/git11.png)

## Выводы

Восстановление файла к предыдущему состоянию

## Задание №12
### Возвращение к предыдущему коммиту
git reset --hard HEAD^

git reset --hard 9019ef71aad7cca1103df075c5bd979ac0b85c2a

### Результат.
![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/git12.png)

## Выводы

Сброс до конкретного и до предыдущего коммита

## Задание №13
### Исправление коммита
git commit --amend

git rebase -i HEAD~3

git rebase --continue

### Результат.
![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/git13.png)

## Выводы

Исправление раннего и предыдущего коммита

## Задание №14
### Разрешение конфликтов при слиянии

### Результат.
![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/git14.1.png)
![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/git14.2.png)

## Выводы

Конфликт слияния был решен

## Задание №15
### Настройка .gitignore

### Результат.
![Меню](https://github.com/DanilAlexeevich/DanilKholkin/raw/main/git15.png)

## Выводы

gitignore
