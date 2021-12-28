# Основные команды

### Создание удаленного репозитория
На github.com создаем новый репозиторий:

![Создание удаленного репозитория](.\resurce\img-02.png)

### Клонирование существующего репозитория (clone)

Перейти в папку где планируется создать папку с будущим проектом

```console
$ git clone <url>
```
```console
$ git clone https://github.com/AndreyIvantsov/LearnGit
```
```console
$ git clone git@github.com:AndreyIvantsov/LearnGit.git
```

![Ссылка на репозиторий](.\resurce\img-01.png)

### Инициализация Git для проекта

В папке проекта выполняем команду (далее все команды
выполняются в папке проекта)

```console
$ git init
```

### Связь локального репозитория c адресом удаленного репозитория

```console
$ git remote add origin https://github.com/AndreyIvantsov/LearnGit
```
```console
$ git remote add origin git@github.com:AndreyIvantsov/LearnGit.git
```

Для того, чтобы посмотреть какие удаленные репозитории у нас имеются на данный момент, можно воспользоваться командами:

```console
$ git remote
```
```console
$ git remote -v
```

### Добавление файлов проекта в Git

Для того, чтобы изменения в файлах проекта отслеживались в Git, необходимо добавить их в локальный репозиторий.

```console
$ git add <file_name>
```
```console
$ git add -all
```
```console
$ git add .
``` 

### Игнорирование файлов
Создаем файл: **.gitignore**
Содержимое файла может быть примерно таким (для Java –проекта):
```
.idea/*
*.class
*.war
*.jar
*.ear
```
Далее добавляем данный файл в локальный репозиторий:

```console
$ git add .gitignore
```

### Посмотреть статус проекта

```console
$ git status
```

### Внесение изменений в Git (commit)

После того, как все необходимые файлы добавлены в локальный репозиторий для отслеживания Git мы можем зафиксировать все изменения, сделанные в проекте.

```console
$ git commit -m “Initial commit of the project”
```

Убедимся, что вес изменения внесены

```console
$ git status
```

### Отправка изменений в удаленный репозиторий (push)

```console
$ git push <имя репозитория> <ветка>
```
```console
$ git push origin main
```

Перед внесением изменения Git запросит имя пользователя и пароль, если не настроен ssh-key.

### Получение изменений из удаленного репозитория (pull)

```console
$ git pull <имя репозитория> <ветка>
```
```console
$ git pull origin master
```

### Посмотреть историю изменений

```console
$ git log
```

Расширенная информация

```console
$ git log -p
```

### Добавление версии проекта

```console
$ git tag “ver_1.0”
```
