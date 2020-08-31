# Upload file for contract

Add contract file to the specific company.

**URL** : `/Files/Upload`

**Method** : `POST`

**Auth required** : YES (auth-key and auth-secret in headers)

## Request body (form-data)

```json
file: byte[],
description: "description of the file"
```


## Success Response

**Code** : `200 OK`

**Content examples**

Id of the created contract link and it's name

```json
{
    "Id": 18577,
    "Message": "hard-delete-company-changes.txt"
}
```
