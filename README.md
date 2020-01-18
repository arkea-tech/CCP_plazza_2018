# CCP_plazza_2018

Second year project in C++. The purpose of this project is to realize a simulation of a pizzeria, which is composed of the reception that accepts new commands, of several kitchens, themselves with several cooks, themselves cooking several pizzas.
Kitchens are represented by processes, cooks by threads themselves sheduled by a thread pool.
The threads are handled with the help of conditional variables and mutex.
Receptions and kitchens communicate through an IPC shared memory to serialize and send informations to child processes and threads. When kitchens are full, the program allocate a new kitchen by forking a process. if all cooks are busy, the thread pool trigger/allocate a new thread.
When an order is ready, the reception displays the informations to the user and keep a record.
The user send his commmands with the help of an interactive shell.

USING :

      Make
      
      ./plazza [COOK_TIME : 0 - 1] [NB_COOKS][REPLACE_STOCK_TIME].
      
      S := TYPE SIZE NUMBER [; TYPE SIZE NUMBER]*.
      TYPE := [a..zA..Z]+.      
      SIZE := S|M|L|XL|XXL.
      NUMBER := x[1..9][0..9]*.
   
EXEMPLE :
      
      > ./plazza 2 5 2000
      
      > regina XXL x2; fantasia M x3; margarita S x1.

      > status.



