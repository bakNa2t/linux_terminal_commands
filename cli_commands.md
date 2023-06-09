## Several basic linux terminal commands to work in CLI:
1. `man <command>`: просмотреть справочную информацию о команде _**command**_;
2. `pwd`: просмотреть текущую директорию;
3. `less <file.txt>`: просмотреть содержимое файла _**'file.txt'**_;
    * `less -N <file.txt>`: просмотреть содержимое файла _**'file.txt'**_ и отобразить номера строк;
    * `less +<N> <file.txt>`: просмотреть содержимое файла _**'file.txt'**_, начиная с заданного номера строки _**'N'**_;
    * `less -X <file.txt>`: просмотреть содержимое файла _**'file.txt'**_ и оставить содержимое файла на экране;
4. `cd`
    * `cd  <directory/some_path>`: сменить директорию;
    * `cd  ..`: вернуться в директорию на уровень выше;
    * `cd  -`: вернуться в предыдущую директорию;
    * `cd  ~`: вернуться в корневую директорию;
5. `ls`
    * `ls`: просмотреть список файлов в директории;
    * `ls <directory_path>`: просмотреть файлы определенной директории;
    * `ls -R`: просмотреть список подкаталогов рекурсивно (включая вложенные директории);
    * `ls -l`: просмотреть список файлов с дополнительной информацией;
    * `ls -a`: просмотреть список со скрытыми файлами;
6. `cat`
    * `cat <file.txt>`: просмотреть содержимое _**'file.txt'**_;
    * `cat <file1.txt> <file2.txt> <file3.txt>`: просмотреть содержимое некскольких файлов;
    * `cat <file1.txt> <file2.txt> > <new_file.txt>`: объединение содержимого нескольких файлов в новый файл;
    * `cat <file1.txt> >> <file2.txt>`: добавить содержимое _**'file1.txt'**_ в _**'file2.txt'**_;
    * `cat <file.txt> | <another_command>`: передать содержимое файла в качестве входных данных для другой команды;
    * `cat -s <file.txt>`:удаление нескольких пустых строк;
    * `cat -n <file.txt>`: просмотреть номера строк в файле;
    * `cat -b <file.txt>`: просмотреть номера строк только для непустых выходных строк;
7. `mkdir`
    * `mkdir <directory>`: создать директорию в текущем каталоге;
    * `mkdir <directory>/<new_directory1> <dir>/<new_directory2>`: создать более одной директории;
    * `mkdir <directory>/{<new_directory1>,<new_directory2>}`: создать нескольких директорий в каталоге;
    * `mkdir -m a=rwx <directory>`: cоздать директорию и установить права доступа к файлу;
    * `mkdir -m 777 <directory>`: cоздать директорию и установить права доступа к файлу, используя числовые значения;
8. `rmdir`
    * `rmdir <directory>`: удалить пустую директорию;
    * `rmdir -v -p <directory>`: для отображения подробной информации и удаления как родительской директории, так и директории этого родителя;
9. `rm`
    * `rm <file.txt>`: удалить файл;
    * `rm *`: удалить все файлы в рабочей директории;
    * `rm -r <directory>`: удалить _**'directory'**_ и все содержащиеся в ней файлы и директории;
    * `rm -rf <directory>`: удалить директорию с файлами в ней (не требует подтверждения от пользователя и сразу удаляет);
10. `mv`
    * `mv <file1.txt> <new_file2.txt>`: переименовать файлы в текущей директории;
    * `mv <file> <directory>/ `: переместить файл в другую директорию;
    * `mv <file> <directory>/<new_file>`: переместить файл в **_'directory'_** и переименовать его в **_'new_file'_**;
    * `mv <file1> <file2> <file3> <directory>/ `: переместить несколько файлов одной командой;
    * `mv *.txt <directory>/` : переместить несколько файлов c определенным расширением;
11. `cp`
    * `cp`: копировать файлы и директории;
    * `cp <file> <new_file>`: cкопировать файл в текущей директории;
    * `cp <file> <directory>/<file>`: cкопировать файл в **_'directory'_**;
    * `cp <file> <directory>/<new_file>`: cкопировать файл в **_'directory'_** с новым именем;
    * `cp *.txt <directory>/`: cкопировать все файлы с расширением **_'.txt'_** в **_'directory'_**;
    * `cp -r <directory> <directory1>`: cкопировать все файлы, включая все поддиректории и файлы в них, из **_'directory'_** в **_'directory1'_** (или использовать тэг `-R`);
12. `touch`
    * `touch`: создать файл;
    * `touch <file>`: создать файл в текущем каталоге;
    * `touch <file> <directory>/`: создать файл в **_'directory'_**;
13. `tail`
    * `tail <file>`: просмотреть последние строки файла (10 строк по умолчанию);
    * `tail -n <number> <file>`: просмотреть указанное _**'number'**_  количество последних отображаемых строк файла;
    * `tail <file1> <file1>`: просмотреть последние 10 строк каждого файла;
14. `head`
    * `head <file>`: просмотреть первые строки файла (10 строк по умолчанию);
    * `head -n <number> <file>`: просмотреть указанное _**'number'**_  количество первых отображаемых строк файла;
15. `find`
    * `find . -name <file.txt>`: найти все файлы с именем _**'file.txt'**_ в текущем рабочем каталоге;
    * `find /<directory> -name <file.txt>`: найти все файлы с именем _**'file.txt'**_ в каталоге _**'directory'**_;
    * `find /<directory> -iname <file.txt>`: найти все файлы с именем _**'file.txt'**_, содержащим как заглавные, так и строчные буквы в каталоге _**'directory'**_;
    * `find / -type d -name <temp>`: найти все директории c именем _**'temp'**_ в каталоге _**' / '**_;
    * `find / -type f -name <file.py>`: найти все файлы _**'php'**_ c именем _**'file.py'**_ в каталоге _**' / '**_;
    * `find / -type f -name "*.py"`: найти все файлы _**'.py'**_ в каталоге _**' / '**_;
    * `find . -type f -name "file.txt" -exec rm -f {} \;`: найти единственный файл с именем _**"file.txt"**_ в каталоге _**' / '**_ и удалить его;
16. `grep`
    * `grep`:  **global regular expression printing** - печать глобального регулярного выражения;
    * `grep "regex" <file.txt>`: найти все строки файла _**'file.txt'**_ с заданным регулярным выражением _**"regex"**_;
    * `grep "regex" <file*>`: найти данную строку _**"regex"**_ в нескольких файлах _**'file*'**_, не учитывая расширение файла (_**'file.txt'**_, _**'file.html'**_);
    * `grep -i "regex" <file.txt>`: найти заданное регулярное выражение _**"regex"**_  без учета регистра в файле _**'file.txt'**_;

17. `sort`
    * `sort <file.txt>`: сортировка файлов по умолчанию с учетом регистра в алфавитном порядке;
    * `sort -r <file.txt>`: сортировка файлов по умолчанию с учетом регистра в обратном порядке;
    * `sort -u <file.txt>`: сортировка файлов без учета дубликатов;
    * `sort -n <file.txt>`: сортировка файлов по числовому значению строки;
    * `sort --ignore-case <file.txt>`: сортировка файлов без учета регистра;

18. `echo`
    * `echo`: вывести текст на экран;
    * `echo "display Hello"`: вывести список строк _**'display Hello'**_ в командной строке;
    * `echo -e "display \nHello"`: вывести список строк после _**\n**_ с новой строки (_**-e**_ включить экранирование обратного слэша);
    * `echo -e "display \bHello"`: вывести список строк и удалить пробелы между строками, используя _**\b**_;
19. `chmod`
    * `chmod <file.txt>`: установить/изменить права доступа к файлу _**'file.txt'**_ ;
    * `chmod u=rwx, g=rx, o=rx <file.txt>`: установить права доступа _**'rwxr-xr-x (755)'**_ к файлу _**'file.txt'**_ ;
    * `chmod 777 <file.txt>`: отобразить права доступа всем категориям _**'r w x'**_ к файлу _**'file.txt'**_ ;
    * `chmod a-x <file.txt>`: удалить права доступа _**'-x'**_ всем категориям (_**'a'**_)  к файлу _**'file.txt'**_ ;
    * `chmod g+w <file.txt>`: добавить права доступа _**'-w'**_ для группы (_**'g'**_) к файлу _**'file.txt'**_ ;
    * `chmod ug+rw <file.txt>`: добавить права доступа _**'-r, -w'**_ для пользователя/владельца (_**'u'**_) и для группы (_**'g'**_) к файлу _**'file.txt'**_ ;