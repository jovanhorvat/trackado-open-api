# TRACKADO OPEN API

## Endpoints that require Authentication

Closed endpoints require a valid auth-key and auth-secret to be included in the headers of the
request.

## Authentication

Every request needs to come with authentication key and secret authentication key, that are company specific and generated by the app.

### Business partner endpoints

Each endpoint manipulates or displays information related to the Business partner, specified by the user.

* [List business partners](business-partners/list-business-partners.md) : `POST /api/v2/businesspartnersapi/List`
* [Add business partner](business-partners/add-business-partner.md) : `POST` `/api/v2/businesspartnersapi/add`
* [Update business partner](business-partners/update-business-partner.md) : `POST` `/api/v2/businesspartnersapi/update`
* [Delete business partner](business-partners/delete-business-partner.md) : `POST` `/api/v2/businesspartnersapi/delete?id=xxxxx`

### Category endpoints

Each endpoint manipulates or displays information related to the Category, specified by the user.

* [List categories](categories/get-categories.md) : `GET /api/v2/categoryapi/GetCategories`

### Business unit endpoints

Each endpoint manipulates or displays information related to the Business unit, specified by the user.

* [List business units](business-units/get-business-units.md) : `GET /api/v2/businessunitapi/GetBusinessunits`

### Organizational unit endpoints

Each endpoint manipulates or displays information related to the Organizational unit, specified by the user.

* [List organization units](organization-units/get-organization-units.md) : `GET /api/v2/organizationunitapi/GetOrganizationalUnits`

### Users endpoints

Each endpoint manipulates or displays information related to the Users, specified by the user.

* [List users](users/get-users.md) : `GET /api/v2/usersapi/GetUsers`

### Custom fields endpoints

Each endpoint manipulates or displays information related to the Custom fields, specified by the user.

* [List custom fields](custom-fields/get-custom-fields.md) : `GET /api/v2/customfieldapi/GetCustomFields`

### Contract endpoints

Each endpoint manipulates or displays information related to the contracts, specified by the user.

* [List contracts](contracts/list-contracts.md) : `POST` `/api/v2/contractapi/List`
* [Add contract](contracts/add-contract.md) : `POST` `/api/v2/contractapi/Add`
* [Update contract](contracts/update-contract.md) : `POST` `/api/v2/contractapi/Update`
* [Delete contract](contracts/delete-contract.md) : `POST` `/api/v2/contractapi/Delete?Id=xxxxx`
* [Add contract to inbox](contracts/add-contract-to-inbox.md) : `POST` `/api/v2/contractapi/AddContractToInbox`

### Contract billing transactions endpoints

Each endpoint manipulates or displays information related to the contract billing transactions, specified by the user.
Each endpoint manipulates or displays information related to the contract billing transactions, specified by the user.

* [List billing transactions](transaction-billings/list-transactions.md) : `POST` `/api/v2/contractapi/List`
* [Delete billing transaction](transaction-billings/delete-transaction.md) : `POST` `/api/v2/contractapi/Add`
* [Update billing transcation](transaction-billings/update-transaction.md) : `POST` `/api/v2/contractapi/Update`
* [Delete billing transcation](transaction-billings/delete-transaction.md) : `POST` `/api/v2/contractapi/Delete?Id=xxxxx`
* [List exchange rates](transaction-billings/get-exchange-rates.md) : `GET` `/api/v2/contracttransactionsapi/getexchangerates`

### General endpoints

Each endpoint manipulates or displays information related to the general state of the application.

* [Get countries](general/get-countries.md) : `GET` `/api/v2/generalapi/GetCountries`
