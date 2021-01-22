#js_best-practices

## 1. Всегда объявляйте локальные переменные.

- Нужно всегда объявлять локальные переменные и постоянные также с помощью let или const. В противном случае переменная будет объявлена как глобальная и как свойство объекта window.

**Плохой пример**

```
a = 5;
```

**Хороший пример**

```
let a=5;
```
## 2. Всегда завершайте переключатели (switch) по умолчанию значением default. Даже если вы думаете, что в этом нет необходимости.

- Блок кода после default будет выполняться, только если ни один case не совпал со значением переключателя.

**Пример**

```
switch (new Date().getMonth()) {
  case 0:
    month = "January";
    break;
  case 1:
    month = "February";
    break;
  case 2:
    month = "March";
    break;
  case 3:
    month = "April";
    break;
  case 4:
    month = "May";
    break;
  case 5:
    month = "June";
    break;
  case 6:
    month = "July";
    break;
  default:
    month = "Unknown";
}
```

## 3. Используйте camelCase для названий переменных, объектов и функций.

**Плохой пример**

```
let personname = 'Kate';
```

**Хороший пример**

```
let userName = 'Kate';
```

## 4. Всегда используйте let или const для объявления каждой переменной.

 **Плохой пример:**
 ```
var a = 2; //устаревшее объявление переменной
a = 2; //объявление переменной нет, ошибка.
 ```

 **Хороший пример :**
 ```
 let user = "Marina";
 const a = 2;
 ```

## 5. Операторы сравнения

- Следует использовать строгое сравнение (=== или !==) вместо нестрогого (== или !=)
- Это позволит избавиться от неявного преобразования типа данных.

**Плохой пример**

```
  if (answer == 4) {
    console.log(true);
  }
  if (attempts != 0) {
    console.log('Ошибка')
  }
```

**Хороший пример**

```
  if (answer === 4) {
    console.log(true);
  }
  if (attempts !== 0) {
    console.log('Ошибка')
  }
  ```
## 6. Для объявления объекта рекомендуется использовать фигурные скобки.

**Пример:**

```
let user = {      
  name: 'John',  
  age: 30        
};
```
## 7. Рекомендуется использовать одиночные кавычки, либо обратные при использовании шаблонных строк


**Плохой пример**

```
  const username = "John";
```

**Хороший пример**

```
  const username = 'Mark';
  const greeting = `Oh hi ${username}!`
```

## 8. Размещать скрипты в конце страницы

- Script размещаем внутри тега body в самом конце. Это делает загрузку страницы максимально быстрой для пользователя.

## 9. Не используйте new Object()
- Используйте {} вместо new Object()
- Используйте "" вместо new String()
- Используйте 0 вместо new Number()
- Используйте false вместо new Boolean()
- Используйте [] вместо new Array()
- Используйте /()/ вместо new RegExp()
- Используйте function (){} вместо new Function()

  **Пример**

```
let x1 = {};           // new object
let x2 = "";           // new primitive string
let x3 = 0;            // new primitive number
let x4 = false;        // new primitive boolean
let x5 = [];           // new array object
let x6 = /()/;         // new regexp object
let x7 = function(){}; // new function object
```

## 10. Ставьте точку с запятой в конце строки.

**Хороший пример**

```
const name = 'Marina';
```

**Плохой пример**

```
const name = 'Marina'
```
