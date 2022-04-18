# Git Bash HW1 Linux terminal (GitBash) commands

1. Посмотреть где я
   > pwd
2. Создать папку
   > mkdir courses
3. Зайти в папку
   > cd courses
4. Создать 3 папки
   > mkdir lesson_1 lesson_2 lesson_3
5. Зайти в любоую папку
   > cd lesson_2
6. Создать 5 файлов (3 txt, 2 json)
   > touch one.txt two.txt three.txt four.json five.json
7. Создать 3 папки
   > mkdir folder_1 folder_2 folder_3
8. Вывести список содержимого папки

   > ls -la

9. Открыть любой txt файл
   > vim one.txt
10. Написать туда что-нибудь, любой текст

    > в открывшемся текстовом редакторе vim (из п.9) нажать латинскую кнопку "i",
    > мы окажемся в режиме "INSERT", набираем любой текст

11. Сохранить и выйти
    > выйти из режима "INSERT" с помощью клавиши ESC, ввести :wq (сохранить и выйти)
12. Выйти из папки на уровень выше

    > cd ..

13. Переместить любые 2 файла, которые вы создали, в любую другую папку
    > mv {five.json,two.txt} /d/courses/lesson_1/
14. Скопировать любые 2 файла, которые вы создали, в любую другую папку
    > cp {four.json,three.txt} /d/courses/lesson_3/
15. Найти файл по имени
    > find -name two.txt
16. Просмотреть содержимое в реальном времени (команда grep) изучите как она работает
    > tail -f one.txt | grep "searchkey"
17. Вывести несколько первых строк из текстового файла
    > head -2 one.txt
18. Вывести несколько последних строк из текстового файла
    > tail -3 one.txt
19. Просмотреть содержимое длинного файла (команда less) изучите как она работает
    > less one.txt
20. Вывести дату и время
    > date

---

# Дополнительные Задание

## Отправить http запрос на сервер.
   http://162.55.220.72:5005/terminal-hw-request

> 1.  отправляем запрос: curl http://162.55.220.72:5005/terminal-hw-request
>     получаем ответ: {"Intro":"Hello!! This is your the first response from server","Tasks":{"Task_1":"Send the next URL in terminal: http://162.55.220.72:5005/get_method?name=(set_your_String)&age=(set_your_number)","result":["Your_String","Your_number"]}}

> 2.  изменяем запрос: curl "http://162.55.220.72:5005/get_method?name=evgeniy&age=28"
>     получаем ответ: ["evgeniy","28"]

---

## Написать скрипт который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13

> 1.  touch onescript.txt
> 2.  vim onescript.txt

> #!/bin/bash

> cd courses
> mkdir lesson_1 lesson_2 lesson_3
> cd lesson_2
> touch one.txt two.txt three.txt four.json five.json
> mkdir folder_1 folder_2 folder_3
> ls -la
> mv {five.json,two.txt} /d/courses/lesson_1/

> 3.  chmod u+x onescript.txt
> 4.  ./onescript.txt
