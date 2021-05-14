# Add contract

Add contract draft to the inbox of a specific company.

**URL** : `/api/v2/contractapi/AddContractToInbox`

**Method** : `POST`

**Auth required** : YES (auth-key and auth-secret in headers)

## Request body (form-data)

*For the property "Status" refer to the [Contract Status enum](./enums/contract-status.md)*<br>
*For the property "LifecycleType" refer to the [Lifecycle Type enum](./enums/lifecycle-type.md)*<br>
*For the property "EndDateHandling" refer to the [End Date Handling enum](./enums/end-date-handling.md)*<br>
*For the property "NoticeTermType" refer to the [Time Period enum](./enums/time-period.md)*<br>
*For the property "ProlongationPeriodType" refer to the [Time Period enum](./enums/time-period.md)*<br>
*For the property "LifecycleFixedPeriodType" refer to the [Lifecycle Fixed Period Type enum](./enums/lifecycle-fixed-period-type.md)*<br>

*Title is the only required field*
*All entity related fields should be filled with the name of the entity that already exists for the specific company*
*All correctly attached files to the form-data will be processed and attached to the contract draft*

```json
{
  "Title": "test-contract-draft",
  "Description": "test-contract-description",
  "ContractOwners": ["contract-owner-email-from-existing-user-entity", "contract-owner-email-from-existing-user-entity"] (serialized array),
  "BusinessPartners": ["business-partner-name-from-existing-business-partner-entity", "business-partner-name-from-existing-business-partner-entity"] (serialized array),
  "CategoryName": "category-name-from-existing-category-entity",
  "ContractNumber": "contract-number",
  "LifecycleType": 0,
  "ContractLifecycleStartDate": "2020-08-13",
  "ContractLifecycleEndDate": "2020-08-15",
  "NoticeTermPeriodAmount": 2,
  "NoticeTermPeriodType": 0,
  "ProlongationPeriodAmount": 2,
  "ProlongationPeriodType": 0,
  "EndDateHandling": 0,
  "BusinessUnitName": "business-unit-name-from-existing-business-unit-entity",
  "OrganizationalUnitName": "organizational-unit-name-from-existing-organizational-unit-entity",
  "AdditionalContactPerson": "additional-contact-person-test",
  "Status": 0
};
```

## Success Response

**Code** : `200 OK`

**Content examples**

Id of the created contract in the "Result" field

```json
{
    "CompanyId": 1,
    "UserId": 1,
    "Title": "test-contract-draft",
    "Description": "test-contract-description",
    "ImportSource": 2,
    "Status": 0,
    "ContractNumber": "contract-number",
    "ContractLifecycleStartDate": "2020-08-13T00:00:00.000Z",
    "ContractLifecycleEndDate": "2020-08-15T00:00:00.000Z",
    "AdditionalContactPerson": "additional-contact-person-test",
    "CategoryName": "category-name-from-existing-category-entity",
    "LifecycleType": 2,
    "BusinessPartners": [
        "business-partner-name-from-existing-business-partner-entity", "business-partner-name-from-existing-business-partner-entity"    ],
    "ContractOwners": [
        "contract-owner-email-from-existing-user-entity", "contract-owner-email-from-existing-user-entity"
    ],
    "OrganizationalUnitName": "organizational-unit-name-from-existing-organizational-unit-entity",
    "BusinessUnitName": "business-unit-name-from-existing-business-unit-entity",
    "NoticeTermPeriodAmount": 2,
    "NoticeTermPeriodType": 2,
    "ProlongationPeriodAmount": 1,
    "ProlongationPeriodType": 2,
    "EndDateHandling": 0,
    "ContractDraftAttachments": [
        {
            "Link": "https://trackadoteststorage.blob.core.windows.net/contracts/rsa-contract-draft-161-1MImDhM29ZOF0dvxZhgM-dummy-pdf.pdf",
            "ContractDraftId": 161,
            "Size": 13264,
            "Type": 0,
            "OriginalFileName": "dummy-pdf.pdf",
            "ObfuscatedFileName": null,
            "Description": null,
            "ContractDraft": null,
            "Id": 1,
            "CreatedOn": "2021-05-14T12:56:24.273Z"
        },
        {
            "Link": "https://trackadoteststorage.blob.core.windows.net/contracts/rsa-contract-draft-161-DjWiTAae8yqlD8eHLZUf-dummy-pdf.pdf",
            "ContractDraftId": 161,
            "Size": 13264,
            "Type": 0,
            "OriginalFileName": "dummy-pdf.pdf",
            "ObfuscatedFileName": null,
            "Description": null,
            "ContractDraft": null,
            "Id": 2,
            "CreatedOn": "2021-05-14T12:56:24.570Z"
        }
    ],
    "Initiator": null,
    "Id": 161,
    "CreatedOn": "2021-05-14T12:56:17.397Z"
}
```

