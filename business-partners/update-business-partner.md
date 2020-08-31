# Update business partners

Update the business partner for the specific company.

**URL** : `/api/v2/businesspartnersapi/update`

**Method** : `POST`

**Auth required** : YES (auth-key and auth-secret in headers)

## Request body

Any changed properties that are being left out will default to null or empty string.

```json
{
    "Id": 15398,
    "Name": "test"
}
```


## Success Response

**Code** : `200 OK`

**Content examples**

Updated business partner response body.

```json
{
    "Id": 15398,
    "Name": "test",
    "Address": "",
    "City": "",
    "Email": "",
    "Phone": "",
    "FiscalInformation": "",
    "VATNumber": ""
}
```
