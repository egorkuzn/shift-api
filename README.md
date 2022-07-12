**API DESCRIPTION**

*Авторизация/Регистрация*

>/login
```
POST:      |PUT:       |PATCH:     
input:     |input:     |input:
{          |{          |{
  email,   |  email,   |  tempID,
  password |  password,|  emailCode
}          |  name,    |}
           |  surname, |
output:    |  phone,   |
           |}          |output:
{          |           |{
 userID    |           |  userID
}          |output:    |}
           |{          |
           |  tempID,  |
           |}          |
           
```



*Карточки пользователя*

>/me/{variable}
>>{variable} - подстрока, которая может быть
- own
```
POST:    |PUT:          |PATCH:
input:   |input:        |input:
{        |{             |{
  userID |  userID,     | userID,
}        |  imageURL,   | cardID,
         |  description,| what,
output:  |  price,      | onWhat
{        |  term,       |}
 cardsID |  category    |output:
}        | }            |{
         |output:       | true
         |{             |}
         |  true        |
         |}             |
```
<uw>
<li>rent</li>
<li>liked</li>
</uw>

```
POST:    |PUT:          |DELETE:
input:   |input:        |input:
{        |{             |{
  userID |  userID,     | userID,
}        |  cardID      | cardID,
         |}             |} 
output:  |              | 
{        |              |
  imgIDs |              |output:
}        |              |{
         |output:       | true
         |{             |}
         |  true        |
         |}             |
```
*База всех объявлений*
>/cards?id={cardID}
```
GET:
output:
{
  cardID,
  imageURL,
  description,
  price,
  ownerID,
  rentStatus,
  customerID,
  term,
  category
}
```

*Выгрузка объявлений одной категории*
>/cards/{category}
```
GET:
output:
{
  imgIDs
}
```


*Редактирование/Получение информации пользователя*
>/me/settings
>> ***whatChange*** и ***paramName*** принимают:
<uw>
  <li>email</li>
  <li>name</li>
  <li>surname</li>
  <li>phone</li>
  <li>userIconURL</li>
</uw>



```
POST:        |PUT:
input:       |input:
{            |
  userID,    |{
  paramName  |  userID,
}            |  whatChange,
             |  onWhatChange
output:      |}
{            |output:
  paramValue |{
  Person     |  true
}            |}             
```
# ЖДУ ВАШИХ ПРЕДЛОЖЕНИЙ
*Мессенджер*

>/messages


*Лента*

>/feed
\[от, до\]
