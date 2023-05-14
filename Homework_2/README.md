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
## result

![first](https://github.com/h1stav/Postman/assets/83788756/837d3c4e-7137-4c95-9acf-1cb94322ac48)

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
