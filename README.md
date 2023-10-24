#Лабораторная работа 2
##Лабораторная работа 1
Условие:

Создать файл sh и bat, который выполняет следующее:  
##На вход пакетному файлу приходит число (как параметр пакетного файла). Данное число является количеством секунд, по прошествию которых будет создан файл, в него записаны запущенные текущие процессы, затем создан второй файл, куда будет записано количество запущенных процессов.


## Работа bat:
bash
```@echo off

REM Получаем количество секунд из аргументов командной строки
set seconds=%1

REM Создаем файл, в который будет записаны запущенные процессы
tasklist > process_list.txt

REM Ждем указанное количество секунд
ping 127.0.0.1 -n %seconds% > nul

REM Создаем второй файл, в который будет записано количество запущенных процессов
tasklist /FO csv | find /c /v "" > process_count.txt
```

Описание переменных:

+%1 - Это переменная, которая получает значение первого аргумента командной строки. Она используется для определения количества секунд ожидания.

+/FO csv - Этот аргумент задает формат вывода команды tasklist в виде CSV (Comma-Separated Values), что позволяет легко обрабатывать вывод с помощью других инструментов.

+/c - Этот аргумент указывает команде find выполнить поиск и подсчет соответствующих строк во вводе.

+/v "" - Этот аргумент указывает команде find искать все строки, которые не содержат пустую строку. Таким образом, он используется для подсчета строк вывода команды tasklist.

Эти аргументы используются в сценарии для следующих целей:

Первый аргумент (%1) используется для определения количества секунд ожидания. Значение этого аргумента передается в переменную seconds, которая затем используется в команде ping для ожидания указанного количества секунд.

Аргумент /FO csv используется в команде tasklist, чтобы получить список процессов в формате CSV, который записывается в файл process_list.txt.

Аргументы /c и /v "" используются в команде find, чтобы подсчитать количество строк вывода команды tasklist (т.е. количество запущенных процессов) и записать это значение в файл process_count.txt.

Таким образом, аргументы в данном сценарии используются для определения времени ожидания, формата вывода команды tasklist и подсчета количества запущенных процессов.

<img width="1306" alt="пример запуска" src="https://github.com/JIEBOH/JIEBOH/assets/146937124/aed5c8c5-2a85-4b9f-bb46-b69be58a5eec">
<img width="1427" alt="ример выполнения" src="https://github.com/JIEBOH/JIEBOH/assets/146937124/00e2a43c-4bd7-458c-9ce9-17e7b6131cbb">
