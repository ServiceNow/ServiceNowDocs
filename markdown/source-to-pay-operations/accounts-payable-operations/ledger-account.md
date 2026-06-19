---
title: Ledger account
description: Field descriptions for the \[sn\_fin\_gl\_account\] table, which stores ledger account data fetched from an ERP system, and used when viewing or updating general ledger account records associated with invoice generation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/ledger-account.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [APO, Accounts Payable Operations, invoice automation, AP automation, invoice management]
breadcrumb: [Data required for invoice processing, Reference, Accounts Payable Operations, Finance and Supply Chain]
---

# Ledger account

Field descriptions for the \[sn\_fin\_gl\_account\] table, which stores ledger account data fetched from an ERP system, and used when viewing or updating general ledger account records associated with invoice generation.

## sn\_fin\_gl\_account table

You can view records in any of the general ledger tables and make changes if necessary.

|Field|Data type|Description|
|-----|---------|-----------|
|Account Name|String|Display name of the ledger account fetched from ERP.|
|Currency|Reference|Currency that the expense is valued in.|
|Ledger account|String|Ledger account code fetched from ERP. Example: 160020.|

**Parent Topic:**[Data required for invoice processing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/master-data-table-apo.md)

