# Git-yandex-practice

## Команды консоли.
*clip* - команда для копирования в буфер обмена из файла указанном в аргументе: (где test.txt - файл, откуда было скопировано содержимое)
```bash
clip < test.txt
```
---
*cd* - навигация по папкам. В аргумент принимает название папки: (где test - папка, в которую хотим перейти)
```bash
cd test/ 
```
---
*pwd* - показывает путь до текущей директории, начиная с корневой:
```bash
pwd
```
---
*ls* - показывает содержание текущей директории:
```bash
ls
```

Вызов команды *ls* флагом *-a* - показывает скрытые файлы:
```bash
ls -a
```
---
*mkdir* - создать директорию (по умолчанию в текущей директории). В аргумент принимает название новой директории: (где test - название новой директории)
```bash
mkdir test/
```
---
*touch* - создать файл (по умолчанию в текущей директории). В аргумент принимает название нового файла и так же принято писать расширение нового файла: (где test.txt - название нового файла)
```bash
touch test.txt
```
---
*cp* - копирует файлы из одной директории в другую. Принимает 2 аргумента:
- Название файла в текущей директории. (может быть несколько)
- В какую директорию необходимо скопировать файлы.

В примере скопировали *test.txt* из текущей директории в дочернюю директорию *src*.
```bash
cp test.txt ./src
```
---
*mv* - перемещение файлов и директорий(может быть несколько). Принимает 2 аргумента:
- Название файла для перемещения в текущей директории (может быть несколько)
- В какую директорию необходимо переместить.

В примере переместили *test.txt* из текущей директории в корневую *~*.
```bash
mv test.txt ~
```
---
*rm* - удалить файл. В аргумент принимает название файла: (где test.txt - назваие файла)
```bash
rm test.txt
```
---
*rmdir* - удалить пустую **!** директорию. В аргумент принимает название директории: (где test - название директории)
```bash
rmdir test/
```
---
*rm -r* - удалить директорию с файлами. Флаг *-r* означает, что команда *rm* будет применена рекурсивно для каждой поддиректории.

Сначала будут удалены все файлы внутри одной директории, а затем сама директория, 
до тех пор, пока не удалится указанная в аргументе директория: (где test - название директории)
```bash
rm -r test
```
---
*cat* - вывести в консоль содержимое файла. В аргумент принимает название файла: (где test.txt - название файла)
```bash
cat test.txt
```


## SSH-ключи:
*ssh-keygen -t ed25519 -C "email"* - команда для генерации пары ssh-ключей: (ed25519 - кодировка ключа. она может быть разной)
```bash
ssh-keygen -t ed25519 -C "email"
```

Публичный ключ - шифрует данные. Им можно поделиться.

Приватный ключ - расшифровывает данные. Им НЕЛЬЗЯ делиться!

SSH-ключи позволяют предоставить доступ к интернет-ресурсам, как например к GitHub`у.

## GIT && GitHub.
Git - система контроля версий. Консольный инструмент - *CLI*.

GitHub - место хранения удаленных репозиториев. Это платформа, которая упрощает командное взаимодействие GIT`ом


## Команды GIT.
*git init* - инициализирует гит в текущей директории:
.git папка скрыта, но её можно увидеть с помощью `ls -a`.
```bash
git init
```
---
**При случайной инициализации** - можно удалить директорию .git с помощью `rm -r .git` и тогда папка "отгититься". 
---
*git remote add* - связать удаленный репозиторий с локальным. В аргумент принимает 2 параметра:
- Имя удаленного репозитория - обычно указывается origin.
- Его URL
```bash
git remote add origin URL
```
---
*git remote -v* - проверить связку удаленного и локального репозитория. Флаг *-v* является сокращением от *--verbose* (то есть, подробный, подробное описание):
```bash
git remote -v
```
---
*git add* - подготовить файлы к сохранению. В аргументы принимает список файлов, которые нужно подготовить.
Или же можно подготовить всю текущую директории с помощью `.`, или же с помощью флага *--all*
```bash
git add . || git add --all || git add README.md
```
---
*git commit* - сохранить файлы (закоммитить файлы). Обычно применяется с флагом *-m* - данный флаг позволяет добавить информативное сообщение к коммиту.
Принимает в аргументы сообщение для коммита.
```bash
git commit -m "message"
```
---
*git push* - отправить сохраненные файлы (коммит) в удаленный репозиторий: (где branch_name - имя ветки, в которую нужно отправить изменения)
```bash
git push origin branch_name
```

## Markdown.
`*cursive* || _cursive_` - сделать текст курсивным.

`**bold** || __bold__` - сделать текст жирным.

`~~crossed~~` - зачеркнутый текст.

`<br>` - сделать переход на новую строку (или 2 пробела).

`
1. первый пункт  
2. второй пункт
` - создать нумированный список (цифры + пробел).

`
( - || * ) первый пункт 
( - || * ) второй пункт 
` - создать ненумированный список.

Ссылка:
`[Яндекс](https://yandex.ru)` - создание ссылки. 

- В квадратных скобках написано то, как будет отображаться ссылка. 
- В круглых - адрес ссылки.

`[Яндекс](https://yandex.ru "Яндекс!")` - после адреса ссылки можно написать в кавычках подсказку при наведении.

Код:
`/``````\` - в тройных кавычках *`* можно записать код. Стоит указать язык после первой тройки. Вторая (и последняя) тройка должна находится на отдельной странице.