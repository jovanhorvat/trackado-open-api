# List business partners

Get the business partners for the specific company.

**URL** : `api/v2/businesspartnersapi/List`

**Method** : `POST`

**Auth required** : YES (auth-key and auth-secret in headers)

## Request body

Getting business partners requires the user to specify the Page and PageSize. Page size needs to be a number between 1-100.

```json
{
    "Page": 1,
    "PageSize": 100
}
```


## Success Response

**Code** : `200 OK`

**Content examples**

List from a local database - BusinessPartnersCount represents the number of business partner objects in the database relating to the company

```json
{
    "BusinessPartners": [
        {
            "Id": 12855,
            "Name": "Testadr",
            "Address": "E123",
            "City": "Australia",
            "Email": "",
            "Phone": "",
            "FiscalInformation": "Q123",
            "VATNumber": ""
        }
     ],
    "BusinessPartnersCount": 118
}
```
