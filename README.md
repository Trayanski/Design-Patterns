# Design-Patterns

Required Reading

Prentice Hall - Applied Java Patterns

Design Patterns - Elements of Reusable Object-Oriented Software

James Cooper - The Design Patterns Java Companion

Big Transitions in small Steps

Use your singletons wisely

Задачи:

1 - Abstract Factory
Create an Abstract Factory implementation which should be responsible for the creation of HousePart objects (Window, Door, Floor and etc) which are required for construction of a House.

You have to experiment and with another pattern named Factory Method. There should be 2 implementations of this pattern:

By using regular instantiation with "new"

By using Reflection

2 - Singleton
The Design Pattern Singleton should be realized. Create a class called Singleton.The class should have a private constructor only. The class should be implemented in an appropriate way such that only a single instance of it should be created (i.e. no more than one instance should be instantiated in the memory).

//constructor  

private Singleton() {  
  System.out.println("Singleton created");  
}  

3 - Да се направи пълния pool (Object Instance Pattern).
Да се гарантира, че в кой да е момент в pool-а ще има максимум N на брой инстанции от даден клас, т.е. имаме ограничение на ресурсите. Рool-а трябва да извършва следните 2 действия:

acquire() - заема ресурс;

release()- освобождава ресурс;

Няма действие createInstance(), a acquire(). Ако няма свободна инстанция се връща грешка.

Упътване: 
Например имаме ограничение за максимум 10 инстанции от клас в pull-а.

10 пъти се извиква acquire() - ОК;
11-ти път път се извиква acquire() - грешка! - няма свободен ресурс.

4 - Да се направи Proxy на клас - обект представящ се за друг.
Клиента работи с обект от клас А, но реално вижда че работи само с клас Б.
Реален клас <- ->Proxy
Integer class <- ->IntegerProxy
Да се направи IntegerProxy. Има 1 мениджър (IntegerFactory), който създава инстанции чрез метода сиcreateInstance(). Клиентите работят само с IntegerProxy, а не с реалния Integer.

5 - Observer
Да се направи програма за поддържане на статистика на стоки. Трябва да има един клас, който да поддържа статистика за наличните стоки и един, в който има списък с продадените стоки (тези, които вече не са налични). Класът който е регистриран като слушателда следи за премахване на стари или добавяне на нови стоки.
