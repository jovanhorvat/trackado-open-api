# Get custom fields for company

Get the custom fields for the specific company.

**URL** : `/api/v2/customfieldapi/GetCustomFields`

**Method** : `GET`

**Auth required** : YES (auth-key and auth-secret in headers)

## Request body

No body.

## Success Response

**Code** : `200 OK`

**Notes**: 
Custom field can be of type:
```json
Text = 0,
Dropdown = 1,
MultiSelectDropdown = 2,
Date = 3,
Number = 4
```

Only the dropdown and multi select dropdown fields contain values in the options array since they are fields with pre-set values that the user can choose from.
IsHidden field shows if the field is hidden by the administrator.

**Content examples**

```json
[
    {
        "Id": 9219,
        "Name": "Sample Text Field",
        "IsHidden": false,
        "Type": {
            "Type": 0,
            "TypeValue": "Text"
        },
        "Options": []
    },
    {
        "Id": 9220,
        "Name": "Sample Dropdown Field",
        "IsHidden": false,
        "Type": {
            "Type": 1,
            "TypeValue": "Dropdown"
        },
        "Options": [
            "Option 1",
            "Option 2",
            "Sample Dropdown Field",
            "This did not exist",
            "Option 3",
            "Option 4"
        ]
    },
    {
        "Id": 9229,
        "Name": "qwe",
        "IsHidden": false,
        "Type": {
            "Type": 1,
            "TypeValue": "Dropdown"
        },
        "Options": [
            "test",
            "qwe"
        ]
    },
    {
        "Id": 9230,
        "Name": "test-field-test",
        "IsHidden": true,
        "Type": {
            "Type": 0,
            "TypeValue": "Text"
        },
        "Options": []
    },
    {
        "Id": 9231,
        "Name": "Agreement",
        "IsHidden": false,
        "Type": {
            "Type": 0,
            "TypeValue": "Text"
        },
        "Options": []
    },
    {
        "Id": 9232,
        "Name": "Tester",
        "IsHidden": false,
        "Type": {
            "Type": 0,
            "TypeValue": "Text"
        },
        "Options": []
    },
    {
        "Id": 9233,
        "Name": "DateFIELD",
        "IsHidden": false,
        "Type": {
            "Type": 3,
            "TypeValue": "Date"
        },
        "Options": []
    },
    {
        "Id": 9234,
        "Name": "TestMULTI",
        "IsHidden": false,
        "Type": {
            "Type": 2,
            "TypeValue": "MultiSelectDropdown"
        },
        "Options": [
            "test",
            "TestMULTI",
            "ABABA",
            "HAHA"
        ]
    },
    {
        "Id": 9244,
        "Name": "Num field",
        "IsHidden": false,
        "Type": {
            "Type": 4,
            "TypeValue": "Number"
        },
        "Options": []
    }
]
```
