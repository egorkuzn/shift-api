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
           |  username |output:
{          |}          |{
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

>/cards/{username}
```
GET:     |POST:         |PUT:
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
>/user/{username}
```
POST:        |PUT:
input:       |input:
{            |{
  userID,    |  userID,
  paramName  |  whatChange,
}            |  onWhatChange
output:      |}
{            |output:
  paramValue |{
}            |  true
             |}             
```
*База всех объявлений*
>/cards
```
GET:
input:
{
  cardID,
}
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





