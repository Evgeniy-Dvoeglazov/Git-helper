# Шпаргалка по Git

## Базовые команды в консоли

### Навигация

```
pwd - показать, что в папке
ls -a - показать файлы в текещей папке (включая скрытые)
cd first-project - перейти в папку first-project
cd .. - перейти на уровень выше
сd ~ - перейти в домашнюю директорию
св / - перейти в корневую директорию
```

### Работа с файлами и папками

```
touch index.html - создать файл index.html в текущей папке
mkdir second-project - создать папку в текущей папке
cp file.txt ~/my-dir - копировать файл в my-dir
mv file.txt ~/my-dir - переместить файл в my-dir
cat file.txt - посмотреть содержимое текстового файла
rm about.html - удалить файл
rmdir images - удалить папку
rm -r second-project - удалить папку вместе с содержимым
&& - можно указывать сразу несколько команд, разделяя их двумя амперсандами 
```

### Инициализируем репозиторий

```
git init - делает текущую папку репозиторием
rm -rf .git - "разгитить" папку
git status - посмотреть текущее состояние репозитория
```

### Добавляем файлы в репозиторий и делаем коммит

```
git add readme.txt - подготовить к сохранению файл readme.txt
git add --all - подготовить все файлы к сохранению
git add . - подготовить к сохранению всю текущую папку
git commit -m "Сообщение коммита" - создать коммит и сохранить изменения в истории
git push - отправить изменения на удаленный репозиторий
git log - посмотреть историю коммитов 
```

### Как исправить коммит

```
git commit --amend --no-edit - дополнить коммит новыми или измененными файлами, не исправляя сообщение
git commit --amend -m "Новое сообщение" - дополнить коммит и изменить сообщение
```

### Выполнить unstage изменений

```
git restore --staged <file> - убирает файл из staging area
git restore --staged . - убирает из staging все файлы текущей папки
```

### «Откатить» коммит 

```
git reset --hard <commit hash> - возвращает к более раннему состоянию репозитория (удаляет последующие коммиты)
```

### «Откатить» изменения, которые не попали ни в staging, ни в коммит

```
git restore <file> - возвращает файл к состоянию последнего коммита
```

## Генерация SSH-ключа для GitHub

```
ssh-keygen -t ed25519 -C "электронная почта, к которой привязан ваш аккаунт на GitHub"
ls -a ~/.ssh - проверить ключи
clip < ~/.ssh/id_ed25519.pub - скопировать содержимое ключа в буфер обмена
cat ~/.ssh/id_ed25519.pub - показать содержимое ключа для копирования вручную
```