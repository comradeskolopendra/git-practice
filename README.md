# Git-yandex-practice

## Команды консоли.

_clip_ - команда для копирования в буфер обмена из файла указанном в аргументе: (где test.txt - файл, откуда было скопировано содержимое)

```bash
clip < test.txt
```

---

_cd_ - навигация по папкам. В аргумент принимает название папки: (где test - папка, в которую хотим перейти)

```bash
cd test/
```

---

_pwd_ - показывает путь до текущей директории, начиная с корневой:

```bash
pwd
```

---

_ls_ - показывает содержание текущей директории:

```bash
ls
```

Вызов команды _ls_ флагом _-a_ - показывает скрытые файлы:

```bash
ls -a
```

---

_mkdir_ - создать директорию (по умолчанию в текущей директории). В аргумент принимает название новой директории: (где test - название новой директории)

```bash
mkdir test/
```

---

_touch_ - создать файл (по умолчанию в текущей директории). В аргумент принимает название нового файла и так же принято писать расширение нового файла: (где test.txt - название нового файла)

```bash
touch test.txt
```

---

_cp_ - копирует файлы из одной директории в другую. Принимает 2 аргумента:

-   Название файла в текущей директории. (может быть несколько)
-   В какую директорию необходимо скопировать файлы.

В примере скопировали _test.txt_ из текущей директории в дочернюю директорию _src_.

```bash
cp test.txt ./src
```

---

_mv_ - перемещение файлов и директорий(может быть несколько). Принимает 2 аргумента:

-   Название файла для перемещения в текущей директории (может быть несколько)
-   В какую директорию необходимо переместить.

В примере переместили _test.txt_ из текущей директории в корневую _~_.

```bash
mv test.txt ~
```

---

_rm_ - удалить файл. В аргумент принимает название файла: (где test.txt - назваие файла)

```bash
rm test.txt
```

---

_rmdir_ - удалить пустую **!** директорию. В аргумент принимает название директории: (где test - название директории)

```bash
rmdir test/
```

---

_rm -r_ - удалить директорию с файлами. Флаг _-r_ означает, что команда _rm_ будет применена рекурсивно для каждой поддиректории.

Сначала будут удалены все файлы внутри одной директории, а затем сама директория,
до тех пор, пока не удалится указанная в аргументе директория: (где test - название директории)

```bash
rm -r test
```

---

_cat_ - вывести в консоль содержимое файла. В аргумент принимает название файла: (где test.txt - название файла)

```bash
cat test.txt
```

*echo* - вывести в консоль строку, переданную в в аргумент:
```bash
echo "Привет!"
```
*echo* может так же записывать с символами перенаправления вывода (*>>*), и тогда она запишет аргумент в файл, указанный вторым аргументом:
```bash
echo "Привет!" >> test.txt
```
Перенаправление - это в целом возможность всего bash'а, и его можно использовать с любой другой командой, которая выводит что-то на экран.
Одинарный символ *>* тоже перенаправит вывод, но перед этим очистит файл:
```bash
echo "Привет!" > test.txt
```

## SSH-ключи:

_ssh-keygen -t ed25519 -C "email"_ - команда для генерации пары ssh-ключей: (ed25519 - кодировка ключа. она может быть разной)

```bash
ssh-keygen -t ed25519 -C "email"
```

Публичный ключ - шифрует данные. Им можно поделиться.

Приватный ключ - расшифровывает данные. Им НЕЛЬЗЯ делиться!

SSH-ключи позволяют предоставить доступ к интернет-ресурсам, как например к GitHub`у.

## GIT && GitHub.

Git - система контроля версий. Консольный инструмент - _CLI_.

GitHub - место хранения удаленных репозиториев. Это платформа, которая упрощает командное взаимодействие GIT`ом

## Команды GIT.

_git init_ - инициализирует гит в текущей директории:
.git папка скрыта, но её можно увидеть с помощью `ls -a`.

**При случайной инициализации** - можно удалить директорию .git с помощью `rm -r .git` и тогда папка "отгититься".

```bash
git init
```

---

_git remote add_ - связать удаленный репозиторий с локальным. В аргумент принимает 2 параметра:

-   Имя удаленного репозитория - обычно указывается origin.
-   Его URL

```bash
git remote add origin URL
```

---

_git remote -v_ - проверить связку удаленного и локального репозитория. Флаг _-v_ является сокращением от _--verbose_ (то есть, подробный, подробное описание):

```bash
git remote -v
```

---

_git add_ - подготовить файлы к сохранению. В аргументы принимает список файлов, которые нужно подготовить.
Или же можно подготовить всю текущую директории с помощью `.`, или же с помощью флага _--all_

```bash
git add . || git add --all || git add README.md
```

---

_git commit_ - сохранить файлы (закоммитить файлы). Обычно применяется с флагом _-m_ - данный флаг позволяет добавить информативное сообщение к коммиту.
Принимает в аргументы сообщение для коммита.

```bash
git commit -m "message"
```

---

_git push_ - отправить сохраненные файлы (коммит) в удаленный репозиторий: (где branch_name - имя ветки, в которую нужно отправить изменения)

```bash
git push origin branch_name
```

## Markdown.

`*cursive* || _cursive_` - сделать текст курсивным.

`**bold** || __bold__` - сделать текст жирным.

`~~crossed~~` - зачеркнутый текст.

`<br>` - сделать переход на новую строку (или 2 пробела).

`1. первый пункт  2. второй пункт` - создать нумированный список (цифры + пробел).

`( - || * ) первый пункт 
( - || * ) второй пункт ` - создать ненумированный список (1 символ в скобках + пробел).

## Ссылка:

`[Яндекс](https://yandex.ru)` - создание ссылки.

-   В квадратных скобках написано то, как будет отображаться ссылка.
-   В круглых - адрес ссылки.

`[Яндекс](https://yandex.ru "Яндекс!")` - после адреса ссылки можно написать в кавычках подсказку при наведении.

## Код:

` ```test``` ` - в тройных кавычках можно записать код.

Стоит указать язык после первой тройки.

Вторая (и последняя) тройка должна находится на отдельной строке.

## Коммиты

## Хеш - идентификатор коммита.

**Хеширование** - это способ преобразить набор данных и получить их _отпечаток_ (fingerprint - идентификатор).
Информация о коммите - это набор данных: когда был сделан коммит, содержимое файлов в репозитории на момент коммита и ссылка на предыдущий коммит.
Git хеширует инфомрацию о коммите с помощью алгоритма SHA-1.
Обычно хеш - небольшая строка, состоящая из цифр 0-9 и латинских буква A-F (регист не важен).
Если хеш получить дважды для одного и того же набор данных - то он будет одинаковый гарантировано.
Если что-то изменилось в исходных данных - то хеш тоже изменится (достаточно сильно изменится).

Git хранит таблицу соответствий _хеш -> информация о коммите_. Если есть хеш - есть информация и о авторе коммита, дате и содержимом коммита.
Хеш - основной идентификатор коммита.
Хеш можно передавать разным git-командам, чтобы указать, с каким коммитом нужно произвести то или иное действие.
Все хеши и таблицу соответствий Git хранит в скрытой директории .git, внутри проекта.

## Исследуем лог

_git log_ - команда для отображения списка коммитов в проекте.

```bash
git log
```

Описание состоит из:

-   Строка из цифр и латинских букв (A-F) после слова коммит - хеш коммита.
-   Author - имя автора и его электронная почта.
-   Date - дата и время создания коммита.
-   В конце обычно находится сообщение коммита.

_git log --oneline_ - команда для получения сокращенного списка коммитов в проекте.

```bash
git log --oneline
```

Сокращенный хеш, полученный с помощью `git log --oneline`, можно использовать так же, как и обычный хеш.
Команда старается подобрать такую длину сокращенных хешей, чтобы они были уникальными в пределах репозитория и Git всегда мог понять, о каком коммите идет речь.
Количество символов в сокращенном хеше - автоматически подбирается оптимальное количество.

## HEAD - всему голова.

_HEAD_ - один из служебных файлов папки .git. Он указывает на коммит, который был сделан последним (самый новый). <br>
Если вывести в консоль последние HEAD при помощи cat, то там будет ссылка на служебный файл (refs/heads/master). <br>
Если же заглянуть в этот файл, то можно увидеть хеш последнего коммита. <br>
Когда делается новый коммит - git обновляет refs/heads/master - записывает в него хеш последнего коммита. Соответственно, HEAD тоже обновляется. <br>
При работе с gitом указатель `HEAD` упоминается достаточно часто. Для команд, в которых используется аргументом хеш коммита - можно передать аргумент HEAD,
и .git поймет, что мы обращаемся к последнему коммиту. <br>

## Статусы файло в Git.

Одна из ключевых задач git - отслеживать изменение файлов в репозитории. Для этого каждый файл помечается каким-либо статусом:

-   untracked - неотслеживаемый. Гит видит, что такое файл существует, но не следит за изменениями в нем. У файла с этим статусом нет предыдущих версий.
-   staged - подготовленный к коммиту. После выполнения `git add` - файл попадает в "staged area", то есть в список файлов, которые попадут в коммит. Иногда состояния staged могут называть indexed или cached.
-   tracked - противоположность untracked. В этот статус попадают все файлы, которые уже были зафиксированы с помощью `git commit` или добавлен в staged area с помощью `git add`. То есть, в этом статусе все файлы, в которых гит отслеживает изменения.
-   modified - состояние modified означает, что git сравнил содержимое файла с последней сохраненной версией в проекте и нашел изменения.
    Для файлов со статусом staged и modified обычно не указывают, что они так же со статусом tracked, но это подразумевается.
<br>
Команда `git add` добавляет в staged area только текущее содерижмое файла. Если этот же файл будет изменен после попадания в staged area - содержимое файла не будет находится staged area. Git сообщает о таком посредством статуса modified. Чтобы снова добавить файл staged area - нужно вновь прописать команду `git add`
<br>

Жизненный цикл файла в git:
<br>

-   Файл создан. Гит ещё не отслеживает изменения в этом файле (untracked).
-   Файл был добавлен в staged area с помощью `git add` (staged + tracked). Возможно файл изменили после добавления в staged area (staged, modified + tracked). Состояние staged и modified у одного и того же файла, но у разных его версий. После выполнения `git add` снова статус снова меняется (staged + tracked)
-   Сделали коммит с помощью команды `git commit` (tracked).
-   Изменили закомиченный файл (modified + tracked).
-   Снова добавили в staged area с помощью `git add` (staged + tracked).
-   Сделали коммит (tracked).

## Как читать git status.

`git status` - показывает только следующие состояния файлов:

-   _staged_ - файлы подготовлены к сохранению
-   _modified_ - файлы были изменены после
-   _untracked_ - неотслеживаемые файлы

_tracked_ статус не отслеживается, потому что каждый раз при `git status` выводились бы все файлы проекта.

## Оформление сообщений к коммитам.

При выводе команды `git log --oneline` умещается максимум 72 первых символа сообщения, поэтому хорошим тоном будет уместить все в 72 символа.
Сообщение коммита должно быть:

-   относительно коротким.
-   легкочитаемым.
-   информативным.

В корпоративном стиле в начале сообщения оыбчно указывают Jira-ID, а после текст сообщения:

```bash
git commit -m "LGS:259: Дополнить список пасхалок новыми числами"
```

Есть так же стандарт Convential Commits - он отличается качественной документацией и подробной проработкой.
Convential Commits предлагает следующий формат коммита `<type>: <message>`, где type - это тип изменений. Примерый типов изменений:

-   _feat_ - для новой функциональности
-   _fix_ - для исправления ошибок.
    Пример такого стиля может быть:

```bash
git commit -m "feat: добавить подсчет суммы заказов за неделю"
```

Помимо, встречается и GitHub-стиль. В Github можно вести так же и список задач. Если коммит закрывает или решает какую-то задачу - то в сообщении удобно указывать ссылку на неё. Для этого в сообщении коммита нужно написать `#<номер задачи>`. Пример:

```bash
git commit -m "Исправить #324, добавить график температуры"
```

## Mermaid-тест.

```mermaid
  graph TD;
      A-->B;
      A-->C;
      B-->D;
      C-->D;
```

## Как исправить коммит.
Иногда в только что созданном коммите нужно что-то поменять - например, добавить ещё пару файлов или заменить сообщение на другое.
Правки в уже сделанный коммит можно добавить с помощью опции `--amend` у команды `git commit`. <br>
`--amend` - работает только с последним коммитом (HEAD).
<br>
Дополнить коммит новыми файлами можно с помощью `git commit --amend -- no-edit`. C опцией `--amend` команда `git commit` не создаст новый коммит, а дополнит последний. Опция `--no-edit` же говорит о том, что сообщение коммита нужно оставить как было.
С помощью `git commit --amend --no-edit` можно так же добавить не новый файл, а исправленную версию того, который был в коммите до этого:
```bash
git add main.html
git commit --amend --no-edit
```

Возможно, вместо того, чтобы добавить или изменить файлы в коммите нужно просто поменять сообщение. 
Для этого можно воспользоваться командой.:
```bash
git commit --amend -m "<Новое сообщение>"
```

Если же забыть добавить к `git commit --amend` один из флагов: `--no-edit` или `-m`, то Git предложит отредактировать сообщение коммита вручную.
Для этого он откроект текстовый редактор, который установлен в системе вручную.

## Как откатиться назад, если "все сломалось".
Чтобы убрать из staged area файл нужно использовать команду - `git restore --staged <file>`. (от англ. restore - восстановить).
Перевел test.txt из статуса staged обратно в untracked:
```bash
git restore --staged test.txt
```

Чтобы сбросить все файлы из staged обратно untracked/modified нужно прописать команду `git restore --staged .`.
Данная команда сбросит всю текущую директорию.

Чтобы "откатить" коммита - можно воспользоваться командой `git reset --hard <commit hash>`,
где commit hash - хэш коммита, на которой мы хотим откатиться. Например, если мы хотим убрать последний коммит, то нужно откатиться до предпоследнего коммита.
```bash
git reset --hard <commit hash>
```

Коммит, который мы перескачили был удален. Это может показать команда `git log`. Последующая разработка же будет вестить от коммита, на который мы перешли.
При работе с командой `git reset --hard <hash>` стоит быть осторожным!

Чтобы откатить файл, который находится и не в статусе staged, и не в tracked, а в untracked и modified, то можно воспользоваться командой `git restore <file>`.
Данная команда вернет файл к последней версии, которая была сохранена через `git commit` или `git add`.

**RESTORE РАБОТАЕТ С ФАЙЛАМИ, А RESET - С КОММИТАМИ**

### Просматрвиаем изменения в файлах.
`git diff` - команда git, которая позволяет увидеть изменения между коммитами или между коммитом и локальным репозиторием.
При введении команды `git diff` выведет изменения, произошедшие в локальном репозитории по отношению к последнему коммиту.

Как читать лог команды `git diff`:
- строки `diff --git a/.. b/..` и `index 901da07..aca451 100644` - низкоуровненвая тех. информация.
- строки ---a/test.txt и +++b/test.txt говорят о том, что дальше будет выведен результат сравнения файлов a/test.txt и b/test.txt - исходной и текущей версии.
- строка `@@ -1,2 +1,2 @@` - говорит, что были использованы две строки, начиная с первой. Другой пример, +15,7 - это значит, что участвуют 7 строк начиная с 15-ой. `@@ +<с какой строки>,<сколько строк> @@`.

NOTE: Некоторый диапазон строк позволяет строк в `git diff` нужен для понимания контекста изменений - для чего и почему эти изменения были применены.

По-умолчанию команда `git diff` не показывает изменения в файлах, которые находятся в staged area.
Для того, чтобы посмотреть изменения в файлах со статусом staged нужно применить команду `git diff` с опцией `--staged`:
```bash
git diff --staged
```

## Сопоставляем коммиты.
с помощью команды `git diff` мы можем сравнивать два коммита, передав хэши коммитов в аргументы:
```bash
git diff <first commit hash> <second commit hash>
```
Если мы хоотим сравнить один из предыдущих коммитов с самым последним, то в качестве аргумента одного из хешей можно передать алиас HEAD, ибо он хранит в хеш самого последнего коммита.

По сути, команда `git diff A B` выведет, как превратить состояние A в состояние B.