
# Тема 7. Работа с файлами (ввод, вывод)
Отчет по Теме #7 выполнил(а):
- Поляков Матвей Андреевич
- ИВТ-22-2

| Задание | Лаб_раб | Сам_раб |
| ------ | ------ | ------ |
| Задание 1 | + | + |
| Задание 2 | + | + |
| Задание 3 | + | + |
| Задание 4 | + | + |
| Задание 5 | + | + |
| Задание 6 | + | - |
| Задание 7 | + | - |
| Задание 8 | + | - |
| Задание 9 | + | - |
| Задание 10 | + | - |

знак "+" - задание выполнено; знак "-" - задание не выполнено;

Работу проверили:
- к.э.н., доцент Панов М.А.

  ## Лабораторная №1
  ### Составьте текстовый файл и положите его в одну директорию с программой на Python. Текстовый файл должен состоять минимум из двух строк.
  ```
  Привет!
  ```
  # Результат
![Меню](https://github.com/soft2k/Software_Engineering/blob/Tema7/pic/Screenshot_1.png)
  # Вывод
 Создал файл



   ## Лабораторная №2
  ### Напишите программу, которая выведет только первую строку из вашего файла, при этом используйте конструкцию open()/close().
  
      ```python
     with open('readme.txt','r',encoding='utf-8') as file:
        line = file.readline().strip()
    print(line)
      ```
  # Результат
![Меню](https://github.com/soft2k/Software_Engineering/blob/Tema7/pic/Screenshot_2.png)

  # Вывод
  С помощью open открыли файл txt и вывели первую строчку Привет!



   ## Лабораторная №3
  ### Напишите программу, которая выведет все строки из вашего файла в массиве, при этом используйте конструкцию open()/close().
  
  ```python
    with open('readme.txt','r',encoding='utf-8') as file:
        line = file.readlines()
    print(line)

  ```
  # Результат
![Меню](https://github.com/soft2k/Software_Engineering/blob/Tema7/pic/Screenshot_3.png)
  # Вывод
  С помощью open открыли файл txt и вывели все строчки




   ## Лабораторная №4
  
  ### Напишите программу, которая выведет все строки из вашего файла в массиве, при этом используйте конструкцию with open().
  ```python
    with open('readme.txt','r',encoding='utf-8') as file:
        line = file.readlines()
    print(line)
  ```

  # Результат
![Меню](https://github.com/soft2k/Software_Engineering/blob/Tema7/pic/Screenshot_4.png)
  # Вывод
    С помощью open открыли файл txt и вывели все строчки


## Лабораторная №5
  
  ### Напишите программу, которая выведет каждую строку из вашего файла отдельно, при этом используйте конструкцию with open().
  ```python
  with open('readme.txt','r',encoding='utf-8') as file:
   for line in file:
      print(line.strip())
  ```
  # Результат
![Меню](https://github.com/soft2k/Software_Engineering/blob/Tema7/pic/Screenshot_5.png)

  # Вывод
   С помощью open открыли файл txt и вывели все строчки по отдельности



   ## Лабораторная №6
  
  ### Напишите программу, которая будет добавлять новую строку в ваш файл, а потом выведет полученный файл в консоль. Вывод можно осуществлять любым способом. Обязательно проверьте сам файл, чтобы изменения в нем тоже отображались.

  ```python
      with open('readme.txt','a',encoding='utf-8') as file:
        file.write('\nНовая строка')
      with open('readme.txt','r',encoding='utf-8') as file:
        print(file.read())
  ```
  # Результат
![Меню](https://github.com/soft2k/Software_Engineering/blob/Tema7/pic/Screenshot_6.png)

  # Вывод
  С помощью file.write добавили новую строчку и 
    
  ## Лабораторная №7
  ### Напишите программу, которая перепишет всю информацию, которая была у вас в файле до этого, например напишет любые данные из произвольно вами составленного списка. Также не забудьте проверить что измененная вами информация сохранилась в файле.
  
  ```python
      string = ['Первая строка', 'Вторая строка', 'Третья строка']
    with open('readme.txt','w',encoding='utf-8') as file:
        for line in string:
            file.write(line + '\n')
    with open('readme.txt','r',encoding='utf-8') as file:
        print(file.read())
  ```
  # Результат
![Меню](https://github.com/soft2k/Software_Engineering/blob/Tema7/pic/Screenshot_7.png)
  # Вывод
   С помощью file.write добавили новые строчки,перепесали данные 

  
   ## Лабораторная №8

   
  ### Выберите любую папку на своем компьютере, имеющую вложенные директории. Выведите на печать в терминал ее содержимое, как и всех подкаталогов при помощи функции print_docs(directory).
  ```python
      import os
    def print_docs(directory):
        for root, dirs, files in os.walk(directory):
            for name in files:
                print(os.path.join(root, name))
    print_docs(r'C:\Users\matve\OneDrive\Рабочий стол\pic')
  ```
  # Результат
![Меню](https://github.com/soft2k/Software_Engineering/blob/Tema7/pic/Screenshot_8.png)

  # Вывод
  Все скриншоты выводится в терминал


   ## Лабораторная №9

   
  ### Документ «input.txt» содержит следующий текст: Приветствие Спасибо Извините Пожалуйста До свидания Ты готов? Как дела? С днем рождения! Удача! Я тебя люблю. Требуется реализовать функцию, которая выводит слово, имеющее максимальную длину (или список слов, если таковых несколько). Проверьте работоспособность программы на своем наборе данных.
  
  ```python
      def max(filename):
        with open(filename, 'r', encoding='utf-8') as file:
            words = file.read().split()
        max_length = max(len(word) for word in words)
        return [word for word in words if len(word) == max_length]
    print(max('readme.txt'))
  ```
  # Результат
![Меню](https://github.com/soft2k/Software_Engineering/blob/Tema7/pic/Screenshot_9.png)

  # Вывод
  С помощью \n разделил Hello и World



   ## Лабораторная №10

   
  ### Требуется создать csv-файл «rows_300.csv» со следующими столбцами: • № - номер по порядку (от 1 до 300); • Секунда – текущая секунда на вашем ПК; • Микросекунда – текущая миллисекунда на часах. Для наглядности на каждой итерации цикла искусственно приостанавливайте скрипт на 0,01 секунду.
  
  ```python
import csv
import time
with open('rows_300.csv', 'w', newline='') as csvfile:
    writer = csv.writer(csvfile)
    writer.writerow(['№', 'Секунда', 'Микросекунда'])
    for i in range(1, 301):
        seconds = time.localtime().tm_sec
        microseconds = int(time.time() * 1e6) % 1e6
        print(f"Строка {i}: Секунды - {seconds}, Микросекунды - {microseconds}")
        writer.writerow([i, seconds, microseconds])
        time.sleep(0.01)
  ```
  # Результат
![Меню](https://github.com/soft2k/Software_Engineering/blob/Tema7/pic/Screenshot_10.png)


  # Вывод
  Создали csv файл и занесли в него данные


  ## Самостоятельная работа №1
  ### Выведите в консоль булевую переменную False, не используя слово False в строке или изначально присвоенную булевую переменную. Программа должна занимать не более двух строк редактора кода.
  ```python
      from collections import Counter
    with open('aaa.txt', 'r', encoding='utf-8') as file:
        text = file.read()
    words = text.split()
    word_count = len(words)
    word_freq = Counter(words)
    most_common_word, most_common_count = word_freq.most_common(1)[0]
    print(f'Количество слов: {word_count}')
    print(f'Самое частое слово: "{most_common_word}" (встречается {most_common_count} раз)')
  ```
  # Результат
![Меню](https://github.com/soft2k/Software_Engineering/blob/Tema7/pic/Screenshot_11.png)

  # Вывод
  Вывел в сколько всего слов и частое слова


   ## Самостоятельная работа №2
  ### У вас появилась потребность в ведении книги расходов, посмотрев все существующие варианты вы пришли к выводу что вас ничего не устраивает и нужно все делать самому. Напишите программу для учета расходов. Программа должна позволять вводить информацию о расходах, сохранять ее в файл и выводить существующие данные в консоль. Ввод информации происходит через консоль. Результатом выполнения задачи будет: скриншот файла с учетом расходов, листинг кода, и вывод в консоль, с демонстрацией работоспособности программы.
  
  ```python
  # expense_tracker.py

def add_expense(expenses_file):
    expense = input("Введите описание расхода: ")
    cost = float(input("Введите стоимость расхода: "))
    with open(expenses_file, 'a', encoding='utf-8') as file:
        file.write(f"{expense}: {cost}\n")

def view_expenses(expenses_file):
    with open(expenses_file, 'r', encoding='utf-8') as file:
        expenses = file.readlines()
    for expense in expenses:
        print(expense.strip())

def main():
    expenses_file = 'expenses.txt'
    while True:
        print("1. Добавить расход")
        print("2. Просмотреть расходы")
        print("3. Выход")
        choice = input("Выберите опцию: ")
        if choice == '1':
            add_expense(expenses_file)
        elif choice == '2':
            view_expenses(expenses_file)
        elif choice == '3':
            break
        else:
            print("Неверная опция. Пожалуйста, попробуйте снова.")

if __name__ == "__main__":
    main()
  ```
  # Результат
![Меню](https://github.com/soft2k/Software_Engineering/blob/Tema7/pic/Screenshot_12.png)
  # Вывод
  Создали программу которая добавляет ии показывает записи расходов



   ## Самостоятельная работа №3
  ### Имеется файл input.txt с текстом на латинице. Напишите программу, которая выводит следующую статистику по тексту: количество букв латинского алфавита; число слов; число строк. • Текст в файле: Beautiful is better than ugly. Explicit is better than implicit. Simple is better than complex. Complex is better than complicated. • Ожидаемый результат: Input file contains: 108 letters 20 words 4 lines
  
  ```python
 def text_statistics(filename):
    with open(filename, 'r', encoding='utf-8') as file:
        content = file.readlines()


    line_count = len(content)


    word_count = 0
    letter_count = 0

    for line in content:
        words = line.split()
        word_count += len(words)
        letter_count += sum(c.isalpha() for c in line)

    return letter_count, word_count, line_count

def main():
    filename = 'readme.txt'
    letters, words, lines = text_statistics(filename)
    print(f"Input file contains: {letters} letters {words} words {lines} lines")

if __name__ == "__main__":
    main()
  ```
  # Результат
![Меню](https://github.com/soft2k/Software_Engineering/blob/Tema7/pic/Screenshot_13.png)
  # Вывод
  Программа выводит количество букв, слов и строк из файла.



   ## Самостоятельная работа №4
  
  ### Напишите программу, которая получает на вход предложение, выводит его в терминал, заменяя все запрещенные слова звездочками * (количество звездочек равно количеству букв в слове). Запрещенные слова, разделенные символом пробела, хранятся в текстовом файле input.txt. Все слова в этом файле записаны в нижнем регистре. Программа должна заменить запрещенные слова, где бы они ни встречались, даже в середине другого слова. Замена производится независимо от регистра: если файл input.txt содержит запрещенное слово exam, то слова exam, Exam, ExaM, EXAM и exAm должны быть заменены на ****. • Запрещенные слова: hello email python the exam wor is • Предложение для проверки: Hello, world! Python IS the programming language of thE future. My EMAIL is ksusha.katkova2468@yandex.ru PYTHON is awesome!!!! • Ожидаемый результат: *****, ***ld! ****** ** *** programming language of *** future. My ***** ** ksusha.katkova2468@yandex.ru ****** ** awesome!!!!
  ```python
   import re
def censor_text(input_text, banned_words):
    for word in banned_words:
        input_text = re.sub(word, '*' * len(word), input_text, flags=re.IGNORECASE)
    return input_text
with open('readme.txt', 'r', encoding='utf-8') as file:
    banned_words = file.read().strip().split()
sentence = input("Введите предложение для проверки: ")
censored_sentence = censor_text(sentence, banned_words)
print(censored_sentence)
  ```
  # Результат

![Меню](https://github.com/soft2k/Software_Engineering/blob/Tema7/pic/Screenshot_14.png)
  # Вывод
  


   ## Самостоятельная работа №5
  
  ### Создать программу, которая читает текстовый файл, подсчитывает частоту каждого слова в нем и записывает результаты в новый файл.
  ```python
   def read_names(filename):
    try:
        with open(filename, 'r', encoding='utf-8') as file:
            names = file.readlines()
        return [name.strip() for name in names]
    except FileNotFoundError:
        print(f"Ошибка: Файл '{filename}' не найден.")
        return []

def greet_names(names):
    for name in names:
        print(f"Привет, {name}!")

def main():
    names = read_names('readme.txt')
    if names:
        print("Приветствия:")
        greet_names(names)

if __name__ == "__main__":
    main()
  ```
  # Результат
![Меню](https://github.com/soft2k/Software_Engineering/blob/Tema7/pic/Screenshot_15.png)
  # Вывод 



   

  






