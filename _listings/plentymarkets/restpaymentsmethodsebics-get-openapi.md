---
swagger: "2.0"
x-collection-name: Plentymarkets
x-complete: 0
info:
  title: Plentymarkets Get EBICS Accounts
  description: Get ebics accounts.
  contact:
    name: plentymarkets
    url: https://forum.plentymarkets.com/c/rest-api
  version: 1.0.0
host: example.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /rest/accounting/locations/existing_accounts:
    get:
      summary: Get all unique posting accounts
      description: Get all unique posting accounts.
      operationId: getRestAccountingLocationsExistingAccounts
      x-api-path-slug: restaccountinglocationsexisting-accounts-get
      responses:
        200:
          description: OK
      tags:
      - Unique
      - Posting
      - Accounts
  /rest/accounting/locations/posting_accounts:
    get:
      summary: Get all posting accounts
      description: Get all posting accounts.
      operationId: getRestAccountingLocationsAddingAccounts
      x-api-path-slug: restaccountinglocationsposting-accounts-get
      responses:
        200:
          description: OK
      tags:
      - Posting
      - Accounts
    post:
      summary: Save posting accounts
      description: Save posting accounts.
      operationId: postRestAccountingLocationsAddingAccounts
      x-api-path-slug: restaccountinglocationsposting-accounts-post
      responses:
        200:
          description: OK
      tags:
      - Save
      - Posting
      - Accounts
  /rest/accounting/locations/{locationId}/debtor_accounts/{mode}:
    get:
      summary: Lists the debtor accounts by mode.
      description: Lists the debtor accounts of an accounting location by mode. The
        ID of the accounting location and the mode have to be specified.
      operationId: getRestAccountingLocationsLocationDebtorAccountsMode
      x-api-path-slug: restaccountinglocationslocationiddebtor-accountsmode-get
      parameters:
      - in: path
        name: locationId
      - in: path
        name: mode
      responses:
        200:
          description: OK
      tags:
      - Lists
      - Debtor
      - Accounts
      - By
      - Mode
  /rest/accounting/locations/{locationId}/posting_accounts:
    get:
      summary: Get all posting accounts by locationId
      description: Get all posting accounts by locationid.
      operationId: getRestAccountingLocationsLocationAddingAccounts
      x-api-path-slug: restaccountinglocationslocationidposting-accounts-get
      parameters:
      - in: path
        name: locationId
      responses:
        200:
          description: OK
      tags:
      - Posting
      - Accounts
      - By
      - LocationId
  /rest/accounting/locations/{locationId}/{type}/posting_accounts:
    get:
      summary: Get all posting accounts by locationId and type
      description: Get all posting accounts by locationid and type.
      operationId: getRestAccountingLocationsLocationTypeAddingAccounts
      x-api-path-slug: restaccountinglocationslocationidtypeposting-accounts-get
      parameters:
      - in: path
        name: locationId
      - in: path
        name: type
      responses:
        200:
          description: OK
      tags:
      - Posting
      - Accounts
      - By
      - LocationId
      - Type
  /rest/accounts:
    get:
      summary: List accounts
      description: List accounts.
      operationId: getRestAccounts
      x-api-path-slug: restaccounts-get
      parameters:
      - in: query
        name: createdAt
        description: Filter that restricts the search result to accounts that were
          created according to given filters
      - in: query
        name: updatedAt
        description: Filter that restricts the search result to accounts that were
          updated according to given filters
      responses:
        200:
          description: OK
      tags:
      - List
      - Accounts
  /rest/accounts/contacts/{contactId}/banks:
    get:
      summary: List bank accounts
      description: Lists bank accounts of the contact. The ID of the contact must
        be specified.
      operationId: getRestAccountsContactsContactBanks
      x-api-path-slug: restaccountscontactscontactidbanks-get
      parameters:
      - in: path
        name: contactId
      responses:
        200:
          description: OK
      tags:
      - List
      - Bank
      - Accounts
  /rest/items/sales_prices/{id}/accounts:
    get:
      summary: List referrer accounts
      description: Lists all activated referrer accounts of a sales price.
      operationId: getRestItemsSalesPricesAccounts
      x-api-path-slug: restitemssales-pricesidaccounts-get
      parameters:
      - in: path
        name: id
      responses:
        200:
          description: OK
      tags:
      - List
      - Referrer
      - Accounts
  /rest/payments/methods/ebics:
    get:
      summary: Get EBICS Accounts
      description: Get ebics accounts.
      operationId: getRestPaymentsMethodsEbics
      x-api-path-slug: restpaymentsmethodsebics-get
      responses:
        200:
          description: OK
      tags:
      - EBICS
      - Accounts
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---