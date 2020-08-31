# Get business units for company

Get the business units for the specific company.

**URL** : `/api/v2/businessunitapi/GetBusinessunits`

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
      "Id": 7283,
      "Name": "test-business-unit",
      "Description": "my-first-business-unit"
    },
    {
        "Id": 7284,
        "Name": "qwe1236",
        "Description": "55"
    }
]
```
