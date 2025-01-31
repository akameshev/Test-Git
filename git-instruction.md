# Инструкция по работе с git
![Официальный логотип git](logo.png)

## Lesson 1

## Что такое git и контроль версий
**Системы контроль версий** - это системы, которые: 
1. обеспечивают сохранение содержимого файлов и папок(их *версий*)
2. Обеспечивают передвижение по *версиям* этих файлов и папок

**git** - это самая известная и используемая на данный момент реализация контроля версий с командным интерфейсом

**Локальный репозиторий** - это хранилище *изменений* Git в виде папки.

## Инициализация локального репозитория

Для того чтобы сказать git, что данная папка является локальным репозиторием нужно зайти в папку и ввести в ней команду

*git init*

Также, если этого раньше не делалось, то нужно определить ваше имя пользователя и email командами:
. git config --global user.name "your name"
. git config --global user.email your email 

## Добавление файлов под контроль версий

Для этого нужно ввести команду:
*git add имена файлов*
Теперь имена и содержимое этих файлов можно сохронять

## Делаем коммит

Для того, чтобы изменения представляли собой отдельную версию, к которой можно возвращаться и манипулировать после добавления под **контроль версий**, нужно ввести команду:

*git commit -m "Название версии"*

Можно также добавить под контроль версий и сформировать коммит для всех  файлов и папок одной командой:
*git commit -am "Название версии"

## Просмотр текущего состояния репозитория
Для вывода текущего состояния локального репозитория используются команды:

>git status - просмотр состояния файлов и папок в репозитории

> git diff - просмотр самих изменений файлов и папок

## Просмотр всех изменений репозитория

Для просмотра истории изменений от начала и последнего коммита нужно ввести:

*git log*

git status - команда, вывод состояния репозитория
git init - иницыализация git
## Lesson 2
git branch - выводит список ответвлений </br>
git branch name - создание ответвления</br>
git checkout branch_name - позволяет переключиться на выбранное ответвление

## Lesson3
### Работа с удаленными репозиторями
Удаленные репозитории — это версии проектов, которые хранятся на удаленных серверах. Добавляя удаленный репозиторий, вы показываете Git, где хранится код проекта в интернете.</br>

### Работа над своим репозиторием
**Краткий справочник команд**</br>
**git pull** - используется для извлечения и загрузки содержимого из удаленного репозитория и немедленного обновления локального репозитория этим содержимым

**git push** - позволяет передать изменения из локального репозитория (набора файлов из папки .git) в удаленный.

**git clone** - позволяет создать копию удаленного репозитория

**Fork** - опция на сервисе удаленных репозиториев, позволяет создать ответвление от стороннего репозитория

Для начала необходимо создать удаленный репозиторий на сервисах типа github. gitlab...</br>
После этого нужно добавить удаленный репозиторий локально.
Для того чтобы добавить удаленный репозиторий локально можно пойти 2-мя путями:

1. Создать новый локальный репозиторий в терминале:
+ echo "# repository_name" >> README.md
+ git init
+ git add README.md
+ git commit -m "first commit"
+ git branch -M main
+ git remote add origin https://github.com/user_name/repository_name.git
+ git push -u origin main

2. запустить в существующем репозитории в терминале
+ git remote add origin https://github.com/user_name/repository_name.git
+ git branch -M main
+ git push -u origin main

#### Работа над сторонним репозиторием
> _Прежде всего для того чтобы работать с чужим репозиторием необходимо учесть несколько нюансов_
> 1. Удаленный репозиторий должен иметь модификатор доступа  **public** либо вам должны быть известны учетные данные для доступа к нему.
> 2. Вам должен быть известен путь к данному репозиторию.

Для того чтобы добавить сторонний удаленный репозиторий локально также можно пойти 2-мя путями:
1. Клонировать. запуск клонирования репозитория осушествляется командой **git clone**. Пример:
+ git clone https://github.com/other_user_name/repository_name.git

2. Можно создать собственное ветвление через опцию **fork** на сервисах удаленных репозиториев github, gitlab...
После созднания собственного ответвления необходимо закрыть все окна, и в пустом окне выбрать опцию **Clone Git repository**. Пример:
После внесения изменений выполнить команды **git add** и **git commit**. В завершении всего отправить изменения на удаленный репозиторий командой **git push**

