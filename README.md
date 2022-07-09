**API DESCRIPTION**

*Авторизация/Регистрация*

>/login
```
GET:       |PUT:       |POST:     
input:     |input:     |input:
{          |{          |{
  password,|  password,|  tempID,
  email    |  email,   |  emailCode
}          |  name,    |}
           |  surname, |
output:    |  phone    |output:
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
GET:         |POST:
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
  castomerID,
  term,
  category
}
```





