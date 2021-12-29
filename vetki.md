# Ветки Git

### Добавление новой ветки 

![Ветки](.gitbook\assets\img-03-vetki.png)


Добавляем новую ветку **dev**

`$ git branch dev`

### Просмотр существующих веток

`$ git branch`

\* master    _<-- текущая ветка_
   dev

### Переключение между ветками

`$ git checkout <имя ветки>`

Переключимся на ветку **dev**

`$ git checkout dev`

Посмотрим какая ветка активна в данный момент

`$ git branch`

   master
\* dev       _<-- текущая ветка_

### Слияние веток (merge)

Если необходимо внести изменения в основную ветку master из ветки разработчика develop выполним следующие действия:

1. Перейдем в основную ветку

   `$ git checkout master`
   
2. Внесем изменения из ветки **dev** в ветку **master**

   `$ git merge develop`

### Удаление ненужной ветки

`$ git branch -D <имя удаляемой ветки>`

`$ git branch --delete <имя удаляемой ветки>`

`$ git branch -D dev`

`$ git branch --delete dev`
