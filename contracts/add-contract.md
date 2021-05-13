# Add contract

Add contract to specific company.

**URL** : `/api/v2/contractapi/Add`

**Method** : `POST`

**Auth required** : YES (auth-key and auth-secret in headers)

## Request body

*For the property "Status" refer to the [Contract Status enum](./enums/contract-status.md)*
*For the property "LifecycleType" refer to the [Lifecycle Type enum](./enums/lifecycle-type.md)*
*For the property "EndDateHandling" refer to the [End Date Handling enum](./enums/end-date-handling.md)*
*For the property "NoticeTermType" refer to the [Time Period enum](./enums/time-period.md)*
*For the property "ProlongationPeriodType" refer to the [Time Period enum](./enums/time-period.md)*
*For the property "LifecycleFixedPeriodType" refer to the [Lifecycle Fixed Period Type enum](./enums/lifecycle-fixed-period-type.md)*

```json
{
    "Title": "Test contract",
    "Number": "Test number",
    "Description": "Test description",
    "Status": 1 [Contract Status enum values](./enums/contract-status.md),
    "BusinessPartnerIds": [12322, 12321],
    "BusinessUnitId": 7277,
    "CompanyId": 8189,
    "ContractLifecycle": {
        "StartDate": "2020-08-13",
        "EndDate": "2020-08-13",
        "LifecycleType": 0,
        "EndDateHandling": 0,
        "NoticeTermAmount": 1,
        "NoticeTermType": 0,
        "ProlongationPeriodAmount": 1,
        "ProlongationPeriodType": 0,
        "LifecycleFixedPeriodType": 0
    },
    "ContractOrganization": {
        "AdditionalContractPerson": "jovan",
        "ContractOwnerIds": [9282],
        "OrganizationUnitId": 11952
    },
    "ContractBillings": [
        {
            "BillingCycle": 0,
            "BillingAmount": 1000.0,
            "FirstBillingDate": "2020-01-01",
            "LastBillingDate": "2020-03-03",
            "BillingType": 0,
            "Description": "test billing"
        }
    ],
    "CustomFields": [
        {
            "CustomFieldId": 9234,
            "Type": 2,
            "Values": ["test", "ABABA"]
        },
        {
            "CustomFieldId": 9244,
            "Type": 4,
            "Value": 20
        }
    ],
    "AttachmentIds": [
        18576
    ],
    "ContractLinks": [
        {
            "Link": "https://test.com",
            "Description": "description"
        }
    ]
}

```

## Success Response

**Code** : `200 OK`

**Content examples**

Id of the created contract in the "Result" field

```json
{
    "Result": 30270,
    "IsFaulted": false,
    "IsSystemFault": false,
    "ErrorMessages": []
}
```


