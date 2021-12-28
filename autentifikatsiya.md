# Аутентификация

### Настройка SSH-Key (Linux)

Необходимо сгенерировать ***ssh*** ключи: ***private*** и ***pubic***. 

Ключи будут размещены в домашней папке `~/.ssh`.

Выполним команду (на все запросы нажимаем Enter):

```console
$ ssh-keygen
```

Проверим, что ключи созданы

```console
console$ ll ~/.ssh/
```

Выведем в консоль содержимое публичного ключа

```console
$ cat ~/.ssh/id_rsa.pub
```

Скопируем все содержимое файла из консоли в буфер обмена и перейдем на сайт ***github.com*** в раздел настроек.

![Настройки](.\resurce\img-04.png)

![SSH-KEY](.\resurce\img-05.png)

Создадим новый ***ssh-key*** скопировав в него содержимое публичного ключа из буфера обмена.

### Настройка SSH-Key (Windows)

Установить оболочку [Git Bash](https://gitforwindows.org/). 

Выполнить действия аналогичные при настройке по Linux.

Место хранения ключей:

```console
C:\Users\<имя пользователя>\.ssh\id_rsa.pub
```

![SHH-KEY](.\resurce\img-08-shh-key.png)

### Перевод аутентификации с https на ssh-key

Посмотрим с какой ссылкой соединен наш локальный репозиторий:

```console
$ git remote -v
```
```console
learngit https://github.com/AndreyIvantsov/LearnGit.git (fetch)
learngit https://github.com/AndreyIvantsov/LearnGit.git (push)
```
Поменяем соединение на ***ssh***

```console
$ git remote set-url learngit git@github.com:AndreyIvantsov/LearnGit.git
```

![SHH](.\resurce\img-06-shh.png)

### Проверим соединение

```console
$ git remote -v
```

```
learngit git@github.com:AndreyIvantsov/LearnGit.git (fetch)
learngit git@github.com:AndreyIvantsov/LearnGit.git (push)
```


### Перевод аутентификации с ssh-key на https

Посмотрим с какой ссылкой соединен наш локальный репозиторий:

```console
$ git remote -v
```
``` 
learngit git@github.com:AndreyIvantsov/LearnGit.git (fetch)
learngit git@github.com:AndreyIvantsov/LearnGit.git (push)
```
Поменяем соединение на ***https***

```console
$ git remote set-url learngit https://github.com/AndreyIvantsov/LearnGit.git
```

![HTTPS](.\resurce\img-07-https.png)

### Проверим соединение

```console
$ git remote -v
```
```
learngit https://github.com/AndreyIvantsov/LearnGit.git (fetch)
learngit https://github.com/AndreyIvantsov/LearnGit.git (push)
```

