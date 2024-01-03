# GIT && GitHub.
Git - система контроля версий. Консольный инструмент - *CLI*.

GitHub - место хранения удаленных репозиториев. Это платформа, которая упрощает командное взаимодействие.

# Команды консоли.
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
mkdir test
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
rmdir test
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
---
