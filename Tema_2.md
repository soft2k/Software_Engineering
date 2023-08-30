# Тема 2. Базовые операции языка Python
Отчет по Теме #2 выполнил(а):
- Панов Михаил Александрович
- ИВТ-21-1

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

## Задание 1
### Выведите в консоль три строки. Первая – любое число. Вторая – любое число в виде строки. Третья – любое число с плавающей точкой.

```python
print(123)
print('123')
print(1.23)
```
### Результат.


![Меню](https://github.com/S1GARETA/UnityLab1/blob/main/Demo%20files/Menu.jpg)

### Выполнение основного задания
На первой сцене было создано 3 объекта: Plane, Cube, Sphere. Для объекта Sphere был установлен Collider в режиме триггера. Для объекта Cube был применён материал красного цвета, а так же компонент RigidBody в режиме гравитации, чтобы у него появилась физика. Чтобы Cube не проваливался под Plane, объекту Plane также был добавлен компонент RigidBody, но уже в режиме кинематики.

Дальше, для объекта Sphere был написан [скрипт SphereCollisions](https://github.com/S1GARETA/UnityLab1/blob/main/Practice%201/Assets/Scripts/SphereCollisions.cs). Его работа заключается в том, чтобы при столкновении с объектом Cube в консоль выводилось сообщение о том, что произошло столкновение, и Cube менял цвет с красного на зелёный, и обратно на красный, когда оно завершилось.


using UnityEngine;

public class SphereCollisions : MonoBehaviour
{
    private void OnTriggerEnter(Collider other) 
    {
        if (other.gameObject.name == "Cube") 
        {
            Debug.Log("Произошло столкновение с " + other.gameObject.name);
            other.GetComponent<Renderer>().material.SetColor("_Color", Color.green);
        }
    }

    private void OnTriggerExit(Collider other) 
    {
        if (other.gameObject.name == "Cube")
        {
            Debug.Log("Завершили столкновение с " + other.gameObject.name);
            other.GetComponent<Renderer>().material.SetColor("_Color", Color.red);
        }
    }
}
```

![gif](https://github.com/S1GARETA/UnityLab1/blob/main/Demo%20files/Task1.gif)
![ConsoleLog](https://github.com/S1GARETA/UnityLab1/blob/main/Demo%20files/ConsoleLog.jpg)


## Задание 2
### Продемонстрируйте на сцене в Unity следующее:
- Что произойдёт с координатами объекта, если он перестанет быть дочерним?
- Создайте три различных примера работы компонента RigidBody.
### Ход работы:
- Что произойдёт с координатами объекта, если он перестанет быть дочерним?

На данный вопрос я не могу ответить, так как с Unity полноценно и осознанно начал работать только на этом курсе. Но очень интересно было бы во всём разобраться с преподавателем и узнать ответ.

- Создайте три различных примера работы компонента RigidBody.

На второй сцене было создано 3 примера работы компонента RigidBody на основе объекта Cube.
1. Включена только гравитация. У кубов присутствует своя физика, они ведут себя, как в реальной жизни.
![gif](https://github.com/S1GARETA/UnityLab1/blob/main/Demo%20files/Task2_Example1.gif)
2. Отключена гравитация и кинематика. Объекты ведут себя статично до тех пор, пока с ними не столкнётся другой объект. После этого кубы ведут себя так, будто они находятся в невесомости.
![gif](https://github.com/S1GARETA/UnityLab1/blob/main/Demo%20files/Task2_Example2.gif)
3. Включена только кинематика. Кубы ведут себя статично, остаются в том же положении, в каком они были созданы и поставлены. Даже после столкновения с другим объектом, они остаются в том же положении.
![gif](https://github.com/S1GARETA/UnityLab1/blob/main/Demo%20files/Task2_Example3.gif)

## Задание 3
### Реализуйте на сцене генерацию n кубиков. Число n вводится пользователем после старта сцены.
## Ход работы:

Для осуществления данного задания, была создана ещё одна сцена. Перейдя на неё, пользователь может ввести любое число в отдельное окно ввода, а затем нажать на кнопку "Создать", чтобы сгенерировалось то число кубиков, которое ввёл пользователь.

![gif](https://github.com/S1GARETA/UnityLab1/blob/main/Demo%20files/Task3.gif)

Перед тем, как написать скрипт, был создан [*префаб*](https://github.com/S1GARETA/UnityLab1/tree/main/Practice%201/Assets/Prefabs) (шаблон) объекта Cube. У него установлен компонент RigidBody в режиме гравитации и применён материал красного цвета. Для создания генерации по нажатию на кнопку, был написал [скрипт CreateObjects](https://github.com/S1GARETA/UnityLab1/blob/main/Practice%201/Assets/Scripts/CreateObjects.cs).

В нём определено 4 переменные:
- __InputText__ - Переменная, в которую передаётся тот текст, который вводит пользователь в окно ввода (в нашем случае число).
- __inputField__ - Данная переменная нужна для определения самого окна ввода.
- __Nums__ - Переменная типа integer, в которую будет преобразовываться переменная InputText.
- __obj__ - Это переменная типа GameObject, в ней будет храниться созданный префаб.

```cs
    [SerializeField] private Text InputText;
    [SerializeField] private InputField inputField;
    [SerializeField] private int Nums;
    public GameObject obj;
```

Данный скрипт повешан на UI элемент Canvas (Background), который в свою очередь вызывается по нажатию на кнопку "Создать". При нажатии вызывается метод __SaveText__.

```cs
    public void SaveText()
    {
        Nums = int.Parse(InputText.text);
        CreateCube(Nums);
    }
    public void CreateCube(int nums)
    {
        for(int i = 0; i < nums; i++)
        {
            Instantiate(obj, new Vector3(RandomNumber(), 5, RandomNumber()), Quaternion.Euler(0, 0, 0));
        } 
    }
    private float RandomNumber()
    {
        return Random.Range(-5, 5);
    }
```

В методе __SaveText__, в переменную Nums преобразовывается введёный текст и вызывается метод __CreateCube__. В нём через цикл создаются кубы с помощью функции __Instantiate__. Метод __RandomNumber__ нужен для создания рандомного числа, чтобы кубы не появлялись в одном месте.

Также, можно заметить, что кубы можно удалить по нажатию на "L". Для этого был написан [скрипт DestroyObj](https://github.com/S1GARETA/UnityLab1/blob/main/Practice%201/Assets/Scripts/DestroyObj.cs), который повешан на префаб.

```cs
using UnityEngine;

public class DestroyObj : MonoBehaviour
{
    void Update()
    {
        if(Input.GetKey (KeyCode.L))
        {
            Destroy(gameObject);
        }
    }
}
```

В данном скрипте есть метод __Update__, который работает постоянно, пока объект существует. В нём идёт проверка, если пользователь нажмёт на клавиатуре кнопку "L", то объект уничтожится.

## Выводы

Был создан новый проект, в котором было реализовано простенькое меню с навигацией по заданиям. В первом задании научился создавать объекты и работать с ними. Во втором задании более подробно познакомился с таким компонентом, как RigidBody. В третьем задании научился работать с UI элементами, а также создавать и удалять объекты с помощью скрипта.

Очень много нового и полезного узнал для себя, так как, повторюсь, осознанно познакомился с Unity только сейчас.
