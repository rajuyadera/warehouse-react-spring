# USER SPECIFITAION

## Register User

Endpoint : POST /api/register

Request Body :

```json
{
  "name": "admin",
  "username": "raju",
  "password": "raju123123",
  "confirmPassword": "raju123123"
}
```

Response Body(Success) :

```json
{
  "message": "User Created"
}
```

Response Body(Error) :

```json
{
  "message": "password not match"
}
```

## Login User

Endpoint : POST /api/login

Request Body :

```json
{
  "name": "admin",
  "username": "raju",
  "password": "raju123123"
}
```

Response Body(Success) :

```json
{
  "message": {
    "token": "random string",
    "expiredAt": 9287589273 //millisecond
  }
}
```

Response Body(failed, 404) :

```json
{
  "message": "password can`t be null"
}
```

## Get User

Endpoint : GET /api/user

Response Body(Success) :

```json
{
    "data": [
        {
         "uuid" : "123hui32h4iu12",
         "name" : "raju",
         "username" : "raju yadera"
        },
        {
         "uuid" : "123hui32h4iu12",
         "name" : "aji",
         "username" : "aji ambatukam"
        },
        {
         "uuid" : "123hui32h4iu12",
         "name" : "parit",
         "username" : "parit pempek"
        },
    ]
}
```

Response Body(Error) :

```json
{
  "message": "cannot get user"
}
```

## Get user by UUID

Endpoint : GET /api/user/{uuid}

Response Body(Success) :

```json
{
    "data": {
        "uuid" : "123hui32h4iu12",
        "name" : "raju",
        "username" : "raju yadera",
    `}
}`
```

Response Body(Error) :

```json
{
  "message": "cannot get user"
}
```

## Update User

## Delete User
