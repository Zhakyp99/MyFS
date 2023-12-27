# cli программу на java, которая будет выполнять пользовательские команды для работы с файлами
# После запуска программа должна вывести список команд и их описание; далее ожидать команды от пользователя.

Пример:

$ java Main
MyFS 1.0 команды:
ls <path>               выводит список всех файлов и директорий для `path`
ls_py <path>            выводит список файлов с расширением `.py` в `path`
is_dir <path>           выводит `true`, если `path` это директория, в других случаях `false`
define <path>           выводит `директория` или `файл` в зависимости от типа `path`
readmod <path>          выводит права для файла в формате `rwx` для текущего пользователя
setmod <path> <perm>    устанавливает права для файла `path`
cat <path>              выводит контент файла
append <path>           добавляет строку `# Autogenerated line` в конец `path`
bc <path>               создает копию `path` в директорию `/tmp/${date}.backup` где, date - это дата в формате `dd-mm-yyyy`
greplong <path>         выводит самое длинное слово в файле
help                    выводит список команд и их описание
exit                    завершает работу программы
> ls ../
dir1 dir2 hello_world.py .secret_file
> is_dir ../dir1
true
> readmod ./dir2
rw-
> ls_py ../
hello_world.py
> cat ../hello_world.py
print("hello cruel world")
> exit
Goodbye
$
# entire code in Main.java class 
