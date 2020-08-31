# Add business partner

Add business partner to the specific company.

**URL** : `/api/v2/businesspartnersapi/add`

**Method** : `POST`

**Auth required** : YES (auth-key and auth-secret in headers)

## Request body

```json
{
    "Name": "test business partner 222",
    "Address": "test address",
    "PostalCode": "1000",
    "City": "Skopje",
    "Website": "trackado.com",
    "ContactPerson": "tester",
    "Email": "trackado@trackado.com",
    "Phone": "20432430",
    "FiscalInformation": "fiscal info test",
    "VATNumber": "test123"
}
```


## Success Response

**Code** : `200 OK`

**Content examples**

Id of the created business partner and his parameters

```json
{
    "Id": 1,
    "Name": "test business partner",
    "Address": "test address",
    "PostalCode": "1000",
    "City": "Skopje",
    "Website": "trackado.com",
    "ContactPerson": "tester",
    "Email": "test@test.com",
    "Phone": "20432430",
    "FiscalInformation": "fiscal info test",
    "VATNumber": "test123"
}
```
