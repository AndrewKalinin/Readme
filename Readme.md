# Инструкция по работе с Git

## Что такое Git?

Git - одна из реализаций распределенных систем контроля версий, имеющая как локальную версионность, так и версионность на сервере. Git является самой популярной системой контроля версий на сегодняшний день. 

## Подготовка репозитория

Для того, чтобы создать указанный репозиторий в папке используется команда *git init*. Для этого достаточно написать команду *git init* в папке с будущим репозиторием.

## Создание фиксаций

### Создание коммитов
Для создания новой фиксации необходимо использовать команду *git commit*. Используется она следующим образом: в папке с репозиторием пишется команда *git commit -m "<Сообщение к коммиту>*. Все файлы к коммиту должны быть предворительно добавлены с помощью комманды *git add*. Сообщение к коммиту писать ***ОБЯЗАТЕЛЬНО!***

### Добавление файла к коммиту
Для того, чтобы добавить новый файл к коммиту ("сохранению") необходимо использовать команду *git add*. Используется она следующим образом: в папке с репозиторием пишем команду *git add <имя файла>*.

### Просмотр информации об изменениях
Для того, чтобы посмотреть информацию об изменениях, сделанных в текущей ветке, необходимо использовать команду *git status*. Для этого достаточно использовать *git status* в папке с репозиторием.

## Перемещение между сохранениями

Для переключения между сохранениями (коммитами), необходимо использовать команду *git checkout* следующим образом: *git checkout <номер коммита для переключения>*. Номер коммита берётся из истории коммитов и на него произойдёт переключение.

## Журнал изменений

Для просмотра журнала изменений используется команда *git log*. С её помощью выводятся на экран все ранее сохраненные изменения и коммиты. Если коммитов большое количество, то, как правило, сначала выводятся три последних сохраненных коммита.

## Ветки в Git

Ветки создаются командой *git branch <имя ветки>*. Для перехода на нужную ветку используется команда *git checkout <имя ветки перехода>*. Для того, чтобы проверить в какой ветке находится пользователь используется команда *git branch*.

## Слияние веток и разрешение конфликтов

### Слияние веток
Слияние веток производится командой *git merge <имя объединяемой ветки>*. Данная команда производится из основной ветки, куда должно произойти слияние.

### Разрешение конфликтов

Конфликты при слиянии разрешаются либо вручную, либо с помощью вариантов, предложенных системой *объединить с заменой*, *оставить оба варианта* и т.д. 

## Удаление веток

Удаление веток производится из основной ветки с помощью команды *git branch -d <имя удаляемой ветки>*. Также, возможно безусловное удаление ветки без слияния с помощью команды *git branch -D <имя удаляемой ветки>*. (**Не рекомендуется для использования**).

## Работа с удаленными репозиториями

### Настройка и начало работы
1. Создать аккаунт на github.com.
2. Создать локальный репозиторий.
3. Объединить локальный и удаленный репозитории. Github при создании репозитория подскажет как это сделать.
4. С помощью команды *git push* отправить локальный репозиторий на удаленный. Возможно потребуется авторизация на Github.
5. Внести изменения с локального компьютера на удаленный сервер github.
6. С помощью команды *git pull* скачать актиальное состояние с удаленного репозитория.

### Работа с новой веткой в удаленном репозитории
1. На платформе Github c помощью команды *fork* создается новое ветвление, в интересующем нас репозитории.
2. С помощью команды *git clone* создаем дубликат необходимого репозитория.
3. Создаем новую ветку с предлагаемыми изменениями. Все изменения производятся только в данной ветке.
4. С помощью команды *git push* отправляем новые изменения в свой аккаунт на платформе Github.
5. На платформе появляется возможность предложить ваши изменения создателю репозитория. Кнопка *pull request*.