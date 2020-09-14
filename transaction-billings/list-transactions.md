# List contracts

Get the contracts billings for the specific company.

**URL** : `/api/v2/contracttransactionsapi/listtransactions`

**Method** : `POST`

**Auth required** : YES (auth-key and auth-secret in headers)

## Request body

Getting contract billings requires the user to specify the Page and PageSize. Page size needs to be a number between 1-100.

```json
{
    "Page": 1,
    "PageSize": 25
}
```


## Success Response

**Code** : `200 OK`

**Content examples**

List from a database - Count represents the number of ALL (no matter the page size specified) contract billing objects in the database relating to the company

```json
{
    "ContractBillings": [
        {
            "BillingAmount": 386500.0000,
            "BillingType": 0,
            "BillingCycle": 0,
            "Description": "One-off Consultancy agreement",
            "FirstBillingDate": "2019-07-15T00:00:00",
            "LastBillingDate": "9999-12-31T00:00:00",
            "TransactionAmount": 0.0,
            "ExchangeRateId": null,
            "Id": 10108
        },
        {
            "BillingAmount": 8000.0000,
            "BillingType": 0,
            "BillingCycle": 0,
            "Description": "Services Agreement - P&C Development Workshop",
            "FirstBillingDate": "2019-12-01T00:00:00",
            "LastBillingDate": "9999-12-31T00:00:00",
            "TransactionAmount": 0.0,
            "ExchangeRateId": null,
            "Id": 10109
        }
    ],
    "Count": 174
}
```
