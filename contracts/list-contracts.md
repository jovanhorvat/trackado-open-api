# List contracts

Get the contracts for the specific company.

**URL** : `/api/v2/contractapi/List`

**Method** : `POST`

**Auth required** : YES (auth-key and auth-secret in headers)

## Request body

Getting contracts requires the user to specify the Page and PageSize. Page size needs to be a number between 1-100.

```json
{
    "Page": 1,
    "PageSize": 100
}
```


## Success Response

**Code** : `200 OK`

**Content examples**

List from a database - Count represents ALL (no matter the page size specified) of the contract objects in the database relating to the company

```json
[
  {
            "Id": 30272,
            "Title": "~~~~~!!!!!!!!TESTAMETESTERI",
            "Number": "qwe",
            "Description": "qwe",
            "ContractStatus": {
                "Status": 1,
                "Value": "Active"
            },
            "BusinessUnit": {
                "Id": 7275,
                "Name": "General",
                "Description": null
            },
            "MasterContract": {
                "Id": 0,
                "Title": "!!!!!!!!!fixer-period-without-renewal",
                "Number": null,
                "Description": null,
                "ContractStatus": {
                    "Status": 0,
                    "Value": "Draft"
                },
                "BusinessUnit": null,
                "MasterContract": null,
                "Category": null,
                "OrganizationalUnit": null,
                "ContractLifecycle": null,
                "BusinessPartners": [],
                "ContractOwners": [],
                "CustomFields": [],
                "ContractBillings": [],
                "ContractLinks": []
            },
            "Category": {
                "Id": 12971,
                "Name": "Application"
            },
            "OrganizationalUnit": {
                "Id": 11953,
                "Name": "Finance"
            },
            "ContractLifecycle": {
                "StartDate": "2020-07-28T00:00:00",
                "EndDate": "2020-09-05T00:00:00",
                "LifecycleType": 0,
                "EndDateHandling": 0,
                "NoticeTermAmount": 2,
                "NoticeTermType": 2,
                "ProlongationPeriodAmount": 5,
                "ProlongationPeriodType": 2,
                "DurationAmount": null,
                "DurationTermType": null,
                "LifecycleFixedPeriodType": null,
                "Id": 0,
                "CreatedOn": "2020-08-31T16:48:50.8397789Z"
            },
            "BusinessPartners": [
                {
                    "Id": 12314,
                    "Name": "Alan Whitelock Jones",
                    "Address": "",
                    "City": "",
                    "Email": "",
                    "Phone": "",
                    "FiscalInformation": "",
                    "VATNumber": ""
                }
            ],
            "ContractOwners": [
                {
                    "Id": 9282,
                    "FirstName": "jovan",
                    "LastName": "horvat",
                    "Email": null,
                    "PhoneNumber": null
                }
            ],
            "CustomFields": [
                {
                    "CompanyId": 0,
                    "CustomFieldId": 9219,
                    "Value": "yeee", - single value
                    "Values": null
                },
                {
                    "CompanyId": 0,
                    "CustomFieldId": 9234,
                    "Value": "[\"TestMULTI\",\"HAHA\"]", - multi select
                    "Values": null
                }
            ],
            "ContractBillings": [
                {
                    "BillingAmount": 2222.0000,
                    "BillingType": 0,
                    "BillingCycle": 0,
                    "Description": "2",
                    "FirstBillingDate": "2020-08-20T00:00:00",
                    "LastBillingDate": null,
                    "TransactionAmount": 0.0,
                    "Id": 0,
                    "CreatedOn": "2020-08-31T16:48:50.838781Z"
                }
            ],
            "ContractLinks": [
                {
                    "Link": "https://google.com",
                    "ContractId": null,
                    "Type": 1, - uploaded file
                    "WorkflowId": null,
                    "OriginalFileName": null,
                    "ObfuscatedFileName": null,
                    "Description": null
                },
                {
                    "Link": "",
                    "ContractId": null,
                    "Type": 0, - external file
                    "WorkflowId": null,
                    "OriginalFileName": "hard-delete-company-changes.txt",
                    "ObfuscatedFileName": null,
                    "Description": ""
                }
            ],
            "Count": 203
        },

```
