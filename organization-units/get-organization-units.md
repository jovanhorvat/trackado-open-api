# Get organization units for company

Get the organiaztional units for the specific company.

**URL** : `/api/v2/organizationunitapi/GetOrganizationalUnits`

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
        "Id": 11951,
        "Name": "Aftersales"
    },
    {
        "Id": 11952,
        "Name": "Development"
    }
]
```
