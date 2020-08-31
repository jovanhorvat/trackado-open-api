# Get users for company

Get the users for the specific company.

**URL** : `/api/v2/usersapi/GetUsers`

**Method** : `GET`

**Auth required** : YES (auth-key and auth-secret in headers)

## Request body

No body.

## Success Response

**Code** : `200 OK`

**Content examples**

```json
[
    {
        "Id": 9295,
        "FirstName": "Test",
        "LastName": "Testeson",
        "Email": "test@trackado.com",
        "PhoneNumber": "123123123123123"
    },
]
```
