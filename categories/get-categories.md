# Get categories for company

Get the categories for the specific company.

**URL** : `/api/v2/categoryapi/GetCategories`

**Method** : `POST`

**Auth required** : YES (auth-key and auth-secret in headers)

## Request body

No body.

## Success Response

**Code** : `200 OK`

**Content examples**

```json
[
    {
        "Id": 12971,
        "Name": "Application"
    },
    {
        "Id": 12969,
        "Name": "Claims"
    }
]
```
