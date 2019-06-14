public class Solution {

    public static void main(String[] args) throws Exception { // вызов главного метода 
        System.out.println(min2(12, 33)); // вводим данные в виде цифр с привязкой к переменной min2 и тут же после обработки в public static int min2 распечатываем его
        System.out.println(min2(-20, 0));
        System.out.println(min2(-10, -20));
    }
    public static int min2(int a, int b) { //создание публичной статичного цифрового метода  min2 и передача параметров или аргументов
      int min2 = Math.min (a, b); // обработка аргументов методом Math.min и  перезагрузка переменной
      return min2; // возврат ее в метод main
    }
}
=========

public class MethodCall
{
   public static void main(String[] args)
   {
      int a = 5, b = 7; // создаем две переменных а и b
      int m = min(a, b); // получаем статичный метод min и присваиваем переменной m
      System.out.println("The minimum is "+ m);
   }

   public static int min(int c, int d) // создание публичной статичного цифрового метода  min и передача параметров или аргументов
   {
      int m2; // cоздаем переменную m2 и присваиваем 0;
      if (c < d) // сравниваем
           m2 = c; // переопределяем переменную
      else
           m2 = d;

      return m2; // возврат в главный метод
   }
}
--
такой же метод
public class MethodCall
{
   public static void main(String[] args)
   {
      int a = 5, b = 7; // cоздаем переменные
      int c = a, d = b; // переопределяем их 
      int m2; // создаем переменную m2
      if (c < d) // сравниваем
           m2 = c;
      else
           m2 = d;

      int m = m2; // присваиваем m2 новосозданной переменной m
      System.out.println("The minimum is "+ m);
   }
}
======================

package com.codegym.task.task01.task0136;

/* 
Even to the moon!

*/

public class Solution {
    public static void main(String[] args) {
        System.out.println(getWeight(888)); // распечатываем метод getWeight с параметром
    }

    public static double getWeight(int earthWeight) { // создание метода с параметром earthWeight
       double getWeight = earthWeight * 0.17; // делаем необходимое действие
       return getWeight; // возврат в главный метод
       
        // write your code here
    }
}
================
package com.codegym.task.task02.task0216;

/* 
Minimum of three numbers

*/
public class Solution {

    public static void main(String[] args) throws Exception {
        System.out.println(min3(1, 2, 3)); // получение готовых результатов из метода public static int min3
        System.out.println(min3(-1, -2, -3));
        System.out.println(min3(3, 5, 3));
        System.out.println(min3(5, 5, 10));
    }
    public static int min3(int a, int b, int c) { // создаем метод
        int d = Math.min(a, b); // создаем новую переменную d и присваиваем минимум из аргументов а и b
        int min3 = Math.min(d, c); // извлекаем минимум
        return min3; // возврат в главный метод
        //write your code here
    }


}
=============
package com.codegym.task.task02.task0217;

/* 
Minimum of four numbers

*/
public class Solution {

    public static void main(String[] args) throws Exception {
        System.out.println(min(-20, -10));
        System.out.println(min(-20, -10, -30, -40));
        System.out.println(min(-20, -10, -30, 40));
        System.out.println(min(-40, -10, -30, 40));
    }
    public static int min(int a, int b, int c, int d) { //  
        // write your code here 
        return min(min(a, b), min(c, d)); // передача метода как параметра, то есть переменная e летит через метод min нижний сюда в скобки 
		// полиморфизм - когда один и тот же метод вызывается с разными параметрами 
    } 
    public static int min(int n, int k) { // создается еще один такой же метод, но он совсем не имеет ничего общего с первым, у них разное количество параметров, -20 и -10 попадают сюда, но сюда же попадают и данные из первого min -- min(a, b), min(c, d)
        int e = Math.min(n, k); // метод Math
        return e; // cвязан с методом min и летит распечатываться
        //write your code here 
    } 
} // или по типу(int) или по количеству выборка (2 или 4)

// методы нельзя создаться с одинаковыми параметрами
======================
package com.codegym.task.task02.task0218;

/* 
Repetition is the mother of all learning

*/
public class Solution {

    public static void main(String[] args) { // то есть он его пролетает, летит к методам
        print3("I love you!");
    } 
	public static void print3(String s) { // образование метода print3 с одним параметром, который связан с print3("I love you!");
        System.out.println(s);
        System.out.println(s);
        System.out.println(s); 
    }

}
=====================
package com.codegym.task.task02.task0219;

/* 
Print three times

*/
public class Solution {    
    public static void main(String[] args) {
        print3("window");
        print3("file");
    }
	public static void print3(String s) { 
        System.out.print(s+" "+s+" "+s);

    }
}
==============================
package com.codegym.task.task03.task0301;

/* 
Dividing is good

*/

public class Solution {
    public static void main(String[] args) {
        div(6, 3);
        div(10, 6);
        div(2, 4);
    }

    public static void div(int a, int b) {
        int c = a / b; 
        System.out.println(c); 
       //write your code here
    }
}
==========
Эти три примера эквивалентны
-
Cat cat = new Cat("Oscar");
System.out.println("The cat is " + cat);
-.
Cat cat = new Cat("Oscar");
System.out.println("The cat is " + cat.toString());
-
Cat cat = new Cat("Oscar");
String catText = cat.toString();
System.out.println("The cat is " + catText);
===========
package com.codegym.task.task03.task0302;

/* 
Display right away

*/
public class Solution {
	
    public static void main(String[] args) {
        printString("Hello, Amigo!"); // сюда передается printString (String s ), то есть то что он делает в своих скобках
    }
    public static void printString (String s ){        
        System.out.println(s); 
    }
        
}
================
package com.codegym.task.task03.task0303;

/* 
Currency exchange

*/

public class Solution {
    public static void main(String[] args) { 
         System.out.println(convertEurToUsd(88,78));
         System.out.println(convertEurToUsd(68,78));
                 //write your code here
    } 
    public static double convertEurToUsd(int eur, double exchangeRate) { 
        double convertEurToUsd = eur * exchangeRate;
        return convertEurToUsd;
    }
} 
==================
package com.codegym.task.task03.task0304;

/* 
Task with percentages

*/

public class Solution {
    public static void main(String[] args) {
        System.out.println(addTenPercent(9));
    }
    public static double addTenPercent(int i) {
        double addTenPercent = i * 1.1;
        return addTenPercent;
        //write your code here
    }
} 
===============
package com.codegym.task.task03.task0305;

/* 
Red scare 
*/ 
public class Solution {
    public static void main(String[] args) {
        System.out.print("MAY 13 1972"); 
        //write your code here
    }
}
==============
package com.codegym.task.task03.task0307;

/* 
Hello, StarCraft!

*/

public class Solution {
    public static void main(String[] args) {
        Zerg zerg = new Zerg();
        zerg.name = "Kevin";
        Zerg zerg2 = new Zerg();
        zerg2.name = "Kevin2";
        Zerg zerg3 = new Zerg();
        zerg3.name = "Kevin3";
        Zerg zerg4 = new Zerg();
        zerg4.name = "Kevin4";
        Zerg zerg5 = new Zerg();
        zerg5.name = "Kevin6";
        
        Protoss protoss = new Protoss();
        protoss.name = "Kevi";
        Protoss protoss2 = new Protoss();
        protoss2.name = "Kevi2";
        Protoss protoss3 = new Protoss();
        protoss3.name = "Kevi3";
        
        Terran terran = new Terran();
        terran.name = "Ke";
        Terran terran2 = new Terran();
        terran2.name = "Ke2";
        Terran terran3 = new Terran();
        terran3.name = "Ke3";
        Terran terran4 = new Terran();
        terran4.name = "Ke4";
        
        
        
        //write your code here
    }

    public static class Zerg {
        public String name;
    }

    public static class Protoss {
        public String name;
    }

    public static class Terran {
        public String name;
    }
}
------------
package com.codegym.task.task03.task0308;

/* 
Product of 10 numbers

*/

public class Solution {
    public static void main(String[] args) {
        int i = 1*2*3*4*5*6*7*8*9*10;
        
         System.out.println(i);
        //write your code here
    }
}
--
package com.codegym.task.task03.task0308;

/* 
Product of 10 numbers

*/

public class Solution {
    public static void main(String[] args) {
        System.out.println(mul(1));
    }
    public static int mul(int a){
        
        for(int i = 1;i <= 10; i++)
        
        a =a * i;
        return a;   
        
        
        //write your code here
    }
}
==============
package com.codegym.task.task03.task0309;

/* 
Sum of 5 numbers

*/

public class Solution {
    public static void main(String[] args) {
       int pre = 0; //establish a variable outside the for loop to store previous for loop value
        for (int i = 1; i < 6; i++) { //establish i variable as 1, increase it by 1 until i is 5 ( < 6 )
           int p = i + pre; // add previous sum with i increased by 1
           System.out.println(p);
           pre = p; // write your code here
		}
	}
}
=====================
package com.codegym.task.task01.task0134;

/* 
Fill a pool with water

*/

public class Solution {
    public static void main(String[] args) {
        System.out.println(getVolume(25, 5, 2));
    }

    public static long getVolume(int a, int b, int c) {
        long getVolume = a * b * c * 1000;
        return getVolume;
        
        //write your code here
    }
}
-------------------------
package com.codegym.task.task03.task0311;

/* 
Printing strings

*/

public class Solution {
    public static void main(String[] args) {
        writeToConsole("Hello, World!");
    }

    public static void writeToConsole(String s) {
       System.out.println("printing: " + s);
        //write your code here
    }
}
==================================
package com.codegym.task.task03.task0312;

/* 
Time conversion

*/

public class Solution {
    public static void main(String[] args) {
         System.out.println(convertToSeconds(10));
         System.out.println(convertToSeconds(40));
        //write your code here
    }
    public static int convertToSeconds (int hour ){
       int convertToSeconds = hour * 3600;
       return convertToSeconds;
        
    }    
    //write your code here
}
================
package com.codegym.task.task03.task0314;

/* 
Multiplication table

*/

public class Solution {
    public static void main(String[] args) {
       
        for (int i = 1; i <= 10; i++) {  
           int p = i;  
           System.out.print(p + " "); 
         }
        System.out.println(""); 
      //  int pre = 2;   
        for (int i = 1; i <= 10; i++) {  
           int p = i * 2;   
           System.out.print(p + " ");
          // pre = p;  
         }
        System.out.println(""); 
      //  int pre = pre + 1;   
        for (int i = 1; i <= 10; i++) {  
           int p = i * 3;   
           System.out.print(p + " ");
          // pre = p;  
         }
        System.out.println(""); 
      //  int pre = pre + 1;   
        for (int i = 1; i <= 10; i++) {  
           int p = i * 4;   
           System.out.print(p + " ");
          // pre = p;  
         }
        System.out.println(""); 
      //  int pre = pre + 1;   
        for (int i = 1; i <= 10; i++) {  
           int p = i * 5;   
           System.out.print(p + " ");
          // pre = p;  
         }
        System.out.println(""); 
      //  int pre = pre + 1;   
        for (int i = 1; i <= 10; i++) {  
           int p = i * 6;   
           System.out.print(p + " ");
          // pre = p;  
         }
        System.out.println(""); 
      //  int pre = pre + 1;   
        for (int i = 1; i <= 10; i++) {  
           int p = i * 7;   
           System.out.print(p + " ");
          // pre = p;  
         }
        System.out.println(""); 
      //  int pre = pre + 1;   
        for (int i = 1; i <= 10; i++) {  
           int p = i * 8;   
           System.out.print(p + " ");
          // pre = p;  
         }
        System.out.println(""); 
      //  int pre = pre + 1;   
        for (int i = 1; i <= 10; i++) {  
           int p = i * 9;   
           System.out.print(p + " ");
          // pre = p;  
         }
        System.out.println(""); 
      //  int pre = pre + 1;   
        for (int i = 1; i <= 10; i++) {  
           int p = i * 10;   
           System.out.print(p + " ");
          // pre = p;  
         } 
    }
}
============
тоже самое
package com.codegym.task.task03.task0314;

/* 
Multiplication table
таблица умножения
*/

public class Solution {
    public static void main(String[] args) {
      int row = 0;
        for (int i = 1; i <= 10; i++) {
            for (int j = 1; j <= 10; j++) {
                row = row + j;
                System.out.print(i * j + " ");
            }
            System.out.println("");
        }
    }
}
==================
package com.codegym.task.task03.task0315;

/* 
Roy G. Biv…

*/

public class Solution {
    public static void main(String[] args) {
        new Red(); // обьект видимо  
        new Orange(); // обьект
        new Yellow(); // обьект
        new Green(); // обьект
        new Blue(); // обьект
        new Indigo(); // обьект
        new Violet(); // обьект
        
        //write your code here
    }

    public static class Red {  
        public Red() { // конструктор
            System.out.println("Red");
        }
    }
	
/* 	Существует статический вложенный класс, этому [статическому вложенному] классу не нужен экземпляр окружающего класса, чтобы он сам был создан,

Эти классы [статические вложенные] могут обращаться к только статическим членам охватывающего класса [поскольку он не имеет ссылки на экземпляры окружающего класса...]

пример кода:

public class Test { 
  class A { } 
  static class B { }
  public static void main(String[] args) { 
    /*will fail - compilation error, you need an instance of Test to instantiate A 
    A a = new A(); 
    /*will compile successfully, not instance of Test is needed to instantiate B  
    B b = new B(); 
  }
}
И вот еще
Да, в java есть статический вложенный класс. Когда вы объявляете вложенный класс static, он автоматически становится самостоятельным классом, который может быть создан без необходимости создавать экземпляр внешнего класса, к которому он принадлежит.

Пример:

public class A
{

 public static class B
 {
 }
}
Поскольку class B объявлен static, вы можете явно создать экземпляр как:

B b = new B();
Обратите внимание, что если class B не был объявлен static, чтобы сделать его автономным, вызов объекта экземпляра выглядел бы следующим образом:

A a= new A();
B b = a.new B();
 */
    public static class Orange {
        public Orange() {// конструктор
            System.out.println("Orange");
        }
    }

    public static class Yellow {
        public Yellow() {// конструктор
            System.out.println("Yellow");
        }
    }

    public static class Green {
        public Green() {// конструктор
            System.out.println("Green");
        }
    }

    public static class Blue {
        public Blue() {
            System.out.println("Blue");
        }
    }

    public static class Indigo {
        public Indigo() {
            System.out.println("Indigo");
        }
    }

    public static class Violet {
        public Violet() {
            System.out.println("Violet");
        }
    }
}
=======================
package com.codegym.task.task03.task0316;

/* 
Escaping characters

*/

public class Solution {
    public static void main(String[] args) {
      System.out.println("This is a Windows path: \"C:\\Program Files\\Java\\jdk1.8.0_172\\bin\"");
      System.out.println("This is a Java string: \\\"C:\\\\Program Files\\\\Java\\\\jdk1.8.0_172\\\\bin\\\"");
       
			Screen output from the program (System.out)
			This is a Windows path: "C:\Program Files\Java\jdk1.8.0_172\bin"
			This is a Java string: \"C:\\Program Files\\Java\\jdk1.8.0_172\\bin\"
        //write your code here
    }
}
===========================
InputStream inputStream = System.in;
«Но System.in и BufferedReader несовместимы, поэтому мы используем другой адаптер - другой объект InputStreamReader ».
Reader inputStreamReader = new InputStreamReader(inputStream);
BufferedReader bufferedReader = new BufferedReader(inputStreamReader);
объект BufferedReader  прочитать строку с клавиатуры

передать объект, с которого вы собираетесь читать данные. В этом случае System.in
String name = bufferedReader.readLine(); //Read a string from the keyboard
String sAge = bufferedReader.readLine(); //Read a string from the keyboard
int nAge = Integer.parseInt(sAge); //Convert the string to a number.
--
BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));

String name = reader.readLine();
String sAge = reader.readLine();
int nAge = Integer.parseInt(sAge);
--
Scanner scanner = new Scanner(System.in);
String name = scanner.nextLine();
int age = scanner.nextInt();
==================================
package com.codegym.task.task03.task0318;

/* 
Plan to conquer the world

*/
import java.io.FileInputStream;
import java.io.IOException;
import java.io.InputStreamReader;
import java.io.*;

public class Solution {
    public static void main(String[] args) throws Exception {
       
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        String sAge = reader.readLine(); 
        String name = reader.readLine();
// int nAge = Integer.parseInt(sAge);
          System.out.print(name + " will take over the world in " + sAge +" years. Mwa-ha-ha!")  ;
        //write your code here
    }
}
=======================================
package com.codegym.task.task03.task0319;

/* 
Predictions

*/

import java.io.*;

public class Solution {
    public static void main(String[] args) throws Exception {
       BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        String name = reader.readLine();
        String number1 = reader.readLine(); 
        String number2 = reader.readLine(); 
// int nAge = Integer.parseInt(sAge);
          System.out.print(name + " will receive " + number1 +" in " + number2 +" years. ")  ;
        //write your code here
    }
}
==================================
package com.codegym.task.task03.task0320;


/* 
The humble programmer

*/

import java.io.*;

public class Solution {
    public static void main(String[] args) throws Exception {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        String name = reader.readLine(); 
        System.out.print(name + " makes $120,000 a year. Ha-ha-ha!")  ;
        //write your code here
    }
}
=====================================
package com.codegym.task.task01.task0131;

/* 
More conversions

*/

public class Solution {
    public static void main(String[] args) {
        System.out.println(getFeetFromInches(243));
    }

    public static int getFeetFromInches(int inches) {
        
        int getFeetFromInches = inches / 12;
        return getFeetFromInches;
        //write your code here
    }
}
===============================================
package com.codegym.task.task03.task0322;


/* 
Deep and pure love

*/

import java.io.*;

public class Solution {
    public static void main(String[] args) throws Exception {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        String name1 = reader.readLine(); 
        String name2 = reader.readLine(); 
        String name3 = reader.readLine(); 
        System.out.print(name1 + " + " + name2 + " + " + name3 + " = Pure love. Ooo la-la!");  
    }
}
======================================
package com.codegym.task.task01.task0132;

/* 
Sum of the digits of a three-digit number

*/ 
public class Solution {

    public static void main(String[] args) {
        System.out.println(sumDigitsInNumber(546));
    }
    public static int sumDigitsInNumber(int number) {  
        int sum ;
        int n;
        sum = 0; 
        while(number > 0){
            n = number % 10;
            sum = sum + n;
			 
            number = number / 10;
 
        } 
        return sum; 
        //write your code here
    } 
}
6 5 4 3 2 1
========================
package com.codegym.task.task03.task0325;

import java.io.*;

/* 
Financial expectations

*/
import java.io.FileInputStream;
import java.io.IOException;
import java.io.InputStreamReader;
import java.io.*;
import java.util.Random;// importing the random class to generate random number 
import javax.swing.JOptionPane;
public class Solution {
    public static void main(String[] args) throws Exception {
             BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));

      //  int n;
        String sAge = reader.readLine();
        int sAge2 = Integer.parseInt(sAge);
        System.out.print("I will earn $" + sAge2 + " per hour");
    }
    private static int sAge2;
}
Число надо вводить через консоль !!!!!!!!!!!!!!!!!!!!!!
=================

package com.codegym.task.task04.task0401;

/* 
This age doesn't work for me…

*/
public class Solution {
    public static void main(String[] args) { 
        Person person = new Person();
        System.out.println("Age: " + person.age);
        person.adjustAge(person.age);
        System.out.println("Adjusted age: " + person.age);
    }

    public static class Person {
        public int age = 20; // метод 20

        public void adjustAge(int age) { // этот метод летит сюда
   // Проблема была в this==============        
			this.age = this.age + 20;
         //  age = age + 20;
            System.out.println("The age in adjustAge() is " + age);
        }
    }
} 
Каждый раз, когда создается объект класса Person, возраст объекта изначально устанавливается равным 20. Затем мы печатаем возраст человека. (т.е. 20) После этого мы вызываем метод экземпляра (AdjustAge). Здесь цель состоит в том, чтобы изменить ссылку объекта на возраст до 40. Суть метода заключается в том, что как переменная в классе Person, так и аргумент в методе 'AdjustAge' оба являются 'возрастом'. При запуске программы изменяется только переменная класса age, а не ссылка на объект. Чтобы конкретно изменить ссылку на возраст объекта, мы используем «this». this.age = this.age + 20;

к ульянову
===============
package com.codegym.task.task04.task0402;

/* 
Price of apples

*/
public class Solution {
    public static void main(String[] args) {
        Apple apple = new Apple();
        apple.addPrice(50); // что такое addPrice
        Apple apple2 = new Apple();
        apple2.addPrice(100);
        System.out.println("The cost of apples is " + Apple.applePrice);
    }

    public static class Apple {
        public static int applePrice = 0;

        public static void addPrice(int applePrice) {
          Apple.applePrice = applePrice + Apple.applePrice;
		  // Статические методы и переменные не связаны с объектами класса; они связаны с самим классом. В данном случае Apple
         // или так --  Apple.applePrice += applePrice 
            
            
            // нам нужно обновить статическую переменную applePrice, а не локальную переменную applePrice. Для этого вы должны сложить локальную переменную к статической переменной. чтобы получить доступ к статической переменной после объявления локальной переменной с тем же именем, вы должны использовать classname.variableName и добавить к ней локальную переменную, объявленную в параметре метода (в нашем случае ее applePrice)
        }
    }
}
к ульянову
============
Cхема
class Main
{
    public int count = 0;     //  объявляет переменную экземпляра

    public void run() /// Вот что происходит, когда выполняется метод run
    {
        count = 15;           // получаем доступ к переменной экземпляра и присваиваем ей значение 15
        int count = 10;       // объявляем (создаем) новую локальную переменную : count она маскирует переменную экземпляра. Локальная переменная - это то, что увидит весь последующий код в методе (доступ)
        count++;             // Access the method variable
    }
}
--
Давайте посмотрим, как работает нестатический метод:

Cat cat = new Cat();
String name = cat.getName();
cat.setAge(17);
cat.setChildren(cat1, cat2, cat3);

Cat cat = new Cat();
String name = Cat.getName(cat);
Cat.setAge(cat,17);
Cat.setChildren(cat, cat1, cat2, cat3);

"Когда вы вызываете метод, используя  <object> dot <method name> , вы фактически вызываете метод класса и передаете тот же объект, что и первый аргумент. Внутри метода объект называется 'this' . Все операции в Метод выполняется на этом объекте и его данных. "
-
И так работает статический метод
Cat cat1 = new Cat();
Cat cat2 = new Cat();
int catCount = Cat.getAllCatsCount();

Cat cat1 = new Cat();
Cat cat2 = new Cat();
int catCount = Cat.getAllCatsCount(null);

Когда вы вызываете статический метод, в него не передается никакой объект. Другими словами, « this » равно нулю . Вот почему статический метод не может получить доступ к нестатическим переменным и методам (поскольку у него нет « this » для передачи»). к этим методам)

==========================================================
package com.codegym.task.task04.task0403;

/* 
What's the cat's name?

*/

public class Cat {
   
    public static void main(String[] args) {
        Cat cat = new Cat();
        cat.setName("Simba");
        System.out.println(cat.name);
    }

	private String name = "nameless cat";

    public void setName(String name) {  
       this.name = name; 
       //write your code here
    }

}
к ульянову
=-----------
f you made a constructor such as : 

public class Cat {

    String name;
    int age;

    public Cat(String name, int age) {
        this.name = name;
        this.age = age;
    }

That would work.  However,  private void setName(String name) is not a constructor, its just a method with String name being in the paramater. 

 Try  :     this.name = name;  instead of the above.  this. refers within the method instead of the global variable String name = "nameless cat";

I think this is how it works anways... 

You have entered Cat.name = name;   
=========================
package com.codegym.task.task04.task0404;

/* 
Cat register

*/

public class Cat {
    
	public static void main(String[] args) {

    }
	private static int catCount = 0;

    public static void addNewCat() {
         
      catCount++;
        
        //write your code here
    } 
}
=================================
package com.codegym.task.task04.task0405;

/* 
Setting the number of cats

*/

public class Cat {
    public static void main(String[] args) {

    }
    private static int catCount = 0;

    public static void setCatCount(int catCount) { 
      Cat.catCount=catCount;
        //write your code here
    }
}
=================================
package com.codegym.task.task04.task0406;

/* 
Name register

*/

public class Cat {
    public static void main(String[] args) {
         Cat cat = new Cat(); 
         cat.setName("ami", "go");
         System.out.println(cat.fullName);
    }
    private String fullName;
       
    public void setName(String firstName, String lastName) {
        String fullName = firstName + " " + lastName;
        this.fullName = fullName;
    }
}
=======================================
package com.codegym.task.task04.task0407;

/* 
Cats in the Universe

*/

public class Solution {
    public static void main(String[] args) {
        Cat cat1 = new Cat();
        Cat.count++; //write your code here

        Cat cat2 = new Cat();
        Cat.count++;//write your code here

        System.out.println("The cat count is " + Cat.count);
    }

    public static class Cat {
        public static int count = 0;
    }
}
=============================
package com.codegym.task.task04.task0408;

/* 
Good or bad?

*/

public class Solution {
    public static void main(String[] args) {
        compare(3);
        compare(6);
        compare(5);
    }

    public static void compare(int a) {
        if (a < 5) {
            System.out.println("The number is less than 5");
        }
        else if (a > 5) {
              System.out.println("The number is greater than 5");
        }
        else  {
              System.out.println("The number is equal  to 5");
        }
            //write your code here
    }
}
=========================
package com.codegym.task.task04.task0409;

/* 
Closest to 10

*/

public class Solution {
    public static void main(String[] args) {
        displayClosestToTen(8, 11);
        displayClosestToTen(7, 14);
    }

    public static void displayClosestToTen(int a, int b) {
       if( abs((a-10)) > abs((b-10)) )
           System.out.println(b);
        else 
           System.out.println(a);
        // write your code here

    }

    public static int abs(int a) {
        if (a < 0) {
            return -a;
        } else {
            return a;
        }
    }
}
=================================
package com.codegym.task.task04.task0410;

/* 
Come on, lucky seven!

*/

public class Solution {
    public static void main(String[] args) {
        checkInterval(60);
        checkInterval(112);
        checkInterval(10);
    }

    public static void checkInterval(int a) {
        if ((a < 50) ||  (a > 100)) {
            System.out.println("The number " + a + " is not in the interval.");
        } 
        else  {
              System.out.println("The number " + a + " is in the interval.");
        }
       
        //write your code here
    }
}
=================================
package com.codegym.task.task04.task0411;

/* 
Seasons on Terra

*/

public class Solution {
    public static void main(String[] args) {
        checkSeason(12);
        checkSeason(4);
        checkSeason(7);
        checkSeason(10);
    }

    public static void checkSeason(int month) {
    
        if ((month < 6) &  (month > 2)) {
            System.out.println("spring");
        } 
      else  if ((month < 9) &  (month > 5)) {
            System.out.println("summer");
        } 
        else  if ((month > 8) &  (month < 12)) {
              System.out.println("autumn");
        }
       if (month >=12 || month <=2)
System.out.println("winter");
        //write your code here
    }
}
===========
package com.codegym.task.task04.task0412;

/* 
Positive and negative numbers

*/

import java.io.*;

public class Solution {
    public static void main(String[] args) throws Exception {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        String sAge = reader.readLine();
        int nAge = Integer.parseInt(sAge);
               if  (nAge < 0)  {
                    nAge++; 
                    System.out.println(nAge);
                 } 
                else  if (nAge > 0)  {
                    nAge = nAge * 2; 
                    System.out.println(nAge);
                 } 
                else  if (nAge == 0)  { 
                    System.out.println(nAge);
                 }  
        //write your code here

    }

}
======================
package com.codegym.task.task04.task0413;

/* 
Day of the week

*/

import java.io.*;

public class Solution {
    public static void main(String[] args) throws Exception {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        String sAge = reader.readLine();
        int nAge = Integer.parseInt(sAge);
               if  (nAge == 1)  { 
                    System.out.println("Monday");
                 } 
                else  if (nAge == 2)  { 
                    System.out.println("Tuesday");
                 } 
                else  if (nAge == 3)  { 
                    System.out.println("Wednesday");
                 }  
                else  if (nAge == 4)  { 
                    System.out.println("Thursday");
                 }  
                else  if (nAge == 5)  { 
                    System.out.println("Friday");
                 }  
                else  if (nAge == 6)  { 
                    System.out.println("Saturday ");
                 }  
                else  if (nAge == 7)  { 
                    System.out.println("Sunday");
                 }  
                else     { 
                    System.out.println("No such day of the week");
                 }  
       
        //write your code here
    }
}
=======================================
package com.codegym.task.task04.task0414;

/* 
Number of days in the year

*/

import java.io.*;

public class Solution {
    public static void main(String[] args) throws Exception {
         BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        String sAge = reader.readLine();
        int nAge = Integer.parseInt(sAge);
               if  (((nAge % 4) == 0) && (((nAge % 100) != 0) || ((nAge % 400) == 0))){ 
                    System.out.println("Number of days in the year: 366");
                 } 
                else   { 
                    System.out.println("Number of days in the year: 365");
                 }  
        
        //write your code here
    }
}
=========================
package com.codegym.task.task04.task0415;

/* 
Rule of the triangle

*/

import java.io.*;

public class Solution {
    public static void main(String[] args) throws Exception {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        String sAge1 = reader.readLine();
        int nAge1 = Integer.parseInt(sAge1);
        String sAge2 = reader.readLine();
        int nAge2 = Integer.parseInt(sAge2);
        String sAge3 = reader.readLine();
        int nAge3 = Integer.parseInt(sAge3);
               if  (((nAge1 + nAge2) > nAge3) && (((nAge3 + nAge2) > nAge1) && ((nAge1 + nAge3) > nAge2))){ 
                    System.out.println("The triangle is possible.");
                 } 
                else   { 
                    System.out.println("The triangle is not possible.");
                 }  
       
       
       
        //write your code here
    }
}
=================================
package com.codegym.task.task04.task0416;

/* 
Crossing the road blindly

*/

import java.io.*;

public class Solution {
    public static void main(String[] args) throws Exception {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        String sAge1 = reader.readLine();
     //   int nAge1 = Integer.parseInt(sAge1); 
         double a = Double.parseDouble(sAge1);
         double t = a % 5.0;
             if (( t % 5 >= 0 ) && (t % 5 < 3))
                {   
                    System.out.println("green");                    
                }
                else if (( t % 5 >= 3 ) && ( t % 5 < 4 ))
                {
                    System.out.println("yellow");
                }
                else if ((t % 5 >= 4 )&&( t % 5 < 5))
                {
                    System.out.println("red");
                }
        //write your code here
    }
}
===========
package com.codegym.task.task04.task0417;

/* 
Do we have a pair?

*/

import java.io.*;

public class Solution {
    public static void main(String[] args) throws Exception {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        String sAge1 = reader.readLine();
        int nAge1 = Integer.parseInt(sAge1);
        String sAge2 = reader.readLine();
        int nAge2 = Integer.parseInt(sAge2);
        String sAge3 = reader.readLine();
        int nAge3 = Integer.parseInt(sAge3);
           if((nAge1==nAge2)&&(nAge2==nAge3))//checking whether 3 numbers are same
              System.out.println(nAge1+" "+nAge2+" "+nAge3);
//if three numbers are not same it will go through else block and check for remaining conditions
              else{  
        if(nAge1==nAge2)
            System.out.println(nAge1+" "+nAge2);
        if(nAge1==nAge3)
            System.out.println(nAge1+" "+nAge3);
         if(nAge2==nAge3)
            System.out.println(nAge2+" "+nAge3);
            if((nAge1==nAge2)&&(nAge2==nAge3))
              System.out.println(nAge1+" "+nAge2+" "+nAge3);
        //write your code here
    }
}
}
================================
package com.codegym.task.task04.task0418;

/* 
Minimum of two numbers

*/

import java.io.*;

public class Solution {
    public static void main(String[] args) throws Exception {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        String sAge1 = reader.readLine();
        int nAge1 = Integer.parseInt(sAge1);
        String sAge2 = reader.readLine();
        int nAge2 = Integer.parseInt(sAge2); 
        if (nAge1 <= nAge2){
            System.out.println(nAge1);
        }
        else {
            System.out.println(nAge2);
        }
       
        //write your code here
    }
}
=============================
package com.codegym.task.task04.task0419;

/* 
Maximum of four numbers

*/

import java.io.*;

public class Solution {
    public static void main(String[] args) throws Exception {
         BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        String sAge1 = reader.readLine();
        int nAge1 = Integer.parseInt(sAge1);
        String sAge2 = reader.readLine();
        int nAge2 = Integer.parseInt(sAge2); 
        String sAge3 = reader.readLine();
        int nAge3 = Integer.parseInt(sAge3);
        String sAge4 = reader.readLine();
        int nAge4 = Integer.parseInt(sAge4);  
         System.out.println(min3(nAge1, nAge2, nAge3, nAge4));
    }
     public static int min3(int nAge1, int nAge2, int nAge3, int nAge4) { // создаем метод
        int d = Math.max (nAge1, nAge2); 
        int min2 = Math.max(d, nAge3);  
        int min3 = Math.max(min2, nAge4);  
        return min3;
    }
}
==============================
package com.codegym.task.task04.task0420;

/* 
Sorting three numbers

*/

import java.io.*;

public class Solution {
    public static void main(String[] args) throws Exception {
        
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        String sAge1 = reader.readLine();
        int nAge1 = Integer.parseInt(sAge1);
        String sAge2 = reader.readLine();
        int nAge2 = Integer.parseInt(sAge2); 
        String sAge3 = reader.readLine();
        int nAge3 = Integer.parseInt(sAge3); 
        
         if ((nAge1 <= nAge2) && (nAge2 <= nAge3)) {
            System.out.print(nAge3 + " " + nAge2 + " " + nAge1);
        }
        else  if ((nAge1 >= nAge2) && (nAge2 >= nAge3)) {
            System.out.print(nAge1 + " " + nAge2 + " " + nAge3);
        }
        else  if ((nAge1 >= nAge2) && (nAge2 <= nAge3)) {
            System.out.print(nAge3 + " " + nAge1 + " " + nAge2);
        }
        else  if ((nAge1 <= nAge2) && (nAge1 >= nAge3)) {
            System.out.print(nAge2 + " " + nAge1 + " " + nAge3);
        }
        else  if ((nAge3 <= nAge2) && (nAge1 <= nAge3)) {
            System.out.print(nAge2 + " " + nAge3 + " " + nAge1);
        }
        else  if ((nAge1 >= nAge3) && (nAge2 <= nAge3)) {
            System.out.print(nAge1 + " " + nAge3 + " " + nAge2);
        }
        
    } 
}
==============================
package com.codegym.task.task04.task0421;

/* 
Jen or Jen?

*/

import java.io.*;

public class Solution {
    public static void main(String[] args) throws Exception {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        String sAge1 = reader.readLine(); 
        String sAge2 = reader.readLine();  
       if (sAge2.equals(sAge1)){
           System.out.println("The names are identical");
       }
       else if((sAge1.length()) == (sAge2.length())){
           System.out.println("The names are the same length");
       } 
    }
}
=============================
package com.codegym.task.task04.task0422;

/* 
18+

*/

import java.io.*;

public class Solution {
    public static void main(String[] args) throws Exception {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        String sAge2 = reader.readLine();
        String sAge1 = reader.readLine();
        int nAge1 = Integer.parseInt(sAge1);
        
        if (nAge1 < 18) {
            System.out.print("Grow up a little more ");
        }
    }
}
===========
package com.codegym.task.task04.task0424;

/* 
Sorting three numbers

*/

import java.io.*;

public class Solution {
    public static void main(String[] args) throws Exception {
        
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        String sAge1 = reader.readLine();
        int nAge1 = Integer.parseInt(sAge1);
        String sAge2 = reader.readLine();
        int nAge2 = Integer.parseInt(sAge2); 
        String sAge3 = reader.readLine();
        int nAge3 = Integer.parseInt(sAge3); 
        
         if (nAge1 == nAge2)  {
            System.out.print("3");
        }
        else  if (nAge1 == nAge3)  {
            System.out.print("2");
        }
        else  if (nAge3 == nAge2)  {
            System.out.print("1");
        }         
    } 
}
===========================
package com.codegym.task.task04.task0425;

/* 
Target locked!

*/

import java.io.*;

public class Solution {
    public static void main(String[] args) throws Exception {
          BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        String sAge1 = reader.readLine();
        int a = Integer.parseInt(sAge1);
        String sAge2 = reader.readLine();
        int b = Integer.parseInt(sAge2);  
        
         if (( a > 0) && (b > 0))  {
            System.out.print("1");
        }
        else if (( a < 0) && (b > 0))  {
            System.out.print("2");
        }
        else if (( a < 0) && (b < 0))  {
            System.out.print("3");
        }        
        else if (( a > 0) && (b < 0))  {
            System.out.print("4");
        }            
       
        
    }
}
===================
package com.codegym.task.task04.task0426;

/* 
Labels and numbers

*/

import java.io.*;

public class Solution {
    public static void main(String[] args) throws Exception {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        String sAge1 = reader.readLine();
        int a = Integer.parseInt(sAge1); 
        
         if (( a > 0) && (a % 2 == 0))  {
            System.out.print("Positive even number");
        }
        else  if (( a < 0) && (a % 2 == 0))  {
            System.out.print("Negative even number");
        }
        else if ( a == 0)   {
            System.out.print("Zero");
        }        
      else  if (( a < 0) && (a % 2 != 0))  {
            System.out.print("Negative odd number");
        }       
      else  if (( a > 0) && (a % 2 != 0))  {
            System.out.print("Positive odd number");
        }            
       
    }
}
====================================
package com.codegym.task.task04.task0427;

/* 
Describing numbers

*/

import java.io.*;

public class Solution {
    public static void main(String[] args) throws Exception {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        String sAge1 = reader.readLine();
        int a = Integer.parseInt(sAge1); 
 
       if(((sAge1.length()) == (1)) && (a % 2 == 0) && (a > 0) && (a < 1000)){
           System.out.println("even single-digit number");
       }  
      else  if(((sAge1.length()) == (1)) && (a % 2 != 0) && (a > 0) && (a < 1000)){
           System.out.println("odd single-digit number");
       }  
      else  if(((sAge1.length()) == (2)) && (a % 2 == 0) && (a > 0) && (a < 1000)){
           System.out.println("even two-digit number");
       }  
      else  if(((sAge1.length()) == (2)) && (a % 2 != 0) && (a > 0) && (a < 1000)){
           System.out.println("odd two-digit number");
       }  
      else  if(((sAge1.length()) == (3)) && (a % 2 == 0) && (a > 0) && (a < 1000)){
           System.out.println("even three-digit number");
       }  
      else  if(((sAge1.length()) == (3)) && (a % 2 != 0) && (a > 0) && (a < 1000)){
           System.out.println("odd three-digit number");
       }    
        
        //write your code here

    }
}
odd single-digit number
========================================
package com.codegym.task.task04.task0428;

/* 
Positive number

*/

import java.io.*;

public class Solution {
    public static void main(String[] args) throws Exception {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        String sAge1 = reader.readLine();
        int nAge1 = Integer.parseInt(sAge1);
        String sAge2 = reader.readLine();
        int nAge2 = Integer.parseInt(sAge2); 
        String sAge3 = reader.readLine();
        int nAge3 = Integer.parseInt(sAge3); 
        int a = 0;
         if (nAge1 > 0)  {
            a++;
        }
        if (nAge2 > 0)  {
              a++;
        }
        if (nAge3 > 0)  {
               a++;
        } 
        System.out.print(a);
       
        //write your code here

    }
}
how many 2
1
-5
8
==========================================
package com.codegym.task.task04.task0429;

/* 
Positive and negative numbers

*/

import java.io.*;

public class Solution {
    public static void main(String[] args) throws Exception {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        String sAge1 = reader.readLine();
        int nAge1 = Integer.parseInt(sAge1);
        String sAge2 = reader.readLine();
        int nAge2 = Integer.parseInt(sAge2); 
        String sAge3 = reader.readLine();
        int nAge3 = Integer.parseInt(sAge3); 
        int a = 0;
        int b = 0;
        if (nAge1 > 0)  {
            a++; 
        }  
        else  if (nAge1 < 0)  {
            b++;
        }
        if (nAge2 > 0)  {
              a++;
        } 
        else  if (nAge2 < 0)  {
            b++;
        }
        if (nAge3 > 0)  {
               a++;
        }  
        else  if (nAge3 < 0)  {
            b++;
        }
        System.out.println("Number of negative numbers: " + b);
        System.out.println("Number of positive  numbers: " + a);
        //write your code here

    }
}
Number of negative numbers: 1
Number of positive  numbers: 2
1
-5
8
============================  
boolean isExit = false;
while (!isExit)
{
    String s = buffer.readLine();
    isExit = s.equals("exit");
}
The program will print strings from the keyboard until the string 'exit' is input.
===============================
while (true)
{
    String s = buffer.readLine();
    if (s.equals("exit"))
        break;
}
==============
package com.codegym.task.task04.task0430;

/* 
1 to 10

*/

import java.io.*;

public class Solution {
    public static void main(String[] args) throws Exception {
        int i = 1;
        while (i < 11)
        {
            System.out.println(i);
            i++;
        }
        //write your code here

    }
} 
===================
package com.codegym.task.task04.task0431;

/* 
From 10 to 1

*/

import java.io.*;

public class Solution {
    public static void main(String[] args) throws Exception {
        int i = 10;
        while (i > 0)
        {
            System.out.println(i);
            i--;
        }
        //write your code here

    }
}
10
9
8
7
6
5
4
3
2
1
===============================
package com.codegym.task.task04.task0432;



/* 
You can't have too much of a good thing

*/

import java.io.*;

public class Solution {
    public static void main(String[] args) throws Exception {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        String sAge1 = reader.readLine(); 
        String sAge2 = reader.readLine();
        int nAge2 = Integer.parseInt(sAge2);  
        while (nAge2 > 0)
        {
            System.out.println(sAge1);
            nAge2--;
        }
       
        //write your code here

    }
}
java
java
java
java
java
java
java
java

======================== 
package com.codegym.task.task04.task0433;
/* 
Seeing dollars in your future
*/
import java.io.*;
public class Solution {
    public static void main(String[] args) throws Exception {
        int i = 10;
        int a = 9;
        while (i > 0)
        {
          while (a > 0)
            {
                System.out.print("$");               
                a--;
            }
             System.out.println("$");
            i--;
            a = 9;
        }       
        //write your code here
    }
}
$$$$$$$$$$
$$$$$$$$$$
$$$$$$$$$$
$$$$$$$$$$
$$$$$$$$$$
$$$$$$$$$$
$$$$$$$$$$
$$$$$$$$$$
$$$$$$$$$$
$$$$$$$$$$
======================
package com.codegym.task.task04.task0434;
/* 
Multiplication table
*/
import java.io.*;
public class Solution {
    public static void main(String[] args) throws Exception {
       int row = 0;
       int i = 1;
        while ( i <= 10 ) {
            int j = 1;
            while ( j <= 10 ) {
                row = row + j;
                System.out.print(i * j + " ");
                j++;
            }
            System.out.println("");
          i++;    
        }       
        //write your code here
    }
}
1 2 3 4 5 6 7 8 9 10 
2 4 6 8 10 12 14 16 18 20 
3 6 9 12 15 18 21 24 27 30 
4 8 12 16 20 24 28 32 36 40 
5 10 15 20 25 30 35 40 45 50 
6 12 18 24 30 36 42 48 54 60 
7 14 21 28 35 42 49 56 63 70 
8 16 24 32 40 48 56 64 72 80 
9 18 27 36 45 54 63 72 81 90 
10 20 30 40 50 60 70 80 90 100 
===========================
package com.codegym.task.task04.task0435;

/* 
Even numbers


*/

public class Solution {
    public static void main(String[] args) throws Exception {
        int pre = 0;  
        for (int i = 1; i <= 100; i++) {  
           if  ((i % 2) == 0){
            System.out.println(i);
           }
		} 
	}
}
2
4
6
8
10
12
14
16
18
20
22
24
26
28
30
32
34
36
38
40
42
44
46
48
50
52
54
56
58
60
62
64
66
68
70
72
74
76
78
80
82
84
86
88
90
92
94
96
98
100
========================
package com.codegym.task.task04.task0436;


/* 
Drawing a rectangle

*/

import java.io.*;

public class Solution {
    public static void main(String[] args) throws Exception {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        String sAge1 = reader.readLine();
        int m = Integer.parseInt(sAge1);
        String sAge2 = reader.readLine();
        int n = Integer.parseInt(sAge2);  
       
        int row = 0;
        for (int i = 1; i <= m; i++) {
            for (int j = 1; j < n; j++) {
                row = row + j;
                System.out.print("8");
            }
            System.out.println("8");
        }
        //write your code here
    }
}
8888
8888
8888
==============================
package com.codegym.task.task04.task0437;


/* 
Triangle of eights

*/

public class Solution {
    public static void main(String[] args) throws Exception {
       
        int b = 0;
        for (int i = 1; i <= 10; i++) {
            for (int j = 0; j < b; j++) {
                System.out.print("8");
            }
            System.out.println("8");
            b++;
        }
        //write your code here

    }
}
8
88
888
8888
88888
888888
8888888
88888888
888888888
8888888888
==================
package com.codegym.task.task04.task0438;

/* 
Drawing lines

*/

public class Solution {
    public static void main(String[] args) throws Exception {
        int b = 0;
        for (int i = 1; i <= 11; i++) {
            for (int j = b; j < 9; j++) {
                System.out.print("8");
            }
            System.out.println("8");
            b = 10;
        }
       
        //write your code here

    }
}
8888888888
8
8
8
8
8
8
8
8
8
================
package com.codegym.task.task04.task0439;

/* 
Chain letter

*/

import java.io.*;

public class Solution {
    public static void main(String[] args) throws Exception {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        String sAge1 = reader.readLine(); 
        for (int i = 1; i <= 10; i++) {
            System.out.println(sAge1 + " loves me.");
        } 
        //write your code here 
    }
}
java loves me.
java loves me.
java loves me.
java loves me.
java loves me.
java loves me.
java loves me.
java loves me.
java loves me.
java loves me.
=========
public class Main {

   public static void main(String[] args) {

       String s1 = "CodeGym is the best website for learning Java!";
       String s2 = new String("CodeGym is the best website for learning Java!");
       System.out.println(s1 == s2.intern());
   }
}
=================
public class Main {

   public static void main(String[] args) {

       String address1 = "2311 Broadway Street, San Francisco";
       String address2 = new String("2311 BROADWAY STREET, SAN FRANCISCO");
       System.out.println(address1.equalsIgnoreCase(address2));
   }
}
-------------
public class Main {

   public static void main(String[] args) {

       String s1 = "CodeGym is the best website for learning Java!";
       String s2 = new String("CODEGYM IS THE BEST WEBSITE FOR LEARNING JAVA!");
       System.out.println(s1.equals(s2));
   }
}
=============
public class Main {

   public static void main(String[] args) {

       int x = 342;
       System.out.println(Integer.toBinaryString(x));
   }
}
двоичная форма
тоже самое
public class Main {

   public static void main(String[] args) {

       int x = 342;
       System.out.println(~x);
   }
}

====================
package com.codegym.task.task04.task0441;


/* 
Somehow average

*/
import java.io.*;

public class Solution {
    public static void main(String[] args) throws Exception {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        String sAge1 = reader.readLine();
        int nAge1 = Integer.parseInt(sAge1);
        String sAge2 = reader.readLine();
        int nAge2 = Integer.parseInt(sAge2); 
        String sAge3 = reader.readLine();
        int nAge3 = Integer.parseInt(sAge3); 
       
        if ((nAge1 >= nAge2) && (nAge2 >= nAge3)) {
           System.out.println(nAge2);
        }  
        else if ((nAge3 >= nAge2) && (nAge2 >= nAge1)) {
           System.out.println(nAge2);
        }  
        else if ((nAge1 >= nAge3) && (nAge3 >= nAge2)) {
           System.out.println(nAge3);
        }
        else if ((nAge2 >= nAge3) && (nAge3 >= nAge1)) {
           System.out.println(nAge3);
        }
       
        else if ((nAge2 >= nAge1) && (nAge1 >= nAge3)) {
           System.out.println(nAge1);
        }
        else if ((nAge3 >= nAge1) && (nAge1 >= nAge2)) {
           System.out.println(nAge1);
        }
       
        //write your code here
    }
}
вывод среднего числа
90
55 
555
==============================
package com.codegym.task.task04.task0442;


/* 
Adding

*/

import java.io.*;

public class Solution {
    public static void main(String[] args) throws Exception {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        int sum = 0;
      //  int number = 0; 
        int nAge1 = 0;
          while (true)
       {
            String sAge1 = reader.readLine();
              int   number = Integer.parseInt(sAge1);
           if (number != -1)
           {
               sum += number;
           }
           else
           {
               sum += number;
               break;
           }
       }
       
       System.out.println(sum);
        //write your code here
    }
}
-
или так
-
package com.codegym.task.task04.task0442;


/* 
Adding

*/

import java.io.*;

public class Solution {
    public static void main(String[] args) throws Exception {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
      //  int y = -1;
        int number = 0;
        int nAge1 = 0;
           while (nAge1 != -1) {
                String sAge1 = reader.readLine();
                 nAge1 = Integer.parseInt(sAge1);
                 number += nAge1;
                 
            }
            System.out.println(number);
       
       
        //write your code here
    }
}
Используйте клавиатуру для ввода цифр . 
Если пользователь вводит -1 , отобразите сумму всех введенных чисел и завершите программу. 
-1 должен быть включен в сумму.

Подсказка: одно из решений этой проблемы использует следующую конструкцию:

while (true) {
    int number = read the number;
    if (check whether the number is -1)
        break;
}
====================
Cat cat1 = new Cat();
cat1.name =  "Oscar";

Cat cat2 = new Cat();
cat2.name = "Smudge";

System.out.println(cat1.name);
System.out.println(cat2.name);
==================
package com.codegym.task.task05.task0501;

/* 
Creating a cat

*/

public class Cat { 
	public static void main(String[] args) {

    }

    String name;
    int age;
    int weight; 
    int strength;
    //write your code here
  
}
============= 
package com.codegym.task.task05.task0502;

/* 
Implement the fight method

*/

public class Cat {
   public static void main(String[] args) { 
        Cat cat1 = new Cat();
        Cat cat2 = new Cat();
        cat1.age = 4;
        cat1.weight = 24;
        cat1.strength = 98;
        cat1.name = "Favorite cat";
        cat2.age = 4;
        cat2.weight = 24;
        cat2.strength = 99;
        cat2.name = "Unknown cat";
        
        System.out.println(cat1.fight(cat2));
        System.out.println(cat2.fight(cat1));
    }

	public int age;
    public int weight;
    public int strength;
    String name;

    public Cat() {
    }

    public boolean fight(Cat anotherCat) {
        boolean won = false; 
        if ((this.age> anotherCat.age || this.weight> anotherCat.weight || this.strength> anotherCat.strength))
        won = true;   
        return won;
    }

  
}
=================
public String getName() {
        return name;
    }

public void setName(String name) {
        this.name = name;
    }
=========
package com.codegym.task.task05.task0503;
/* 
Getters and setters for the Dog class
*/
public class Dog { 
     public static void main(String[] args) {
         Dog dog1 = new Dog();  
         dog1.getName();
         dog1.setName("doggy");
         dog1.getAge();
         dog1.setAge(23);
    }

	String name;
    int age;

    public String getName() {
            return name;
        }
    public int getAge() {
            return age;
        }
    public void setName(String name) {
            this.name = name;
        }
    public void setAge(int age) {
            this.age = age;
        }
         
} 
=========================
package com.codegym.task.task05.task0504;


/* 
The Three "Muscateers"

*/

public class Solution {
    public static void main(String[] args) { 
        
        Cat cat1 = new Cat("Kitty",6,12,13); // аргументы передаются в public Cat в скобки
        Cat cat2 = new Cat("Kitty",6,12,13);
        Cat Cat3 = new Cat("Kitty",6,12,13);

    
        //write your code here
    }

    public static class Cat {
        private String name;
        private int age;
        private int weight;
        private int strength;

        public Cat(String name, int age, int weight, int strength) {
            this.name = name;
            this.age = age;
            this.weight = weight;
            this.strength = strength;
        }
    }
}
==================
package com.codegym.task.task05.task0505;

/* 
Feline carnage

*/

public class Solution {
    public static void main(String[] args) {
        Cat cat1 = new Cat("Kitty",5,12,13); // заполняем значения , которые летят в Cat(String name, int age, int weight, int strength)
        Cat cat2 = new Cat("Kitty1",6,153,183);
        Cat cat3 = new Cat("Kitty2",4,152,13);
         System.out.println(cat1.fight(cat2));
        System.out.println(cat2.fight(cat1));
         System.out.println(cat1.fight(cat3)); 
        //write your code here
    }

    public static class Cat {
        protected String name;
        protected int age;
        protected int weight;
        protected int strength;

        public Cat(String name, int age, int weight, int strength) {
            this.name = name;
            this.age = age;
            this.weight = weight;
            this.strength = strength;
        }

        public boolean fight(Cat anotherCat) { // здесь они все считаются и летят обратно в метод майн на распечатку
            int ageAdvantage = this.age > anotherCat.age ? 1 : 0;
            int weightAdvantage = this.weight > anotherCat.weight ? 1 : 0;
            int strengthAdvantage = this.strength > anotherCat.strength ? 1 : 0;

            int score = ageAdvantage + weightAdvantage + strengthAdvantage;
            return score > 2; // return score > 2 ? true : false;
        }
    }
}
===============
package com.codegym.task.task05.task0506;

/* 
People

*/

public class Person {
    String name; 
    int age; 
    String address; 
    char sex;
    //write your code here

    public static void main(String[] args) {

    }
}
===================
package com.codegym.task.task05.task0507;

/* 
Arithmetic mean

*/
import java.io.BufferedReader;
import java.io.InputStreamReader;
public class Solution {
    public static void main(String[] args) throws Exception {
       BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
       //  int y = -1;
        double couter = -1;
        double number = 0;
        int nAge1 = 0;
           while (nAge1 != -1) {
                String sAge1 = reader.readLine();
                 nAge1 = Integer.parseInt(sAge1);
                 number += nAge1;
                 couter++;
                 
            }
            number ++;
            double number1 = number / couter;
            System.out.println(number1); 
       
        //write your code here
    }
}
========================
package com.codegym.task.task05.task0508;

/* 
Getters and setters for the Person class

*/

public class Person {
     

	String name;
    int age;
    char sex;

    public String getName() {
            return name;
        }
    public int getAge() {
            return age;
        }
    public char getSex() {
            return sex;
        }
    public void setName(String name) {
            this.name = name;
        }
    public void setAge(int age) {
            this.age = age;
        }
    public void setSex(char sex) {
            this.sex = sex;
        }
    //write your code here 

    public static void main(String[] args) {
         
    }
}
======================
MyFile file2 = new MyFile();
file2.initialize("a.txt");

String text = file2.readText();
===============
package com.codegym.task.task05.task0509;

/* 
Create a Friend class

*/

public class Friend {

    public static void main(String[] args) {

    }
    //write your code here
    private String name = null;
    private int age=0;
    private char sex;
    
    public void initialize(String name)
    {
        this.name = name;
    }
    public void initialize(String name, int age)
    {
        this.name = name;
        this.age = age;
    }
    public void initialize(String name, int age, char sex)
    {
        this.name = name;
        this.age = age;
        this.sex = sex;
    } 
}
==============================
package com.codegym.task.task05.task0510;

/* 
Initializing cats

*/

public class Cat {
     public static void main(String[] args) {

    } 

//write your code here
    private String name = null;
    private int age = 10;
    private int weight = 5;
    private String address = null;
    private String color = "null";
    
    public void initialize(String name)
    {
        this.name = name;
    }
    public void initialize(String name, int weight, int age)
    {
        this.name = name;
        this.age = age;
        this.weight = weight;
    }
    public void initialize(String name, int age )
    {
        this.name = name;
        this.age = age; 
    } 
    public void initialize(int weight, String color )
    {
        this.weight = weight;
        this.color = color; 
    } 
    public void initialize(int weight, String color, String address )
    {
        this.weight = weight;
        this.color = color; 
        this.address = address;
    } 
}
===============================
package com.codegym.task.task05.task0511;

/* 
Create a Dog class

*/

public class Dog { 
    
    public static void main(String[] args) {

    }
     

    private String name = null; 
    private int height = 5; 
    private String color = "null";
    
    public void initialize(String name)
    {
        this.name = name;
    }
    public void initialize(String name, int height )
    {
        this.name = name;
        this.height = height; 
    } 
    public void initialize(String name, int height, String color)
    {
        this.name = name;
        this.color = color;
        this.height = height;
    }
}
=================================
package com.codegym.task.task05.task0512;

/* 
Create a Circle class

*/

public class Circle {
    //write your code here

    public static void main(String[] args) {

    } 
    private int centerX = 5;  
    private int centerY = 5;  
    private int radius = 5;  
    private int width = 5;  
    private int color = 5;  
    
    public void initialize(int centerX, int centerY, int radius)
    {
        this.centerX = centerX;
        this.centerY = centerY;
        this.radius = radius;
    }
     public void initialize(int centerX, int centerY, int radius, int width)
    {
        this.centerX = centerX;
        this.centerY = centerY;
        this.radius = radius;
        this.width = width;
    } 
     public void initialize(int centerX, int centerY, int radius, int width, int color)
    {
        this.centerX = centerX;
        this.centerY = centerY;
        this.radius = radius;
        this.width = width;
        this.color = color;
    } 
}
=================
public void initialize(int left, int top){
   this.left = left;
   this.top = top;
   height = 0;
   width = 0;
  // requirements say "width/height is not specified (both are 0)"
}
public void initialize(int left, int top, int height){
   this.left = left;
   this.top = top;
   this.height = height;
   width =height
  // requirements say "height is not specified (it is equal to the width), we'll create a square"
}
// ↓ just like declaring an object without the = new ..... , this is how you pass one ↓
public void initialize(Rectangle tempRec){
   tempRec.left = left;
   tempRec.top = top;
   tempRec.height = height;
   tempRec.width = width;
} // then set each property of the passed rectangle to this one.
=================
package com.codegym.task.task05.task0513;

/* 
Let's put together a rectangle

*/

public class Rectangle {
    //write your code here
    public static void main(String[] args) {

    } 
    private int left = 5;  
    private int top = 5;  
    private int width = 0;  
    private int height = width;  
    
    public void initialize(int left)
    {
        this.left = left; 
    }
    public void initialize(int left, int top )
    {
        this.left = left;
        this.top = top; 
    } 
	public void initialize(int left, int top, int width){
        this.left = left;
        this.top = top; 
        this.width = width; 
    } 
	public void initialize(Rectangle tempRec){
	   tempRec.left = left;
	   tempRec.top = top;
	   tempRec.height = height;
	   tempRec.width = width;
	} 
}
=========================
package com.codegym.task.task05.task0514;

/* 
A programmer creates a person

*/

public class Solution {
    public static void main(String[] args) {
        Person person = new Person();       
        person.initialize("Vania", 18);
		System.out.println(person.name);
        //write your code here
    }

    static class Person {
     private  String name ;
     private  int age ;
     
     public void initialize (String name, int age){
         this.name = name;
         this.age = age;
     }
        //write your code here
    }
}
================
package com.codegym.task.task05.task0515;

/* 
Initializing objects

*/

public class Person {
    String name;
    char sex;
    int money;
    int weight;
    double size;
 

    public void initialize(String name, int money, char sex, int weight, double size) {
        this.name = name;
        this.money = money;
        this.sex = sex;
        this.size = size;
        this.weight = weight;
    }

    public static void main(String[] args) {

    }
}
===================
Без конструктора	
class MyFile
{
  private String filename = null;

  public void initialize(String name)
  {
    this.filename = name;
  }

  public void initialize(String folder, String name)
  {
    this.filename = folder + name;
  }

  public void initialize(MyFile file, String name)
  {
    this.filename = file.getFolder() + name;
  }

…
}
С конструктором
class MyFile
{
  private String filename = null;

  public MyFile(String name)
  {
    this.filename = name;
  }

  public MyFile(String folder, String name)
  {
    this.filename = folder + name;
  }

  public MyFile(MyFile file, String name)
  {
    this.filename = file.getFolder() + name;
  }

…
}
=================
Без конструктора	
MyFile file = new MyFile(); 
file.initialize("c:\data\a.txt");
String text = file.readText();
С конструктором
MyFile file = new MyFile("c:\data\a.txt");
String text = file.readText();


MyFile file = new MyFile();
file.name = "23";
=======================
package com.codegym.task.task05.task0516;

/* 
You can't buy friends
Конструкторы!!!!!!!!!!!!!!!!!!!!!!!!!!
*/

public class Friend {
    public static void main(String[] args) {

    } 
    String name = "олдодл";
    int age;
    char sex;

  public Friend(String name)//// Friend имя класса вставляем
  {
    this.name = name;
  } 
  public Friend(String name, int age)
  {
    this.name = name;
    this.age = age;
  } 
  public Friend(String name, int age, char sex)
  { 
    this.name = name;
    this.age = age;
    this.sex = sex;
  } 
    //write your code here
}
====================
package com.codegym.task.task05.task0517; 
/* 
Creating cats 
*/ 
public class Cat {
	String name;
    int weight;
    int age; 
    String color;
    String address;
  public Cat(String name) 
  {
    this.name = name;
    weight =5;
    color = "green";
    age = 3;
  } 
  public Cat(String name, int weight, int age)
  {
    this.name = name;
    this.age = age;
    this.weight = weight;
    color = "red";
  } 
  public Cat(String name, int age)
  { 
    this.name = name;
    this.age = age; 
    name = "Misha";
    color = "yellow";
  } 
  public Cat(int weight, String color){
      this.weight= weight;
      this.color = color;
      age =3;
      
  }    
  public Cat(int weight, String color, String address){
      this.weight = weight;
      this.color = color;
      this.address = address;
      age = 4; // инициализируется на ходу
  }
    
    //write your code here

    public static void main(String[] args) {
        Cat cat = new Cat("ivan");
        Cat cat1 = new Cat("sonia", 4, 5); //как он определяет какой должен заполнять конструктор? в данном случае по типам данных - int, string и тд. Ну и по их количеству тоже
        Cat cat2 = new Cat("dusia", 12);
        Cat cat3 = new Cat(10, "black");
        Cat cat4 = new Cat(4, "white", "Lenina str");
        
    }
}
================
package com.codegym.task.task05.task0518;

/* 
Dog registration
*/ 
public class Dog {
    //write your code here
    int centerX;
    int centerY;
    int radius;  
    int width;   
 
- centerX, centerY, radius
- centerX, centerY, radius, width
- centerX, centerY, radius, width, color
 
  public Dog(int centerX, int) 
  {
    this.name = name; 
  } 
  public Dog(String name, int height)
  {
    this.name = name; 
    this.height = height; 
  } 
  public Dog(String name, int height, String color)
  { 
    this.name = name;
    this.height = height;  
    this.color = color;  
  }   
    public static void main(String[] args) {
        Dog dog = new Dog("ivan");
        Dog dog1 = new Dog("sonia", 4); //как он определяет какой должен заполнять конструктор? в данном случае по типам данных - int, string и тд. Ну и по их количеству тоже
        Dog dog2 = new Dog("dusia", 12, "black"); 
    }
}
========================================
package com.codegym.task.task05.task0519;

/* 
Walking in circles

*/


public class Circle {
    int centerX;
    int centerY;
    int radius;  
    int width;   
    int color;
 
  public Circle(int centerX, int centerY, int radius) 
  {
    this.centerX = centerX; 
    this.centerY = centerY; 
    this.radius = radius; 
  }  
  public Circle(int centerX, int centerY, int radius, int width) 
  {
    this.centerX = centerX; 
    this.centerY = centerY; 
    this.radius = radius; 
    this.width = width; 
  }  
  public Circle(int centerX, int centerY, int radius, int width, int color) 
  {
    this.centerX = centerX; 
    this.centerY = centerY; 
    this.radius = radius; 
    this.width = width; 
    this.color = color; 
  }  
    public static void main(String[] args) {
        
    }
}
==============================
package com.codegym.task.task05.task0520;
/* 
Create a Rectangle class
*/
public class Rectangle {
    
    private int left;
    private int top;
    private int width;  
    private int height;  
 
    public Rectangle(int left) 
  { 
    this.left = left;  
  }   
  
    public Rectangle(int left, int top) 
  {
    this.top = top;  
    this.left = left;  
  }   
    public Rectangle(int left, int top, int width) 
  {
    this.top = top; 
    width = 0; 
    this.left = left; 
  }   
    public Rectangle(int left, int top, int width, int height) 
  {
    this.top = top; 
    width = 0; 
    this.left = left; 
    height = 0;
  }   
    public void initialize(Rectangle tempRec){ // копия четвертого прямоугольника rectangle
      tempRec.left = left;
      tempRec.top = top;
      height = 0;
      width = 0;
    }
    public static void main(String[] args) {
        
    } 
}
==============
package com.codegym.task.task05.task0521;

/* 
Calling a constructor from a constructor

*/

public class Circle {

    public double x;
    public double y;
    public double radius;

    public Circle(double x, double y, double radius) {
        this.x = x;
        this.y = y;
        this.radius = radius;
    }

    public Circle(double x, double y) {
          this(x, y, 10);// вызов конструктора из конструктора
          //Следующие три строки не нужны. Вы передаете значения x, y и radius первому конструктору через второй конструктор, чтобы инициализировать объект. Снова инициализация переменных x, y и radius во втором конструкторе не требуется.
    }

    public Circle() {
        this(5, 5, 1);
    }

    public static void main(String[] args) {
        Circle circle = new Circle();
        System.out.println(circle.x + " " + circle.y + " " + circle.radius);
        Circle anotherCircle = new Circle(10, 5);
        System.out.println(anotherCircle.x + " " + anotherCircle.y + " " + anotherCircle.radius);
    }
}
===================================
package com.codegym.task.task05.task0522;

/* 
Max constructors

*/

public class Circle {
    public double x;
    public double y;
    public double radius;

    public Circle(){
        x = 5;
    }
    public Circle(double x){
        this.x= x;
    }
    public Circle(double x, double y){
        this.x = x;
        this.y = y;
    }
    public Circle(double x , double y , double radius){
        this.x = x;
        this.y = y;
        this.radius = radius;
    }
    //write your code here

    public static void main(String[] args) {

    }
}
======================
public class GuessGame{
	Player p1;
	Player p2;
	Player p3;
	
	public void startGame(){
		p1 = new Player();
		p2 = new Player();
		p3 = new Player();
		
		int guessp1 = 0;
		int guessp2 = 0;
		int guessp3 = 0;
		
		boolean p1isRight = false;
		boolean p2isRight = false;
		boolean p3isRight = false;
		
		int targetNumber = (int) (Math.random() * 10);
		System.out.println("я загадываю число от 0 до 9...");
		
		while(true){
			System.out.println("число, которое нужно угадать - " + targetNumber);
			
			p1.guess();
			p2.guess();
			p3.guess();
			
			guess1 = p1.number;
			System.out.println("Первый игрок думает, что это " + guessp1);
			
			guess2 = p2.number;
			System.out.println("Второй игрок думает , что это " + guess2);
			
			guess3 = p3.number;
			System.out.println("Третий игрок думает, что это " + guess3);
			
			if (guess1 == targetNumber){
				p1isRight = true;
			}
			
			if(guess2 == targetNumber){
				p2isRight == true;
			}
			
			if(guess3 == targetNumber){
				p3isRight == true;
			}
			
		if(p1isRight || p2isRight || p3isRight){
			System.out.println("у нас есть победитель!");
			System.out.println("первый игрок угадал?" + p1isRight);
			System.out.println("второй игрок угадал?" + p2isRight);
			System.out.println("третий игрок угадал?" + p3isRight);
			System.out.println("конец игры");
			break;
		} else{
			System.out.println("Игроки должны попробовать еще раз");
		}
		}
	}
}
public class Player{
	int number = 0;
	public void guess(){
		number = (int) (Math.random() * 10);
		System.out.println("Думаю, это число " + number);
	}
}
public class GameLauncher{
	public static void main (String[] args){
		GuessGame game = new GuessGame();
		game.startGame();
	}
}
===================
package com.codegym.task.task05.task0523;

/* 
Constructor

*/

public class Circle {
    public Color color;

    public static void main(String[] args) {
        Circle circle = new Circle();
        circle.color.setDescription("Red");
        System.out.println(circle.color.getDescription());
    }
// ошибка была в возвращаемом типе void, в конструкторе его нельзя
    public ===void== Circle() {
        color = new Color();
    }

    public class Color {
        String description;

        public String getDescription() {
            return description;
        }

        public void setDescription(String description) {
            this.description = description;
        }
    }
}
================
package com.codegym.task.task05.task0524;

/* 
The basis of a wheel

*/

public class Circle {
    public double x;
    public double y;
    public double r;

    //write your code here
     public Circle(double x , double y , double r){
        this.x = x;
        this.y = y;
        this.r = r;
    }
    public static void main(String[] args) {

    }
}
==========
Конструктор по умолчанию исключается из класса после создания конструктора с аргументами. !!!!!!!!!!!!!!!!!!!!!!!!!!!

На самом деле, мы уже видели подтверждение этому выше. Это было в этом коде:

public class Cat {

   String name;
   int age;

   public Cat(String name, int age) {
       this.name = name;
       this.age = age;
   }

   public static void main(String[] args) {

       Cat smudge = new Cat(); //Error!
   }
}
========================
Мы не смогли создать Cat без имени и возраста, потому что мы объявили Cat конструктор string и int параметров. Это заставило конструктор по умолчанию немедленно исчезнуть из класса. Поэтому не забывайте, что если вам нужно несколько конструкторов в вашем классе, включая конструктор без аргументов, вам придется объявить его отдельно . Например, предположим, что мы создаем программу для ветеринарной клиники. Наша клиника хочет делать добрые дела и помогать бездомным котятам, чьи имена и возраст неизвестны. Тогда наш код должен выглядеть так:
public class Cat {

   String name;
   int age;

   // For cats with owners
   public Cat(String name, int age) {
       this.name = name;
       this.age = age;
   }

   // For street cats
   public Cat() {
   }

   public static void main(String[] args) {

       Cat smudge = new Cat("Smudge", 5);
       Cat streetCat = new Cat();
   }
}
=================
public class Cat {

   String name;
   int age;

   public Cat(int age, String name) {
       this.name = name;
       this.age = age;
   }

   public static void main(String[] args) {

       Cat smudge = new Cat("Smudge", 10); // Error!
   }
}
Почему ошибка ? Потому что сначала должно быть число, а потом строка
===================
public class Animal {

   public Animal() {
       System.out.println("Animal constructor executed");
   }
}


public class Cat extends Animal {

   public Cat() {
       System.out.println("Cat constructor executed!");
   }

   public static void main(String[] args) {
       Cat cat = new Cat();
   }
}
=============================
На самом деле, это работает именно так! Зачем? Одна из причин заключается в том, чтобы избежать дублирования полей, общих для двух классов. Например, у каждого животного есть сердце и мозг, но не у каждого животного есть хвост. Мы могли бы объявить поля мозга и сердца , которые являются общими для всех животных, в Animalродительском классе, и хвостовое поле в Catподклассе. , Теперь мы объявим Catконструктор класса, который принимает аргументы для всех 3 полей.
public class Cat extends Animal {

   String tail;

   public Cat(String brain, String heart, String tail) {
       this.brain = brain;
       this.heart = heart;
       this.tail = tail;
   }

   public static void main(String[] args) {
       Cat cat = new Cat("Brain", "Heart", "Tail");
   }
}
===========================
Достаточно вызвать конструктор родительского класса и передать необходимые аргументы:

public class Animal {

   String brain;
   String heart;

   public Animal(String brain, String heart) {
       this.brain = brain;
       this.heart = heart;
   }

public class Cat extends Animal {

   String tail;

   public Cat(String brain, String heart, String tail) {
       super(brain, heart); // super () всегда должен быть первым в конструкторе! 
	   // Компилятор знает, что при создании объекта дочернего класса конструктор базового класса вызывается первым. И если вы попытаетесь вручную изменить это поведение, компилятор не допустит этого.
       this.tail = tail;
   }

   public static void main(String[] args) {
       Cat cat = new Cat("Brain", "Heart", "Tail");
   }
}
=====================
public class Animal {

   String brain = "Initial value of brain in the Animal class";
   String heart = "Initial value of heart in the Animal class";

   public static int animalCount = 7700000;

   public Animal(String brain, String heart) {
       System.out.println("Animal base class constructor is running");
       System.out.println("Have the variables of the Animal class already been initialized?");
       System.out.println("Current value of static variable animalCount = " + animalCount);
       System.out.println("Current value of brain in the Animal class = " + this.brain);
       System.out.println("Current value of heart in the Animal class = " + this.heart);
       System.out.println("Have the variables of the Cat class already been initialized?");
       System.out.println("Current value of static variable catCount = " + Cat.catCount);

       this.brain = brain;
       this.heart = heart;
       System.out.println("Animal base class constructor is done!");
       System.out.println("Current value of brain = " + this.brain);
       System.out.println("Current value of heart = " + this.heart);
   }
}

public class Cat extends Animal {

   String tail = "Initial value of tail in the Cat class";

   static int catCount = 37;

   public Cat(String brain, String heart, String tail) {
       super(brain, heart);
       System.out.println("The cat class constructor has started (The Animal constructor already finished)");
       System.out.println("Current value of static variable catCount = " + catCount);
       System.out.println("Current value of tail = " + this.tail);
       this.tail = tail;
       System.out.println("Current value of tail = " + this.tail);
   }

   public static void main(String[] args) {
       Cat cat = new Cat("Brain", "Heart", "Tail");
   }
}
Итак, теперь мы можем ясно видеть порядок инициализации переменных и вызовов конструктора при создании нового объекта:

Статические переменные базового класса ( Animal) инициализируются. В нашем случае Animalпеременная класса animalCount установлена ​​в 7700000.

Статические переменные дочернего класса ( Cat) инициализируются.

Примечание: мы все еще внутри Animalконструктора, и мы уже отобразили:

Работает конструктор базового класса Animal
Переменные класса Animal уже инициализированы? 
Текущее значение статической переменной animalCount = 7700000 
Текущее значение мозга в классе Animal = Начальное значение мозга в классе Animal 
Текущее значение сердца в классе Animal = Начальное значение сердца в классе Animal 
Уже есть переменные класса Cat были инициализированы? 
Текущее значение статической переменной catCount = 37


Затем нестатические переменные базового класса инициализируются. Мы специально присвоили им начальные значения, которые затем заменяются в конструкторе. Конструктор Animal еще не закончен, но начальные значения мозга и сердца уже заданы:

Работает конструктор базового класса Animal 
Переменные класса Animal уже инициализированы? 
Текущее значение статической переменной animalCount = 7700000 
Текущее значение мозга в классе Animal = Начальное значение мозга в классе Animal 
Текущее значение сердца в классе Animal = Начальное значение сердца в классе Animal


Начнется конструктор базового класса . 
Мы уже убедились, что этот шаг четвертый: в первых трех шагах в начале Animalконструктора многим переменным уже были присвоены значения.


Нестатические поля дочернего класса ( Cat) инициализируются. 
Это происходит до Cat запуска конструктора. 
Когда он начинает работать, переменная tail уже имеет значение:

Запуск конструктора класса cat (конструктор Animal уже завершен) Текущее значение статической переменной catCount = 37 Текущее значение tail = Начальное значение tail в классе Cat


Конструктор Cat дочернего класса называется

И вот как выглядит создание объекта в Java!

Должен сказать, что мы не большие поклонники rote-learning, но лучше запомнить порядок инициализации переменных и вызовов конструктора .
====================================
public class Cat {

   private String name;
   private int age;
   private int weight;

   public Cat(String name, int age, int weight) {
       this.name = name;
       this.age = age;
       this.weight = weight;
   }

   public Cat() {
   }

   public void sayMeow() {
       System.out.println("Meow!");
   }

   public String getName() {
       return name;
   }

   public void setName(String name) {
       this.name = name;
   }

   public int getAge() {
       return age;
   }

   public void setAge(int age) {
       this.age = age;
   }

   public int getWeight() {
       return weight;
   }

   public void setWeight(int weight) {
       this.weight = weight;
   }
}
===============
public class Main {

   public static void main(String[] args) {

       Cat smudge = new Cat("Smudge", 5, 4);

       System.out.println("Cat's original name: " + smudge.getName());
       smudge.setName("Mr. Smudge");
       System.out.println("Cat's new name: " + smudge.getName()); // поменялось имя
   }
}
Здесь мы используем как геттеры, так и сеттеры. Сначала мы используем геттер, чтобы получить и отобразить оригинальное имя кота. Затем мы используем установщик, чтобы назначить новое имя («Mr. Smudge»). И затем мы используем получатель еще раз, чтобы получить имя (чтобы проверить, действительно ли оно изменилось).  
И в отличие от поля, метод позволяет вам написать логику проверки, необходимую для предотвращения недопустимых значений. Например, вы можете легко предотвратить назначение отрицательного числа в качестве возраста:

public void setAge(int age) {
   if (age >= 0) {
       this.age = age;
   } else {
       System.out.println("Error! Age can't be negative!");
   }
}
====================
package com.codegym.task.task05.task0525;

/* 
The whole duck isn't enough

*/

public class Solution {

    public static void main(String[] args) {
        Duck duck1 = new Duck();
        Duck duck2 = new Duck();
        System.out.println(duck1);
        System.out.println(duck2);
        Dog dog1 = new Dog();
        Dog dog2 = new Dog();
        System.out.println(dog1);
        System.out.println(dog2);
        Cat cat1 = new Cat();
        Cat cat2 = new Cat();
        System.out.println(cat1);
        System.out.println(cat2);

        //write your code here
    }

    public static class Duck {
        public String toString() {
            return "Duck";
        }
    }
    public static class Cat {
        public String toString() {
            return "Cat";
        }
    }
    public static class Dog {
        public String toString() {
            return "Dog";
        }
    }

    //write your code here
}
===========================
package com.codegym.task.task05.task0526;

/* 
Man and woman

*/

public class Solution {
    
   public static void main(String[] args) {
        Man man = new Man("Kitty",5,"Address 12"); 
        Man man1 = new Man("Kittвy",53,"Address 122"); 
       
        
     //    System.out.println(man.name + " " + man.age + " " + man.address); 
     //    System.out.println(man1.name + " " + man1.age + " " + man1.address); 
        Woman woman = new Woman("Kitty",5,"Address 12"); 
        Woman woman1 = new Woman("Kitty",5,"Address 12"); 
       
        
     //    System.out.println(name + " " + age + " " + address); 
      //   System.out.println(woman1.name + " " + woman1.age + " " + woman1.address); 
        //write your code here
    }

    public static class Man {
        protected String name;
        protected int age;
        protected String address; 

        public Man(String name, int age, String address) {
            this.name = name;
            this.age = age; 
            this.address = address;
             System.out.println(name + " " + age + " " + address);
        } 
    }
    public static class Woman {
        protected String name;
        protected int age;
        protected String address; 

        public Woman(String name, int age, String address) {
            this.name = name;
            this.age = age; 
            this.address = address;
               System.out.println(name + " " + age + " " + address);
        } 
    }
   
    
    //write your code here
}
==============================
package com.codegym.task.task05.task0527;

/* 
Tom and Jerry

*/

public class Solution {
    public static void main(String[] args) {
        Mouse jerryMouse = new Mouse("Jerry", 12, 5);
        Cat jerryCat = new Cat("Jer", 22, 53);
        Dog jerryDog = new Dog("tom", 122, 15);

        //write your code here
    }

    public static class Mouse {
        String name;
        int height;
        int tail;

        public Mouse(String name, int height, int tail) {
            this.name = name;
            this.height = height;
            this.tail = tail;
        }
    }
    public static class Dog {
        String name;
        int height;
        int tail;

        public Dog(String name, int height, int tail) {
            this.name = name;
            this.height = height;
            this.tail = tail;
        }
    }
    public static class Cat {
        String name;
        int height;
        int tail;

        public Cat(String name, int height, int tail) {
            this.name = name;
            this.height = height;
            this.tail = tail;
        }
    }

    //write your code here
}
================
package com.codegym.task.task05.task0528;

/* 
Display today's date

*/
import java.util.*;
import java.text.*;
public class Solution {
 
 

  public static void main(String args[]) {
      Date dateNow = new Date();
      SimpleDateFormat formatForDateNow = new SimpleDateFormat("MM dd yyyy");

      System.out.println(formatForDateNow.format(dateNow));
   }
}
=================
package com.codegym.task.task05.task0528;

/* 
Display today's date

*/
import java.util.*;
import java.text.*;
public class Solution {
 
 

  public static void main(String args[]) {
      Date dateNow = new Date();
      SimpleDateFormat formatForDateNow = new SimpleDateFormat("MM dd yyyy");

      System.out.println(formatForDateNow.format(dateNow));
   }
}
=====================
package com.codegym.task.task05.task0529;

import java.io.BufferedReader;
import java.io.InputStreamReader;

/* 
Console-based piggy bank

*/

public class Solution {
    public static void main(String[] args) throws Exception {
      
    
        BufferedReader buffer = new BufferedReader(new InputStreamReader(System.in));
        int sum = 0;
      //  int number = 0;
        int nAge1 = 0;
          while (true)
       {
           	String sAge1 = buffer.readLine();
           
        	if (sAge1.equals("sum"))
        		break;
    		int   number = Integer.parseInt(sAge1);
    	    sum += number;
       }
       
       System.out.println(sum);
        //write your code here
    }      
       
}
===============
package com.codegym.task.task05.task0530;

import java.io.*;

/* 
Boss, something weird is happening

*/

public class Solution {
    public static void main(String[] args) throws Exception {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        String a = reader.readLine();
        int number1 = Integer.parseInt(a);
        String b = reader.readLine();
        int number2 = Integer.parseInt(b);
        // ошибка была в том, что  reader.readLine() преобразовывает данные только в string а не в int

        int sum = number1 + number2;
        System.out.println("Sum = " + sum);
    }
}
====================
package com.codegym.task.task05.task0531;

import java.io.BufferedReader;
import java.io.InputStreamReader;

/* 
Improving functionality

*/

public class Solution {

    public static void main(String[] args) throws Exception {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        int a = Integer.parseInt(reader.readLine());
        int b = Integer.parseInt(reader.readLine());
        int c = Integer.parseInt(reader.readLine());
        int d = Integer.parseInt(reader.readLine());
        int e = Integer.parseInt(reader.readLine()); 

        int mi = min(a, b, c, d, e); 
        System.out.println("Minimum = " + mi);
    } 
     public static int min(int a, int b, int c, int d, int e) {
        int n = Math.min(a, b); 
        int min3 = Math.min(n, c); 
        int min4 = Math.min(min3, d);
        int min = Math.min(min4, e); 
        return min;  
       
    }
}
// this lines declares a variable 'm2' and sets it to (a is less than b) ?
//'a' if that is true :  'b' if that is false
int m2 =a < b ? a : b;  //'m2' now holds the lessor of 'a' and 'b'

// this line now checks if 'm2' is less than 'c' and sets it to 'm2' if that is true or
// 'c' if that is false
m2 = m2 < c ? m2 : c; // 'm2' now holds the lessor of 'm2' and 'c'

// checks if 'm2' is less than 'd' and sets 'm2' to the lower of the '2'
m2 = m2 < d ? m2 : d;

// checks if 'm2' is less than 'e' and sets 'm2' to the lower of the 2
m2 = m2 < e ? m2 : e;

// 'm2' will now hold the lowest value of 'a', 'b', 'c', 'd', 'e'
return m2;
==============================
package com.codegym.task.task05.task0532;

import java.io.*;

/* 
Task about algorithms

*/

public class Solution {
    public static void main(String[] args) throws Exception {
     
      BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
      int maximum = Integer.MIN_VALUE;

        //write your code here
        int N = Integer.parseInt(reader.readLine());
        if (N > 0) {
            while (N  > 0) {
                int numbers = Integer.parseInt(reader.readLine());
                if (numbers > maximum) {
                    maximum = numbers;
                    N -= 1;
                } else {
                    N -= 1;
                }
            }
            System.out.println(maximum);
        }
    }
}
==================
package com.codegym.task.task05.task0532;

import java.io.*;

/* 
Сканирует все значения и показывает их MAX

*/

public class Solution {
    public static void main(String[] args) throws Exception {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        int maximum = Integer.MIN_VALUE;
     while (true)
       {
            String sAge1 = reader.readLine();
            if (sAge1 == null){
                break;
            } 
            int   number = Integer.parseInt(sAge1);
           
           if (number > maximum)
           {
               maximum = number;
           }
           else
           {
              maximum = maximum; 
           }
       }
        System.out.println(maximum);
        
    }
}
==================
package com.codegym.task.task06.task0601;

/* 
Cat's finalize method

*/

public class Cat {
    protected void finalize() throws Throwable{
        
        }//write your code here
    public static void main(String[] args) {

    }
}
=========================
package com.codegym.task.task06.task0602;

/* 
Zombie cats, zombie dogs

*/

public class Cat {
    public static void main(String[] args) {

    }
 protected void finalize() throws Throwable{
        System.out.println("A Cat was destroyed");
        }
    //write your code here

}

class Dog {
    protected void finalize() throws Throwable{
        System.out.println("A Dog was destroyed");
        } //write your code here
}
=============================
package com.codegym.task.task06.task0603;

/* 
Cat and Dog objects: 50,000 each

*/

public class Solution {
    public static void main(String[] args) {
      //  int i = 0;
        for(int i = 1;i <= 50000; i++){
            new  Cat();
            new Dog();  
       } // write your code here
    }
}
class Cat {
    @Override
    protected void finalize() throws Throwable {
        super.finalize();
        System.out.println("A Cat was destroyed");
    }
}
class Dog {
    @Override
    protected void finalize() throws Throwable {
        super.finalize();
        System.out.println("A Dog was destroyed");
    }
}
================================
package com.codegym.task.task06.task0604;

/* 
Cat counter

*/
В конструкторе класса Cat , то есть public Cat () , увеличьте счетчик cat ( статическая переменная catCount класса Cat ) на 1 . Уменьшить его на 1 взавершать метод.
public class Cat {
    public static int catCount = 0;
    public Cat(){// дописать конструктор
        Cat.catCount++;// потом увеличить
    }
     protected void finalize() throws Throwable{ 
        Cat.catCount--; //  и уменьшить
    }
    //write your code here

    public static void main(String[] args) {

    }
}
============================
package com.codegym.task.task06.task0606;

import java.io.*;

/* 
Even and odd digits

*/
Парсит цифру в одной строке делением на 10 == number = number / 10;
public class Solution {

    public static int even;
    public static int odd;

    public static void main(String[] args) throws IOException {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        String sAge1 = reader.readLine();
		int number = Integer.parseInt(sAge1); 
		    if(number > 0){
		    //    123
                while(number > 0){ 
                   // n = number % 10; 
                   if(number % 2 == 0){
        				even++;
        			} else {
        				odd++;
        			} 
        		//	 System.out.println("Идет число: " + number);
        			number = number / 10;
        			
                } 
		    }    
        System.out.println("Even: " + even + " Odd: " + odd);
        //write your code here
    }
}
==================================
Объявление класса
class Cat                        // Class
{
    String name;                 // Variable

    Cat(String name)             // Constructor
    {
        this.name = name;        // Variable initialization
    }
}
Код в основном методе:
Cat cat1 = new Cat("Oscar"); // Create one object whose name variable contains "Oscar"
Cat cat2 = new Cat("Missy"); // Create one object whose name variable contains "Missy"
System.out.println(cat1.name);
System.out.println(cat2.name);
Вывод на экран
Oscar
Missy
==«Несмотря на то, что они объявлены в одном и том же классе (Cat), переменные cat1.nameи cat2.nameсодержат разные значения, потому что они ссылаются на разные объекты»==
«Однако для каждого экземпляра класса существует только одна копия статической переменной, и доступ к ней должен осуществляться с использованием имени класса».

Объявление класса
class Cat                   // Сlass
{
    String name;            // Instance (non-static) variable
    static int catCount;    // Static variable

    Cat(String name)
    {
        this.name = name;
        Cat.catCount++;   // Increment the static variable by 1
    }
}
Код в основном методе:
System.out.println(Cat.catCount);
Cat cat1 = new Cat("Oscar");

System.out.println(Cat.catCount);
Cat cat2 = new Cat("Missy");

System.out.println(cat1.name);
System.out.println(cat2.name);
System.out.println(Cat.catCount);
Вывод экрана:
0
1
Oscar
Missy
2
https://codegym.cc/quests/lectures/questsyntax.level06.lecture06
=============================
package com.codegym.task.task06.task0607;

/* 
Class counter

*/

public class Cat {
   public static int catCount;
   
   public Cat(){ 
        Cat.catCount++;    
   }
   //write your code here

    public static void main(String[] args) {

    }
}
=====================
package com.codegym.task.task06.task0608;

/* 
Static methods for cats

*/

public class Cat {
    private static int catCount = 0;

    public Cat() {
        catCount++;
    }
    public static int getCatCount() {
        return catCount; 
    }
    public static void setCatCount(int catCount) {
        Cat.catCount = catCount; //write your code here 
    }
    public static void main(String[] args) {

    }
}
=====================
package com.codegym.task.task06.task0609;
/* 
Distance between two points
Расчет расстояния между двумя точками
*/
public class Util {
    public static double getDistance(int x1, int y1, int x2, int y2) {
	//	    x1=1;
	//		y1=4;
	//		x2=5;
	//		y2=1;
        double dis = (double)Math.sqrt((x2 - x1)*(x2 - x1) + (y2 - y1)*(y2 - y1));
        return dis;
        //write your code here
    }
    public static void main(String[] args) {
    }
}
========================
package com.codegym.task.task06.task0610;

import java.io.BufferedReader;
import java.io.InputStreamReader;
/* 
ConsoleReader class
*/
public class ConsoleReader {
    public static String readString() throws Exception {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        String readString = reader.readLine();
	    return readString;
    }
    public static int readInt() throws Exception {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        String sAge1 = reader.readLine();
		int readInt = Integer.parseInt(sAge1); 
		return readInt;
    }
    public static double readDouble() throws Exception {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        String readString = reader.readLine();//write your code here
        double readDouble = Double.parseDouble(readString); 
		return readDouble;
    }
    public static boolean readBoolean() throws Exception {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        String readString = reader.readLine();//write your code here
        boolean readBoolean = Boolean.parseBoolean(readString);
        return readBoolean;
    }
    public static void main(String[] args) {

    }
}
===============================
//bro use this
package com.codegym.task.task06.task0611;

/*
StringHelper class

*/
import java.lang.String;
public class StringHelper {
    public static String multiply(String s) {
        String result = ""; 
        result = s.substring(0,s.length()); 
        return result + result + result + result + result;   
    }
    public static String multiply(String s, int count) {
        String result = "";
        for (int i = 0; i < count; i++) {
            result += s;
        }
        return result;
    }
    public static void main(String[] args) {
        StringHelper.multiply("GrigoreTurcan");  
    }
}
======================================
package com.codegym.task.task06.task0605;


import java.io.*;

/* 
Controlling body weight

*/

public class Solution {

    public static void main(String[] args) throws IOException {
        BufferedReader bis = new BufferedReader(new InputStreamReader(System.in));
        double weight = Double.parseDouble(bis.readLine());
        double height = Double.parseDouble(bis.readLine());

        Body.calculateBMI(weight, height);
    }

    public static class Body {
        public static void calculateBMI(double weight, double height) {
             double bmi = weight /  (height * height);
           if (bmi < 18.5){
             System.out.println("Underweight: BMI < 18.5");
           }  else if((bmi >= 18.5) && (bmi <= 24.9)){
              System.out.println("Normal: 18.5 <= BMI <= 24.9");
           } else if((bmi >= 25) && (bmi <= 29.9)){
              System.out.println("Overweight: 25 <= BMI <= 29.9");
           } else if(bmi >= 30){
              System.out.println("Obese: BMI >= 30");
           }
           // write your code here
        }
    }
}
=======================
package com.codegym.task.task06.task0612;

/* 
Calculator

*/

public class Calculator {
    public static int plus(int a, int b) {
       int bv = a + b; //write your code here
        return bv;
    }

    public static int minus(int a, int b) {
        int n = a - b;//write your code here
        return n;
    }

    public static int multiply(int a, int b) {
        int multiply = a * b; //write your code here
        return multiply;
    }

    public static double divide(int a, int b) {
        double d = ((double)a / (double)b);
        return d;
    }

    public static double percent(int a, int b) {
        double c = ((double)b / 100) * a;
        return c;
    }

    public static void main(String[] args) {

    }
}
================= 
package com.codegym.task.task06.task0613;

/* 
Cat and statics

*/

public class Solution {
    public static void main(String[] args) {
        for(int i = 1;i <= 10; i++){
            new  Cat(); 
       } 
        System.out.println(Cat.catCount);
        // Create 10 cats

        // Display the value of the variable catCount
    }

    public static class Cat {
         public static int catCount = 0;
         public Cat() {
              Cat.catCount++;
          }
        // Create a static variable catCount

        // Declare a constructor
    }
}
=========================
package com.codegym.task.task06.task0614;
import java.util.ArrayList;
/* 
Static cats

*/
public class Cat {
    //write your code here
    public static ArrayList<Cat> cats = new ArrayList<Cat>() ;
    public Cat() {
        cats.add(this); 
    }
    public static void main(String[] args) {
        //write your code here
        Cat cat1 = new Cat();
        Cat cat2 = new Cat();
        Cat cat3 = new Cat();
        Cat cat4 = new Cat();
        Cat cat5 = new Cat();
        Cat cat6 = new Cat();
        Cat cat7 = new Cat();
        Cat cat8 = new Cat();
        Cat cat9 = new Cat();
        Cat cat10 = new Cat();
           cats.add(cat1);
        cats.add(cat2);
        cats.add(cat3);
        cats.add(cat4);
        cats.add(cat5);
        cats.add(cat6);
        cats.add(cat7);
        cats.add(cat8);
        cats.add(cat9);
        cats.add(cat10);
        printCats();
    }
    public static void printCats() {
        //write your code here
        for(Cat cat :cats )
			System.out.println(cat);
    }
}
=====================
package com.codegym.task.task06.task0615;
/* 
Feng Shui and statics
*/
public class Solution {

    public static int A = 5;
    public int B = 2;
    public int C = A * B;

    public static void main(String[] args) {
        A = 15;
    }
}
============================
package com.codegym.task.task06.task0616;

/* 
Minimum number of statics

*/

public class Solution {
    public static int step;

    public static void main(String[] args) {
        method1();
    }

    public static void method1() {
        method2();
    }

    public static void method2() {
        new Solution().method3();
    }

    public  void method3() {
        method4();
    }

    public  void method4() {
        step++;
        for (StackTraceElement element : Thread.currentThread().getStackTrace())
            System.out.println(element);
        if (step > 1)
            return;
        main(null);
    }
}
===========================
package com.codegym.task.task06.task0617;
/* 
Notepad for new ideas
*/
public class Solution {
    public static void main(String[] args) {
        printIdea(new Idea());
    }    
    public static class Idea {
        public String s = "anny";
        public String getDescription() {
            return s; 
        }
    }
    public static void printIdea(Idea idea) {
        System.out.println(idea.getDescription());
    }
    //write your code here
}
======================
package com.codegym.task.task06.task0618;

/* 
KissMyShinyMetalRearActuator

*/

public class Solution {
    public static class KissMyShinyMetalRearActuator {
        public String toString() {
            return "Cat";
        } 
    }

    public static void main(String[] args) {
        KissMyShinyMetalRearActuator kissMyShinyMetalRearActuator = new KissMyShinyMetalRearActuator();
        //write your code here
        System.out.println(kissMyShinyMetalRearActuator);
    }
}
===========================
package com.codegym.task.task06.task0619;
/* 
Three static name variables
*/
public class Solution {
    public static String name = "anny3"; 
    
    public static class Cat {
         public static String name = "anny"; 
    }

    public static class Dog {
        public static String name = "anny2"; 
    }

    public static void main(String[] args) {

    }
}
=====================================
package com.codegym.task.task06.task0620;

import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;

/* 
Fixing the mistakes of youth

*/

public class Solution {
    public static int max = 100;
    public static int max1 = 100;

    public static void main(String[] args) throws IOException {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));

        String max = "The max is ";
        int a = Integer.parseInt(reader.readLine());
        int b = Integer.parseInt(reader.readLine());
        max1 = a > b ? a : b;

        System.out.println(max + max1);
    }

}
==============================
package com.codegym.task.task06.task0621;

import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;

/* 
Cat relations

*/
public class Solution {
    public static void main(String[] args) throws IOException {
         BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));

        String GrandfatherName = reader.readLine();
        Cat catGrandfather = new Cat(GrandfatherName);
        
        String GrandmotherName = reader.readLine();
        Cat catGrandmother = new Cat(GrandmotherName);        

        String fatherName = reader.readLine();
        Cat catFather = new Cat(fatherName, catGrandfather,null);  

        String motherName = reader.readLine();
        Cat catMother = new Cat(motherName, null, catGrandmother);

        String sonName = reader.readLine();
        Cat catSon = new Cat(sonName, catFather, catMother );

        String daughterName = reader.readLine();
        Cat catDaughter = new Cat(daughterName, catFather, catMother );

        System.out.println(catGrandfather);
        System.out.println(catGrandmother);  
        System.out.println(catFather);
        System.out.println(catMother); 
        System.out.println(catSon);        
        System.out.println(catDaughter);
    }
public static class Cat {
        private String name;
        //private Cat parent;
        private Cat mother;
        private Cat father;


        Cat(String name) {
            this.name = name;
        }

  

        Cat(String name, Cat father, Cat mother) {
            this.name = name;
            this.father = father;
            this.mother = mother;
         }

        @Override
        public String toString() {
            if (mother == null && father != null)
                return "The cat's name is " + name + ", no mother, "+ this.father.name + " is the father";
            else if (father == null && mother != null)
                return "The cat's name is " + name + ", "+ this.mother.name + " is the mother"+ ", no father ";                
            else if (father != null && mother != null)
                return "The cat's name is " + name + ", " + this.mother.name + ", is the mother, " +this.father.name + " is the father";
            else
            return "The cat's name is " + name + ", "  + "no mother, " +  "no father";
        }
    }
}
============================ 
package com.codegym.task.task06.task0622;
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.util.Arrays;
import java.util.Collections;

/* 
Ascending numbers

*/

public class Solution {
    public static void main(String[] args) throws Exception {



        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));

        //write your code here
       
        int a = Integer.parseInt(reader.readLine());
        int b = Integer.parseInt(reader.readLine());
        int c = Integer.parseInt(reader.readLine());
        int d = Integer.parseInt(reader.readLine());
        int e = Integer.parseInt(reader.readLine());

        //create an int array
        int[] numbers = new int[]{a,b,c,d,e}; 
        Arrays.sort(numbers); 
		//   System.out.println("Sorted list of integers:"); 
        for (int i = 0; i < numbers.length ; i++){
            System.out.println(numbers[i]);
         } 
        /* ArrayList<Integer> numbers = new ArrayList<>(Arrays.asList(a,b,c,d,e));

for (i = 0; i < ( numbers.length - 1 ); i++) {
            for (j = 0; j < numbers.length - i - 1; j++) {
                if (numbers[j] > numbers[j+1])
                {
                    temp = numbers[j];
                    numbers[j] = numbers[j+1];
                    numbers[j+1] = temp;
                }
            }  
        Arrays.sort(numbers);
        for(int j = 0; j<numbers.length; j++){
            System.out.println(Arrays.toString(list));
        } 
         if (a > b) {
            int temp = a;
            a = b;
            b = temp;
        }

        if (b  > c) {
            int temp = b;
            b = c;
            c = temp;
        }
        if(c > d){
            int temp = c;
            c = d;
            d = temp;
        }
        if(d > e){
            int temp =d;
            d = e;
            e = temp;
        }

      if (e > d) {
            int temp = e;
            e = d;
            d = temp;
        }


        System.out.println(a);
        System.out.println(b);
        System.out.println(c);
        System.out.println(d);
        System.out.println(e);
*/
				
    }
}
================================
String[] list = new String[5];
Создание String массива с 5 элементами
==
System.out.println(list[0]);
System.out.println(list[1]);
System.out.println(list[2]);
System.out.println(list[3]);
System.out.println(list[4]);
Будут показаны пять значений 'null'.
Чтобы получить доступ к значению определенного элемента массива, используйте квадратные скобки и индекс элемента.
--
int listCount = list.length;
listCount будет присвоено значение 5, которое является количеством элементов в listмассиве. 
list.length хранит длину массива (количество элементов).
list[1] = "Mom";
String s = list[1];
При назначении объектов элементам массива необходимо указать индекс элемента в квадратных скобках.
--
for (int i = 0; i < list.length; i++)
{
     System.out.println(list[i]);
}
Отображение значений всех элементов массива на экране.
===============================
Заполните 10-элементный массив числами от 10 до 1:
public class MainClass
{
    public static void main(String[] args)
    {
        int[] numbers = new int[10];

        for (int i = 0; i < numbers.length; i++)
        {
           numbers[i] = 10 - i;
        }
    }
}
Заполните 10-элементный массив числами от 0 до 9:
public class MainClass
{
    public static void main(String[] args)
    {
        int[] numbers = new int[10];

        for (int i = 0; i < numbers.length; i++)
        {
           numbers[i] = i;
        }
    }
}
Заполните 10-элементный массив числами от 9 до 0:
public class MainClass
{
    public static void main(String[] args)
    {
        int[] numbers = new int[10];

        for (int i = 0; i < numbers.length; i++)
        {
           numbers[i] = 9 - i;
        }
    }
}
Пример 2.
Чтение 10 строк с клавиатуры:
public class MainClass
{
  public static void main(String[] args) throws IOException
  {
    BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
    String[] list = new String[10];

    for (int i = 0; i < list.length; i++)
    {
      list[i] = reader.readLine();
     }
  }
}
Читать 10 чисел с клавиатуры:
public class MainClass
{
  public static void main(String[] args) throws IOException
  {
    BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
    int[] list = new int[10];

    for (int i = 0; i < list.length; i++)
    {
      String s = reader.readLine();
      list[i] = Integer.parseInt(s);
    }
  }
}
Пример 3.
Отображение массива на экране:
public class MainClass
{
    public static void main(String[] args) throws IOException
    {
        int[] list = new int[10];

        // Fill the array
        for (int i = 0; i < list.length; i++)
           list[i] = i;

        // Display the contents of the array
        for (int i = 0; i < list.length; i++)
          System.out.println(list[i]);
    }
}<
===========
Пример 4.
Быстрая (статическая) инициализация. Сложить элементы массива:
public class MainClass
{
    public static void main(String[] args) throws IOException
    {
        // Static initialization
        int[] list = {5, 6, 7, 8, 1, 2, 5, -7, -9, 2, 0};

        // Calculate the sum
        int sum = 0;
        for (int i = 0; i < list.length; i++)
           sum += list[i];

        System.out.println("Sum is " + sum);
    }
}
Пример 5.
Найти наименьший элемент в массиве:
public class MainClass
{
    public static void main(String[] args) throws IOException
    {
        int[] list = {5, 6, 7, 8, 1, 2, 5, -7, -9, 2, 0};

        int min = list[0];
        for (int i = 1; i < list.length; i++)
        {
             if (list[i] < min)
                  min = list[i];
        }

       System.out.println ("Min is " + min);
    }
}
======================
package com.codegym.task.task07.task0701;

import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;

/* 
Maximum in an array

*/

public class Solution {
    public static void main(String[] args) throws Exception {
        int[] array = initializeArray();
        int max = max(array);
        System.out.println(max);
    } 
    public static int[] initializeArray() throws IOException {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        int[] arr = new int[20];
    
        for (int i = 0; i < arr.length; i++)
        {
             arr[i] = Integer.parseInt(reader.readLine());
         } 
        return arr;
    }
    public static int max(int[] array) {
        int max1 = array[0];
     //   int max1 = 0;
        for (int i = 1; i < array.length; i++)
        {
             if (array[i] > max1){
                  max1 = array[i]; 
             }
        }
        // Find the maximum
         return max1;
    }
} 
=================
package com.codegym.task.task07.task0702;

import java.io.BufferedReader;
import java.io.InputStreamReader; 
/* 
String array in reverse order в обратном порядке
*/
public class Solution {
    public static void main(String[] args) throws Exception { 
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        String[] arr = new String[10];
        for (int i = 0; i < 8; i++)
          {
            arr[i] = reader.readLine();
          }
       
       for (int i = 9; i >= 0; i--)
          {
              System.out.println(arr[i]);
         }
    } 
}
==================
package com.codegym.task.task07.task0703;

import java.io.BufferedReader;
import java.io.InputStreamReader;
/* 
Lonely arrays interact
*/
public class Solution {
    public static void main(String[] args) throws Exception {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        String[] stringo = new String[10];
        int[] into = new int[10];
        for (int i = 0; i < 10; i++)
          {
            String stringovar = reader.readLine();
            stringo[i] = stringovar;
            into[i] = stringovar.length();
            System.out.println(into[i]); 
          }
    }
}
===========================
package com.codegym.task.task07.task0704;

import java.io.BufferedReader;
import java.io.InputStreamReader;

/* 
Flip the array

*/

public class Solution {
    public static void main(String[] args) throws Exception {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        int[] arr = new int[10];
        for (int i = 0; i < 10; i++)
          {
              arr[i] = Integer.parseInt(reader.readLine());
          }
       
       for (int i = 9; i >= 0; i--)
          {
              System.out.println(arr[i]);
         }
        //write your code here
    }
}
====================
package com.codegym.task.task07.task0705;

import java.io.BufferedReader;
import java.io.InputStreamReader;

/* 
One large array and two small ones
*/
public class Solution {
    public static void main(String[] args) throws Exception {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in)); 
        int[] intolarge = new int[20];
        for (int i = 0; i < 20; i++)
          {
            intolarge[i] = Integer.parseInt(reader.readLine()); 
          } 
        int[] intosmall1 = new int[10];
        for (int i = 0; i < 10; i++)
          {
            intosmall1[i] = intolarge[i];
         //   System.out.println(intosmall1[i]); 
          } 
       // System.out.println("закончил грузиться первый малый массив");
        
        int[] intosmall2 = new int[10];
        for (int i = 0; i < 10; i++)
          {
            intosmall2[i] = intolarge[i + 10];
            System.out.println(intosmall2[i]); 
          }
         //   System.out.println("закончил грузиться второй малый массив");
        //write your code here
    }
}
===============================
Создать массив из 15 целых чисел.
2. Заполните его значениями с клавиатуры.
3. Пусть индекс массива представляет номер дома. Значение массива по определенному индексу представляет количество людей, проживающих в соответствующем доме.
Дома с нечетными номерами расположены на одной стороне улицы. Те, у кого четные числа, на другой стороне. Узнайте, на какой стороне улицы живет больше людей.
4. Отобразите следующее сообщение: "в нечетных odd домах больше жителей."или" в четных even домах больше жителей."

package com.codegym.task.task07.task0706;

import java.io.BufferedReader;
import java.io.InputStreamReader;

/* 
Streets and houses

*/

public class Solution {
    public static int evenHouses;
    public static int oddHouses;

    public static void main(String[] args) throws Exception {
        //write your code here
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        int[] houses = new int[15];

        for (int i = 0; i < houses.length; i++) {
            houses[i] = Integer.parseInt(reader.readLine());
            if (i % 2 == 0) {
                evenHouses += houses[i];
            } else {
                oddHouses += houses[i];
            }
        }

        if (evenHouses > oddHouses)
            System.out.println("Even-numbered houses have more residents.");
        else if (oddHouses > evenHouses)
            System.out.println("Odd-numbered houses have more residents.");
    }

}
====================================
С массивом
public static void main(String[] args)
{
Reader r = new InputStreamReader(System.in);
BufferedReader reader = new BufferedReader(r);

// Read strings from the keyboard
String[] list = new String[10];
for (int i = 0; i < list.length; i++)
{
  String s = reader.readLine();
  list[i] = s;
}

// Display the contents of the array
for (int i = 0; i < list.length; i++)
{
  int j = list.length - i - 1;
  System.out.println( list[j] );
}
}
--
С ArrayList
public static void main(String[] args)
{
Reader r = new InputStreamReader(System.in);
BufferedReader reader = new BufferedReader(r);

// Read strings from the keyboard
ArrayList<String> list = new ArrayList<String>();
for (int i = 0; i < 10; i++)
{
  String s = reader.readLine();
  list.add(s);
}

// Display the contents of the collection
for (int i = 0; i < list.size(); i++)
{
  int j = list.size() - i - 1;
  System.out.println( list.get(j) );
}
}
=========================
package com.codegym.task.task07.task0707;

import java.util.ArrayList;

/* 
What sort of list is that?

*/

public class Solution {
    public static void main(String[] args) throws Exception {
        ArrayList<String> list = new ArrayList<String>();
          list.add("Денис"); 
          list.add("Маша"); 
          list.add("Федя"); 
          list.add("Коля"); 
          list.add("Миша"); 
         System.out.println(list.size());
        // Display the contents of the collection
        for (int i = 0; i < list.size(); i++)
        { 
          System.out.println(list.get(i));
        }
        
        //write your code here
    }
}
================
package com.codegym.task.task07.task0708;

import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.util.ArrayList;
import java.util.List;

/* 
Longest string

*/

public class Solution {
    private static List<String> strings = new ArrayList<String>();

    public static void main(String[] args) throws Exception {
           
            BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
            for (int i = 0; i < 5; i++)
            {
              String s = reader.readLine();
              int n = s.length();
              strings.add(s);
               if (n > 3){
                  System.out.println( strings.get(i) );
              }
            }
            
        //write your code here
    }
}
==============================
package com.codegym.task.task07.task0709;

import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.util.ArrayList;

/* 
Expressing ourselves more concisely

*/

public class Solution {
    public static void main(String[] args) throws Exception {
        ArrayList<String> list = new ArrayList<String>();
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
          
            int n = 5000;
            for (int i = 0; i < 5; i++)
            {
              String s = reader.readLine(); 
              list.add(s);
              if (n >= s.length()){
                  n = s.length();
                //   System.out.println(n);
              }
            }
           //    System.out.println(n);
            for (int i = 0; i < 5; i++)
            { 
              String m = list.get(i);
              if ( n == m.length()){
                  System.out.println( list.get(i) );
              }
            }
           
            
        //write your code here
    }
}
==========================
package com.codegym.task.task07.task0710;

import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.util.ArrayList;
/* 
To the top of the list
*/
public class Solution {
    public static void main(String[] args) throws Exception {
        ArrayList<String> list = new ArrayList<String>();
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in)); 
            for (int i = 0; i < 10; i++)
            {
              String s = reader.readLine(); 
              list.add(0, s);
            } 
         for (int i = 0; i < 10; i++)
            {  
                System.out.println( list.get(i) ); 
            }
        //write your code here
    }
}
============================
package com.codegym.task.task07.task0711;

import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.util.ArrayList;

/* 
Remove and insert

*/

public class Solution {
    public static void main(String[] args) throws Exception {
        ArrayList<String> list = new ArrayList<String>();
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in)); 
            for (int i = 0; i < 5; i++)
            {
              String s = reader.readLine(); 
              list.add(s);
            } 
         for (int k = 0; k < 13; k++)
            {   
                String t = list.get(4);
                list.add(0, t);
                list.remove(5);
            //    System.out.println( list.get(0) ); 
            } 
          for (int i = 0; i < 5; i++)
            {
               System.out.println( list.get(i) ); 
            } 
    }
}
================================= 
3. Узнайте, какая строка встречается ранее в списке: самая короткая или самая длинная.
Если несколько строк являются самыми короткими или самыми длинными, то рассмотрим самую первую такую строку.
4. Отобразите строку, описанную в шаге 3. Должна отображаться одна строка.
3. Программа должна отображать самую короткую строку, если она предшествует самой длинной.
4. Программа должна отображать самую длинную строку, если она предшествует самой короткой.
package com.codegym.task.task07.task0712;

import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.ArrayList;
/* 
Shortest or longest
*/
public class Solution {
    public static void main(String[] args) throws Exception {
        ArrayList<String> list = new ArrayList<String>();
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in)); 
           int min = 5000;
           int max = 0;
            for (int i = 0; i < 10; i++)
            {
              String s = reader.readLine(); 
              list.add(s);
              if (min >= s.length()){
                  min = s.length(); // минимальный
              }
              if (max <= s.length()){
                  max = s.length(); // максимальный
              }
            } 
            for (int i = 0; i < 10; i++)
            { 
              String m = list.get(i);
              if (( min == m.length()) || ( max == m.length())){
                  System.out.println( list.get(i) );
                  break;
              }
            }
    }
}
======================================
Так же, как и выше, но четные числа добавляются в конец списка, нечетные – в его начало.
public static void main(String[] args) throws IOException
{
    BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
    ArrayList<Integer> list = new ArrayList<Integer>();

    while (true)
    {
        String s = reader.readLine();
        if (s.isEmpty()) break;

        int x = Integer.parseInt(s);
        if (x % 2 == 0)  // Check that the remainder is zero when we divide by two
            list.add(x);         // Add to the end
        else
            list.add(0, x);      // Add to the beginning
    }
}
=============
Чтение списка номеров с клавиатуры
public static void main(String[] args) throws IOException
{
    BufferedReader reader = new BufferedReader(new InputStreamReader(System.in) );
    ArrayList<Integer> list = new ArrayList<Integer>() ;

    while (true)
    {
        String s = reader.readLine();
        if (s.isEmpty()) break;
        list.add(Integer.parseInt(s));
    }
}
=====================
Удалить все номера больше 5:
public static void main(String[] args) throws IOException
{
    BufferedReader reader = new BufferedReader(new InputStreamReader(System.in) );
    ArrayList<Integer> list = new ArrayList<Integer>();

    list.add(1);
    list.add(7);
    list.add(11);
    list.add(3);
    list.add(15);

    for (int i = 0; i < list.size(); ) // We moved the statement that increases i to inside the loop
    {
        if (list.get(i) > 5)
            list.remove(i);  // Don’t increase i if we deleted the current element
        else
            i++;
    }
}
==================================
Разделите массив на две части – четное и нечетное числа
public static void main(String[] args) throws IOException
{
    // Static initialization of the array
    int[] data = {1, 5, 6, 11, 3, 15, 7, 8};

    // Create a list where all elements are Integers
    ArrayList<Integer> list = new ArrayList<Integer> ();

    // Use the array to fill the list
    for (int i = 0; i < data.length; i++) 
		list.add(data[i]);

    ArrayList<Integer> even = new ArrayList<Integer>();  // Even numbers
    ArrayList<Integer> odd = new ArrayList<Integer>();    // Odd numbers

    for (int i = 0; i < list.size(); i++)
    {
        Integer x = list.get(i);
        if (x % 2 == 0)    // If x is even
            even.add(x);   // Add x to the collection of even numbers
        else
            odd.add(x);    // Add x to the collection of odd numbers
    }
}
====================================
Соединить списки
public static void main(String[] args) throws IOException
{
    ArrayList<Integer> list1 = new ArrayList<Integer>();   // Create a list
    Collections.addAll(list1, 1, 5, 6, 11, 3, 15, 7, 8);   // Fill the list

    ArrayList<Integer> list2 = new ArrayList<Integer>();
    Collections.addAll(list2, 1, 8, 6, 21, 53, 5, 67, 18);

    ArrayList<Integer> result = new ArrayList<Integer>();

    result.addAll(list1);   // Add all values from each list to the new list
    result.addAll(list2);

    for (Integer x : result)   // A fast way to loop over all elements, only for collections
    {
        System.out.println(x);
    }
}
=======================================
1. Введите 20 чисел с клавиатуры, сохраните их в списке, а затем отсортируйте их по трем другим спискам:
Числа, делящиеся на 3 (x%3==0), числа, делящиеся на 2 (x%2==0), и все остальные числа.
Числа, одновременно делящиеся на 3 и 2 (например, 6), входят в оба списка.
Порядок, в котором списки были объявлены очень важные.
2. Метод printList должен отображать каждый элемент списка в новой строке.
3. С помощью метода printList отобразите эти три списка. Во-первых, список на х%3, то в списке для X%2, а затем в последний список.
Требования:
1. Объявите и немедленно инициализируйте 4 переменные ArrayList<Integer>. Первый список будет основным. Другие списки будут дополнительными.
2. Прочитайте 20 чисел с клавиатуры и добавьте их в основной список.
3. Добавьте в первый дополнительный список все числа в основном списке, которые делятся на 3.
4. Добавить второй дополнительный список всех чисел в списке, которые делятся на 2.
5. Добавить в третий дополнительный список все остальные номера из основного списка.
6. Метод printList должен отображать каждый элемент переданного списка в новой строке.
7. Программа должна отображать три дополнительных списка с помощью метода printList.
package com.codegym.task.task07.task0713;

import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.util.ArrayList;
import java.util.List;

/* 
Playing Javarella

*/

public class Solution {
    public static void main(String[] args) throws Exception {
      BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        ArrayList<Integer> list = new ArrayList<Integer>();
        ArrayList<Integer> list1 = new ArrayList<Integer>();
        ArrayList<Integer> list2 = new ArrayList<Integer>();
        ArrayList<Integer> list3 = new ArrayList<Integer>();

        // считываем список через forLoop
        for (int i = 0; i < 20; i++)
            list.add(Integer.parseInt(reader.readLine()));

        for (int i = 0; i < 20; i++) {
            Integer x = list.get(i);

            if (x % 3 == 0) {
                list1.add(x);
            }
            if (x % 2 == 0) {
                list2.add(x);
            }
                if ((x % 3 != 0) && (x % 2 != 0)) {
                    list3.add(x);
                }
            }
        printList(list1);
        printList(list2);
        printList(list3);
    }
    public static void printList(List<Integer> list) {
        //напишите тут ваш код
        for (int i = 0; i < list.size(); i++) {
            System.out.println(list.get(i));

        }
    } 
}
==============
package com.codegym.task.task07.task0714;

import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.util.ArrayList;
import java.util.Collections;

/* 
Words in reverse

*/

public class Solution {
    public static void main(String[] args) throws Exception {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        ArrayList<String> list = new ArrayList<String>(); 

        // считываем список через forLoop
        for (int i = 0; i < 5; i++){
             String s = reader.readLine(); 
             list.add(s);
        }
            list.remove(2);
            int m = list.size();
             m--;
        for (int i = m; i >= 0; i--) {
            System.out.println( list.get(i) ); 
           
        }//write your code here
    }
}
==================================
package com.codegym.task.task07.task0715;

import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.util.ArrayList;

/* 
More Sam-I-Am

*/

public class Solution {
    public static void main(String[] args) throws Exception {
         ArrayList<String> list = new ArrayList<String>();  
       
             list.add("Sam"); 
             list.add("I"); 
             list.add("Am");  
             list.add(1,"Ham");  
             list.add(3, "Ham");  
             list.add("Ham");  
            
        for (int i = 0; i < list.size(); i++) {
            System.out.println( list.get(i) ); 
           
        }//write your code here 
    }
}
==========================
package com.codegym.task.task07.task0716;

import java.util.ArrayList;

/* 
R or L

*/

public class Solution {
    public static void main(String[] args) throws Exception {
        ArrayList<String> list = new ArrayList<String>();
        list.add("rose"); // 0
        list.add("love"); // 1
        list.add("lyre"); // 2
        list = fix(list);

        for (String s : list) {
            System.out.println(s);
        }
    } 
    public static ArrayList<String> fix(ArrayList<String> list) {
        ArrayList <String> list1 = new ArrayList <String> ();
        for(int i = 0; i < list.size(); i++){
            boolean flag = true;
            String s = list.get(i);
            if (s.contains("r")) flag = false;
            if(s.contains("l"))  {
                if (s.contains("r")) {
                    flag = true;
                }
                else {
                    list1.add(s);
                }
            }
       
         if (flag) list1.add(s);
        }
        return list1;
    }
}
==================
package com.codegym.task.task07.task0717;

import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.util.ArrayList;
/* 
Duplicating words
*/
public class Solution {
    public static void main(String[] args) throws Exception {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        ArrayList<String> list = new ArrayList<String>();  
        for (int i = 0; i < 10; i++){
             String s = reader.readLine(); 
             list.add(s);
        }
        // Read strings from the console and declare an ArrayList here

        ArrayList<String> result = doubleValues(list);
            for (String s : result) {
               System.out.println(s);
             }
        // Display result
    }

    public static ArrayList<String> doubleValues(ArrayList<String> list) {
        ArrayList <String> list1 = new ArrayList <String> ();
        for(int i = 0; i < list.size(); i++){ 
            String s = list.get(i);
            list1.add(s);
            list1.add(s);
        }
        return list1;
    }
}
============================================= 
package com.codegym.task.task07.task0718;

import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.ArrayList;

/* 
Checking the order

*/
public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        ArrayList<String> list = new ArrayList<String>();  
        for (int i = 0; i < 10; i++){
             String s = reader.readLine(); 
             list.add(s);
        }
        int max = 0;
         for (int i = 0; i < 10; i++)
            { 
              String m = list.get(i);
              if ( max > m.length()){
                  System.out.println(i);
                  break;
              } else {
                  max = m.length(); // максимальный
                }
              }
     } 
}
==========================================
Так создается массив:

public class Main {

   public static void main(String[] args) {

       String [] birthdays = new String[10];

   }
}
===================
String [] birthdays = new String[10];
String birthdays [] = new String[10];
=======
public class Main {

   public static void main(String[] args) {

       String birthdays [] = new String[10];
       birthdays[0] = "Jana Russell, March 12";
   }
}
==
Получение содержимого из массива
public class Main {

   public static void main(String[] args) {

       String birthdays [] = new String[10];
       birthdays[0] = "Jana Russell, March 12";
       birthdays[1] = "Landon Chan, May 18";
       birthdays[7] = "Rosie Mills, January 3";

       String rosieBirthday = birthdays[7];
       System.out.println(rosieBirthday);
   }
}
=
найти их длину с помощью специального свойства: length .

public class Main {

   public static void main(String[] args) {

       String birthdays [] = new String[10];
       birthdays[0] = "Jana Russell, March 12";
       birthdays[1] = "Landon Chan, May 18";
       birthdays[7] = "Rosie Mills, January 3";

       int birthdaysLength = birthdays.length;
       System.out.println(birthdaysLength);
   }
}
Выход консоли:
10
======
отобразить список всех дней рождения (чтобы убедиться, что никто не забыт). Вы можете сделать это в одном простом цикле:

public class Main {

   public static void main(String[] args) {

       String birthdays [] = new String[10];
       birthdays[0] = "Jana Russell, March 12";
       birthdays[1] = "Landon Chan, May 18";
       birthdays[2] = "Jeremiah Leonard, July 12";
       birthdays [3] = "Kenny Russo, September 7";
       birthdays[4] = "Tommie Barnes, November 9";
       birthdays [5] = "Roman Baranov, August 14";
       birthdays [6] = "Chanice Andersen, April 1";
       birthdays[7] = "Rosie Mills, January 3";
       birthdays [8] = "Keenan West, October 19";
       birthdays [9] = "Abraham McArthur, May 3";

       for (int i = 0; i < birthdays.length; i++) {
           System.out.println(birthdays[i]);
       }
   }
}
========
добавить массив ints, подобный этому:

public class Main {

   public static void main(String[] args) {
       int numbers [] = {7, 12, 8, 4, 33, 79, 1, 16, 2};
   }
}
=
вывести длину
public class Main {

   public static void main(String[] args) {
       int numbers [] = {7, 12, 8, 4, 33, 79, 1, 16, 2};
       System.out.println(numbers.length);
   }
}
==
еперь немного о том, как хранятся массивы в памяти.
Допустим, у нас есть массив из трех Catобъектов:
public class Cat {

   private String name;

   public Cat(String name) {
       this.name = name;
   }

   public static void main(String[] args) {

       Cat[] cats = new Cat[3];
       cats[0] = new Cat("Thomas");
       cats[1] = new Cat("Behemoth");
       cats[2] = new Cat("Lionel Messi");
   }
}
===
 3 массива с 5 коробками в каждом массиве. Если мы хотим поместить объект в третье поле второго массива, мы бы сделали это:
public static void main(String[] args) {
   Cat[][] cats = new Cat[3][5];
   cats[1][2] = new Cat("Fluffy");
}
[1] указывает на второй массив и [2]указывает на третье поле этого массива.

Поскольку двумерный массив состоит из нескольких массивов, для итерации по нему и отображения всех его значений (или заполнения всех его элементов) нам нужен вложенный цикл:

for (int i = 0; i < cats.length; i++) {
   for (int j = 0; j < cats[i].length; j++) {
       System.out.println(cats[i][j]);
   }
}
==
public class Main {

   public static void main(String[] args) {

       int[] numbers = {167, -2, 16, 99, 26, 92, 43, -234, 35, 80};

       for (int i = numbers.length - 1; i > 0; i--) {
           for (int j = 0; j < i; j++) {
           /* Compare the elements in pairs.
             If they are not in the right order,
             then swap them */
               if (numbers[j] > numbers[j + 1]) {
                   int tmp = numbers[j];
                   numbers[j] = numbers[j + 1];
                   numbers[j + 1] = tmp;
               }
           }
       }

   }
}
отсортировать этот массив по возрастанию: от наименьшего к наибольшему.
=============
 задача сортировки массива, с которым мы пытались справиться, решается в одну строку:

public class Main {

   public static void main(String[] args) {

       int[] numbers = {167, -2, 16, 99, 26, 92, 43, -234, 35, 80};

       Arrays.sort(numbers);

       System.out.println(Arrays.toString(numbers));

   }
}
=========
System.out.println(numbers.toString());
=========
копирование также легко выполняется с помощью Arraysкласса:

public class Main {

   public static void main(String[] args) {

       int[] numbers = {167, -2, 16, 99, 26, 92, 43, -234, 35, 80};

       int [] numbersCopy = Arrays.copyOf(numbers, numbers.length);
       System.out.println(Arrays.toString(numbersCopy));

   }
}
=============
public class Main {

   public static void main(String[] args) {

       int[][] numbers = {{1, 2, 3}, {4, 5, 6}, {7, 8, 9}};

       int[][] numbersCopy = Arrays.copyOf(numbers, numbers.length);

       System.out.println("Are these two-dimensional arrays equal?");
       System.out.println(Arrays.deepEquals(numbers, numbersCopy));

       System.out.println(Arrays.deepToString(numbersCopy));
   }
}

Выход:

Равны ли эти двумерные массивы?
true
[[1, 2, 3], [4, 5, 6], [7, 8, 9]]ы
======================
package com.codegym.task.task07.task0719;

import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.ArrayList;

/* 
Display numbers in reverse order
*/
public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        ArrayList<Integer> list = new ArrayList<Integer>(); 
        for (int i = 0; i < 10; i++){
           list.add(Integer.parseInt(reader.readLine()));
        } 
        for (int i = 9; i >= 0; i--)
          {
              System.out.println( list.get(i) ); 
         } 
        //write your code here
    }
}
=================
package com.codegym.task.task07.task0720;

import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.ArrayList;
/* 
Shuffled just in time

*/
public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        ArrayList<String> list = new ArrayList<String>();
    
        int N = Integer.parseInt(reader.readLine());
        int M = Integer.parseInt(reader.readLine());
        
        for(int i = 0;i < N;i++){
            list.add(reader.readLine());
        }
         for(int i = 0;i <  M;i++){
             list.add(list.get(0));
             list.remove(0);
        } 
        for(int i = 0;i < N;i++)
            System.out.println(list.get(i));
    }
} 
=========     
Min и max в массивах
Линия разлома жилой зоны насчитывает всего 20 домов, но их номера были присвоены бессистемно. Оказывается, начальные и конечные номера линии разлома были установлены случайным образом. Вот почему это так интересно и непредсказуемо! Давайте напишем небольшой эмулятор линии разлома: определим, где она начинается и где заканчивается. Чтобы сделать это, мы запихнем жилой блок в массив, заселим его номерами домов и найдем самый большой и самый маленький из них.

package com.codegym.task.task07.task0721;

import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
       import java.util.ArrayList;

/* 
Min and max in arrays

*/

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        int[] list = new int[20];
        for(int i = 0; i < 20; i++){
            list[i] = Integer.parseInt(reader.readLine()); 
        } 
        int max = list[0];
        int min = list[0];
        for(int i = 0; i < 20; i++) {  
              if ( max < list[i]){
                  max = list[i];
               } 
               if ( min > list[i]){
                  min = list[i];
               } 
              } 
        System.out.print(max + " " + min);
    }
}
=======================
package com.codegym.task.task07.task0722;

import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.ArrayList;
import java.util.*; 
/*
The end 
*/ 
public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        ArrayList<String> list = new ArrayList<String>();
        for(int i = 0;i < 0;i++){
            System.out.print("");
        }
        while(true)
        {String a = reader.readLine();
            if(a .equals("end"))
                break;
            else
                list.add(a);
        }
        Iterator itr = list.iterator();
        while(itr.hasNext())
        {

            System.out.println(itr.next());
        }
    }
}
=================
package com.codegym.task.task07.task0723;
import java.io.IOException;
/* 
Countdown

*/

public class Solution {
    public static void main(String[] args) {
        for (int i = 30; i >= 0; i--) {
            System.out.println(i);
            try{
				Thread.sleep(100);		//Приостанавливает поток на 1 секунду
			}
			catch(InterruptedException e){}
        }

        System.out.println("Boom!");
    }
}
=========================
package com.codegym.task.task07.task0724;

/* 
Family census

*/

public class Solution {
  //  Name: Anna, sex: female, age: 21, father: Paul, mother: Kate
// Name: Kate, sex: female, age: 55
// Name: Ben, sex: male, age: 2, father: Michael, mother: Anna
    public static void main(String[] args) {
         Human smudge = new Human("Smudge1", true, 21);
         Human smudg2 = new Human("Smudge2", true, 12);
         Human smudge3 = new Human("Smudgeteen", false, 65);
         Human smudge4 = new Human("Smudgeteen4", true, 44); 
         
         Human smudge253 = new Human("Smudge5", true, 30, smudge3, smudge4);
         Human smudge2534 = new Human("Smudge6", true, 11, smudge3, smudge4);
         Human smudge2535 = new Human("Smudge7", true, 31, smudge3, smudge4);
         Human smudge2536 = new Human("Smudge8", true, 12, smudge3, smudge4);
         Human smudge2537 = new Human("Smudge9", false, 54, smudge3, smudge4);
         
        System.out.println(smudge.toString());
        System.out.println(smudg2.toString());
        System.out.println(smudge3.toString());
        System.out.println(smudge4.toString()); 
        
        System.out.println(smudge253.toString());
        System.out.println(smudge2534.toString());
        System.out.println(smudge2535.toString());
        System.out.println(smudge2536.toString());
        System.out.println(smudge2537.toString());
         
         // write your code here
    }

    public static class Human { 
        private String name; 
        private boolean sex;
        private int age;
        static Human father;
        static Human mother; 
        
        public Human(String name, boolean sex, int age) {
            this.name = name;
            this.sex = sex;
            this.age = age; 
         } 
        public Human(String name, boolean sex, int age, Human father, Human mother) {
            this.name = name;
            this.sex = sex;
            this.age = age;
            Human.father = father;
            Human.mother = mother;
         } 
        // write your code here

        public String toString() {
            String text = "";
            text += "Name: " + this.name;
            text += ", sex: " + (this.sex ? "male" : "female");
            text += ", age: " + this.age;

            if (this.father != null)
                text += ", father: " + this.father.name;

            if (this.mother != null)
                text += ", mother: " + this.mother.name;

            return text;
        }
    }
}
======================
package com.codegym.task.task07.task0725;

/* 
Move one static modifier

*/

public class Solution {
    public final static int A = 5;
    public final static int B = 2;
    public final static int C = A * B;

    public static void main(String[] args) {
    }

    public  int getValue() {
        return C;
    }
}
========================
package com.codegym.task.task07.task0726;

import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.ArrayList;

/* 
Cat code won't compile

*/

public class Solution {
    public final static ArrayList<Cat> CATS = new ArrayList<>();

    public static void main(String[] args) throws IOException {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));

        while (true) {
             try {
                String name = reader.readLine();
                  int age = Integer.parseInt(reader.readLine());
                int weight = Integer.parseInt(reader.readLine());
                int tailLength = Integer.parseInt(reader.readLine()); 
                if (name.isEmpty()){  
                 break;
                }
                else
                {
                 Cat cat = new Cat(name, age, weight, tailLength);
                 CATS.add(cat); 
                } 
            }
            catch (Exception e)
            {
                break;
            }    
        } 
        printList();
    }

    public static void printList() {
        for (Cat cat : CATS) {
            System.out.println(cat);
        }
    }

    public static class Cat {
        private String name;
        private int age;
        private int weight;
        private int tailLength;

        Cat(String name, int age, int weight, int tailLength) {
            this.name = name;
            this.age = age;
            this.weight = weight;
            this.tailLength = tailLength;
        }

        @Override
        public String toString() {
            return "Cat's name: " + name + ", age: " + age + ", weight: " + weight + ", tail: " + tailLength;
        }
    }
}
======================
package com.codegym.task.task07.task0727;

import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.ArrayList;

/* 
Changing functionality

*/

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));

        ArrayList<String> list = new ArrayList<String>();
        while (true) {
            try {
            String s = reader.readLine();
            if (s.isEmpty()) break;
            list.add(s);
            }
            catch (Exception e)
            {
                break;
            }  
        }

        ArrayList<String> listUpperCase = new ArrayList<String>();
        for (int i = 0; i < list.size(); i++) {
            String s = list.get(i);
            listUpperCase.add(s.toUpperCase());
        }

        for (int i = 0; i < listUpperCase.size(); i++) { 
           if (listUpperCase.get(i).length() % 2 != 0)  {
           //   System.out.println(listUpperCase.get(i).length());
              System.out.print(listUpperCase.get(i) + " ");
              System.out.print(listUpperCase.get(i) + " ");
              System.out.println(listUpperCase.get(i) + " ");
             } else {
           //   System.out.println(listUpperCase.get(i).length());
              System.out.print(listUpperCase.get(i) + " ");
              System.out.println(listUpperCase.get(i) + " ");
             }
        }
    }
}
=======================
package com.codegym.task.task07.task0728;
import java.util.Arrays;
import java.io.BufferedReader;
import java.io.InputStreamReader; 
import java.util.Collections;
/* 
In decreasing order 
*/ 
public class Solution {
    public static void main(String[] args) throws Exception {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        Integer[] array = new Integer[20];
        for (int i = 0; i < 20; i++) {
            array[i] = Integer.parseInt(reader.readLine());
        }
 
        sort(array);  
        
        for (int i = 0; i < 20; i++) {
            System.out.println( array[i] ); 
        } 
    } 
    public static void sort(Integer[] array) {
      Arrays.sort(array, Collections.reverseOrder());
        
    }
}
==
package com.codegym.task.task07.task0728;

import java.util.Arrays;
import java.io.BufferedReader;
import java.io.InputStreamReader; 
import java.io.IOException;
import java.util.Collections;
/* 
In decreasing order
*/
public class Solution {
    public static void main(String[] args) throws Exception {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        int[] array = new int[20];
        Integer[] array1 = new Integer[20];
        for (int i = 0; i < 20; i++) {
                array[i] = Integer.parseInt(reader.readLine());  
        }

        sort(array); 
        
        for (int x : array) {
            System.out.println(x);
        }
    }
    public static void sort(int[] array) {
        Arrays.sort(array);
        Integer[] array1 = new Integer[20];
        for (int i = 0; i < 20; i++) {
                array1[i] = array[i];  
        }
        Arrays.sort(array1, Collections.reverseOrder());
         for (int i = 0; i < 20; i++) {
                array[i] = array1[i];  
        }
         //write your code here
    }
    
}
================
Display elements of a List
public static void main(String[] args)
{
    List<String> list = new ArrayList<String>();
    list.add("Rain");
    list.add("In");
    list.add("Spain");

    Iterator<String> iterator = list.iterator();// Get an iterator for the list

    while (iterator.hasNext())      // Check if there is another element
    {
        // Get the current element and move to the next one
        String text = iterator.next();

        System.out.println(text);
    }
}
==
Display elements of a Set
public static void main(String[] args)
{
    Set<String> set = new HashSet<String>();
    set.add("Rain");
    set.add("In");
    set.add("Spain");

     // Get an iterator for the set
     Iterator<String> iterator = set.iterator();

    while (iterator.hasNext())        // Check if there is another element
    {
       // Get the current element and move to the next one
       String text = iterator.next();

        System.out.println(text);
    }
}
==
Display elements of a Map
public static void main(String[] args)
{
    // All elements are stored in pairs
    Map<String, String> map = new HashMap<String, String>();
    map.put("first", "Rain");
    map.put("second", "In");
    map.put("third", "Spain");

    Iterator<Map.Entry<String, String>> iterator = map.entrySet().iterator();

   while (iterator.hasNext())
    {
        // Get a key-value pair
        Map.Entry<String, String> pair = iterator.next();
        String key = pair.getKey();            // Key
        String value = pair.getValue();        // Value
        System.out.println(key + ":" + value);
    }
}
 Сначала мы получаем из коллекции специальный объект-итератор. Итератор имеет только два метода.

1. Метод next () возвращает следующий элемент коллекции.

2. Метод hasNext () проверяет наличие элементов, которые не были возвращены next ()."
=======
Longhand
public static void main(String[] args)
{
  Set<String> set = new HashSet<String>();
    set.add("Rain");
    set.add("In");
    set.add("Spain");

    Iterator<String> iterator = set.iterator();
  while (iterator.hasNext())
  {
    String text = iterator.next();
    System.out.println(text);
  }
}
Shorthand
public static void main(String[] args)
{
    Set<String> set = new HashSet<String>();
    set.add("Rain");
    set.add("In");
    set.add("Spain");

   for (String text : set)
    {
        System.out.println(text);
    }
}
=
Display elements of a Map
public static void main(String[] args)
{
    Map<String, String> map = new HashMap<String, String>();
    map.put("first", "Rain");
    map.put("second", "In");
    map.put("third", "Spain");

    for (Map.Entry<String, String> pair : map.entrySet())
    {
        String key = pair.getKey();                      // Key
        String value = pair.getValue();                  // Value
        System.out.println(key + ":" + value);
    }
}
==========
package com.codegym.task.task08.task0801;

/* 
HashSet of plants

*/

import java.util.HashSet;

import java.util.Collections;
import java.io.IOException;
public class Solution {
    public static void main(String[] args) throws Exception {
        HashSet<String> set = new HashSet<String>();
        set.add("watermelon");
        set.add("banana");
        set.add("cherry");
        set.add("pear");
        set.add("cantaloupe");
        set.add("blackberry");
        set.add("ginseng");
        set.add("strawberry");
        set.add("iris");
        set.add("potato");  

       for (String text : set)
        {
            System.out.println(text);
        }
    //write your code here

    }
}
=============
package com.codegym.task.task08.task0802;

/* 
HashMap of 10 pairs

*/

import java.util.HashMap;
import java.util.Map;

public class Solution {
    public static void main(String[] args) throws Exception {
       HashMap<String, String> map = new HashMap<String, String>();
/* watermelon - melon,
banana - fruit,
cherry - fruit,
pear - fruit,
cantaloupe - melon,
blackberry - fruit,
ginseng - root,
strawberry - fruit,
iris - flower,
potato - tuber. */
        map.put("watermelon", "melon");
        map.put("banana", "fruit");
        map.put("cherry", "fruit");
        map.put("pear", "fruit");
        map.put("cantaloupe", "melon");
        map.put("blackberry", "fruit");
        map.put("ginseng", "root");
        map.put("strawberry", "fruit");
        map.put("iris", "flower");
        map.put("potato", "tuber"); 
    
    for (Map.Entry<String, String> pair : map.entrySet())
    {
        String key = pair.getKey();                      // Key
        String value = pair.getValue();                  // Value
        System.out.println(key + " - " + value);
    }
    //write your code here

    }
}
=======================
package com.codegym.task.task08.task0803;
import java.util.HashMap;
import java.util.Map;
/* 
HashMap of cats
*/
public class Solution {
    public static void main(String[] args) throws Exception {
        String[] cats = new String[]{"Tiger", "Missy", "Smokey", "Marmalade", "Oscar", "Snowball", "Boss", "Smudge", "Max", "Simba"};

        HashMap<String, Cat> map = addCatsToMap(cats);

        for (Map.Entry<String, Cat> pair : map.entrySet()) {
            System.out.println(pair.getKey() + " - " + pair.getValue());
        }
    } 
    public static HashMap<String, Cat> addCatsToMap(String[] cats) {
        HashMap<String, Cat> map = new HashMap<String, Cat>();
 
        for (int i = 0; i < cats.length; i++) { 
            String key = cats[i];
            map.put(key, new Cat(key));
        }
     return map;
	 
        //write your code here
    }
    public static class Cat {
        String name;

        public Cat(String name) {
            this.name = name;
        }

        @Override
        public String toString() {
            return name != null ? name.toUpperCase() : null;
        }
    }
}
===================== 
package com.codegym.task.task08.task0804;

import java.util.HashMap;
import java.util.Map;

/* 
Display a list of keys

Только ключи отобразить!!!!!!!!!!!
*/
public class Solution {
    public static void main(String[] args) throws Exception {
        HashMap<String, String> map = new HashMap<String, String>();
        map.put("Sim", "Sim");
        map.put("Tom", "Tom");
        map.put("Arbus", "Arbus");
        map.put("Baby", "Baby");
        map.put("Cat", "Cat");
        map.put("Dog", "Dog");
        map.put("Eat", "Eat");
        map.put("Food", "Food");
        map.put("Gevey", "Gevey");
        map.put("Hugs", "Hugs");

        printKeys(map);
    }

    public static void printKeys(Map<String, String> map) {
         for (Map.Entry<String, String> pair : map.entrySet()) {
            System.out.println(pair.getKey());
        }//write your code here
    }
}
================
package com.codegym.task.task08.task0805;

import java.util.HashMap;
import java.util.Map;

/* 
Values on the screen!

Только value отобразить!!!!!!!!!!!
*/

public class Solution {
    public static void main(String[] args) throws Exception {
        HashMap<String, String> map = new HashMap<String, String>();
        map.put("Sim", "Sim");
        map.put("Tom", "Tom");
        map.put("Arbus", "Arbus");
        map.put("Baby", "Baby");
        map.put("Cat", "Cat");
        map.put("Dog", "Dog");
        map.put("Eat", "Eat");
        map.put("Food", "Food");
        map.put("Gevey", "Gevey");
        map.put("Hugs", "Hugs");

        printValues(map);
    }

    public static void printValues(Map<String, String> map) {
         for (Map.Entry<String, String> pair : map.entrySet()) {
            System.out.println(pair.getValue());
        }//write your code here
    }
}
===================
package com.codegym.task.task08.task0806;

import java.util.HashMap;
import java.util.Map;
/* 
HashMap of Objects
*/
public class Solution {
    public static void main(String[] args) throws Exception {
        HashMap<String, Object> map = new HashMap<String, Object>();
        map.put("Sim", 5);
        map.put("Tom", 5.5);
        map.put("Arbus", false);
        map.put("Baby", null);
        map.put("Cat", "Cat");
        map.put("Eat", new Long(56));
        map.put("Food", new Character('3'));
        map.put("Gevey", '6');
        map.put("Hugs", 111111111111L);
        map.put("Comp", (double) 123);        
        for (Map.Entry<String, Object> pair : map.entrySet())
			{
				String key = pair.getKey();                      // Key
				Object value = pair.getValue();                  // Value
				System.out.println(key + " - " + value);
			}
    }
}
==================================
Получить текущую дату:
public static void main(String[] args) throws Exception
{
     Date today = new Date();
     System.out.println("Current date: " + today);
}
Рассчитать разницу между двумя датами
public static void main(String[] args) throws Exception
{
    Date currentTime = new Date();           // Get the current date and time
    Thread.sleep(3000);                      // Wait 3 seconds (3000 milliseconds)
    Date newTime = new Date();               // Get the new current time

    long msDelay = newTime.getTime() - currentTime.getTime(); // Calculate the difference
    System.out.println("Time difference is: " + msDelay + " in ms");
}
Проверить, прошло ли определенное время:
public static void main(String[] args) throws Exception
{
    Date startTime = new Date();

    long endTime = startTime.getTime() + 5000;  //    +5 seconds
    Date endDate = new Date(endTime);

    Thread.sleep(3000);              // Wait 3 seconds

    Date currentTime = new Date();
    if(currentTime.after(endDate))// Check whether currentTime is after endDate
    {
        System.out.println("End time!");
    }
}
Определите, сколько времени прошло с начала дня:
public static void main(String[] args) throws Exception
{
    Date currentTime = new Date();
    int hours = currentTime.getHours();
    int mins = currentTime.getMinutes();
    int secs = currentTime.getSeconds();

    System.out.println("Time since midnight " + hours + ":" + mins + ":" + secs);
}
Определите, сколько дней прошло с начала года:
public static void main(String[] args) throws Exception
{
    Date yearStartTime = new Date();
    yearStartTime.setHours(0);
    yearStartTime.setMinutes(0);
    yearStartTime.setSeconds(0);

    yearStartTime.setDate(1);      // First day of the month
    yearStartTime.setMonth(0);     // January (the months are indexed from 0 to 11)

    Date currentTime = new Date();
    long msTimeDifference = currentTime.getTime() - yearStartTime.getTime();
    long msDay = 24 * 60 * 60 * 1000;  // The number of milliseconds in 24 hours

    int dayCount = (int) (msTimeDifference/msDay); // The number of full days
    System.out.println("Days since the start of the year: " + dayCount);
}
===================
если вы собираетесь часто вставлять (или удалять) элементы в середине коллекции, лучше использовать LinkedList . Во всех остальных случаях ArrayList работает лучше.
package com.codegym.task.task08.task0807;

import java.util.ArrayList;
import java.util.LinkedList;
import java.util.List;
//import java.util.*; тоже можно 
/* 
LinkedList and ArrayList

*/

public class Solution {
    public static Object createArrayList() { 
        ArrayList arrayList = new ArrayList();
        return arrayList;
        //write your code here

    }

    public static Object createLinkedList() {
        LinkedList linkedList = new LinkedList();
         return linkedList;
         //write your code here

    }

    public static void main(String[] args) {

    }
}
=================
package com.codegym.task.task08.task0808;

import java.util.ArrayList;
import java.util.LinkedList;
import java.util.List;
/* 
10 thousand deletions and insertions
*/
public class Solution {
    public static void main(String[] args) throws Exception {
        // ArrayList
        ArrayList arrayList = new ArrayList();
        insert10000(arrayList);
        get10000(arrayList);
        set10000(arrayList);
        remove10000(arrayList);
        // LinkedList
        LinkedList linkedList = new LinkedList();
        insert10000(linkedList);
        get10000(linkedList);
        set10000(linkedList);
        remove10000(linkedList);
    }
    public static void insert10000(List list) { 
        for(int i = 0; i < 10000; i++){
              list.add("Rain"); 
        } 
    }
    public static void get10000(List list) {
        for(int i = 0; i < 10000; i++){
               list.get(i);
        } 
    }
    public static void set10000(List list) {
         for(int i = 0; i < 10000; i++){
              list.set(i, "Rain"); 
        } 
    }
    public static void remove10000(List list) { 
        for(int i = 0; i < 10000; i++){
              list.remove(0);
        } 
    }
}
====================
package com.codegym.task.task08.task0809;

import java.util.ArrayList;
import java.util.Date;
import java.util.LinkedList;
import java.util.List;

/* 
Time for 10,000 insertions
*/
public class Solution {
    public static void main(String[] args) {
        System.out.println(getInsertTimeInMs(new ArrayList()));
        System.out.println(getInsertTimeInMs(new LinkedList()));
    }

    public static long getInsertTimeInMs(List list) {
        Date startTime = new Date(); 
        long start = startTime.getTime();
        insert10000(list);

        Date endTime = new Date(); 
        long end = endTime.getTime(); // getTime - время в милисекундах
        return end - start;
    }

    public static void insert10000(List list) {
        for (int i = 0; i < 10000; i++) {
            list.add(0, new Object());
        }
    }
}
===========================
package com.codegym.task.task08.task0810;

import java.util.ArrayList;
import java.util.Date;
import java.util.LinkedList;
import java.util.List;

/* 
Time for 10,000 get calls

*/

public class Solution {
    public static void main(String[] args) {
        System.out.println(getGetTimeInMs(fill(new ArrayList())));
        System.out.println(getGetTimeInMs(fill(new LinkedList())));
    }

    public static List fill(List list) {
        for (int i = 0; i < 10000; i++) {
            list.add(new Object());
        }
        return list;
    }

    public static long getGetTimeInMs(List list) {
        Date startTime = new Date(); 
        long start = startTime.getTime();
       
        get10000(list);

        Date endTime = new Date(); 
        long end = endTime.getTime(); // getTime - время в милисекундах
        return end - start;// write your code here 
    }

    public static void get10000(List list) {
        if (list.isEmpty()) return;
        int x = list.size() / 2;

        for (int i = 0; i < 10000; i++) {
            list.get(x);
        }
    }
}
==================
package com.codegym.task.task08.task0811;

import java.util.ArrayList;
import java.util.LinkedList;
import java.util.List;

/* 
Method quartet

*/

public class Solution {
    public static List getListForGet() {
        ArrayList<Object> list = new ArrayList<>();
        return list;
        //write your code here
    }

    public static List getListForSet() {
        ArrayList<Object> list = new ArrayList<>();
        return list;       //write your code here
    }

    public static List getListForAddOrInsert() {
        LinkedList list = new LinkedList();
        return list;  //write your code here
    }

    public static List getListForRemove() {
        LinkedList list = new LinkedList();
        return list; //write your code here
    }

    public static void main(String[] args) {

    }
}
==================
package com.codegym.task.task08.task0812;

import java.io.*;
import java.util.ArrayList;

/* 
Longest sequence

*/
public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        ArrayList<Integer> list = new ArrayList<Integer>(); 
        ArrayList<Integer> list1 = new ArrayList<Integer>(); 
 
        for (int i = 0; i < 10; i++){
            list.add(Integer.parseInt(reader.readLine()));
            list1.add(list.get(i));
        }
            list1.add(0);
        int t = 0;
        int tnext = 0;
        int count = 1;
        
        ArrayList<Integer> list2 = new ArrayList<Integer>(); 
        for (int i = 0; i < 10; i++) {
            t = list1.get(i); 
            tnext = list1.get(i + 1);
             
             if (t == tnext){
                count++;
             } else {
                 list2.add(count); 
                 count = 1;
             }
            //write your code here
         }
         int max = 0;
          for (int i = 0; i < list2.size(); i++) {
              int m = list2.get(i);
              if ( max > m ){
                  
              } else {
                  max = m; // максимальный
              }
          } 
            System.out.println(max);
    }
}
==
более лучший вариант - нашел на форуме
package com.codegym.task.task08.task0812;

import java.io.*;
import java.util.ArrayList;

/* 
Longest sequence

*/
public class Solution {
    public static void main(String[] args) throws IOException {
        //write your code here
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
       
        ArrayList<Integer> list = new ArrayList<Integer>();
        int max = 0;
        int counter = 1;

        for (int i = 0; i < 10; i++) {
            list.add(Integer.parseInt(reader.readLine()));
        }
        for (int i = 1; i < 10; i++) {

            if (list.get(i - 1).equals(list.get(i))) counter++;
            else counter = 1;

            if (counter > max) max = counter;

        }
        System.out.println(max);
    }
}
==============================
Вот что мы можем сделать с Map:

Operation	Method
Get a set of all pairs - entrySet()
Get a set of all keys -	keySet()
Get a set of all values - values()
Add a pair	- put(key, value)
Get the value for the specified key - get(key)
Check whether the specified key is present - containsKey(key)
Check whether the specified value is present - containsValue(value)
Check whether the Map is empty - isEmpty()
Clear the Map - clear() 
Remove the value for the specified key - remove(key)
===============
package com.codegym.task.task08.task0813;

import java.util.Set;
import java.util.HashSet;

/* 
20 words that start with the letter "L"

*/

public class Solution {
    public static Set<String> createSet() {
        Set<String> set = new HashSet<String>();
        set.add("LvRain");
        set.add("LbIn");
        set.add("LnSpain");
        set.add("LmRain");
        set.add("LfIn");
        set.add("LgSpain");
        set.add("LhRain");
        set.add("LIjn");
        set.add("LrSpain");
        set.add("LtRain");
        set.add("LyIn");
        set.add("LSupain");
        set.add("LR6ain");
        set.add("L7In");
        set.add("L8Spain");
        set.add("L9Rain");
        set.add("L0In");
        set.add("L2Spain");
        set.add("LR3ain");
        set.add("LI4n"); 
        return set;//write your code here

    }

    public static void main(String[] args) {
		createSet();
    }
}
=======================================
package com.codegym.task.task08.task0814;

import java.util.HashSet;
import java.util.Set;
import java.util.Iterator;
/* 
Больше 10? Вы нам не подходите
*/
public class Solution {
    public static HashSet<Integer> createSet() {
      HashSet<Integer> set = new HashSet<>();
      for(int i = 0;i < 20;i++){
      set.add(i);
    }
    return set;
}
    public static HashSet<Integer> removeAllNumbersGreaterThan10(HashSet<Integer> set) {
       for(int i = 0;i < set.size(); i++){
         Iterator<Integer> iterator = set.iterator();
         while (iterator.hasNext())
            {
                if(iterator.next() > 10) {
                    iterator.remove();
                }
            }
       }
    return set; 
    }
    public static void main(String[] args) {
    }
}
== // более полная версия

import java.util.HashSet;
import java.util.Set;
import java.util.Iterator;
/* 
Больше 10? Вы нам не подходите
*/
public class Solution {
    public static HashSet<Integer> createSet() {
      HashSet<Integer> set = new HashSet<>();
      for(int i = 0;i < 20;i++){
      set.add(i);
    }
    return set;
}
    public static HashSet<Integer> removeAllNumbersGreaterThan10(HashSet<Integer> set) {
       for(int i = 0;i < set.size(); i++){
         Iterator<Integer> iterator = set.iterator();
         while (iterator.hasNext())
            {
                if(iterator.next() > 10) {
                    iterator.remove();
                }
            }
       }
	   Iterator<Integer> iterator = set.iterator();
         while (iterator.hasNext())
            {
               System.out.println(iterator.next());
            }
    return set; 
    }
    public static void main(String[] args) {
		HashSet set = createSet();
		HashSet newSet = removeAllNumbersGreaterThan10(set);
    }
}  
======================
package com.javarush.task.task08.task0815;

import java.util.HashMap;
import java.util.HashSet;

/* 
Перепись населения
*/

public class Solution {
    public static HashMap<String, String> createMap() {
        HashMap<String, String> Map = new HashMap<String, String>();
        Map.put("kekSurname3", "kekName1");
        Map.put("kekSurname2", "kekName3");
        Map.put("kekSurnamfe3", "kekName3");
        Map.put("kekSurdname", "kekName");
        Map.put("kekSusrname5", "kekName5");
        Map.put("kekSuvrname", "kekName");
        Map.put("kekSucrname", "kekName");
        Map.put("kekSudrname8", "kekName8");
        Map.put("keksSurname", "kekName");
        Map.put("kehkSurname", "kekName");
        return Map;
    }

    public static int getSameFirstNameCount(HashMap<String, String> map, String name) {
        int i = 0;
        for(String n : map.values())
            if(n.equals(name))
                i++;
        return i;
    }

    public static int getSameLastNameCount(HashMap<String, String> map, String lastName) {
        int i = 0;
        for(String n : map.keySet())
            if(n.equals(lastName))
                i++;
        return i;
    }

    public static void main(String[] args) {

    }
}
 верное верифицированное решение!!!!!!!!!!!!!! 23 попытки
=======================
package com.codegym.task.task08.task0815; 
 
import java.util.HashMap;
import java.util.HashSet;

/* 
Перепись населения
*/

public class Solution {
    public static HashMap<String, String> createMap() {
        HashMap<String, String> map = new HashMap<String, String>();
        for (int i = 0; i < 10; i++) {
           map.put("a1", "a2");
           map.put("b1", "b2");
           map.put("c1", "c2");
           map.put("d1", "d2");
           map.put("e1", "d2");
           map.put("f1", "f2");
           map.put("g1", "g2");
           map.put("h1", "h2");
           map.put("i1", "a2");
           map.put("j1", "j2");
           
        }
        return map;
    }

    public static int getCountTheSameFirstName(HashMap<String, String> map, String name) {
        int countName = 0;
        for (HashMap.Entry<String, String> mapName : map.entrySet()) {
            
				if (mapName.getValue().equals(name)){
					countName++;
				}
			 
        }
	//	System.out.println(countName);
        return countName;
    }

    public static int getCountTheSameLastName(HashMap<String, String> map, String lastName) {
        int countLastName = 0;
        for (HashMap.Entry<String, String> mapLastName : map.entrySet()) {
            if (mapLastName.getKey().equals(lastName)) { 
            countLastName++;
            }
        }
       // 	System.out.println(countLastName);
        return countLastName;
    }

    public static void main(String[] args) {
		getCountTheSameFirstName(createMap(), "a2");
         getCountTheSameLastName(createMap(), "j1");

    }
}
рабочий вариант!!!!!!!!!!!
==
import java.util.HashMap;
import java.util.HashSet;

/*
Перепись населения
*/

public class Solution {
    public static HashMap<String, String> createMap() {
        HashMap<String, String> map = new HashMap<>();
        String firstName [] = {"Александр", "Петр5", "Сергей", "Иван", "Петрt", "Владимир", "Константин", "Борис", "Петр", "Евгений"};
        String lastName [] = {"Губарь", "Лобач", "Петров", "Василевский", "Петров", "Черепанов", "Романов", "Мулгачев", "Косыгин", "Петров"};
        for (int i=0; i<10; i++)
            map.put(lastName[i], firstName[i]);
        for (String key: map.keySet())
            System.out.println(map.get(key));
        return map;
    }

    public static int getCountTheSameFirstName(HashMap<String, String> map, String name) {
        //напишите тут ваш код
        int count=0;
        for (String key: map.keySet())
            if (map.get(key)==name)
                count++;
        return count;
    }

    public static int getCountTheSameLastName(HashMap<String, String> map, String lastName) {
        //напишите тут ваш код
        int count=0;
        for (String key: map.keySet())
            if (key==lastName)
                count++;
        return count;
    }

    public static void main(String[] args) {
        createMap();
    }
}
==
  
// import java.security.acl.LastOwnerException;
import java.util.HashMap;
import java.util.HashSet;
import java.util.Map;

/* 
Перепись населения
*/

public class Solution {
    public static HashMap<String, String> createMap() {
      HashMap <String, String> map = new HashMap <> (  );
      map.hashCode ();

          map.put ("Ivanov","Vasya");
          map.put ("Vasilev","Vasya");
          map.put ("Konstantinov","Vasya");
          map.put ("IvanovVasilev", "Ivan");
          map.put ("IvanovKonstantinov", "Kolya");
          map.put ("Kolkin", "Kolya");
          map.put ("IvanovTemkin", "Tema");
          map.put ("IvanovIvanov", "Maks");
          map.put ("Temkin", "Tema");
          map.put ("IvanovIvanovIvanov", "Petya");

         for (String key: map.keySet ()) {
            System.out.println (key);
         }
        return map;

    }

    public static int getCountTheSameFirstName(HashMap<String, String> map, String name) {
        int count = 0;
        for (Map.Entry <String,String> korzina: map.entrySet ()){
            if (korzina.getValue ().equals ( name )) count++;
			// System.out.println(name + " - " + count);
        }
        System.out.println ("How many name: " + name + " " + count);
        return count;
    }

    public static int getCountTheSameLastName(HashMap<String, String> map, String lastName) {
		int yes = map.containsKey ( lastName ) ? 1:0;
		System.out.println ("Есть ли такая фамилия: " + yes);
        return yes;

    }

    public static void main(String[] args) {
        HashMap <String, String> map =  createMap ();
        getCountTheSameFirstName (map,"Petya");
        getCountTheSameLastName ( map, "IvanovIvanovIvanov" );
    }
}
==
 
// import java.security.acl.LastOwnerException;
import java.util.HashMap;
import java.util.HashSet;
import java.util.Map;

/* 
Перепись населения
*/

public class Solution {
    public static HashMap<String, String> createMap() {
      HashMap <String, String> map = new HashMap <> (  );
      map.hashCode ();

          map.put ("Ivanov","Vasya");
          map.put ("Vasilev","Vasya");
          map.put ("Konstantinov","Vasya");
          map.put ("IvanovVasilev", "Ivan");
          map.put ("IvanovKonstantinov", "Kolya");
          map.put ("Kolkin", "Kolya");
          map.put ("IvanovTemkin", "Tema");
          map.put ("IvanovIvanov", "Maks");
          map.put ("Temkin", "Tema");
          map.put ("IvanovIvanovIvanov", "Petya");

      //  for (String key: map.keySet ()) {
        //    System.out.println (key);
      //   }
        return map;
    }

    public static int getCountTheSameFirstName(HashMap<String, String> map, String name) {
        for (String key: map.keySet ()) {
        //    System.out.println (key);
			
          }
		int countyesname = 0;
        for (Map.Entry<String, String> entry : map.entrySet()){ 
				int yesname = map.containsValue ( name ) ? 1:0; 
				countyesname = countyesname + yesname; 
        }
     //   System.out.println ("How many people with the same name: " + countyesname);
        return countyesname;
    }

    public static int getCountTheSameLastName(HashMap<String, String> map, String lastName) {
         int countSur = 0;
        for (Map.Entry<String, String> entry : map.entrySet()){ 
				int yes = map.containsKey ( lastName ) ? 1:0; 
				countSur = countSur + yes; 
			}
      //  System.out.println ("How many people with the same lastname: " + countSur);
        return countSur;

    }

    public static void main(String[] args) {
		createMap ();
    //    HashMap <String, String> map =  createMap ();
    //     getCountTheSameFirstName (map,"Maks");
    //     getCountTheSameLastName ( map, "Ivanov" );
    }
}
==
  
// import java.security.acl.LastOwnerException;
import java.util.HashMap;
import java.util.HashSet;
import java.util.Map;

/* 
Перепись населения
*/

public class Solution {
    public static HashMap<String, String> createMap() {
      HashMap <String, String> map = new HashMap <> (  );
      map.hashCode ();

          map.put ("Ivanov","Vasya");
          map.put ("Vasilev","Vasya");
          map.put ("Konstantinov","Vasya");
          map.put ("IvanovVasilev", "Ivan");
          map.put ("IvanovKonstantinov", "Kolya");
          map.put ("Kolkin", "Kolya");
          map.put ("IvanovTemkin", "Tema");
          map.put ("IvanovIvanov", "Maks");
          map.put ("Temkin", "Tema");
          map.put ("IvanovIvanovIvanov", "Petya");

         for (String key: map.keySet ()) {
       //     System.out.println (key);
         }
        return map;

    }

    public static int getCountTheSameFirstName(HashMap<String, String> map, String name) {
        int count = 0;
        for (Map.Entry <String,String> korzina: map.entrySet ()){
            if (korzina.getValue ().equals ( name )) count++;
			// System.out.println(name + " - " + count);
        }
      //   System.out.println ("How many name: " + name + " " + count);
        return count;
    }

    public static int getCountTheSameLastName(HashMap<String, String> map, String lastName) {
		int yes = map.containsKey ( lastName ) ? 1:0;
	 //	System.out.println ("Есть ли такая фамилия: " + yes);
        return yes;

    }

    public static void main(String[] args) {
      //  HashMap <String, String> map =  createMap ();
      //  getCountTheSameFirstName (map,"Maks");
      //  getCountTheSameLastName ( map, "Ivanov3" );
    }
}
===================================
package com.codegym.task.task08.task0816;

import java.text.DateFormat;
import java.text.ParseException;
import java.text.SimpleDateFormat;
import java.util.Date;
import java.util.HashMap;
import java.util.Locale;
import java.util.Calendar;
import java.util.Iterator;
import java.util.Map;

/* 
Kind Emma and the summer holidays

*/

public class Solution {
    public static HashMap<String, Date> createMap() throws ParseException {
        DateFormat df = new SimpleDateFormat("MMMMM d yyyy", Locale.ENGLISH);
        HashMap<String, Date> map = new HashMap<String, Date>();
        map.put("Stallone", df.parse("JUNE 1 1980"));
        map.put("Revees", df.parse("MAY 5 1982"));
        map.put("Jolie", df.parse("FEBRUARY 1 1990"));
        map.put("Roberts", df.parse("MARCH 2 1983"));
        map.put("VanDame", df.parse("AUGUST 2 1999"));
        map.put("Pitt", df.parse("JANUARY 5 1997"));
        map.put("Cloonie", df.parse("DECEMBER 5 1995"));
        map.put("DelToro", df.parse("OCTOBER 9 1993"));
        map.put("Denzel", df.parse("NOVEMBER 8 1990"));
        map.put("Trucks", df.parse("MARCH 1 1988"));

        return map;//write your code here
    }

    public static void removeAllSummerPeople(HashMap<String, Date> map) {
        
        Calendar c = Calendar.getInstance();
       // for (String key: map.keySet())
		//		System.out.println(map.get(key));
		//		System.out.println("-----------------------");
        Iterator<Map.Entry<String, Date>> iter = map.entrySet().iterator();
           while (iter.hasNext()) {
			   Map.Entry<String, Date> entry = iter.next();
			   c.setTime(entry.getValue()); // add this
			   if(c.get(Calendar.MONTH) == 5 || c.get(Calendar.MONTH) == 6|| c.get(Calendar.MONTH) == 7){
				  iter.remove();
			   }
            }//write your code here
			//for (String key: map.keySet())
			//	System.out.println(map.get(key));
    }

    public static void main(String[] args) throws Exception{ 
        HashMap<String, Date> map2 = new HashMap<String, Date>(); 
        map2 = createMap();
        removeAllSummerPeople(map2);
    }
}
=================================
package com.codegym.task.task08.task0817;
    
import java.util.HashMap;
import java.util.Map;

import java.util.ArrayList;
/* 
We don't need repeats

*/

public class Solution {
    public static HashMap<String, String> createMap() {
         HashMap <String, String> map = new HashMap <> (  );
      map.hashCode ();
          map.put ("Ivanov","Vasya");
          map.put ("Vasilev","Vasya");
          map.put ("Konstantinov","Vasya");
          map.put ("IvanovVasilev", "Ivan");
          map.put ("IvanovKonstantinov", "Kolya");
          map.put ("Kolkin", "Kolya");
          map.put ("IvanovTemkin", "Tema");
          map.put ("IvanovIvanov", "Maks");
          map.put ("Temkin", "Tema");
          map.put ("IvanovIvanovIvanov", "Petya");
         for (String key: map.keySet ()) {
            // System.out.println (key);
         }		 
		// System.out.println ("==================");
        return map;//write your code here
    }
    public static void removeFirstNameDuplicates(Map<String, String> map) {
		ArrayList<String> test = new ArrayList<>();

		for(Map.Entry<String, String> pair : map.entrySet()){
			if(!test.contains(pair.getValue())) test.add(pair.getValue());
			else{
				removeItemFromMapByValue(map, pair.getValue());
				removeFirstNameDuplicates(map);
				break;
			}
		}
    }
    public static void removeItemFromMapByValue(Map<String, String> map, String value) {
        HashMap<String, String> copy = new HashMap<String, String>(map);
        for (Map.Entry<String, String> pair : copy.entrySet()) {
            if (pair.getValue().equals(value))
                map.remove(pair.getKey());
        }
		for (String key: map.keySet ()) {
           //  System.out.println (key);			 
         }  
    }
    public static void main(String[] args) {
		HashMap<String, String> map3 = new HashMap<String, String>(); 
        map3 = createMap();
        removeFirstNameDuplicates(map3);
    }
}
=======================================
package com.codegym.task.task08.task0818;
  
import java.util.HashMap;
import java.util.Map;

/* 
Only for the rich

*/

public class Solution {
    public static HashMap<String, Integer> createMap() {
           HashMap <String, Integer> map = new HashMap <> (  );
      map.hashCode ();
          map.put ("Ivanov", 3);
          map.put ("Vasilev",54);
          map.put ("Konstantinov",788);
          map.put ("IvanovVasilev", 3);
          map.put ("IvanovKonstantinov", 435);
          map.put ("Kolkin", 45);
          map.put ("IvanovTemkin", 3333);
          map.put ("IvanovIvanov", 324);
          map.put ("Temkin", 331);
          map.put ("IvanovIvanovIvanov", 876);
         for (String key: map.keySet ()) {
               System.out.println (key);
         }		 
	 	  System.out.println ("==================");
        return map; 
        //write your code here
    }

    public static void removeItemFromMap(HashMap<String, Integer> map) {
	HashMap<String, Integer> copy = new HashMap<String, Integer>(map);
        for (Map.Entry<String, Integer> pair : copy.entrySet()) {
            if (pair.getValue() < 500)
                map.remove(pair.getKey());
        }
		for (String key: map.keySet ()) {
               System.out.println (key);			  
         }  
    }
    public static void main(String[] args) {
		HashMap<String, Integer> map3 = new HashMap<String, Integer>(); 
        map3 = createMap();
        removeItemFromMap(map3);
    }
}
==============================
public static void main(java.lang.String[] args) {

   ArrayList<Integer> numbers = new ArrayList<>(Arrays.asList(1,2,3,4,5,6,7));
   System.out.println(Collections.max(numbers));
   System.out.println(Collections.min(numbers));

}
сортировка и реверс
public class Main {

   public static void main(java.lang.String[] args) {

       String mercury = new String("Mercury");
       String venus = new String("Venus");
       String earth = new String("Earth");
       String mars = new String("Mars");
       String jupiter = new String("Jupiter");
       String saturn = new String("Saturn");
       String uranus = new String("Uranus");
       String neptune = new String("Neptune");

       ArrayList<String> solarSystem = new ArrayList<>(Arrays.asList(mercury, venus, earth, mars,
               jupiter, saturn, uranus, neptune));
       Collections.sort(solarSystem);
       Collections.reverse(solarSystem);
       System.out.println(solarSystem);

   }
}
==
смешивание
public class Main {

   public static void main(java.lang.String[] args) {

       ArrayList<Integer> bingoDrum = new ArrayList<>(100);
       for (int i = 1; i <= 100; i++) {

           bingoDrum.add(i);// add the numbers 1 to 100 to the drum
       }

       Collections.shuffle(bingoDrum);// Mix it up
       System.out.println ("Your attention, please! Here are the first 10 numbers from the drum!");
       for (int i = 0; i < 10; i++) {

           System.out.println(bingoDrum.get(i));
       }

   }
}
======== - 
метод unmodifiableList - нельзя добавлять новые элементы - вызовет эксепшн
public class Main {

   public static void main(java.lang.String[] args) {

       String mercury = new String("Mercury");
       String venus = new String("Venus");
       String earth = new String("Earth");
       String mars = new String("Mars");
       String jupiter = new String("Jupiter");
       String saturn = new String("Saturn");
       String uranus = new String("Uranus");
       String neptune = new String("Neptune");

       List<String> solarSystem = Collections.unmodifiableList(new ArrayList<>(Arrays.asList(mercury, venus, earth, mars,
               jupiter, saturn, uranus, neptune)));
       solarSystem.add("Pluto");// Try to add a new element
   }
}
===========
ляется общим для всех видов списков. Еще одна довольно распространенная ситуация, которая может легко возникнуть - программист добавляет элементы в неправильном порядке. Если это произойдет, и мы обнаружим, что Меркурий и Нептун смешаны, мы можем исправить эту ошибку, используя swap()метод:

public class Main {

   public static void main(java.lang.String[] args) {

       String mercury = new String("Mercury");
       String venus = new String("Venus");
       String earth = new String("Earth");
       String mars = new String("Mars");
       String jupiter = new String("Jupiter");
       String saturn = new String("Saturn");
       String uranus = new String("Uranus");
       String neptune = new String("Neptune");

       ArrayList<String> solarSystem = new ArrayList<>(Arrays.asList(neptune, venus, earth, mars
       , jupiter, saturn, uranus, mercury));// The planets are in the wrong order
       System.out.println(solarSystem);

       Collections.swap(solarSystem, solarSystem.indexOf(mercury), solarSystem.indexOf(neptune));
       System.out.println(solarSystem);

   }
}

Мы передаем swap()методу наш список и индексы двух элементов, которые нужно поменять местами. Обратите внимание, что метод работает с индексами, а не ссылками. Итак, здесь нам пришлось использовать ArrayList.indexOf()метод.
======================
Наконец, мы познакомимся с очень интересным способом: disjoint(). Он проверяет, пересекаются ли две коллекции, т. Е. Имеют ли они хотя бы один идентичный элемент . Если они этого не делают, он возвращает истину. Если они это сделают, то он возвращает ложь

public class Main {

   public static void main(java.lang.String[] args) {

       String mercury = new String("Mercury");
       String venus = new String("Venus");
       String earth = new String("Earth");
       String mars = new String("Mars");
       String jupiter = new String("Jupiter");
       String saturn = new String("Saturn");
       String uranus = new String("Uranus");
       String neptune = new String("Neptune");

       ArrayList<String> solarSystemPart1 = new ArrayList<>(Arrays.asList(mercury, venus, earth, mars));
       ArrayList<String> solarSystemPart2 = new ArrayList<>(Arrays.asList(jupiter, saturn, uranus, neptune));

       System.out.println(Collections.disjoint(solarSystemPart1, solarSystemPart2));

   }
}

Как видите, наши два списка имеют совершенно разные элементы, поэтому программа выводит true . Это интересный и очень полезный класс. Мол Arrays, это делает много рутинной, утомительной работы для нас, позволяя нам сосредоточиться на других вещах.
==============
 две карты могут быть объединены в одну . Это достигается с помощью putAll()метода. Мы называем это первым HashMap, передаем второе в качестве аргумента, и элементы второго добавляются к первому:

public static void main(String[] args) {
   HashMap<Integer, String> passportsAndNames = new HashMap<>();
   HashMap<Integer, String> passportsAndNames2 = new HashMap<>();

   passportsAndNames.put (212133, "Bridget Logan");
   passportsAndNames.put (162348, "Ivan the Great");
   passportsAndNames.put(8082771, "Donald John Trump");

   passportsAndNames2.put(917352, "Clifford Patrick");
   passportsAndNames2.put(925648, "Mitchell Salgado");

   passportsAndNames.putAll(passportsAndNames2);
   System.out.println(passportsAndNames);
}

==============
Но есть и более удобный способ, то есть с помощью специальных методов , предоставляемых классом Date: before(), after()и equals(). Все они возвращают логическое значение. В before()методе проверяет , является ли раньше , чем дата передается в качестве аргумента нашей даты:

public class Main {
   public static void main(String[] args) throws InterruptedException {

       Date date1 = new Date();

       Thread.sleep(2000);// Suspend the program for 2 seconds
       Date date2 = new Date();

       System.out.println(date1.before(date2));
   }
}
=====================
 рассмотрим устаревший Date.getHours()метод, который возвращает количество часов, связанных с Date объектом.

public static void main(String[] args) {

   Date date1 = new Date();

   System.out.println(date1.getHours());
}

Если вы начнете код в 14:21 (2:21 PM), он покажет число 14
=============
GregorianCalendar класс. В нем реализован григорианский календарь
Например, он может:
- Добавить месяц или день к текущей дате
- Проверьте, является ли год високосным годом;
- Возврат отдельных компонентов даты (например, извлечение номера месяца из целой даты)
- Он также содержит очень удобную систему констант (многие из которых мы увидим ниже).
25 января 2017 года:

public static void main(String[] args) {

  Calendar calendar = new GregorianCalendar(2017, 0 , 25);
}
==================
public static void main(String[] args) {

   Calendar calendar = new GregorianCalendar(2017, 0 , 25);
   Date date = calendar.getTime();
   System.out.println(date);
}
Выходные данные:
ср 25 января 00:00:00 по Гринвичу 2017 года.
===================
public static void main(String[] args) {
   GregorianCalendar calendar = new GregorianCalendar(2017, Calendar.JANUARY , 25);
}
===============
public static void main(String[] args) {
   Calendar calendar = new GregorianCalendar();
   calendar.set(Calendar.YEAR, 2017);
   calendar.set(Calendar.MONTH, 0);
   calendar.set(Calendar.DAY_OF_MONTH, 25);
   calendar.set(Calendar.HOUR_OF_DAY, 19);
   calendar.set(Calendar.MINUTE, 42);
   calendar.set(Calendar.SECOND, 12);

   System.out.println(calendar.getTime());
}

Выходные данные:

 ср 25 янв. 19:42:12 GMT 2017 
 ==========================
 Например, давайте получим дату за 2 месяца до даты, которую мы создали:

public static void main(String[] args) {
   Calendar calendar = new GregorianCalendar(2017, Calendar.JANUARY , 25);
   calendar.set(Calendar.HOUR, 19);
   calendar.set(Calendar.MINUTE, 42);
   calendar.set(Calendar.SECOND, 12);

   calendar.add(Calendar.MONTH, -2); // To subtract, pass a negative number
   System.out.println(calendar.getTime());
}
=====================
public static void main(String[] args) {
   Calendar calendar = new GregorianCalendar(2017, Calendar.JANUARY , 25);
   calendar.set(Calendar.HOUR, 10);
   calendar.set(Calendar.MINUTE, 42);
   calendar.set(Calendar.SECOND, 12);

   calendar.roll(Calendar.MONTH, -2);
   System.out.println(calendar.getTime());
}
roll не меняет других значчений
=====================
мы можем получить все Calendar поля отдельно. Мы делаем это с помощью get()метода:

public static void main(String[] args) {
   GregorianCalendar calendar = new GregorianCalendar(2017, Calendar.JANUARY , 25);
   calendar.set(Calendar.HOUR, 10);
   calendar.set(Calendar.MINUTE, 42);
   calendar.set(Calendar.SECOND, 12);

   System.out.println("Year: " + calendar.get(Calendar.YEAR));
   System.out.println("Month: " + calendar.get(Calendar.MONTH));
   System.out.println("Week in the month: " + calendar.get(Calendar.WEEK_OF_MONTH));// Week in this month?

   System.out.println("Day: " + calendar.get(Calendar.DAY_OF_MONTH));

   System.out.println("Hours: " + calendar.get(Calendar.HOUR));
   System.out.println("Minutes: " + calendar.get(Calendar.MINUTE));
   System.out.println("Seconds: " + calendar.get(Calendar.SECOND));
   System.out.println("Milliseconds: " + calendar.get(Calendar.MILLISECOND));

}

Выходные данные:

 Год: 2017 Месяц: 0 Неделя в месяце: 5 День: 25 Часы: 10 Минуты: 42 Секунды: 12 Миллисекунды: 0 

=======================
Чтобы создать дату «до нашей эры», вам нужно использовать поле Calendar.ERA. Например, давайте создадим дату для битвы при Каннах, где Ганнибал победил римскую армию. Это произошло 2 августа 216 г. до н.э .:

public static void main(String[] args) {
   GregorianCalendar cannae = new GregorianCalendar(216, Calendar.AUGUST, 2);
   cannae.set(Calendar.ERA, GregorianCalendar.BC);

   DateFormat df = new SimpleDateFormat("MMM dd, yyy GG");
   System.out.println(df.format(cannae.getTime()));
}

Здесь мы использовали SimpleDateFormat класс для печати даты в формате, который нам легче понять (буквы «GG» означают, что мы хотим, чтобы эра отображалась). Выход:

 02 августа 216 г. до н. 
===========================
 Если вам не нравится этот формат даты

 сб 25 ноября 10:42:12 GMT 2017, 

то вы можете SimpleDateFormatлегко сделать его таким, каким вы хотите.

public static void main(String[] args) {

   SimpleDateFormat dateFormat = new SimpleDateFormat("EEEE, MMMM d, yyyy");
   Calendar calendar = new GregorianCalendar(2017, Calendar.JANUARY , 25);
   calendar.set(Calendar.HOUR, 10);
   calendar.set(Calendar.MINUTE, 42);
   calendar.set(Calendar.SECOND, 12);

   calendar.roll(Calendar.MONTH, -2);
   System.out.println(dateFormat.format(calendar.getTime()));
}

Выходной:

 суббота, 25 ноября 2017 г. 
 ========================
 package com.codegym.task.task08.task0819;
import java.util.Iterator;

import java.util.ArrayList;
import java.util.HashSet;
import java.util.Set;
/* 
Set of cats
*/
public class Solution {
    public static void main(String[] args) { 

        Set<Cat> cats = createCats();
		Iterator<Cat> itr = cats.iterator();
        while(itr.hasNext()) {
        	cats.remove(itr.next());
        	break;
        }
        //write your code here. step 3
        printCats(cats);
    }
    public static Set<Cat> createCats() {	
		Set<Cat> set = new HashSet<Cat>();
			Cat cat1 = new Cat();
			Cat cat2 = new Cat();
			Cat cat3 = new Cat(); 
				set.add(cat1); 
				set.add(cat2);
				set.add(cat3);
				
        //write your code here. step 2
        return set;
    }
    public static void printCats(Set<Cat> cats) {
         Iterator<Cat> iterator = cats.iterator();
		  while (iterator.hasNext())
		  {
			Cat text = iterator.next();
			System.out.println(text);
		  }// step 4
    }
	public static class Cat {	} // default constructor
    // step 1
}
============================
package com.codegym.task.task08.task0820;
  
import java.util.HashSet;
import java.util.Set;

import java.util.Iterator;
/* 
Animal set
1. Внутри класса решения создайте общедоступные статические классы Cat и Dog.
2. Реализуйте метод createCats, который должен возвращать набор с 4 кошками.
3. Реализуйте метод createDogs, который должен возвращать набор с 3 собаками.
4. Реализуйте метод join, который должен возвращать объединенный набор всех животных (всех кошек и собак).
5. Реализуйте метод removeCats, который должен удалить из набора домашних животных всех кошек в наборе cats.
6. Реализуйте метод printPets, который должен отображать всех животных в наборе домашних животных. 
Каждое животное должно быть на новой строке.
Требования:
1. Программа должна выводить текст на экран.
2. Внутри класса решения должны быть общедоступные статические классы Cat и Dog.
3. Метод Createcats() класса Solution должен возвращать набор, содержащий 4 кошки.
4. Метод createDogs() класса Solution должен возвращать набор, содержащий 3 собаки.
5. Метод join() класса решения должен возвращать объединенный набор всех животных (всех кошек и собак).
6. Метод removeCats () должен удалить из набора домашних животных всех кошек в наборе кошек.
7. Метод printPets () должен отображать всех животных в наборе домашних животных. Каждое животное должно быть на новой строке.
*/

public class Solution {
    public static void main(String[] args) {
        Set<Cat> cats = createCats();
	//	System.out.println("Вызов метода createCats");
        Set<Dog> dogs = createDogs();
	//	System.out.println("Вызов метода createDogs");

        Set<Object> pets = join(cats, dogs);
	//	System.out.println("Обьединение cats, dogs в pets");
        printPets(pets);
	//	System.out.println("Обьединение прошло успешно, теперь удаление котов");

        removeCats(pets, cats);
	//	System.out.println("Удаление прошло, теперь распечатка оставшихся животных");
        printPets(pets);
    }

    public static Set<Cat> createCats() {
        HashSet<Cat> result = new HashSet<Cat>();
			Cat cat1 = new Cat();
			Cat cat2 = new Cat();
			Cat cat3 = new Cat(); 
			Cat cat4 = new Cat(); 
				result.add(cat1); 
				result.add(cat2);
				result.add(cat3);
				result.add(cat4);
				  
        //write your code here

        return result;
    }

    public static Set<Dog> createDogs() {
        HashSet<Dog> resultdog = new HashSet<Dog>();
			Dog dog1 = new Dog();
			Dog dog2 = new Dog();
			Dog dog3 = new Dog();  
				resultdog.add(dog1); 
				resultdog.add(dog2);
				resultdog.add(dog3); 
        //write your code here
        return resultdog;
    }

    public static Set<Object> join(Set<Cat> cats, Set<Dog> dogs) {
	 HashSet<Object> catsAndDogs = new HashSet<>();

        catsAndDogs.addAll(cats);
        catsAndDogs.addAll(dogs);

        return catsAndDogs;
   }

    public static void removeCats(Set<Object> pets, Set<Cat> cats) {
        for(Cat cat : cats) {
            pets.remove(cat);
        }
		//write your code here
    }

    public static void printPets(Set<Object> pets) {
       Iterator<Object> iterator = pets.iterator();
		  while (iterator.hasNext())
		  {
			Object text = iterator.next();
			System.out.println(text);
		  }
		  //write your code here
    }
	public static class Cat {	} 
	public static class Dog {	} 
    //write your code here
}
============================
package com.codegym.task.task08.task0821;
 
import java.util.HashMap;
import java.util.Map;

/* 
Shared last names and first names
1. Программа должна выводить текст на экран.
2. Класс Solution должен иметь только три метода.
3. Метод createPeopleList () должен создавать и возвращать карту с элементами (String, String). Кроме того, добавьте 10 человек на карту.
4. В методе createPeopleList () необходимо добавить людей с одинаковой фамилией.
5. В методе createPeopleList () необходимо добавить людей с одинаковым именем.
6. Метод printPeopleList () должен отображать всех людей на карте. Отображать каждое значение в новой строке. Фамилия и имя должны быть разделены пробелом.
7. Метод main() должен вызывать метод createPeopleList ().
8. Метод main() должен вызывать метод printPeopleList ().
*/

public class Solution {
    public static void main(String[] args) {
        Map<String, String> map = createPeopleList();
        printPeopleList(map);
    }

    public static Map<String, String> createPeopleList() {
    Map<String, String> map = new HashMap<String, String>();
        map.put("first", "Rain");
        map.put("second", "In");
        map.put("third", "Spain");
        map.put("first", "Rain");
        map.put("second1", "In");
        map.put("third1", "Spain");
        map.put("first2", "Rain");
        map.put("second2", "In");
        map.put("third2", "Spain");
        map.put("first3", "Rain"); 
        //write your code here

        return map;
    }

    public static void printPeopleList(Map<String, String> map) {
        for (Map.Entry<String, String> s : map.entrySet()) {
            System.out.println(s.getKey() + " " + s.getValue());
        }
    }
}
===============================
package com.codegym.task.task08.task0822;

import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.ArrayList;
import java.util.LinkedList;
import java.util.List;
import java.util.Scanner;
/* 
Minimum of N numbers
ПРАВИЛЬНОЕ РЕШЕНИЕ!!!!!!!!!
Задание было неверно понято из за N ввода
То есть первый инпут это количество вводимого!!!!!!! уже кстати было подобное задание
Example intputs:
4      //for n
50    //1
24    //2
62    //3
8      //4
output:
8
*/

public class Solution
{
    public static void main(String[] args) throws Exception {
        List<Integer> integerList = getIntegerList();
        System.out.println(getMinimum(integerList));
    }

    public static int getMinimum(List<Integer> array)
    {
        int minValue = array.get(0);
        for(Integer i : array)
        {
           if (i < minValue) minValue = i;
        }
        return minValue;
    }

    public static List<Integer> getIntegerList() throws IOException
    {
        Scanner sc = new Scanner(System.in);
        List<Integer> list = new ArrayList<>();
        int N = sc.nextInt();

        for(int i = 0; i < N; i++)
        {
            list.add(sc.nextInt());
        }

        return list;
    }
}

=================
 
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.ArrayList;
import java.util.Collections;
import java.util.LinkedList;
import java.util.List;

/* 
Minimum of N numbers
# 1 BufferedReader.read () читает только один символ за раз (который преобразуется в байтовый код ASCII при вставке в int), а не всю строку, вы должны использовать readLine (), чтобы получить всю строку.

#2 вам нужно преобразовать то, что считывается BufferedReader в int, прежде чем вы сможете использовать.... Целое число.parseInt (br.с readline())

Внесите эти изменения в метод getInteger, где это необходимо,и вы должны пройти.
*/

public class Solution {
    public static void main(String[] args) throws Exception {
        List<Integer> integerList = getIntegerList();
        System.out.println(getMinimum(integerList));
    }

    public static int getMinimum(List<Integer> array) {

        int min = Collections.min(array);
        return min;
    }

    public static List<Integer> getIntegerList() throws IOException {

        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));

        int N = Integer.parseInt(reader.readLine());

        List<Integer> Numbers = new ArrayList<>(N);

        for (int i = 0; i < N; i++)
        {
            Integer a = Integer.parseInt(reader.readLine());
            Numbers.add(a);
        }
        return Numbers;
    }
}
=======================
package com.codegym.task.task08.task0823; 
 
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader; 
/* 
Going national
Полный capitalize 
*/

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        String s = reader.readLine();
      char[] ch = s.toLowerCase().trim().toCharArray();
        for(int i = 0; i < ch.length; i++) {
        	ch[0] = Character.toUpperCase(ch[0]);
        	if(Character.isWhitespace(ch[i])) {
        		if(Character.isLetter(ch[i+1]))
        			ch[i+1] = Character.toUpperCase(ch[i+1]);
        	}
        	
        }
        s = String.valueOf(ch);
        System.out.println(s); 
        //write your code here
    }
}
===============
package com.codegym.task.task08.task0823;

import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader; 
/* 
Going national
capitalize для первой буквы
*/

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        String s = reader.readLine();
       
        return str.substring(0, 1).toUpperCase() + str.substring(1).toLowerCase();
        System.out.print(s);
        //write your code here
    }
}
===============
package com.codegym.task.task08.task0824;

/* 
Make a family
1. Создайте человеческий класс со строковым именем, логическим полом, возрастом int и полями ArrayList<Human> children.
2. Создавайте и населяйте объекты так, чтобы в итоге у нас было: два дедушки, две бабушки, один отец, одна мать и трое детей.
3. Отображение всех объектов Human (подсказка: используйте метод toString() класса Human).

Требования:
1. Программа должна выводить текст на экран.
2. Класс людей должен иметь четыре поля.
3. Класс людей должен иметь один метод.
4. Класс Solution должен иметь один метод.
5. Программа должна создавать объекты и заполнять их данными, чтобы получить двух дедушек, двух бабушек, одного отца, одну мать и троих детей. Затем он должен отображать все человеческие объекты на экране.
*/

import java.lang.reflect.Array;
import java.util.ArrayList;

public class Solution {
    public static void main(String[] args) {

        ArrayList<Human> c1 = new ArrayList<Human>();
        ArrayList<Human> c2 = new ArrayList<Human>();
        ArrayList<Human> c3 = new ArrayList<Human>();

        //write your code here
        Human grandpa1 = new Human("Grandpa1",true,45,c2);
        Human grandpa2 = new Human("Grandpa2",true,85,c2);
        Human grandma1 = new Human("Grandma1",false,85,c2);
        Human grandma2 = new Human("Grandma2",false,35,c2);
        Human father = new Human("Father",true,25,c1);
        c2.add(father);
        Human mother = new Human("Mother",false,25,c1);
        c2.add(mother);
        Human chidl1 = new Human("Child1",false,5,c3);
        c1.add(chidl1);
        Human chidl2 = new Human("Child2",false,5,c3);
        c1.add(chidl2);
        Human chidl3 = new Human("Child3",false,5,c3);
        c1.add(chidl3);

        System.out.println(grandpa1.toString());
        System.out.println(grandpa2.toString());
        System.out.println(grandma1.toString());
        System.out.println(grandma2.toString());
        System.out.println(father.toString());
        System.out.println(mother.toString());
        System.out.println(chidl1.toString());
        System.out.println(chidl2.toString());
        System.out.println(chidl3.toString());
    }

    public static class Human {
        //write your code here
        String name = null;
        boolean sex;
        int age;
        ArrayList<Human> children;

        Human(String name, boolean sex, int age, ArrayList<Human> children){
            this.name = name;
            this.sex = sex;
            this.age = age;
            this.children = children;
        }

        public String toString() {
            String text = "";
            text += "Name: " + this.name;
            text += ", sex: " + (this.sex ? "male" : "female");
            text += ", age: " + this.age;

            int childCount = this.children.size();
            if (childCount > 0) {
                text += ", children: " + this.children.get(0).name;

                for (int i = 1; i < childCount; i++) {
                    Human child = this.children.get(i);
                    text += ", " + child.name;
                }
            }

            return text;
        }
    }

}
===========
package com.codegym.task.task08.task0824;

/* 
Make a family
1. Создайте человеческий класс со строковым именем, логическим полом, возрастом int и полями ArrayList<Human> children.
2. Создавайте и населяйте объекты так, чтобы в итоге у нас было: два дедушки, две бабушки, один отец, одна мать и трое детей.
3. Отображение всех объектов Human (подсказка: используйте метод toString() класса Human).

Требования:
1. Программа должна выводить текст на экран.
2. Класс людей должен иметь четыре поля.
3. Класс людей должен иметь один метод.
4. Класс Solution должен иметь один метод.
5. Программа должна создавать объекты и заполнять их данными, чтобы получить двух дедушек, двух бабушек, одного отца, одну мать и троих детей. Затем он должен отображать все человеческие объекты на экране.
*/
 
/* 
Make a family
ВЕРИФИЦИРОВАННЫЙ !!!!!!!!!!!!!!!!!!!!!!!!
*/


import java.util.ArrayList;


public class Solution {
    public static void main(String[] args) {
        //write your code here
        Human child1 = new Human("child1", false, 20);
        Human child2 = new Human("child2", true, 25);
        Human child3 = new Human("child3", true, 28);

        Human father = new Human("F1",true, 50);
        father.children.add(child1);
        father.children.add(child2);
        father.children.add(child3);

        Human mother = new Human("M1", false, 40);

        mother.children.add(child1);
        mother.children.add(child2);
        mother.children.add(child3);

        Human grandF1 = new Human("Gf1", true, 80);
		grandF1.children.add(father);

		Human grandF2 = new Human("Gf2", true, 70);
		grandF2.children.add(mother);

		Human grandM1 = new Human("GM1", false, 69);
		grandM1.children.add(father);

		Human grandM2 = new Human("GM2", false,80);
		grandM2.children.add(mother);

        System.out.println(grandF1);
        System.out.println(grandF2);

        System.out.println(grandM1);
        System.out.println(grandM2);

        System.out.println(father);
        System.out.println(mother);

        System.out.println(child1);
        System.out.println(child3);
        System.out.println(child3);
    }

    public static class Human {
        //write your code here
        String name;
        boolean sex;
        int age;
        ArrayList<Human> children;

        public Human(String name, boolean sex, int age) {
            this.name = name;
            this.sex = sex;
            this.age = age;
            this.children = new ArrayList<>();
        }
        public String toString() {
            String text = "";
            text += "Name: " + this.name;
            text += ", sex: " + (this.sex ? "male" : "female");
            text += ", age: " + this.age;

            int childCount = this.children.size();
            if (childCount > 0) {
                text += ", children: " + this.children.get(0).name;

                for (int i = 1; i < childCount; i++) {
                    Human child = this.children.get(i);
                    text += ", " + child.name;
                }
            }
            return text;
        }
    }

}
Name: Gf1, sex: male, age: 80, children: F1
Name: Gf2, sex: male, age: 70, children: M1
Name: GM1, sex: female, age: 69, children: F1
Name: GM2, sex: female, age: 80, children: M1
Name: F1, sex: male, age: 50, children: child1, child2, child3
Name: M1, sex: female, age: 40, children: child1, child2, child3
Name: child1, sex: female, age: 20
Name: child3, sex: male, age: 28
Name: child3, sex: male, age: 28
=====================
package com.codegym.task.task08.task0825;

/* 
Mixed-up modifier

*/

public class Solution {
    public static int A = 5;
    public static int B = 2;

    public static int C = A * B;
    public  int D = B * A;

    public static void main(String[] args) {
    }

    public  int getValue() {
        return D;
    }

    public  int getValue2() {
        return C;
    }
}
=================================
package com.codegym.task.task08.task0826;

import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.util.Arrays;
 
/* 
Five winners
интересное решение, хотя и не верифицированное
*/

public class Solution {
    public static void main(String[] args) throws Exception {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        int[] array = new int[20];
        for (int i = 0; i < array.length; i++) {
            array[i] = Integer.parseInt(reader.readLine());
        }

        sort(array);

        for(int i = array.length-1; i > array.length-1-5; i--)
            System.out.println(array[i]);
    }

    public static void sort(int[] array) {
        //write your code here
        Arrays.sort(array);
    }
}
=========================================
package com.codegym.task.task08.task0826;

import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.util.Arrays;

import java.util.Collections;
/* 
Five winners
прошло верификацию
*/

public class Solution {
    public static void main(String[] args) throws Exception {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        int[] array = new int[20]; 
        for (int i = 0; i < array.length; i++) {
            array[i] = Integer.parseInt(reader.readLine());
        }

        sort(array);

        System.out.println(array[0]);
        System.out.println(array[1]);
        System.out.println(array[2]);
        System.out.println(array[3]);
        System.out.println(array[4]);
    }

    public static void sort(int[] array) {
     int temp = 0;
        for(int i = 0; i < array.length; i++)
        {
            for(int j = 0 + i; j < array.length; j++)
            {
                //swap elements
                if(array[i] <= array[j])
                {
                    temp     = array[i];
                    array[i] = array[j];
                    array[j] = temp    ;
                }
            }
        }
        //write your code here
    }
}
=====================
package com.javarush.task.task08.task0827;

import java.text.ParseException;
import java.text.SimpleDateFormat;
import java.util.Date;
import java.util.Locale;

/* 
Working with dates
*/

public class Solution {
    public static void main(String[] args) throws ParseException {
        System.out.println(isDateOdd("MAY 1 2013"));
    }

    public static boolean isDateOdd(String date) throws ParseException {

        SimpleDateFormat formated = new SimpleDateFormat("MMMM d yyyy", Locale.ENGLISH);
        //Милисекунд до MAY 1 2013
        Date datan = formated.parse(date);
        // Милисекунд до начала годаMAY 1 2013
        Long DataK = datan.getTime();

//Установим начало годя для MAY 1 2013
        datan.setHours(0);
        datan.setMinutes(0);
        datan.setSeconds(0);
        datan.setDate(1);
        datan.setMonth(0);

        // Милисекунд до начала годаMAY 1 2013
        Long DataN = datan.getTime();
        long msDay = 24 * 60 * 60 * 1000;
        //Разница
        Long res = (DataK/msDay - DataN/msDay)+1;
        if (res % 2 == 0)
            return false;
        else
            return true;
    }
}
======================
package com.codegym.task.task08.task0828;

import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.ArrayList;
import java.util.HashSet;
import java.util.List;
import java.util.Set;

/* 
Month number

*/

public class Solution {
    public static void main(String[] args) throws IOException {
		BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        HashSet<String> monthList = new HashSet<String>();
        monthList.add("January is month 1"); 
        monthList.add("February is month 2"); 
        monthList.add("March is month 3"); 
        monthList.add("April is month 4"); 
        monthList.add("May is month 5"); 
        monthList.add("June is month 6"); 
        monthList.add("July is month 7"); 
        monthList.add("August is month 8"); 
        monthList.add("September is month 9"); 
        monthList.add("October is month 10"); 
        monthList.add("November is month 11"); 
        monthList.add("December is month 12"); 
        
        
        String s = reader.readLine();  
		
		 for (String text : monthList)
        {
		 
			 	if(text.contains(s)){ 
					System.out.println(text);
			 	}	
		 
        } 
            //write your code here  ;   
    }
}
============================= 
Задача: программа определяет, какая семья (фамилия) проживает в доме с указанным номером.
Новая задача: программа должна работать с городами, а не с номерами домов:

Example input:
Chicago
Capone
New York City
Rockefeller
Seattle
Gates

Seattle

Example output:
Gates

Требования:
1. Программа должна выводить текст на экран.
2. Программа должна считывать значения с клавиатуры.
3. Класс Solution должен иметь один метод.
4. Программа должна отображать фамилию семьи на основе введенного города.


     



 String s = reader.readLine();  
		
		 for (String text : monthList)
        {
		 
			 	if(text.contains(s)){ 
					System.out.println(text);
			 	}	
		 
        } 
============================
package com.codegym.task.task08.task0829;


import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.*;

/* 
Software update

*/

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));

        HashMap<String, String> cities = new HashMap<String, String>();

         while (true) {
            String city = reader.readLine();
            if (city.isEmpty()) break;
            String family = reader.readLine();
            cities.put(city, family);
        }

        String city = reader.readLine();

        //read city name
        String familyName = cities.get(city);
        System.out.println(familyName);
    }

    }
==
еще решения	
        while (true) {
            String city = reader.readLine();
            if (city.isEmpty()) break;
            String family = reader.readLine();
            addresses.put(city, family);
        }
        // Read the city entered by the user
        System.out.println(addresses.get(reader.readLine()));

SECOND PIECE (which does not work)
        while (true) {
            String city = reader.readLine();
            String family = reader.readLine();

            if ((family.isEmpty())||(city.isEmpty()))
                break;

            addresses.put(city,family);
        }
        // Read the city entered by the user
        System.out.println(addresses.get(reader.readLine()));
====================================
package com.codegym.task.task08.task0830;

import java.io.BufferedReader;
import java.io.InputStreamReader;

import java.util.*;
/* 
Task about algorithms

*/

public class Solution {
    public static void main(String[] args) throws Exception {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        String[] array = new String[20];
        for (int i = 0; i < array.length; i++) {
            array[i] = reader.readLine();
        }

        sort(array);

        for (String x : array) {
            System.out.println(x);
        }
    }

    public static void sort(String[] array) {
         ArrayList<String> list = new ArrayList<>(Arrays.asList(array));
        Collections.sort(list);
         for(int i = 0; i < array.length;i++){
             array[i] = list.get(i);
         }
         isGreaterThan(array[1], array[0]);
         //write your code here
    }

    // String comparison method: 'a' is greater than 'b'
    public static boolean isGreaterThan(String a, String b) {
        return a.compareTo(b) > 0;
    }
}
bIn
nSpain
mRain
fIn
gSpain
hRain
Ijn
rSpain
tRain
yIn
Supain
R6ain
7In
8Spain
9Rain
0In
2Spain
R3ain
I4n 
sI4n 
=============================================
Получение и отображение текущего стека вызовов:
public class ExceptionExample
{
  public static void main(String[] args)
  {
    method1();
  }

  public static void method1()
  {
    method2();
  }

  public static void method2()
  {
    method3();
  }

  public static void method3()
  {
     StackTraceElement[] stackTraceElements = Thread.currentThread().getStackTrace();
    for (StackTraceElement element : stackTraceElements)
    {
       System.out.println(element.getMethodName());
    }
  }
}
Результат:
getStackTrace
method3
method2
method1
main
======================
package com.codegym.task.task09.task0901;

/* 
Returning a stack trace
Возврат трассировки стека
Написать пять методов, которые вызывают друг друга.
Каждый метод должен возвращать трассировку стека.


Требования:
1. В классе должно быть 5 методов (в дополнение к основному методу).
2. Каждый метод должен назвать следующую: main вызывает метод Method1, метод1 вызовы метода Method2 и т. д.
3. Каждый метод должен возвращать трассировку стека.
4. Чтобы получить трассировку стека, используйте Thread.currentThread().getStackTrace().
*/

public class Solution {
    public static void main(String[] args) throws Exception {
        method1();
    }

    public static StackTraceElement[] method1() {
        method2();
        StackTraceElement[] stackTraceElements = Thread.currentThread().getStackTrace();
        return stackTraceElements;
        //write your code here
    }

    public static StackTraceElement[] method2() {
        method3();
         StackTraceElement[] stackTraceElements = Thread.currentThread().getStackTrace();
        return stackTraceElements;
        //write your code here
    }

    public static StackTraceElement[] method3() {
        method4();
         StackTraceElement[] stackTraceElements = Thread.currentThread().getStackTrace();
        return stackTraceElements;
        //write your code here
    }

    public static StackTraceElement[] method4() {
        method5();
          StackTraceElement[] stackTraceElements = Thread.currentThread().getStackTrace();
        return stackTraceElements;
        //write your code here
    }

    public static StackTraceElement[] method5() {
          StackTraceElement[] stackTraceElements = Thread.currentThread().getStackTrace();
        return stackTraceElements;
        //write your code here
    }
}
======================
Пересмотр трассировки стека
Написать пять методов, которые вызывают друг друга.
Каждый метод должен возвращать имя вызвавшего его метода. Использовать трассировку стека для получения этой информации.


Требования:
1. В классе должно быть 5 методов (в дополнение к основному методу).
2. Каждый метод должен назвать следующую: main вызывает метод Method1, метод1 вызовы метода Method2 и т. д.
3. Каждый метод должен возвращать имя вызвавшего его метода.
4. Чтобы получить имя вызывающего метода используйте метод getMethodName.
Гуадалупе Ганьон 31 Уровень, Тампа
Понедельник, 08:37 
В этой задаче необходимо вывести метод, который вызвал метод. Таким образом, method3 вызывает method4, поэтому внутри method4 ваш код потребности, который выводит "method3".... для метода 2 вам нужен код, который выводит "method1".

**Только 1 элемент, который в одном и том же месте для каждого списка будет отображать способ до***

package com.codegym.task.task09.task0902;

/* 
Stack trace revisited

*/

public class Solution {
    public static void main(String[] args) throws Exception {
        method1();
    }

    public static String method1() {
        method2();
        System.out.println(Thread.currentThread().getStackTrace()[3].getMethodName());
        return Thread.currentThread().getStackTrace()[2].getMethodName();
    }

    public static String method2() {
        method3();
        System.out.println(Thread.currentThread().getStackTrace()[2].getMethodName());
        return Thread.currentThread().getStackTrace()[2].getMethodName();
    }

    public static String method3() {
        method4();
        System.out.println(Thread.currentThread().getStackTrace()[1].getMethodName());
        return Thread.currentThread().getStackTrace()[2].getMethodName();
    }

    public static String method4() {
        method5();
        System.out.println(Thread.currentThread().getStackTrace()[0].getMethodName());
        return Thread.currentThread().getStackTrace()[2].getMethodName();
    }

    public static String method5() {
        System.out.println(Thread.currentThread().getStackTrace()[3].getMethodName());
        return Thread.currentThread().getStackTrace()[2].getMethodName();//write your code here
    }
}

===============
Написать пять методов, которые вызывают друг друга.
Каждый метод должен возвращать номер строки кода, из которого он был вызван. 
Используйте элемент.getLineNumber() метод.

1. В классе должно быть 5 методов (в дополнение к основному методу).
2. Каждый метод должен назвать следующую: main вызывает метод Method1, метод1 вызовы метода Method2 и т. д.
3. Каждый метод должен возвращать номер строки кода, из которого он был вызван.
4. Чтобы получить номер строки, используйте метод getLineNumber класса StackTraceElement.

package com.codegym.task.task09.task0903;
/* 
Who called me?

*/

public class Solution {
    public static void main(String[] args) throws Exception {
        method1();
    }

    public static int method1() {
        method2();
        System.out.println(Thread.currentThread().getStackTrace()[2].getLineNumber());
        return  Thread.currentThread().getStackTrace()[2].getLineNumber();
    }

    public static int method2() {
        method3();
        System.out.println(Thread.currentThread().getStackTrace()[2].getLineNumber());
        return  Thread.currentThread().getStackTrace()[2].getLineNumber();
    }

    public static int method3() {
        method4();
        System.out.println(Thread.currentThread().getStackTrace()[2].getLineNumber());
        return  Thread.currentThread().getStackTrace()[2].getLineNumber();
    }

    public static int method4() {
        method5();
        System.out.println(Thread.currentThread().getStackTrace()[2].getLineNumber());
        return  Thread.currentThread().getStackTrace()[2].getLineNumber();
    }

    public static int method5() {
        System.out.println(Thread.currentThread().getStackTrace()[2].getLineNumber());
        return  Thread.currentThread().getStackTrace()[2].getLineNumber();
    }
}
31
25
19
13
9
========================
Требования:
1. В классе должно быть 10 методов (в дополнение к основному методу).
2. Переменная stackTraceLength должна в конечном итоге быть равна 10.
3. Каждый метод должен вызывать другой метод.
4. Используй Thread.currentThread().getStackTrace() метод. 

package com.codegym.task.task09.task0904;
/* 
Stack trace with 10 calls

*/

public class Solution {
    public static void main(String[] args) throws Exception {
        int stackTraceLength = method1().length - method10().length + 1;
    }

    public static StackTraceElement[] method1() {
        return method2();
    }

    public static StackTraceElement[] method2() {
        return method3(); //write your code here
    }

    public static StackTraceElement[] method3() {
         return method4();//write your code here
    }

    public static StackTraceElement[] method4() {
         return method5();//write your code here
    }

    public static StackTraceElement[] method5() {
         return method6();//write your code here
    }

    public static StackTraceElement[] method6() {
         return method7();//write your code here
    }

    public static StackTraceElement[] method7() {
         return method8();//write your code here
    }

    public static StackTraceElement[] method8() {
         return method9();//write your code here
    }

    public static StackTraceElement[] method9() {
        return method10();
    }

    public static StackTraceElement[] method10() {
        return Thread.currentThread().getStackTrace();
    }
}
====================
Напишите метод, который возвращает глубину трассировки стека, т. е. количество методов в трассировке стека.
Метод должен отображать этот же номер на экране.


Требования:
1. Метод getStackTraceDepth должен возвращать глубину трассировки стека.
2. Метод getStackTraceDepth должен отображать глубину трассировки стека.
3. Используйте Thread.currentThread().getStackTrace().
4. Метод main должен вызывать метод getStackTraceDepth.
package com.codegym.task.task09.task0905;
/* 
In the blue depths of the stack trace…

*/

public class Solution {
    public static void main(String[] args) throws Exception {
        int deep = getStackTraceDepth();
//           System.out.println(deep);
    }

    public static int getStackTraceDepth() {
        // write your code here
         System.out.println(Thread.currentThread().getStackTrace().length);
        return Thread.currentThread().getStackTrace().length;
        
		// write your code here
    }
}
==============================
Реализовать метод log.
Метод отчет должен отображать имя класса и метода, в котором он вызывается, а также переданного сообщения.
Используйте двоеточие и Пробел для разделения имени класса, имени метода и сообщения.

Пример вывода:
com.codegym.task.task09.task0906.Solution: main: In main method


Требования:
1. Метод отчет должен отображать сообщение на экране.
2. Сообщение должно содержать имя класса, метод которого называется метод log.
3. Сообщение должно содержать имя метода, который называется метод log.
4. Отображаемое сообщение должно содержать переданное сообщение.
5. Выходные данные должны соответствовать примеру задачи.
package com.codegym.task.task09.task0906;

/* 
Logging stack traces

*/

public class Solution {
    public static void main(String[] args) {
        log("In main method");
    }

    public static void log(String s) {
        String classname = Thread.currentThread().getStackTrace()[2].getClassName();
        String methodCalled = Thread.currentThread().getStackTrace()[2].getMethodName();
        System.out.println(classname+": "+methodCalled+": " + s);
    }
}
com.javarush.task.task09.task0906.Solution: main: In main method
=====================
public static void main(String[] args)
{
    method1();
}

public static void method1() throws FileNotFoundException, ClassNotFoundException
{
    //Throws FileNotFoundException if the file doesn't exist
    FileInputStream fis = new FileInputStream("C2:\badFileName.txt");
}
==
public static void main(String[] args)  throws FileNotFoundException, ClassNotFoundException
{
    method1();
}

public static void method1() throws FileNotFoundException, ClassNotFoundException
{
    //Throws FileNotFoundException if the file doesn't exist
    FileInputStream fis = new FileInputStream("C2:\badFileName.txt");
}
==
public static void main(String[] args)
{
    try
    {
        method1();
    }
    catch(Exception e)
    {
    }
}

public static void method1() throws FileNotFoundException, ClassNotFoundException
{
    //Throws FileNotFoundException if the file doesn't exist
    FileInputStream fis = new FileInputStream("C2:\badFileName.txt");
}
==
package com.codegym.task.task09.task0907;

/* 
Exception when working with numbers

*/

public class Solution {
    public static void main(String[] args) throws Exception {
        //write your code here
         try
        {
            
               int a = 42 / 0;
            System.out.println("After calling method1. This will never be shown");
        }
        catch (NullPointerException e)
        {
           System.out.println("Null reference. Exception has been caught");
        }
        catch (ArithmeticException e)
        {
            System.out.println("Division by zero. Exception has been caught");
        }
        catch (Exception e)
        {
            System.out.println("Any other errors. Exception has been caught");
        }
         

        //write your code here
    }
}

==
public static void method3() throws ClassNotFoundException
{
   try
    {
        method1();
    }
    catch (FileNotFoundException e)
    {
        System.out.println("FileNotFoundException has been caught.");
    }
}
========================
package com.codegym.task.task09.task0907;

/* 
Exception when working with numbers

*/

public class Solution {
    public static void main(String[] args) throws Exception {
        //write your code here
         try
        {            
            int a = 42 / 0;
         }        
        catch (ArithmeticException e)
        {
            System.out.println(e.getMessage ()); 
            System.out.println(e.getClass());
        }
        //write your code here
    }
}
================
package com.codegym.task.task09.task0908;

/* 
Exception while working with strings

*/

public class Solution {
    public static void main(String[] args) throws Exception {
        try
        {   //write your code here
            String s = null;
            String m = s.toLowerCase();
         }   
        catch (NullPointerException e)
        {
         System.out.println(e.getMessage ()); 
            System.out.println(e.getClass());
        } 
        //write your code here
    }
}
================================
package com.codegym.task.task09.task0909;

/* 
Exception when working with arrays

*/

public class Solution {
    public static void main(String[] args) throws Exception {
        //write your code here
        try
        {   //write your code here
             int[] m = new int[2];
             m[8] = 5;
         }   
        catch (ArrayIndexOutOfBoundsException  e)
        {
         System.out.println(e.getMessage ()); 
            System.out.println(e.getClass());
        } 
        //write your code here
    }
}
==========================
package com.codegym.task.task09.task0910;

import java.util.ArrayList;

/* 
Exception when working with List collections

*/

public class Solution {
    public static void main(String[] args) throws Exception {
        //write your code here
        try
        {   //write your code here
              ArrayList<String> list = new ArrayList<String>();
              String s = list.get(18);
         }   
        catch (IndexOutOfBoundsException  e)
        {
            System.out.println(e.getMessage ()); 
            System.out.println(e.getClass());
        } 
        //write your code here
    }
}
Забавное задание, требовалось ввести тип исключения, в данном случае IndexOutOfBoundsException, поиск в интернете не дал результатов. Потом я просто посмотрел в веб-IDE исключение, и вуаля!! Все сошлось
================================
package com.codegym.task.task09.task0911;

import java.util.HashMap;

/* 
Exception when working with Map collections

*/

public class Solution {
    public static void main(String[] args) throws Exception {
        //write your code here
 try
        {  
        HashMap<String, String> map = new HashMap<String, String>(null);
        map.put(null, null);
        map.remove(null);
 }   
        catch (NullPointerException   e)
        {
     //       System.out.println(e.getMessage ()); 
            System.out.println(e.getClass());
        }
        //write your code here
    }
}
тоже самое вставил, но не проверифицировалось, потом закоментил строку, заработало. NullPointerException ведь тоже взял из выписки эксепшнов, потому должно было работать.
=============================
package com.codegym.task.task09.task0912;

/* 
Exception when working with numbers

*/

public class Solution {
    public static void main(String[] args) throws Exception {
        //write your code here
 try
        {  
        int num = Integer.parseInt("XYZ");
        System.out.println(num);
}   
        catch (NumberFormatException   e)
        {
     //       System.out.println(e.getMessage ()); 
            System.out.println(e.getClass());
        }
        //write your code here
    }
}
===============================
package com.codegym.task.task09.task0913;

import java.io.FileNotFoundException;
import java.net.URISyntaxException;

/* 
Exceptions. Just exceptions.

*/

public class Solution {
    public static void main(String[] args) throws Exception {
        //write your code here

        try { //write your code here
			 method1();
        } 
       catch (NullPointerException | FileNotFoundException e)
       
        { }
        //write your code here
    }

    public static void method1() throws NullPointerException, ArithmeticException, FileNotFoundException, URISyntaxException {
        int i = (int) (Math.random() * 4);
        if (i == 0)
            throw new NullPointerException();
        if (i == 1)
            throw new ArithmeticException();
        if (i == 2)
            throw new FileNotFoundException();
        if (i == 3)
            throw new URISyntaxException("", "");
    }
}

Есть 3 исключения, которые последовательно наследуют исключение (Exception1 расширяет исключение, Exception2 расширяет Exception1, и Exception3 расширяет Exception2). В программе вы найдете общедоступный метод static void method1 (), выбрасывающий метод Exception1, Exception2, Exception3. Задача: напишите блок catch, который поймает все три исключения: Exception1, Exception2 и Exception3.

1. Существует три исключения, которые последовательно наследуют исключение.
2. Класс Исключение_1 распространяется исключение
3. Класс Exception2 расширяет Исключение1
4. Класс Exception3 расширяет Исключение2
5. Существует метод со следующей сигнатурой:
public static void method1 () выбрасывает Exception1, Exception2, Exception3
6. Напишите блок catch, который поймает все три исключения: Exception1, Exception2 и Exception3
Требования:
1. Метод main должен вызывать метод method1.
2. Метод main должен перехватывать исключение Exception1.
3. Метод main должен перехватывать исключение Exception2.
4. Метод main должен перехватывать исключение Exception3.
5. Не изменяйте метод method1.

package com.codegym.task.task09.task0914;

/* 
Catching a group of exceptions

*/

public class Solution {
    public static void main(String[] args) throws Exception {
        try { //write your code here
			 method1();
        } 
       catch (Exception1 e)
         { 
             
         }
    
    }

    public static void method1() throws Exception1, Exception2, Exception3 {
        int i = (int) (Math.random() * 3);
        if (i == 0)
            throw new Exception1();
        if (i == 1)
            throw new Exception2();
        if (i == 2)
            throw new Exception3();
    }
}

class Exception1 extends Exception {
}

class Exception2 extends Exception1 {
}

class Exception3 extends Exception2 {
}
все дело в наследовании исключений!!!!!!!!!!!  
========================= 
package com.codegym.task.task09.task0915;

import java.io.CharConversionException;
import java.io.IOException;
import java.nio.file.FileSystemException;

/* 
Catching custom exceptions

*/

public class Solution {
    public static StatelessBean BEAN = new StatelessBean();

    public static void main(String[] args) {
        try
        {
            handleExceptions();
        }

        catch (FileSystemException e)
        {
            BEAN.log(e);

        }
    }

  
 public static void handleExceptions() throws FileSystemException {

        try
        {
            BEAN.throwExceptions();
        }

        catch (FileSystemException e)
        {
            BEAN.log(e);
            throw  e;
        }

        catch (CharConversionException e)
        {
            BEAN.log(e);
        }

        catch (Exception e)
        {
            BEAN.log(e);
        }
    }
    public static class StatelessBean {
        public void log(Exception exception) {
            System.out.println(exception.getMessage() + ", " + exception.getClass().getSimpleName());
        }

        public void throwExceptions() throws CharConversionException, FileSystemException, IOException {
            int i = (int) (Math.random() * 3);
            if (i == 0)
                throw new CharConversionException();
            if (i == 1)
                throw new FileSystemException("");
            if (i == 2)
                throw new IOException();
        }
    }
}
==============================
package com.codegym.task.task09.task0916;
 
import java.io.IOException;
import java.rmi.RemoteException;

/* 
Catching checked exceptions

*/

public class Solution {
    public static void main(String[] args) {
        handleExceptions(new Solution());

    }

    public static void handleExceptions(Solution obj) {
        try{
        obj.method1();
        obj.method2();
        obj.method3();
        }
        catch(Exception e){
			System.out.println(e);
			}
    }

    public void method1() throws IOException {
        throw new IOException();
    }

    public void method2() throws NoSuchFieldException {
        throw new NoSuchFieldException();
    }

    public void method3() throws RemoteException {
        throw new RemoteException();
    }
}
==============================
package com.codegym.task.task09.task0917;

/* 
Catching unchecked exceptions

*/

public class Solution {
    public static void main(String[] args) {
        handleExceptions(new Solution());
    }

    public static void handleExceptions(Solution obj) {
        try{
        obj.method1();
        obj.method2();
        obj.method3();
        }
        catch(Exception e){
			printStack(e);
			}
    }

    public static void printStack(Throwable throwable) {
        System.out.println(throwable);
        for (StackTraceElement element : throwable.getStackTrace()) {
            System.out.println(element);
        }
    }

    public void method1() {
        throw new NullPointerException();
    }

    public void method2() {
        throw new IndexOutOfBoundsException();
    }

    public void method3() {
        throw new NumberFormatException();
    }
}
===========================================
Существует четыре класса: MyException, MyException2, MyException3 и MyException4.
Наследуйте классы, чтобы получить любые два проверенных исключения и любые два непроверенных исключения.
Намек:
Внимательно изучите классы Exception1, Exception2 и Exception3 из второго задания этого урока.

package com.codegym.task.task09.task0914;

/* 
Catching a group of exceptions

*/

public class Solution {
    public static void main(String[] args) throws Exception {
        try { //write your code here
			 method1();
        } 
       catch (Exception1 e)
         { 
             
         } 
    }

    public static void method1() throws Exception1, Exception2, Exception3 {
        int i = (int) (Math.random() * 3);
        if (i == 0)
            throw new Exception1();
        if (i == 1)
            throw new Exception2();
        if (i == 2)
            throw new Exception3();
    }
}

class Exception1 extends Exception {
}

class Exception2 extends Exception1 {
}

class Exception3 extends Exception2 {
}
===============
public class Jarvis {

   public void sayHi(String...names) { // передается коллекция имен

       for (String name: names) { // упрощенный цикл
           System.out.println("Good evening, " + name + ". How are you?");
       }
   }

   public static void main(String[] args) {
       Jarvis jarvis = new Jarvis();
       jarvis.sayHi("Tony Stark", "Captain America", "Black Widow", "Hulk");
   }
}
==================
public class Person {

   public void introduce(String name, String age) {
       System.out.println("Method with two strings!");
       System.out.println("My name is " + name + ". My age is " + age);
   }

   public void introduce(String name, Integer age) {
       System.out.println("Method with a string and a number!");
       System.out.println("My name is " + name + ". My age is " + age);
   }

   public static void main(String[] args) {

       Person victor = new Person();
       victor.introduce("Victor", (String) null); // string можно указать для NULL или другой любой тип данных .. Для int не надо этого типа писать
   }
}
--
public class Person {

   public void introduce(String name, String age) {
       System.out.println("Method with two strings!");
       System.out.println("My name is " + name + ". My age is " + age);
   }

   public void introduce(String name, int age) {
       System.out.println("Method with a string and a number!!");
       System.out.println("My name is " + name + ". My age is " + age);
   }

   public static void main(String[] args) {

       Person victor = new Person();
       victor.introduce("Victor", null);
   }
}
======================
package com.codegym.task.task09.task0919;

/* 
Dividing by zero

*/

 public class Solution {

    public static void main(String[] args) {

        try
        {
            divideByZero();
        }
        catch(ArithmeticException e)
        {e.printStackTrace();
            //System.out.println("ArithmeticException has been caught.");
            //printStackTrace(e);
        }
    }
    public static void divideByZero()
    {
        int  a = 3;
        int result = a / 0;
        System.out.println(result);
    }
    public static void printStackTrace(Throwable throwable)
    {
        for(StackTraceElement element : throwable.getStackTrace())
        {
            System.out.println(element);
        }

    }
}
=====================
package com.codegym.task.task09.task0920;

/* 
Countdown

*/

public class Solution {
    public static void main(String[] args) {
        for (int i = 10; i >= 0; i--) {
            System.out.println(i);

            try
             {
                Thread.sleep(100);
             }
         catch(Exception e){
               
              }
        //write your code here
        }
    } 
}
 ==============
 package com.codegym.task.task09.task0921;

import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.util.ArrayList;
import java.util.List;

/* 
Method in a try-catch

*/

public class Solution {
    public static void main(String[] args) {
        readData();
    }

    public static void readData() {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        ArrayList<Integer> nList = new ArrayList<Integer>();

        try{
            while (!reader.readLine().isEmpty()) {
                nList.add(Integer.parseInt(reader.readLine()));
            }
        }
        catch(Exception b){
            for (int list: nList){
                System.out.println(list);
            }
        }

    }
}
==
верифицированный 
package com.codegym.task.task09.task0921;

import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.util.ArrayList;
import java.util.List;

/* 
Method in a try-catch

*/

public class Solution {
    public static void main(String[] args) {
        readData();
    }

    public static void readData() {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        ArrayList<Integer> nList = new ArrayList<Integer>();  

        try{
            while (true) {
                nList.add(Integer.parseInt(reader.readLine()));
            }
        }
        catch(Exception b){
            for (int list: nList){
                System.out.println(list);
            }
        }

    }
}
========================
package com.codegym.task.task09.task0922;

import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.text.SimpleDateFormat;
import java.util.Date;
import java.util.Locale;

/* 
What's today's date?

*/

public class Solution {

    public static void main(String[] args) throws Exception {
        //write your code here
        BufferedReader br=new BufferedReader(new InputStreamReader(System.in));
  
  SimpleDateFormat month_date = new SimpleDateFormat("MMM dd, yyyy", Locale.ENGLISH);
SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd");
 String s=br.readLine();
//String s="2013-08-18";

Date date = sdf.parse(s);
 
 
        System.out.println(month_date.format(date).toUpperCase());       
    }
}

===================
 package com.codegym.task.task09.task0923;
   

import java.io.BufferedReader;
import java.io.InputStreamReader;

/* 
Vowels and consonants

*/

import java.util.HashSet;
public class Solution {
    public static char[] vowels = new char[]{'a', 'e', 'i', 'o', 'u'};

    public static void main(String[] args) throws Exception {
        
        HashSet<String> monthList = new HashSet<String>(); 
        HashSet<String> monthList2 = new HashSet<String>(); 
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        String s = reader.readLine();
      //  s = s.replaceAll("\\s+"," "); //убирает пробелы из строки.
        s = s.replace(" ",""); // в s1 пробелов не будет.
     //   s = s.replaceAll('\\s+',' '; //убирает пробелы из строки.
        char[] ch = s.trim().toCharArray();
        for(int i = 0; i < ch.length; i++) {
        	isVowel(ch[i]); 
        	if((isVowel(ch[i])) == true) {
        	   
        	     s = String.valueOf(ch[i]);
                 if (ch[i] != ' ') {
                 monthList2.add(s);  
                }
        	}else{ 
        	     s = String.valueOf(ch[i]);
        	     if (ch[i] != ' ') {
                 monthList.add(s);  
                }
        	}  
        }        
		 
          for (String text : monthList2)
            {  
			 	System.out.print(text + " ");  
			}   
			System.out.println();
			for (String text : monthList)
            {  
			 	System.out.print(text + " ");  
			}
			 
    }  
    // The method checks whether a letter is a vowel
    public static boolean isVowel(char c) {
        c = Character.toLowerCase(c);  // Convert to lowercase

        for (char d : vowels)   // Look for vowels in the array
        {
            if (c == d)
                return true;
        }
        return false;
    }
}
не верифицированное решение
--
а это верифицированное
package com.codegym.task.task09.task0923;
   

import java.io.BufferedReader;
import java.io.InputStreamReader;

/* 
Vowels and consonants

*/

import java.util.HashSet;
public class Solution {
    public static char[] vowels = new char[]{'a', 'e', 'i', 'o', 'u'};

    public static void main(String[] args) throws Exception {
        String s = new BufferedReader(new InputStreamReader(System.in)).readLine().replace(" ", "");
    String a = "", b = "";

    for (Character ch : s.toCharArray()) {
        if (isVowel(ch)) {
            a += ch + " ";//напишите тут ваш код
        } else {
            b += ch + " ";
        }
    }
    System.out.println(a);
    System.out.println(b);
 
			 
    }  
    // The method checks whether a letter is a vowel
    public static boolean isVowel(char c) {
        c = Character.toLowerCase(c);  // Convert to lowercase

        for (char d : vowels)   // Look for vowels in the array
        {
            if (c == d)
                return true;
        }
        return false;
    }
}
=
тоже верифицированное решение, и интересное
public static void main(String[] args) throws Exception {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        String vvod = reader.readLine();// создали переменную для ввода текста
        char[] c = vvod.toCharArray(); // перевели в массив символов
        ArrayList<Character> glasnie = new ArrayList<>(); // создали список типа символов для гласных букв
        ArrayList<Character> soglasnie = new ArrayList<>(); // создали список типа символов для согласных букв
        for (char a : c) { // цикл фор ич, в котором каждому символу а присваивается значение массива с
            if (isVowel(a)) // используем метод isVowel(a) с переменной а
                glasnie.add(a); // если истина записываем в список гласных
            else if (!isVowel(a) && a != ' ') // если ложь или пробел, то в список согласных
                soglasnie.add(a);
        }
        for (int i = 0; i < glasnie.size(); i++) { // вывод каждого значения на экран
            System.out.print(glasnie.get(i) + " ");
        }
        System.out.println();

        for (int i = 0; i < soglasnie.size(); i++) {
            System.out.print(soglasnie.get(i) + " ");
        }
    }
================
1. Когда-то было пять классов: Красная Шапочка, бабушка, пирог, дровосек и волк.
2. Каждый класс имеет 2 поля: ArrayList убил и ArrayList съел.
3. Созданы необходимые объекты (вытяжка, бабушка,...).
4. Правильно выстраивайте отношения в соответствии с тем, кто кого съел и/или убил в сказке "Красная Шапочка".

PS: никто не ел пирог. Его несли только в корзине. Волк немного поел. А потом его убили. 
Требования:
• Основной метод должен изменить состояние (внутренние переменные) объекта волк.
• Основной метод должен изменить состояние (внутренние переменные) объекта дровосека.
Никто не ел пирог.
Волк немного поел.
А потом волка убили. 
package com.codegym.task.task09.task0924;

import java.util.ArrayList;

/* 
A scary fairy tale

*/

public class Solution {
    public static RedRidingHood hood = new RedRidingHood();
    public static Grandmother grandmother = new Grandmother();
    public static Pie pie = new Pie();
    public static Woodcutter woodcutter = new Woodcutter();
    public static Wolf wolf = new Wolf();

    public static void main(String[] args) {
        wolf.ate.add(grandmother); // волк . аррай массив ate (внизу). добавить (бабушка public static ссылка на обьект)
        wolf.ate.add(hood);
        wolf.killed.add(pie);
        hood.killed.add(wolf);
        woodcutter.killed.add(wolf);
        // write your code here
    }

    // Red riding hood
    public static class RedRidingHood extends StoryItem {
    }

    // Grandmother
    public static class Grandmother extends StoryItem {
    }

    // Pie
    public static class Pie extends StoryItem {
    }

    // Woodcutter
    public static class Woodcutter extends StoryItem {
    }

    // Wolf
    public static class Wolf extends StoryItem {
    }

    public static abstract class StoryItem {
        public ArrayList<StoryItem> killed = new ArrayList<>();
        public ArrayList<StoryItem> ate = new ArrayList<>();
    }
}
=========================
package com.codegym.task.task09.task0925;

/* 
Static modifiers are out of place

*/

public class Solution {
    public static int A = 5;
    public static int B = 2 * A;
    public  int C = A * B;
    public static int D = A * B;

    public static void main(String[] args) {
        Solution room = new Solution();
        room.A = 5;

        Solution.D = 5;
    }

    public int getA() {
        return A;
    }

}
=======================
Создать список, элементами которого являются массивы чисел. 
Добавьте в список пять объектов массива длиной 5, 2, 4, 7 и 0 соответственно. 
Заполните массивы любыми данными и выведите их на экран.
Программа не должна считывать данные с клавиатуры.
* Метод createList должен объявить и инициализировать переменную ArrayList<int []>.
* Метод createList должен возвращать созданный список.
* Метод createList должен добавить 5 элементов в список.
• Каждый элемент в списке должен быть массивом чисел. Длина первого массива должна быть 5; второго-2; а остальных — 4, 7 и 0 соответственно.
* Программа должна отображать элементы всех массивов в списке. Каждый элемент в новой строке.

package com.codegym.task.task09.task0926;

import java.util.ArrayList;

/* 
List of number arrays

*/

public class Solution {
    public static void main(String[] args) {
        ArrayList<int[]> list = createList();
        printList(list);
    }

    public static ArrayList<int[]> createList() {  
        ArrayList<int[]> numbers = new ArrayList<int[]>();
        int a1[]={1,2,3,4,5};
        int a2[]={1,2};
        int a3[]={1,2,3,4};
        int a4[]={1,2,3,4,5,4,5};
        int a5[]={};
        numbers.add(0,a1);
        numbers.add(a2);
        numbers.add(a3);
        numbers.add(a4);
        numbers.add(a5); 
        
       return numbers;
        //write your code here
    }

    public static void printList(ArrayList<int[]> list) {
        for (int[] array : list) {
            for (int x : array) {
                System.out.println(x);
            }
        }
    }
}
===========================
package com.codegym.task.task09.task0927;
 
import java.util.HashMap;
import java.util.HashSet;
import java.util.Map;
import java.util.Set;

/* 
Ten cats

*/

public class Solution {
    public static void main(String[] args) {
        Map<String, Cat> map = createMap();
        Set<Cat> set = convertMapToSet(map);
        printCatSet(set);
    }

    public static Map<String, Cat> createMap() {
		String[] cats = new String[]{"Tiger", "Missy", "Smokey", "Marmalade", "Oscar", "Snowball", "Boss", "Smudge", "Max", "Simba"};
		HashMap<String, Cat> map = new HashMap<String, Cat>();
 
        for (int i = 0; i < cats.length; i++) { 
            String key = cats[i];
            map.put(key, new Cat(key));
        }
		return map;
        //write your code here
    }

    public static Set<Cat> convertMapToSet(Map<String, Cat> map) {
        HashSet<Cat> set = new HashSet<>(map.values()); // из map в set
			 
		return set;
		 //write your code here
    }

    public static void printCatSet(Set<Cat> set) {
        for (Cat cat : set) {
            System.out.println(cat);
        }
    }

    public static class Cat {
        private String name;

        public Cat(String name) {
            this.name = name;
        }

        public String toString() {
            return "Cat " + this.name;
        }
    }


}

==================
 






























