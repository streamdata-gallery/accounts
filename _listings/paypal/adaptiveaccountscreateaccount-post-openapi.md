---
swagger: "2.0"
x-collection-name: PayPal
x-complete: 0
info:
  title: Paypal Create Account
  description: The CreateAccount API operation enables you to create a PayPal account
    on behalf of a third party.
  version: 1.0.0
host: svcs.sandbox.paypal.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /AdaptiveAccounts/AddBankAccount:
    post:
      summary: Add Bank Account
      description: The AddBankAccount API operation lets your application set up bank
        accounts as funding sources for PayPal accounts.
      operationId: AdaptiveAccounts.AddBankAccount.post
      x-api-path-slug: adaptiveaccountsaddbankaccount-post
      responses:
        200:
          description: OK
      tags:
      - Payments
      - Bank Account
  /AdaptiveAccounts/AddPaymentCard:
    post:
      summary: Add Payment Card
      description: The AddPaymentCard API operation lets your application set up credit
        cards as funding sources for PayPal accounts.
      operationId: AdaptiveAccounts.AddPaymentCard.post
      x-api-path-slug: adaptiveaccountsaddpaymentcard-post
      responses:
        200:
          description: OK
      tags:
      - Payments
      - Credit Card
  /AdaptiveAccounts/CreateAccount:
    post:
      summary: Create Account
      description: The CreateAccount API operation enables you to create a PayPal
        account on behalf of a third party.
      operationId: AdaptiveAccounts.CreateAccount.post
      x-api-path-slug: adaptiveaccountscreateaccount-post
      parameters:
      - in: header
        name: X-PAYPAL-SANDBOX-EMAIL-ADDRESS
      responses:
        200:
          description: OK
      tags:
      - Payments
  /AdaptiveAccounts/GetUserAgreement:
    post:
      summary: Get User Agreement
      description: The GetUserAgreement API operation lets you retrieve the user agreement
        for the customer to approve the new PayPal account.
      operationId: AdaptiveAccounts.GetUserAgreement.post
      x-api-path-slug: adaptiveaccountsgetuseragreement-post
      responses:
        200:
          description: OK
      tags:
      - Payments
      - Aggreements
  /AdaptiveAccounts/GetVerifiedStatus:
    post:
      summary: Get Verified Status
      description: The GetVerifiedStatus API operation lets you check if a PayPal
        account status is verified. A PayPal account gains verified status under a
        variety of circumstances, such as when an account is linked to a verified
        funding source. Verified status serves to indicate a trust relationship. For
        more information about account verified status, refer to PayPal.com.
      operationId: AdaptiveAccounts.GetVerifiedStatus.post
      x-api-path-slug: adaptiveaccountsgetverifiedstatus-post
      responses:
        200:
          description: OK
      tags:
      - Payments
      - Verified
      - Status
  /AdaptiveAccounts/SetFundingSourceConfirmed:
    post:
      summary: Set Funding Source Confirmed
      description: The SetFundingSourceConfirmed API operation lets your application
        set up bank accounts as funding sources for PayPal accounts.
      operationId: AdaptiveAccounts.SetFundingSourceConfirmed.post
      x-api-path-slug: adaptiveaccountssetfundingsourceconfirmed-post
      responses:
        200:
          description: OK
      tags:
      - Payments
      - Verified
      - Status
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