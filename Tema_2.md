
# Тема 2. Базовые операции языка Python
Отчет по Теме #2 выполнил(а):
- Поляков Матвей Андреевич
- ИВТ-22-2

| Задание | Лаб_раб | Сам_раб |
| ------ | ------ | ------ |
| Задание 1 | + | + |
| Задание 2 | + | + |
| Задание 3 | + | + |
| Задание 4 | + | + |
| Задание 5 | + | + |
| Задание 6 | + | + |
| Задание 7 | + | + |
| Задание 8 | + | + |
| Задание 9 | + | + |
| Задание 10 | + | + |

знак "+" - задание выполнено; знак "-" - задание не выполнено;

Работу проверили:
- к.э.н., доцент Панов М.А.

  ## Лабораторная №1
  ### Выведите в консоль три строки. Первая – любое число. Вторая – любое число в виде строки. Третья – любое число с плавающей точкой.
  ```python
  print("123")
  print(1.23)
  print(123)
  ```
  # Результат
![Меню](https://github.com/soft2k/Software_Engineering/blob/main/pic/Tema2Pic1.png)
  # Вывод
  С помощью print вывели 3 строки - число, текст, число с плавающей точкой


   ## Лабораторная №2
  ### Выведите в консоль три строки. Первая – результат сложения или вычитания минимум двух переменных типа int. Вторая – результат сложения или вычитания минимум двух переменных типа float. Третья – результат сложения или вычитания минимум двух переменных типа int и float.
  
  ```python
  print(123-100)
  print(5.2 + 5.3)
  print(5 + 3.25 + 100 + 6.7)
  ```
  # Результат
![Меню](https://github.com/soft2k/Software_Engineering/blob/main/pic/Tema2Pic2.png)
  # Вывод
  С помощью print вывели 3 строки - число, текст, число с плавающей точкой



   ## Лабораторная №3
  ### Выведите в консоль три строки. Первая – обычная строка. Вторая – F строка с использованием заранее объявленной переменной. Третья – сложите две или более строк в одну.
  
  ```python
  print("Hello world!")

  world = "world"
  print(f"Hello {world}!")
  
  one = "Hello "
  two = "world!"
  print(one + two)
  ```
  # Результат
![Меню](https://github.com/soft2k/Software_Engineering/blob/main/pic/Tema2Pic3.png)
  # Вывод
  С помощью print вывели 3 строки - обычная строка, строка с -f и использование переменной в print и сложили две переменные в print



   ## Лабораторная №4
  
  ### Выведите в консоль три строки. Первая – трансформация любого типа переменной в bool. Вторая – трансформация любого типа переменной в float или int. Третья – трансформация любого типа переменной в str.
  ```python
    one = "hello"
    print(bool(one))
    
    two = 100
    print(float(two))
    
    three = None
    print(str(three))
  ```
  # Результат
![Меню](https://github.com/soft2k/Software_Engineering/blob/main/pic/Tema2Pic4.png)
  # Вывод
  С помощью print вывели 3 строки:
  
  1)Трансформация в bool
  2)Трансформация в float
  3)Трансформация в string
  


## Лабораторная №5
  
  ### Присвойте трем переменным различные значения, воспользовавшись функцией input()
  ```python
  one = input("one: ")
  two = input("two: ")
  three = input("three: ")
  print(one, two, three)
  ```
  # Результат
![Меню](https://github.com/soft2k/Software_Engineering/blob/main/pic/Tema2Pic5.png)
  # Вывод
  С помощью input() присвоил трем переменным значения



   ## Лабораторная №6
  
  ### Создайте две любые числовые переменные и выполните над ними несколько математических операций: возведение в степень, обычное деление, целочисленное деление, нахождение остатка от деления. При желании вы можете проверить как работают эти вычисления с разными типами данных, например, сначала создать две переменные int, затем создать две переменные float и наконец создать переменные типа int и float и провести над ними операции, прописанные выше.

  ```python
      a = 5
      b = 10
      print("В степени ", a ** b )
      print("Деление ", a / b)
      print("Целочисленное деления ", a // b)
      print("Нахождения остатка от деления ", a % b)
  ```
  # Результат
![Меню](https://github.com/soft2k/Software_Engineering/blob/main/pic/Tema2Pic6.png)
  # Вывод
  Знаков *,/,% выполнили математические операции
1)Возведениен в степень
2)Деление
3)Целочисленное деления
4)Нахождения остатка от деления

   ## Лабораторная №7
  ### Создайте любую строковую переменную и произведите над ней математическое действие умножение на любое число.
  ```python
  word = 'hello '
  print(word * 6)
  ```
  # Результат
![Меню](https://github.com/soft2k/Software_Engineering/blob/main/pic/Tema2Pic7.png)
  # Вывод
  Мы произвели умножение над строковой перменной и получили результат,где это слово было продублированно на число умножения

  
   ## Лабораторная №8

   
  ### Посчитайте сколько раз символ ‘o’ встречается в строке ‘Hello World
  ```python
  str = "hello world"
  print(str.count("o"))
  ```
  # Результат
![Меню](https://github.com/soft2k/Software_Engineering/blob/main/pic/Tema2Pic8.png)
  # Вывод
  С помощью count мы посчитатли сколько буква "О" встречается в выражение "hello world" 


   ## Лабораторная №9

   
  ### Напишите предложение ‘Hello World’ в две строки. Написанная программа должна занимать одну строку в редакторе кода
  
  ```python
  print("Hello\nWorld")
  ```
  # Результат
![Меню](https://github.com/soft2k/Software_Engineering/blob/main/pic/Tema2Pic9.png)
  # Вывод
  С помощью \n разделил Hello и World



   ## Лабораторная №10

   
  ### Из предложения ‘Hello World’ выведите в консоль только 2 символ, а затем выведите слово ‘Hello’
  
  ```python
  str = "hello world"
  print(str.count("o"))
  ```
  # Результат
![Меню](https://github.com/soft2k/Software_Engineering/blob/main/pic/Tema2Pic10.png)
  # Вывод
  С помощью count мы посчитатли сколько буква "О" встречается в выражение "hello world" 



  ## Самостоятельная работа №1
  ### Выведите в консоль булевую переменную False, не используя слово False в строке или изначально присвоенную булевую переменную. Программа должна занимать не более двух строк редактора кода.
  ```python
  false = ""
  print(bool(false))
  ```
  # Результат
![Меню](https://github.com/soft2k/Software_Engineering/blob/main/pic/Tema2Pic11.PNG)
  # Вывод
  Вывел в строковую переменную пустоту и трансформировал в bool 


   ## Самостоятельная работа №2
  ### Присвоить значения трем переменным и вывести их в консоль, используя только две строки редактора кода
  
  ```python
  a, b, c = 1, 2, 3
  print(a, b, c)
  ```
  # Результат
![Меню](https://github.com/soft2k/Software_Engineering/blob/main/pic/Tema2Pic12.PNG)
  # Вывод
  С помощью перечислениям запятой,можно выводить и присваивать значения



   ## Самостоятельная работа №3
  ### Реализуйте ввод данных в программу, через консоль, в виде только целых чисел (тип данных int). То есть при вводе буквенных символов в консоль, программа не должна работать. Программа должна занимать не более двух строк редактора кода.
  
  ```python
  print(int(input()))
  ```
  # Результат
![Меню](https://github.com/soft2k/Software_Engineering/blob/main/pic/Tema2Pic13.PNG)
  # Вывод
  С int и input он не принимает str выражения



   ## Самостоятельная работа №4
  
  ### Создайте только одну строковую переменную. Длина строки должна не превышать 5 символов. На выходе мы должны получить строку длиной не менее 16 символов. Программа должна занимать не более двух строк редактора кода
  ```python
    str = "qwer"
    print(str * 5)
  ```
  # Результат

![Меню](https://github.com/soft2k/Software_Engineering/blob/main/pic/Tema2Pic14.PNG)
  # Вывод
  С помощью * умножил str на число и получил не менее 16 символов


   ## Самостоятельная работа №5
  
  ### Создайте три переменные: день (тип данных - числовой), месяц (тип данных - строка), год (тип данных - числовой) и выведите в консоль текущую дату в формате: “Сегодня день месяц год. Всего хорошего!” используя F строку и оператор end внутри print(), в котором вы должны написать фразу “Всего хорошего!”. Программа должна занимать не более двух строк редактора кода

  ```python
   day, month, year = 31, "декабря", 2024
    print(f"Сегодня {day} {month} {year}. ", end="Всего хорошего!");
  ```
  # Результат
![Меню](https://github.com/soft2k/Software_Engineering/blob/main/pic/Tema2Pic15.PNG)
  # Вывод
  Вывел три переменные 



   ## Самостоятельная работа №6
  
  ### В предложении ‘Hello World’ вставьте ‘my’ между двумя словами. Выведите полученное предложение в консоль в одну строку. Программа должна занимать не более двух строк редактора кода.

  ```python
     str = 'Hello World'
     print (str[:-5], 'my', str[5:])
  ```
  # Результат
![Меню](https://github.com/soft2k/Software_Engineering/blob/main/pic/Tema2Pic16.PNG)
  # Вывод
  

   ## Самостоятельная работа №7
  ### Узнайте длину предложения ‘Hello World’, результат выведите в консоль. Программа должна занимать не более двух строк редактора кода
  ```python
  str = "Hello World"
  print(len(str))
  ```
  # Результат
![Меню](https://github.com/soft2k/Software_Engineering/blob/main/pic/Tema2Pic17.PNG)
  # Вывод
 Благодаря len мы получили кол-во символов длины выражения

  
   ## Самостоятельная работа №8

   
  ### Переведите предложение ‘HELLO WORLD’ в нижний регистр. Программа должна занимать не более двух строк редактора кода
  ```python
  str = "HELLO WORLD"
  print(str.lower())
  ```
  # Результат
![Меню](https://github.com/soft2k/Software_Engineering/blob/main/pic/Tema2Pic18.PNG)
  # Вывод
  С помощью lower мы перевели в нижний регистр


   ## Самостоятельная работа №9

   
  ### Напишите программу, которая проверяет, является ли введенное число четным.
  
  ```python
      int =  int(input())
    if int % 2 == 0:
        print("Четное")
    else:
        print("Не четное")
  ```
  # Результат
![Меню](https://github.com/soft2k/Software_Engineering/blob/main/pic/Tema2Pic19.PNG)


   ## Самостоятельная работа №10

   
  ### Переведите предложение ‘hello world’ в верхний регистр
  
  ```python
  str = "hello world"
  print(str.upper())
  ```
  # Результат
![Меню](https://github.com/soft2k/Software_Engineering/blob/main/pic/Tema2Pic20.PNG)
  # Вывод
  С помощью upper мы перевели в нижний регистр


  






