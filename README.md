## Лабораторная работа 2
**Студента группы ИУ8-23**
**Лахтионова Александра**
##Часть 1
1. Создайте пустой репозиторий на сервисе github.com (или gitlab.com, или bitbucket.com).
2. Выполните инструкцию по созданию первого коммита на странице репозитория, созданного на предыдещем шаге.

 ```
 $ mkdir projects/lab02 && cd projects/lab02
```
<details>
<p>
<summary>

```
$git init
```

</summary>
</p>
<p>

```
Инициализирован пустой репозиторий Git в /home/alex/projects/lab02/.git/
```

</p>
</details>

```
$ git remote add origin https://github.com/${GITHUB_USERNAME}/lab02.git
```

<details>
<p>
<summary>

```
& git pull origin main
```

</summary>
</p>
<p>

```
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Распаковка объектов: 100% (3/3), 1.43 КиБ | 1.43 МиБ/с, готово.
Из https://github.com/Beedy1122/lab02
 * branch            main       -> FETCH_HEAD
 * [новая ветка]     main       -> origin/main
```

</p>
</details>

```
$ touch README.md
```

```
$ git add README.md
```

<details>
<p>
<summary>

```
$ git commit -m"added README.md"
```

</summary>
</p>
<p>

```
[master b7883dd] added README.md
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 README.md
```

</p>
</details>
<details>
<p>
<summary>

```
$ git push origin master
```

</summary>
</p>
<p>

```
Перечисление объектов: 4, готово.
Подсчет объектов: 100% (4/4), готово.
При сжатии изменений используется до 3 потоков
Сжатие объектов: 100% (2/2), готово.
Запись объектов: 100% (3/3), 279 байтов | 279.00 КиБ/с, готово.
Всего 3 (изменений 0), повторно использовано 0 (изменений 0), повторно использовано пакетов 0
remote: 
remote: Create a pull request for 'master' on GitHub by visiting:
remote:      https://github.com/Beedy1122/lab02/pull/new/master
remote: 
To https://github.com/Beedy1122/lab02.git
 * [new branch]      master -> master
```

</p>
</details>
