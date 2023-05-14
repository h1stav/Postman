# HomeWork_2

## 1. Запрос /first

**1.** _Отправить запрос._ 

http://162.55.220.72:5005/first 

**2.** _Статус код 200_ 

В разделе **Snippets** выбираем `Status code: Code is 200`


```
pm.test("Status code is 200", function () {                          
    pm.response.to.have.status(200);                     # В Tests отображается написаный код
});
```
**3.** _Проверить, что в body приходит правильный string._ 

Также в разделе **Snippets** выбираем `Response body: Contains string`
```
pm.test("Body matches string", function () {
    pm.expect(pm.response.text()).to.include("This is the first responce from server!ss");
});
```

Сохраним запрос и запустим тест.

## result

![first](https://github.com/h1stav/Postman/assets/83788756/837d3c4e-7137-4c95-9acf-1cb94322ac48)

=========================================================================


# 2. Запрос /user_info_3

**1.** _Отправить запрос._

http://162.55.220.72:5005/user_info_3 


**2.** _Статус код 200_ 

В разделе **Snippets** выбираем `Status code: Code is 200`

```
pm.test("Status code is 200", function () {                          
    pm.response.to.have.status(200);                     # В Tests отображается написаный код
});
```
## result

![Status 200 ](https://github.com/h1stav/Postman/assets/83788756/a957b453-110b-42a7-ab80-82904be8b693)


**3.** _Спарсить response body в json._
```
var resp = pm.response.json();
```


**4.** _Проверить, что name в ответе равно name s request (name вбить руками.)_
```
pm.test("Name in the response is equal to name", function () {
    pm.expect(resp.name).to.eql("Denis");
});
```
## result

![Name ](https://github.com/h1stav/Postman/assets/83788756/401fc6ff-bb24-4a81-ad9e-2fc1601976e2)


**5.** _Проверить, что age в ответе равно age s request (age вбить руками.)_
```
pm.test("Age in the response is equal to age", function () {
   pm.expect(resp.age).to.eql("33");
});
```
## result

![age ](https://github.com/h1stav/Postman/assets/83788756/1c49512c-2bae-4e42-aa4d-7945336cd781)


**6.** _Проверить, что salary в ответе равно salary s request (salary вбить руками.)_
```
pm.test("Salary in the response is equal to salary", function () {
    pm.expect(resp.salary).to.eql(1000);
});
```
## result

![salary](https://github.com/h1stav/Postman/assets/83788756/a45099fe-8ae1-49a8-8e14-8a36de12b6bb)


**7.** _Спарсить request._ 
```
var req = request.data;
```


**8.** _Проверить, что name в ответе равно name s request (name забрать из request.)_
```
pm.test("Name in the response is equal to name", function () {
    pm.expect(resp.name).to.eql(req.name);
});
```
## result

![req name](https://github.com/h1stav/Postman/assets/83788756/98902a70-7654-4f32-96b6-255b3e215b3f)


**9.** _Проверить, что age в ответе равно age s request (age забрать из request.)_
```
pm.test("Age in the response is equal to age", function () {
    pm.expect(resp.age).to.eql(req.age);
});
```
## result

![req age](https://github.com/h1stav/Postman/assets/83788756/6aba9299-9ef8-4650-a185-352571ac94ea)


**10.** _Проверить, что salary в ответе равно salary s request (salary забрать из request.)_ 
```
pm.test("Salary in the response is equal to salary", function () {
    pm.expect(resp.salary).to.eql(Number(req.salary));
});
```
## result

![req salary](https://github.com/h1stav/Postman/assets/83788756/23b7d8d3-25eb-457a-84ae-3e4e8ffc6c30)


**11.** _Вывести в консоль параметр family из response. _
```
console.log(resp.family)
```


**12.** _Проверить что u_salary_1_5_year в ответе равно salary*4 (salary забрать из request)_
```
pm.test("U salary 1.5 year in the response is equal to salary *4", function () {
    pm.expect(resp.family.u_salary_1_5_year).to.eql(req.salary * 4);
});
```
## result

![req salary 4](https://github.com/h1stav/Postman/assets/83788756/e40013a3-bd0f-4e4f-a3c7-99a57a01fcf0)



=========================================================================

## 3. Запрос /object_info_3

**1.** _Отправить запрос._ 

http://162.55.220.72:5005/object_info_3 

**2.** _Статус код 200_ 

В разделе **Snippets** выбираем `Status code: Code is 200`


```
pm.test("Status code is 200", function () {                          
    pm.response.to.have.status(200);                     # В Tests отображается написаный код
});
```
## result

![object_info_3_status_200](https://github.com/h1stav/Postman/assets/83788756/234eda0b-373d-4a34-b1c1-4c8ffb1f8f27)

**3.** _Спарсить response body в json._
```
var resp = pm.response.json();
```
## result

![object_info_3_Json](https://github.com/h1stav/Postman/assets/83788756/d7df6647-431e-4d92-953e-27d4de9cdb2a)

**4.** _Спарсить request._
```
var req = pm.request.url.query.toObject ();
```
## result

![object_info_3_toObject](https://github.com/h1stav/Postman/assets/83788756/58a14181-430e-46ee-9568-4fe48852f163)

**5.** _Проверить, что name в ответе равно name s request (name забрать из request.)_
```
pm.test("Name in the response is equal to name request", function () {
    pm.expect(resp.name).to.eql(req.name);
});
```
## result

![object_info_req_name](https://github.com/h1stav/Postman/assets/83788756/01f6ee18-6cf6-4f13-acf9-b1cc9c0821f0)

**6.** _Проверить, что age в ответе равно age s request (age забрать из request.)_
```
pm.test("Age in the response is equal to age request", function () {
    pm.expect(resp.age).to.eql(req.age);
});
```
## result

![object_info_req_age](https://github.com/h1stav/Postman/assets/83788756/aa634289-e492-4ac8-8575-9cf89327344c)

**7.** _Проверить, что salary в ответе равно salary s request (salary забрать из request.)_
```
pm.test("Salary in the response is equal to salary request", function() {
    pm.expect(String(resp.salary)).to.eql(req.salary);
});
```
## result

![object_info_req_salary](https://github.com/h1stav/Postman/assets/83788756/bca1779e-e8ef-471c-ab03-15de63af642d)

**8.** _Вывести в консоль параметр family из response._
```
console.log(resp.family);
```
## result

![object_info_concole](https://github.com/h1stav/Postman/assets/83788756/58d9533b-08b4-42e1-aed0-dd108e0b01d0)

**9.** _Проверить, что у параметра dog есть параметры name._
```
pm.test("Check that the dog parameter has name parameters", function () {
    pm.expect(resp.family.pets.dog).to.property("name");
});
```
## result

![object_info_dog_name](https://github.com/h1stav/Postman/assets/83788756/7f4d2d8d-bc88-4716-990e-47a465056190)

**10.** _Проверить, что у параметра dog есть параметры age._
```
pm.test("Check that the namy parameter has Luky parameters", function () {
    pm.expect(resp.family.pets.dog).to.property("age");
});
```
## result

![object_info_dog_age](https://github.com/h1stav/Postman/assets/83788756/074191a9-0f7a-4df7-b8fa-8c0b78093bce)

**11.** _Проверить, что параметр name имеет значение Luky._
```
pm.test("Check that the namy parameter has Luky parameters", function () {
    pm.expect(resp.family.pets.dog.name).to.eql('Luky');
});
```
## result

![object_info_Luky](https://github.com/h1stav/Postman/assets/83788756/887c8fed-a63c-45d0-a274-faad663ef9d5)

**12.** _Проверить, что параметр age имеет значение_ 
```
pm.test("Check that the age parameter has the value", function () {
    pm.expect(resp.family.pets.dog.age).to.eql(4);
});
```
## result

![object_info_age4](https://github.com/h1stav/Postman/assets/83788756/8d7fa64d-22d3-4058-921d-e0ac503496e9)
