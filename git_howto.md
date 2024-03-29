# Подсказка по Git


## Начало работы

Первая команда для инициализации Git
```sh
git init
```

Указывает имя пользователя работающего с Git
```sh
git config --global user.name "Alexey"
```

Указывает email пользователя работающего с Git
```sh
git config --global user.email "alexey@gmail.com"
```

Просмотр содержания переменной Git
```sh
git config user.email
```
## Работа с Git
Узнать текущий статус Git
```sh
git status
```

Показывает отличия
```sh
git diff
```

Добавление файла для отслеживания в Git
```sh
git add cmd.md
```

Создаем commit
```sh
git commit -m "Создали репозитарий"
```

Посмотреть информацию об архиве (видим хеш коммита)
```sh
git log
```
Выйти из просмотра можно по клавише "q"

Посмотреть информацию об архиве в укороченном виде
```sh
git log --oneline
```

Узнать информацию об архиве с элементами визуализации
```sh
git log --graph
```


## Работа с ветками

Переключение в состояние указываемое хешем или названием
```sh
git checkout <имя ветки>
```

Переключение в нужную ветку
```sh
git checkout master
```

Отменяем все изменения до предыдущей фиксации
```sh
git restore
```

Отображение всех веток
```sh
git branch
```

Создать новую ветку
```sh
git branch text_formatting
```

Соединить две ветки (Вызываем из той ветки, куда сливаем)
```sh
git merge lists
```

Удаление ветки
```sh
git branch -d branch_to_delete
```

Все файлы, которые необходимо игнорировать можно перечислить в файле .gitignore
Сам файл .gitignore необходимо включить в архив с помощью команды "git add .gitignore"


## Создание удаленного репозитария

1. Создали аккаунт на Github.com
2. Создать локальный репозиторий
3. "Подружить" ваш локальный и удаленный репозитории. GitHub при создании нового репозитория подскажет как это можно сделать)
4. Отправить (push) ваш локальный репозиторий в удаленный (на Github), при этом вам, возможно, нужно будет авторизоваться на удаленном репозитории.
5. Провести изменения "с другого компьютера".
6. Выкачать (pull) актуальное состояние из удаленного репозитория.

## Добавление исправлений в чужой репозиторий

1. Делаем форк (fork) интересующего нас аккаунта.
2. Мы делаем git clone для нашей версии этого репозитория.
3. Мы создаем ветку с предлагаемыми изменениями.
4. Производим все изменения только в этой ветке.
5. Отправляем эти изменения на свой аккаунт (push).
6. В окне на GitHub появляется возможность отправить pull request.