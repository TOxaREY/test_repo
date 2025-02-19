## Основные команды Git 
### Создание репозитория:
```
$ git init
```
### Проверка состояние репозитория:
```
$ git status
```
### Подготовка файлов к сохранению:
```
$ git add --all
```
### Сделать коммит:
```
$ git commit -m 'Мой первый коммит!'
```
### Просмотреть историю коммитов:
```
$ git log
```
```
$ git log --onelane //сокращенный log
```
### Файл HEAD:
Внутри HEAD — ссылка на служебный файл: refs/heads/master (или refs/heads/main в зависимости от названия ветки). Если заглянуть в этот файл, можно увидеть хеш последнего коммита.
### Статусы untracked/tracked, staged и modified:


```mermaid
graph LR;
  untracked -- "git add" --> staged(+ tracked);
  staged(+ tracked) -- "git commit" --> tracked;
  tracked -- "изменения" --> modified (+ tracked);
  modified -- "git add" --> staged(+ tracked);

```  