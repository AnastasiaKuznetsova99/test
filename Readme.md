# Инструкция для работы с Git и удалёнными репозиториями


![гит](Git-logo.jpg)

## Что такое Git?
Git - это одна из реализаций распределённых систем контроля версий, имеющая как и локальные, так и удалённые репозитории. Является самой популярной реализацией систем контроля версий в мире.
## Подготовка репозитория
Для создание репозитория необходимо выполнить команду *git init*  в папке с репозиторием и у Вас создаться репозиторий (появится скрытая папка .git)

## Создание коммитов

### Git add
Для добавления измений в коммит используется команда *git add*. Чтобы использовать команду *git add* напишите *git add *имя файла*

### Просмотр состояния репозитория
Для того, чтобы посмотреть состояние репозитория используется команда *git status*. Для этого необходимо в папке с репозиторием написать *git status*, и Вы увидите были ли измения в файлах, или их не было.

### Создание коммитов
Для того, чтобы создать коммит(сохранение) необходимо выполнить команду *git commit*. Выполняется она так: *git commit -m "*сообщение к коммиту*". Все файлы для коммита должны быть ***ДОБАВЛЕНЫ*** и сообщение к коммиту писать ***ОБЯЗАТЕЛЬНО***.

## Перемещение между сохранениями
Для того, чтобы перемещаться между коммитами, используется команда *git checkout*. Используется она в папке с пепозиторием следующим образом: *git checkout *номер коммита*

## Журнал изменений
Для того, чтобы посмтреть все сделанные изменения в репозитории, используется команда *git log*. Для этого достаточно выполнить команду *git log* в папке с репозиторием

## Изображения в Git

### Добавление картинки

Для того, чтобы добавить картинку нужно ее скачать с интернета и добавить в редактируемую папку, тогда чтобы вставить изображение в текст достаточно написать следующее:

![] ()

В квадратных скобках мы указываем текст, который будет отображаться, если картинка не загрузится. В круглых скобках нужно писать имя файла картинки с расширением, например, Картинка.png

### Добавление файлов в Git

Обычно текстовые файлы и все остальные файлы, например, с изображениями, хранятся отдельно. Поэтому, чтобы Git не добавлял изображение и не следил за этим файлом, нужно его добавить в папку игнорирования. Для этого:
* Создаем файл в нашей папке с именем .gitignore;
* Добавляем в него наш файл с изображением;
* Сохраняем файл.

**Важно!** Не допустить ошибки в названии файла, т.е. название пишется через точку .gitignore.

Теперь нам нужно этот файл закоммитить:

* Выполняем команду git add .gitignore
* Далее выполняем команду git commit -m "*Сообщение*"

Если мы посмотрим статус, то все файлы, которые добавлены в файл .gitignore не добавляются в репозиторий и Gti их игнорирует.

## Ветки в Git

### Создание ветки

Для того, чтобы создать ветку, используется команда *git branch*. Делается это следующим образом в папке с репозиторием: *git branch *название новой ветки*

## Слияние веток

Для того чтобы дабавить ветку в текущую ветку используется команда *git merge "*name branch*". Для этого сначала переходим в ту ветку, в которую хотим слить информацию из ветки "черновик" и в команже git merge *"имя ветки "черновика""*.

## Конфликт при слиянии веток

Если мы хотим с одной ветки "черновик" слить информацию в ветку "чистовик", но при этом мы вносили изменения в ветку "чистовик", тогда может произойти CONFLICT. Нам нужно самостоятельно разрешить его и выбрать: принять текущую версию, входящие изменения (то, что пришло с другой ветки) или оставить оба варианта и вручную отредактировать.

## Визуализация всех имеющихся коммитов (веток)

Для того, чтобы увидеть дерево коммитов, нужно ввести команду "git log -graph".

Если ветки "черновики" исполнили свою роль, мы их удаляем.

## Удаление веток
Для удаления ветки ввести команду "git branch -d 'name branch'"