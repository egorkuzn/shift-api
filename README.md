**API DESCRIPTION**

*Авторизация/Регистрация*

>/login
```
PATCH:     |POST:      |PUT:     
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
input:
{}
output:
{
  нужно согласовать
}
```
*Карточки пользователя*

>/cards
```
PATCH:   |POST:         |PUT:
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
*Редактирование/Получение информации пользователя*
>/me
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





