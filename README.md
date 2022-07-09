**API DESCRIPTION**

1st: Authorization of user

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
// We take ids of cards by user id and cards' type.
//types would be strings ONLY from that range: "own", "liked", "rent"

/user/{username}
GET: {userID, param} -> param // Taking param info
PUT: {userID, whatToChange, param} -> status // Changing users params

/cards
GET: {cardID} -> Card // Taking Card.json by its id
