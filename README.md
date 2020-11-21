### КодоЛаба: Структуры данных в Go. Стандартная библиотека.
##### Программирование на Go, Школа Программистов 2020

***

В данной кодолабе вам нужно будет написать программу, которая работает как знаменитый `ls`

В итоге у вас получится полноценная программа, которая работает с флагами командной строки и файлами.

#### Шаг 0. Что есть сейчас ?

Сейчас программа умеет выводить просто файлы в текущей директории.

Чтобы задать другую директорию, можно передать флаг -d.

Если добавить флаг -a, то в выводе также будет дата изменения и размер файла.

Для работы вам пригодится документация по `os.FileInfo`


```
$ go run main.go -a -d .
>> 4492 Nov 19 19:21 README.md 
   474 Nov 19 19:14 main.go 
```

#### Шаг 1. Размер файла по красоте.

1. Допишите в программу новый флаг `h`. Если данный флаг задан, то размер файла должен выводиться в человеко-читаемом формате. Вместо `4335` должно быть `4KB`.

2. Реализуйте функцию `hrSize`, которая по размеру файла в байтах возвращает наибольший целый размер в КБ или МБ. Например, 640 -> 1KB, 1800 -> 2KB 


#### Шаг 2. Сортировка по дате.

1. Добавьте флаг `sort`.
2. Если у флага стоит значение `date`, то отсортируйте файлы по дате изменения.

(Сортировку реализуйте самостоятельно с помощью функции)

