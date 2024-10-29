
# Тема 8. Введение в ООП
Отчет по Теме #8 выполнил(а):
- Поляков Матвей Андреевич
- ИВТ-22-2

| Задание | Лаб_раб | Сам_раб |
| ------ | ------ | ------ |
| Задание 1 | + | + |
| Задание 2 | + | + |
| Задание 3 | + | + |
| Задание 4 | + | + |
| Задание 5 | + | + |
| Задание 6 | - | - |
| Задание 7 | - | - |
| Задание 8 | - | - |
| Задание 9 | - | - |
| Задание 10 | - | - |

знак "+" - задание выполнено; знак "-" - задание не выполнено;

Работу проверили:
- к.э.н., доцент Панов М.А.

  ## Лабораторная №1
  ### Создайте класс “Car” с атрибутами производитель и модель. Создайте объект этого класса. Напишите комментарии для кода, объясняющие его работу. Результатом выполнения задания будет листинг кода с комментариями.
  ```python
        class Car: # Определение класса Car
      def __init__(self,make,model):#Инициализурем класс car с двумя аргументами make и model
          self.make = make #  присваиваем значение make
          self.model = model  #  присваиваем значение model
  
  my_car = Car('Lada','Vesta')#  создаем экземпляр класса Car с аргументами 'Lada' и 'Vesta'
  ```
  # Результат
  ![Alt text](https://github.com/soft2k/Software_Engineering/blob/Tema8/pic/Screenshot_1.png)
  # Вывод
 
 Этот код создает класс Car для хранения информации об автомобиле (марки и модели) и создает конкретный экземпляр автомобиля Lada Vesta.


   ## Лабораторная №2
  ### Дополните код из первого задания, добавив в него атрибуты и методы класса, заставьте машину “поехать”. Напишите комментарии для кода, объясняющие его работу. Результатом выполнения задания будет листинг кода с комментариями и получившийся вывод в консоль.
  
      ```python
      class Car: # Определение класса Car
          def __init__(self,make,model):#Инициализурем класс car с двумя аргументами make и model
              self.make = make #  присваиваем значение make
              self.model = model  #  присваиваем значение model
      
          def driver(self):
              print(f'Driving the {self.make} {self.model}')#  метод driver который выводит на экран сообщение с именем машины
      
  
      
      my_car = Car('Lada','Vesta')#  создаем экземпляр класса Car с аргументами 'Lada' и 'Vesta'
      my_car.driver()# вызываем метод driver() экземпляра my_car
      ```
  # Результат
![Меню](https://github.com/soft2k/Software_Engineering/blob/Tema8/pic/Screenshot_2.png)

  # Вывод
   Этот код создает класс Car для хранения информации об автомобиле (марки и модели) и создает конкретный экземпляр автомобиля Lada Vesta и выводит сообщение



   ## Лабораторная №3
  ### Создайте новый класс “ElectricCar” с методом “charge” и атрибутом емкость батареи. Реализуйте его наследование от класса, созданного в первом задании. Заставьте машину поехать, а потом заряжаться.
  
  ```python
      class Car: # Определение класса Car
          def __init__(self,make,model):#Инициализурем класс car с двумя аргументами make и model
              self.make = make #  присваиваем значение make
              self.model = model  #  присваиваем значение model
      
      
      
      class ElectricCar(Car):
          def __init__(self, make, model, battery_size):# Инициализурем класс ElectricCar с тремя аргументами
              super().__init__(make, model) # вызываем метод __init__ из класса Car
              self.battery_size = battery_size # присваиваем значение battery_size
      
          def driver(self):
              print(f'Driving the {self.make} {self.model}')# 
              
          def charge(self):
              print(f'Charging the {self.make} {self.model} battery with {self.battery_size} kWh')
      
      my_car = ElectricCar('Tesla','Model S',100)#  создаем экземпляр класса Car с аргументами 'Lada' и 'Vesta'
      my_car.driver()# вызываем метод driver() экземпляра my_car
      my_car.charge()

  ```
  # Результат
![Меню](https://github.com/soft2k/Software_Engineering/blob/Tema8/pic/Screenshot_3.png)
  # Вывод
  
  Код создает иерархию классов для представления электромобиля (наследуя от обычного автомобиля) с возможностью вождения и зарядки




   ## Лабораторная №4
  
  ### Реализуйте инкапсуляцию для класса, созданного в первом задании. Создайте защищенный атрибут производителя и приватный атрибут модели. Вызовите защищенный атрибут и заставьте машину поехать. Напишите комментарии для кода, объясняющие его работу. Результатом выполнения задания будет листинг кода с комментариями и получившийся вывод в консоль
  ```python
class Car: # Определение класса Car
    def __init__(self,make,model):#Инициализурем класс car с двумя аргументами make и model
        self._make = make #  присваиваем значение make
        self.__model = model  #  присваиваем значение model

    def driver(self):
        print(f'Driving the {self._make} {self.__model}')# 

my_car = Car('Tesla','Model S')#  создаем экземпляр класса Car с аргументами 'Lada' и 'Vesta'
print(my_car._make) #  выводит значение make
my_car.driver()# вызываем метод driver() экземпляра my_car
  ```

  # Результат
![Меню](https://github.com/soft2k/Software_Engineering/blob/Tema8/pic/Screenshot_4.png)
  # Вывод
   Код демонстрирует использование инкапсуляции в Python через защищенный (_make) и приватный (__model) атрибуты класса Car, с возможностью вывода информации о машине.


## Лабораторная №5
  
  ### Реализуйте полиморфизм создав основной (общий) класс “Shape”, а также еще два класса “Rectangle” и “Circle”. Внутри последних двух классов реализуйте методы для подсчета площади фигуры. После этого создайте массив с фигурами, поместите туда круг и прямоугольник, затем при помощи цикла выведите их площади. Напишите комментарии для кода, объясняющие его работу

  ```python
    class Shape:
        def area(self):
            pass
    
    class Rectangle(Shape):
        def __init__(self,width,height):
            self.width = width
            self.height = height
    
    
        def area(self):
            return self.width * self.height
    
    
    class Circle(Shape):
        def __init__(self,radius):
            self.radius = radius
    
        def area(self):
            return 3.14 * (self.radius ** 2)
    
    def create_shape():
        shape_type = input("Введите тип фигуры (rectangle/circle): ").lower()
        
        if shape_type == "rectangle":
            width = float(input("Введите ширину прямоугольника: "))
            height = float(input("Введите высоту прямоугольника: "))
            return Rectangle(width, height)
        elif shape_type == "circle":
            radius = float(input("Введите радиус круга: "))
            return Circle(radius)
        else:
            print("Неизвестный тип фигуры")
            return None
    
    shape = create_shape()
    if shape:
        print(f"Площадь фигуры: {shape.area():.2f}")
  ```
  # Результат
![Меню](https://github.com/soft2k/Software_Engineering/blob/Tema8/pic/Screenshot_5.png)

  # Вывод
Код создает иерархию классов для вычисления площади геометрических фигур, где базовый класс Shape наследуется классами Rectangle и Circle, реализующими свои методы расчета площади.


  ## Самостоятельная работа №1
  ### Самостоятельно создайте класс и его объект. Они должны отличаться, от тех, что указаны в теоретическом материале (методичке) и лабораторных заданиях. Результатом выполнения задания будет листинг кода и получившийся вывод консоли.
  ```python
      class Computer:
    def __init__(self, cpu, ram, storage):
        self.cpu = cpu
        self.ram = ram
        self.storage = storage
        self.is_on = False
    
    def turn_on(self):
        self.is_on = True
        print("Компьютер включен")


my_pc = Computer("Intel i5", 16, 512)
my_pc.turn_on()
  ```
  # Результат
![Меню](https://github.com/soft2k/Software_Engineering/blob/Tema8/pic/Screenshot_6.png)

  # Вывод
 Этот код создает класс Computer, инициализирует объект компьютера с заданными характеристиками и включает его, выводя сообщение о включении.


   ## Самостоятельная работа №2
  ### Самостоятельно создайте атрибуты и методы для ранее созданного класса. Они должны отличаться, от тех, что указаны в теоретическом материале (методичке) и лабораторных заданиях. Результатом выполнения задания будет листинг кода и получившийся вывод консоли.
  
  ```python
class Computer:
    def __init__(self, cpu, ram, storage):
        self.cpu = cpu
        self.ram = ram
        self.storage = storage
        self.is_on = False
        self.temperature = 20 
    
    def turn_on(self):
        self.is_on = True
        self.temperature += 10
        print("Компьютер включен")

    def run_vs(self):
        if self.is_on:
            print("Запуск Visual Code...")
            self.temperature += 20
            print(f"Температура процессора повысилась до {self.temperature}°C")
        else:
            print("Невозможно запустить бенчмарк. Компьютер выключен")

my_pc = Computer("Intel i5", 16, 512)
my_pc.turn_on()
my_pc.run_vs()
  ```
  # Результат
![Меню](https://github.com/soft2k/Software_Engineering/blob/Tema8/pic/Screenshot_7.png)
  # Вывод
 
  Этот код создает класс Computer с базовыми характеристиками, включает компьютер и запускает Visual Code, отслеживая при этом изменение температуры процессора.



   ## Самостоятельная работа №3
  ### Имеется файл input.txt с текстом на латинице. Напишите программу, которая выводит следующую статистику по тексту: количество букв латинского алфавита; число слов; число строк. • Текст в файле: Beautiful is better than ugly. Explicit is better than implicit. Simple is better than complex. Complex is better than complicated. • Ожидаемый результат: Input file contains: 108 letters 20 words 4 lines
  
  ```python
class Computer:
    def __init__(self, cpu, ram, storage):
        self.cpu = cpu
        self.ram = ram
        self.storage = storage
        self.is_on = False
        self.temperature = 20 
    
    def turn_on(self):
        self.is_on = True
        self.temperature += 10
        print("Компьютер включен")

    def run_vs(self):
        if self.is_on:
            print("Запуск Visual Code...")
            self.temperature += 20
            print(f"Температура процессора повысилась до {self.temperature}°C")
        else:
            print("Невозможно запустить бенчмарк. Компьютер выключен")

class GamingPC(Computer):
    def __init__(self, cpu, ram, storage, gpu, rgb):
        super().__init__(cpu, ram, storage)
        self.gpu = gpu
        self.rgb = rgb
        self.game_mode = False

    def enable_game_mode(self):
        if self.is_on:
            self.game_mode = True
            self.temperature += 15
            print(f"Игровой режим включен! RGB подсветка: {self.rgb}")
            print(f"Температура выросла до {self.temperature}°C")
        else:
            print("Сначала включите компьютер!")

gaming_pc = GamingPC("AMD Ryzen 9", 32, 2000, "RTX 4090", "Rainbow")
gaming_pc.turn_on()
gaming_pc.run_vs()
gaming_pc.enable_game_mode()
  ```
  # Результат
![Меню](https://github.com/soft2k/Software_Engineering/blob/Tema8/pic/Screenshot_8.png)
  # Вывод
 Этот код создает класс Computer с базовыми характеристиками, включает компьютер и запускает Visual Code, отслеживая при этом изменение температуры процессора.



   ## Самостоятельная работа №4
  
  ### Самостоятельно реализуйте инкапсуляцию, продолжая работать с ранее созданным классом. Она должна отличаться, от того, что указана в теоретическом материале (методичке) и лабораторных заданиях. Результатом выполнения задания будет листинг кода и получившийся вывод консоли.
  
  ```python
class Computer:
    def __init__(self, cpu, ram, storage):
        self.cpu = cpu
        self.ram = ram
        self.storage = storage
        self.is_on = False
        self.temperature = 20 
    
    def turn_on(self):
        self.is_on = True
        self.temperature += 10
        print("Компьютер включен")

    def run_vs(self):
        if self.is_on:
            print("Запуск Visual Code...")
            self.temperature += 20
            print(f"Температура процессора повысилась до {self.temperature}°C")
        else:
            print("Невозможно запустить бенчмарк. Компьютер выключен")

class GamingPC(Computer):
    def __init__(self, cpu, ram, storage, gpu, rgb):
        super().__init__(cpu, ram, storage)
        self.gpu = gpu
        self.rgb = rgb
        self.game_mode = False

    def enable_game_mode(self):
        if self.is_on:
            self.game_mode = True
            self.temperature += 15
            print(f"Игровой режим включен! RGB подсветка: {self.rgb}")
            print(f"Температура выросла до {self.temperature}°C")
        else:
            print("Сначала включите компьютер!")

gaming_pc = GamingPC("AMD Ryzen 9", 32, 2000, "RTX 4090", "Rainbow")
gaming_pc.turn_on()
gaming_pc.run_vs()
gaming_pc.enable_game_mode()
  ```
  # Результат

![Меню](https://github.com/soft2k/Software_Engineering/blob/Tema8/pic/Screenshot_9.png)
  # Вывод
  


   ## Самостоятельная работа №5
  
  ### Самостоятельно реализуйте полиморфизм. Он должен отличаться, от того, что указан в теоретическом материале (методичке) и лабораторных заданиях. Результатом выполнения задания будет листинг кода и получившийся вывод консоли.
  ```python
class Computer:
    def __init__(self, name, cpu, ram):
        self.name = name
        self.cpu = cpu
        self.ram = ram
        self.is_on = False

    def turn_on(self):
        self.is_on = True
        print(f"{self.name} включен.")

    def run_task(self):
        if self.is_on:
            print(f"{self.name} выполняет базовую задачу.")
        else:
            print(f"{self.name} выключен. Сначала включите компьютер.")

class WorkStation(Computer):
    def __init__(self, name, cpu, ram, gpu):
        super().__init__(name, cpu, ram)
        self.gpu = gpu

    def run_task(self):
        if self.is_on:
            print(f"{self.name} выполняет сложные вычисления на CPU {self.cpu} и GPU {self.gpu}.")
        else:
            print(f"{self.name} выключен. Сначала включите рабочую станцию.")

class GamingPC(Computer):
    def __init__(self, name, cpu, ram, gpu):
        super().__init__(name, cpu, ram)
        self.gpu = gpu

    def run_task(self):
        if self.is_on:
            print(f"{self.name} запускает игру с высокими настройками графики на GPU {self.gpu}.")
        else:
            print(f"{self.name} выключен. Сначала включите игровой компьютер.")

class Server(Computer):
    def __init__(self, name, cpu, ram, storage):
        super().__init__(name, cpu, ram)
        self.storage = storage

    def run_task(self):
        if self.is_on:
            print(f"{self.name} обрабатывает запросы и управляет данными объемом {self.storage} ТБ.")
        else:
            print(f"{self.name} выключен. Сначала включите сервер.")
def run_computer_task(computer):
    computer.turn_on()
    computer.run_task()
    print()
basic_pc = Computer("Базовый ПК", "Intel i3", "8GB")
workstation = WorkStation("Рабочая станция", "AMD Threadripper", "64GB", "NVIDIA Quadro")
gaming_pc = GamingPC("Игровой ПК", "Intel i9", "32GB", "RTX 3080")
server = Server("Сервер", "Xeon", "128GB", 100)
computers = [basic_pc, workstation, gaming_pc, server]

for computer in computers:
    run_computer_task(computer)
  ```
  # Результат
![Меню](https://github.com/soft2k/Software_Engineering/blob/Tema8/pic/Screenshot_10.png)
  # Вывод 



   

  






