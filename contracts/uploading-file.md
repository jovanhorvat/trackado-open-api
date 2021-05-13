# Upload file for contract

Add contract file to the specific company.

**URL** : `/Files/Upload`

**Method** : `POST`

**Auth required** : YES (auth-key and auth-secret in headers)

## Request body (form-data)

```json
fileName: byte[],
description: "description of the file",
contractId: 29204
```


## Success Response

**Code** : `200 OK`

**Content examples**

Id of the created contract link and it's name

```json
{
    "Id": 19049,
    "Name": "post-request-email.txt",
    "Description": "",
    "ContractId": 29204
}
```
