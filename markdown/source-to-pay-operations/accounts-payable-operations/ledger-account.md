---
title: Ledger account
description: A reference field for the account used to generate the  invoice.​
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/accounts-payable-operations/ledger-account.html
release: zurich
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Data required for invoice processing, Reference, Accounts Payable Operations, Finance and Supply Chain]
---

# Ledger account

A reference field for the account used to generate the  invoice.​

## sn\_fin\_gl\_account table

You can view records in any of the general ledger tables and make changes if necessary.

|Field|Data type|Description|
|-----|---------|-----------|
|Account Name|String|Display name of the ledger account fetched from ERP.|
|Currency|Reference|Currency that the expense is valued in.|
|Ledger account|String|Summarizes the transactions for reporting. Ledger account code fetched from ERP. Example: 160020.|
|Sub-ledger account|String|Detailed tracking for specific financial areas.|

**Parent Topic:**[Data required for invoice processing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/master-data-table-apo.md)

