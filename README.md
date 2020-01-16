# CCP_plazza_2018

Second year project in C++. The purpose of this project is to realize a simulation of a pizzeria, which is composed of the reception that accepts new commands, of several kitchens, themselves with several cooks, themselves cooking several pizzas.
Kitchens are represented by processes, cooks by threads themselves shedule by a thread pool. The threads are handled with the help of conditional variables and mutex.
Receptions and kitchens communicate through an IPC shared memory to serialize and send informations to child processes and threads.
When an order is ready, the reception displays the information to the user and keep a record.

USING :

1) Make && ./plazza [COOK_TIME : 0 - 1] [NB_COOKS][REPLACE_STOCK_TIME]
2) - S := TYPE SIZE NUMBER [; TYPE SIZE NUMBER]* TYPE := [a..zA..Z]+
   - status
   {SIZE := S|M|L|XL|XXL}
   {NUMBER := x[1..9][0..9]*}
   
EXEMPLE :

> regina XXL x2; fantasia M x3; margarita S x1
> status



