# HomeWork_1

_Создаем в Postman **Create new collection** через `+`_  

![new collection](https://github.com/h1stav/postman/assets/83788756/d9a5c523-38e4-449d-8599-bfeee9ac5fbc)

_В текущей коллекции создаем запросы в Postman, нажимаем на **`add a request`**_

![add a request](https://github.com/h1stav/postman/assets/83788756/b7d5f11c-a9d6-4ff6-93bf-0e9cd924d1d6)

```
Protocol: http
IP: 162.55.220.72
Port: 5005

EP_1
Method: GET
EndPoint: /get_method
request url params: 
 name: str
 age: int
 
 response: 
[
    “Str”,
    “Str”
]
```
_Выбераем метод **`GET`**_

_В поле `Enter URL or paste text` вводим **Protocol**, **IP**, **Port** и **EndPoint**_

_В `Params` передаем параметры в URL, так как написано в документации_ 

_Нажимаем **`Save`**, чтобы сохранить все введенные данные. Для того чтобы отправить запрос нажимаем **`Send`**_

![get_method](https://github.com/h1stav/postman/assets/83788756/e034899e-a353-40a5-a860-429240bd5ca9)

==================
```
EP_2
Method: POST
EndPoint: /user_info_3
request form data: 
 name: str
 age: int
 salary: int

response: 
{'name': name,
          'age': age,
          'salary': salary,
          'family': {'children': [['Alex', 24], ['Kate', 12]],
                     'u_salary_1_5_year': salary * 4}}
```
_Через **`...`** в коллекции, нажимаем на **`add request`**, чтобы создать новый запрос_

_Выбераем метод **`POST`**_

_В поле `Enter URL or paste text` вводим **Protocol**, **IP**, **Port** и **EndPoint***_

_Параметры в медоте `POST` передаются в кнопке `Body`_

_Чтобы добавить данные нужно нажать на кнопку `none`  и выбрать `form-data`, после этого вводим данные как в документации_

_Нажимаем **`Save`**, чтобы сохранить все введенные данные. Для того чтобы отправить запрос нажимаем **`Send`**_

![user_info_3](https://github.com/h1stav/postman/assets/83788756/dc753c17-5193-4070-8e12-9329950d4022)

==================
```
EP_3
Method: GET
EndPoint: /object_info_1
request url params: 
 name: str
 age: int
 weight: int

response: 
{'name': name,
          'age': age,
          'daily_food': weight * 0.012,
          'daily_sleep': weight * 2.5}
```

_Так же чтобы постоянно не переписывать запрос, можно его копировать комбинацией клавиш `Ctrl + D`_

_Меняем название запроса_

_Выбераем метод **`GET`**_

_В поле `Enter URL or paste text` меняем **EndPoint***_

_В `Params` передаем параметры в URL, так как написано в документации_ 

_Нажимаем **`Save`**, чтобы сохранить все введенные данные._  _Для того чтобы отправить запрос нажимаем **`Send`**_


![object_info_1](https://github.com/h1stav/postman/assets/83788756/96840f99-e5b1-4f24-82d0-22ee959afd40)

==================
```
EP_4
Method: GET
EndPoint: /object_info_2
request url params: 
 name: str
 age: int
 salary: int

response: 
{'start_qa_salary': salary,
          'qa_salary_after_6_months': salary * 2,
          'qa_salary_after_12_months': salary * 2.7,
          'qa_salary_after_1.5_year': salary * 3.3,
          'qa_salary_after_3.5_years': salary * 3.8,
          'person': {'u_name': [user_name, salary, age],
                     'u_age': age,
                     'u_salary_5_years': salary * 4.2}
          }
```
_Нажимаем комбинацию кнопок `Ctrl + D`, наш запрос продубливаролся_

_Меняем название запроса_

_Метод остается тот же **`GET`**_

_В поле `Enter URL or paste text` меняем **EndPoint***_

_В `Params` передаем параметры в URL, так как написано в документации_ 

_Нажимаем **`Save`**, чтобы сохранить все введенные данные. Для того чтобы отправить запрос нажимаем **`Send`**_

![object_info_2](https://github.com/h1stav/postman/assets/83788756/3b08f98d-a03e-4944-9518-a7c73801c56e)

==================
```
EP_5
Method: GET
EndPoint: /object_info_3
request url params: 
 name: str
 age: int
 salary: int

response: 
{'name': name,
          'age': age,
          'salary': salary,
          'family': {'children': [['Alex', 24], ['Kate', 12]],
                     'pets': {'cat':{'name':'Sunny',
                                     'age': 3},
                              'dog':{'name':'Luky',
                                     'age': 4}},
                     'u_salary_1_5_year': salary * 4}
          }
```
_Нажимаем комбинацию кнопок `Ctrl + D`, наш запрос продубливаролся_

_Меняем название запроса_

_Метод остается тот же **`GET`**_

_В поле `Enter URL or paste text` меняем **EndPoint***_

_В `Params` передаем параметры в URL, так как написано в документации_ 

_Нажимаем **`Save`**, чтобы сохранить все введенные данные. Для того чтобы отправить запрос нажимаем **`Send`**_

![object_info_3](https://github.com/h1stav/postman/assets/83788756/3de26dd9-8747-49a5-9e5d-b07f528496e3)

==================
```
EP_6
Method: GET
EndPoint: /object_info_4
request url params: 
 name: str
 age: int
 salary: int

response: 
{'name': name,
          'age': int(age),
          'salary': [salary, str(salary * 2), str(salary * 3)]}
```
_Нажимаем комбинацию кнопок `Ctrl + D`, наш запрос продубливаролся_

_Меняем название запроса_

_Метод остается тот же **`GET`**_

_В поле `Enter URL or paste text` меняем **EndPoint***_

_В `Params` передаем параметры в URL, так как написано в документации_ 

_Нажимаем **`Save`**, чтобы сохранить все введенные данные. Для того чтобы отправить запрос нажимаем **`Send`**_

![object_info_4](https://github.com/h1stav/postman/assets/83788756/d1ac0bfc-0d73-46a6-b9ed-232f3e5d34f2)

==================
```
EP_7
Method: POST
EndPoint: /user_info_2
request form data: 
 name: str
 age: int
 salary: int

response: 
{'start_qa_salary': salary,
          'qa_salary_after_6_months': salary * 2,
          'qa_salary_after_12_months': salary * 2.7,
          'qa_salary_after_1.5_year': salary * 3.3,
          'qa_salary_after_3.5_years': salary * 3.8,
          'person': {'u_name': [user_name, salary, age],
                     'u_age': age,
                     'u_salary_5_years': salary * 4.2}
          }
```
_В коллекции нажимаем на готовый запрос `/user_info_1` и нажимаем комбинацию кнопок `Ctrl + D`, наш запрос продубливаролся_

_Меняем название запроса_

_Метод остается тот же **`POST`**_

_В поле `Enter URL or paste text` меняем **EndPoint***_

_как мы уже знаем, параметры в медоте `POST` передаются в кнопке `Body`_

_Нажимаем **`Save`**, чтобы сохранить все введенные данные. Для того чтобы отправить запрос нажимаем **`Send`**_

![user_info_2](https://github.com/h1stav/postman/assets/83788756/839cd405-17a2-4c73-b614-f4e67a67287a)
