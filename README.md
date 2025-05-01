## Лабораторная работа 2
**Студента группы ИУ8-23**
**Лахтионова Александра**
## Часть 1
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

3. Создайте файл hello_world.cpp в локальной копии репозитория (который должен был появиться на шаге 2). Реализуйте программу Hello world на языке C++ используя плохой стиль кода. Например, после заголовочных файлов вставьте строку using namespace std;.
<details>
<p>
<summary>

```
$ cat > examples/Hello_world.cpp <<EOF
```

</summary>
</p>
<p>

```
> #include <iostream>
> using namespace std;
> int main(int argc, char** argv)
> {
> cout<<"Hello World \n";
> }
> EOF
```

</p>
</details>
4.Добавьте этот файл в локальную копию репозитория.

```
$ git add Hello_world.cpp
```

5. Закоммитьте изменения с осмысленным сообщением.
<details>
  <p>
  <summary> 

```
$ git commit -m"Hello world added"
```

</summary>
</p>
<p>

```
[master 44b94fb] Hello world added
 1 file changed, 6 insertions(+)
 create mode 100644 examples/Hello_world.cpp
```

</p>
</details>

6. Изменитьте исходный код так, чтобы программа через стандартный поток ввода запрашивалось имя пользователя. А в стандартный поток вывода печаталось сообщение Hello world from @name, где @name имя пользователя.
<details>
<p>
<summary>

```
$ nano Hello_world.cpp
```

</summary>
</p>
<p>

```
#include <iostream>
#include <string>
using namespace std;
int main(int argc, char** argv)
{
string name;
cout<<"Enter your name \n";
cin>>name;
cout<<Hello world from" <<name<<endl;
}
```

</p>
</details>

7. Закоммитьте новую версию программы. Почему не надо добавлять файл повторно git add?
<details>
<p>
<summary>

```
$ git commit -a
```

</summary>
</p>
<p>

```
[master 7b36c19] file
 1 file changed, 5 insertions(+), 1 deletion(-)
```

</p>
</details>

8. Запуште изменения в удалёный репозиторий.
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
Перечисление объектов: 9, готово.
Подсчет объектов: 100% (9/9), готово.
При сжатии изменений используется до 3 потоков
Сжатие объектов: 100% (6/6), готово.
Запись объектов: 100% (8/8), 845 байтов | 845.00 КиБ/с, готово.
Всего 8 (изменений 1), повторно использовано 0 (изменений 0), повторно использовано пакетов 0
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/Beedy1122/lab02.git
   b7883dd..7b36c19  master -> master
```

</p>
</details>

9. Проверьте, что история коммитов доступна в удалёный репозитории.

<details>
  <p>
  <summary> 

```
$ git log
```
  </summary>
  </p>
  <p>

```
commit 7b36c19e708e11043e9ca8ce62b396e4f2bf1ed1 (HEAD -> master, origin/master)
Author: Beedy1122 <sashabeedy@gmail.com>
Date:   Thu May 1 19:42:49 2025 +0300

    file

commit 44b94fb164e3c9370979a80102cd781decf2b843
Author: Beedy1122 <sashabeedy@gmail.com>
Date:   Thu May 1 19:35:59 2025 +0300

    Hello world added

commit b7883dd4ad7abd3858df474f609d86003ad6d99b
Author: Beedy1122 <sashabeedy@gmail.com>
Date:   Mon Apr 28 21:49:11 2025 +0300

    added README.md

commit a1fafb08bd9ce7c699e49ad095d996d5adc831f7 (origin/main)
Author: Beedy1122 <sashabeedy@gmail.com>
Date:   Thu May 1 18:36:19 2025 +0300
```

</p>
</details>

## Часть 2
1. В локальной копии репозитория создайте локальную ветку patch1.

<details>
  <p>
  <summary> 

```
$ git checkout -b 'patch1'
```

 </summary>
 </p>
 <p>

```
Переключились на новую ветку «patch1»
```

 </p>
</details>

2.Внесите изменения в ветке patch1 по исправлению кода и избавления от using namespace std;.
<details>
  <p>
  <summary> 

```   
$ nano Hello_world.cpp
$ cat Hello_world.cpp
```

</summary>
</p>
<p>

```
#include <iostream>
#include <string>
int main(int argc, char** argv)
{
std::string name;
std::cout<<"Enter your name \n";
std::cin>>name;
std::cout<<Hello world from" <<name<<std::endl;
}
```
</p>
</details>

3. commit, push локальную ветку в удалённый репозиторий.

```
$ git add Hello_world.cpp
```

<details>
<p>
<summary>

```
$ git commit -m"New Hello World in patch1"
```

</summary>
</p>
<p>

```
[patch1 b31bea4] New Hello World in patch1
 1 file changed, 4 insertions(+), 5 deletions(-)
```

</p>
</details>
<details>
<p>
<summary>

```
$ git push origin patch1
```

</summary>
</p>
<p>

```
Перечисление объектов: 7, готово.
Подсчет объектов: 100% (7/7), готово.
При сжатии изменений используется до 3 потоков
Сжатие объектов: 100% (3/3), готово.
Запись объектов: 100% (4/4), 393 байта | 393.00 КиБ/с, готово.
Всего 4 (изменений 2), повторно использовано 0 (изменений 0), повторно использовано пакетов 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote: 
remote: Create a pull request for 'patch1' on GitHub by visiting:
remote:      https://github.com/Beedy1122/lab02/pull/new/patch1
remote: 
To https://github.com/Beedy1122/lab02.git
 * [new branch]      patch1 -> patch1
```

</p>
</details>

4.Проверьте, что ветка patch1 доступна в удалёный репозитории.
 <details>
  <p>
  <summary> 

```
$ git log
```

</summary>
</p>
<p>

```
commit b31bea4f9565d50a2a79d3ef684556fe998cb1f1 (HEAD -> patch1, origin/patch1)
Author: Beedy1122 <sashabeedy@gmail.com>
Date:   Thu May 1 19:57:12 2025 +0300

    New Hello World in patch1

commit 7b36c19e708e11043e9ca8ce62b396e4f2bf1ed1 (origin/master, master)
Author: Beedy1122 <sashabeedy@gmail.com>
Date:   Thu May 1 19:42:49 2025 +0300

    file

commit 44b94fb164e3c9370979a80102cd781decf2b843
Author: Beedy1122 <sashabeedy@gmail.com>
Date:   Thu May 1 19:35:59 2025 +0300

    Hello world added

commit b7883dd4ad7abd3858df474f609d86003ad6d99b
Author: Beedy1122 <sashabeedy@gmail.com>
Date:   Mon Apr 28 21:49:11 2025 +0300

    added README.md

commit a1fafb08bd9ce7c699e49ad095d996d5adc831f7 (origin/main)
Author: Beedy1122 <sashabeedy@gmail.com>
Date:   Thu May 1 18:36:19 2025 +0300
Initial commit
```

</p>
</details>
5.Создайте pull-request patch1 -> master.
6. локальной копии в ветке patch1 добавьте в исходный код комментарии.
  <details>
  <p>
  <summary>

```
$ nano Hello_world.cpp
$ cat Hello_world.cpp
```

</summary>
</p>
<p>

```
#include <iostream>
#include <string>
int main(int argc, char** argv)
{
std::string name;
std::cout<<"Enter your name \n";
std::cin>>name;
std::cout<<Hello world from" <<name<<std::endl;//res
}
```

</p>
</details>

7.commit, push.
  <details>
  <p>
  <summary> 

```
$ git commit -a
```

</summary>
</p>
<p>

```
[patch1 10f7ccb] Commets
 1 file changed, 1 insertion(+), 1 deletion(-)
```

</p>
</details>
<details>
<p>
<summary>

```
$ git push origin patch1
```

</summary>
</p>
<p>

```
Перечисление объектов: 7, готово.
Подсчет объектов: 100% (7/7), готово.
При сжатии изменений используется до 3 потоков
Сжатие объектов: 100% (3/3), готово.
Запись объектов: 100% (4/4), 335 байтов | 335.00 КиБ/с, готово.
Всего 4 (изменений 2), повторно использовано 0 (изменений 0), повторно использовано пакетов 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Beedy1122/lab02.git
   b31bea4..10f7ccb  patch1 -> patch1
```

</p>
</details>

8. Проверьте, что новые изменения есть в созданном на шаге 5 pull-request
<details>
<p>
<summary>

```
$ git log
```

</summary>
</p>
<p>

```
commit 10f7ccb04653647774d2bf09e0d0e86d3fd4a02e (HEAD -> patch1, origin/patch1)
Author: Beedy1122 <sashabeedy@gmail.com>
Date:   Thu May 1 23:15:02 2025 +0300

    Commets

commit b31bea4f9565d50a2a79d3ef684556fe998cb1f1
Author: Beedy1122 <sashabeedy@gmail.com>
Date:   Thu May 1 19:57:12 2025 +0300

    New Hello World in patch1

commit 7b36c19e708e11043e9ca8ce62b396e4f2bf1ed1 (origin/master, master)
Author: Beedy1122 <sashabeedy@gmail.com>
Date:   Thu May 1 19:42:49 2025 +0300

    file

commit 44b94fb164e3c9370979a80102cd781decf2b843
Author: Beedy1122 <sashabeedy@gmail.com>
Date:   Thu May 1 19:35:59 2025 +0300

    Hello world added

commit b7883dd4ad7abd3858df474f609d86003ad6d99b
Author: Beedy1122 <sashabeedy@gmail.com>
Date:   Mon Apr 28 21:49:11 2025 +0300

    added README.md

commit a1fafb08bd9ce7c699e49ad095d996d5adc831f7 (origin/main)
Author: Beedy1122 <sashabeedy@gmail.com>
Date:   Thu May 1 18:36:19 2025 +0300

    Initial commit
```

</p>
</details>

9. В удалённый репозитории выполните слияние PR patch1 -> master и удалите ветку patch1 в удаленном репозитории.
10. Локально выполните pull.
  <details>
  <p>
  <summary> 

```
$ git checkout master
```

  </summary>
  </p>
  <p>

```
Переключились на ветку «master»
```

</p>
</details>
<details>
<p>
<summary>

```
$ git pull origin master
```

</summary>
</p>
<p>

```
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Распаковка объектов: 100% (1/1), 890 байтов | 890.00 КиБ/с, готово.
Из https://github.com/Beedy1122/lab02
 * branch            master     -> FETCH_HEAD
   7b36c19..fbd9713  master     -> origin/master
Обновление 7b36c19..fbd9713
Fast-forward
 examples/Hello_world.cpp | 9 ++++-----
 1 file changed, 4 insertions(+), 5 deletions(-)
```

</p>
</details>

 11. С помощью команды git log просмотрите историю в локальной версии ветки master.
    <details>
  <p>
  <summary> 

```
$ git log master
```

  </summary>
  </p>
  <p>
    
```
commit fbd9713b338290d556b3ff8fd5ecb8d813ceee7e (HEAD -> master, origin/master)
Merge: 7b36c19 10f7ccb
Author: Beedy1122 <sashabeedy@gmail.com>
Date:   Thu May 1 23:21:35 2025 +0300

    Merge pull request #1 from Beedy1122/patch1
    
    New Hello World in patch1

commit 10f7ccb04653647774d2bf09e0d0e86d3fd4a02e (origin/patch1, patch1)
Author: Beedy1122 <sashabeedy@gmail.com>
Date:   Thu May 1 23:15:02 2025 +0300

    Commets

commit b31bea4f9565d50a2a79d3ef684556fe998cb1f1
Author: Beedy1122 <sashabeedy@gmail.com>
Date:   Thu May 1 19:57:12 2025 +0300

    New Hello World in patch1

commit 7b36c19e708e11043e9ca8ce62b396e4f2bf1ed1
Author: Beedy1122 <sashabeedy@gmail.com>
Date:   Thu May 1 19:42:49 2025 +0300

    file

commit 44b94fb164e3c9370979a80102cd781decf2b843
Author: Beedy1122 <sashabeedy@gmail.com>
Date:   Thu May 1 19:35:59 2025 +0300

    Hello world added

commit b7883dd4ad7abd3858df474f609d86003ad6d99b
Author: Beedy1122 <sashabeedy@gmail.com>
Date:   Mon Apr 28 21:49:11 2025 +0300

    added README.md

commit a1fafb08bd9ce7c699e49ad095d996d5adc831f7 (origin/main)
Author: Beedy1122 <sashabeedy@gmail.com>
Date:   Thu May 1 18:36:19 2025 +0300

    Initial commit
```

</p>
</details>

12. Удалите локальную ветку patch1.
     <details>
  <p>
  <summary> 

```
$ git branch -D patch1
```

</summary>
</p>
<p>

```
Ветка patch1 удалена (была 10f7ccb).
```

</p>
</details>

## Часть 3
  
