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
*Лента*

>/feed
```
GET:
output:
{
  нужно согласовать
}
```
*Карточки пользователя*

>/me/{variable}
>>{variable} - подстрока, которая может быть
- liked
- own
- rent
```
POST:    |PUT:          |PATCH:
input:   |input:        |input:
{        |{             |{
  userID,|  userID,     | userID,
  type   |  imageURL,   | cardID,
}        |  description,| what,
output:  |  price,      | onWhat
{        |  term,       |}
  imgIDs |  category    |output:
}        | }            |{
         |output:       | true
         |{             |}
         |  true        |
         |}             |
```
*База всех объявлений*
>/cards/{id}
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
*Редактирование/Получение информации пользователя*
>/me/settings
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
}            |  true
             |}             
```





