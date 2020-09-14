# Delete contract transaction billing

Delete contract transaction billing.

**URL** : `/api/v2/contracttransactionsapi/deletetransaction?contractBillingId=xxxx&contractId=xxxx`

**Method** : `POST`

**Auth required** : YES (auth-key and auth-secret in headers)

Request query parameters
contractBillingId - the id of the billing
contractId - the id of the contract

## Success Response

**Code** : `200 OK`

**Content examples**

Id of the deleted contract billing

```json
"Id": xxxx
```
