# Add contract transaction billing

Add contract transaction billing to the specific company.

**URL** : `api/v2/contracttransactionsapi/addtransaction`

**Method** : `POST`

**Auth required** : YES (auth-key and auth-secret in headers)

## Request body

```json
    ExchangeRateId is an optional field
```

```json
    BillingCycle:
        OneTime = 0,
        Monthly = 1,
        Quarterly = 2,
        Yearly = 3,
        HalfYearly = 4
```

```json
    BillingType:
        Cost = 0,
        Revenue = 1
```

```json
{
    "ContractId": xxxx,
    "BillingCycle": 0,
    "BillingAmount": 200,
    "FirstBillingDate": "2020-02-02",
    "LastBillingDate": "2020-04-01",
    "Description": "My billing transaction",
    "ExchangeRateId": 1
}
```


## Success Response

**Code** : `200 OK`

**Content examples**

Id of the created contract billing

```json
"Id": xxxx
```
