# справка по работе с  git
Для создания истории нужно ввести команду:
> **git init**

Чтобы получить состояние нашего репозитори:
> **git status**

Чтобы добавить информацию жмем Ctrl+S, либо в настройках выставить "Автосохранение". Далее, командой: 
> **git add <наименование файла>**

*Чтобы добавить комит, нужно* 
> **git commit -m "Ввод комментария"**

Чтобы не писать перед комитом команду add для уже добавленных к отслеживанию можно использовать тег -a
> **git commit -a -m "Ввод комментария"**

**Чтобы переходить от одного комита к другому**
> git checkout "первые 5 символов комита без кавычек"

*Чтобы вернуться к актуальному (последнему) и продолжить работу необходимо:*
> git checkout master

***Чтобы вывести все комиты, нужно:***
> git log

# **Создание веток**

для отображения всех веток можно ввести команду:
> **git branch**

Ветка branch_name создается с помощью команды:
> **git branch branch_name**

чтобы переключиться к ветке branch_name, нужно:
> **git checkout branch_name**

Чтобы слить информацию из ветки branch_name в текущую ветку,нужно:
> **git merge branch_name**

Для удаления ветки можно использовать команду:
> **git branch -d branch-name**

она удалит ветку, если в ветке нет замерженных (объединенных) изменений. 

Иначе, нужно использовать ту же команду, только с большой D:

> **git branch -D branch-name**

она удалит ветку, несмотря на что :)

Можно посмотреть историю веток (визуально) с помощью:
> **git log --graph**

Чтобы увидеть разницу между текущим файлом и закомиченным (последним сохр), нужно:
> **git diff**

## ***Специально для создания конфликта!!!***   
Чтобы создать нумерованные списки, ставим цифру и точку. Например:
1. элемент 1
2. элемент 2
3. элемент 3

Чтобы создать ненумерованные списки, ставим * пробел, например:
* элемент 1
* элемент 2
* элемент 3

Иногда по директориям проекта встречаются файлы, которые не хочется постоянно видеть в сводке git status. Например, вспомогательные файлы текстовых редакторов, временные файлы и прочий мусор.
Заставить git status игнорировать определенные файлы можно, создав в корне или глубже по дереву (если ограничения должны быть только в определенных директория) файл .gitignore. В этих файлах можно описывать шаблоны игнорируемых файлов определенного формата.

Пример содержимого такого файла:

#все txt-файлы...
*.txt 

#все rar-файлы...
*.rar

#все файлы цифрой 1...
*.1

либо все в игнор
*

# **Работа с текстом**

Чтобы выделить заголовок используется (#). Количество (#) задает уровень заголовка (до 6). Например:
# Заголовок

"=" ИЛИ "-" подчеркиванием этими сомволами (не менее 3 подряд) выделяют заголовки первого ("=") и второго ("-") уровней.

две (**) или (__) **Полужирный текст** или __Полужирное начертание__

одна (*) или (_) - *Курсивный текст* или _курсивный текст_

три (***) - ***Полужирное курсивное начертание***

## Работа с удаленным репозиторием.

Для клонирования внешнего репозитория на
локальный ПК:
 > git clone <url-адрес репозитория>

 Для получения изменений и слияние с локальной версией с удаленного реп-рия:
 > git pull (тянуть)
 !!! НО Ветки сольются автоматичечски (Merge) !!!

Для отправки локальной версии репозитория на внешний:
> git push (толкать)




![мозг заработал](%D0%91%D0%9F.jpg)

Спасибо!