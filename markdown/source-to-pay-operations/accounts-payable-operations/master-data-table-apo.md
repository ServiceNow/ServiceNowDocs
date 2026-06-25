---
title: Data required for invoice processing
description: Reference information for the key tables and required data used to process invoices in Accounts Payable Operations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/master-data-table-apo.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [APO, Accounts Payable Operations, invoice automation, AP automation, invoice processing]
breadcrumb: [Reference, Accounts Payable Operations, Finance and Supply Chain]
---

# Data required for invoice processing

Reference information for the key tables and required data used to process invoices in Accounts Payable Operations.

## Data required for invoice processing

Data in the following key tables should be populated for processing an invoice within Accounts Payable Operations.

-   [Purchase order](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/purchase-order-table.md)
-   [Purchase order lines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/purchase-order-lines.md)
-   [Supplier](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/supplier.md)
-   [Supplier Legal Entity Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/supplier-legal-entity-mapping.md)
-   [Supplier contact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/supplier-contact.md)
-   [Legal entity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/legal-entity.md)
-   [Cost center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/cost-center.md)
-   [Ledger account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/ledger-account.md)
-   [Payment terms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/payment-terms.md)
-   [Tax code fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/create-tax-code-fields.md)
-   [Tax type fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/tax-type-fields.md)
-   [Organization tax details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/organization-tax-details.md)

-   **[Purchase order](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/purchase-order-table.md)**  
Field descriptions for the purchase order record in the \[sn\_shop\_purchase\_order\] table used for reviewing or completing purchase order details for invoice processing.
-   **[Purchase order lines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/purchase-order-lines.md)**  
Field descriptions for the \[sn\_shop\_purchase\_order\_line\] table, which stores individual line items under a purchase requisition or sourcing request.
-   **[Supplier](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/supplier.md)**  
Field descriptions for the \[sn\_fin\_supplier\] table used to manage supplier records and associated products in primary data.
-   **[Supplier Legal Entity Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/supplier-legal-entity-mapping.md)**  
Field descriptions for the Supplier Legal Entity Mapping table in APO, which links supplier and customer legal entities to route invoices, purchase orders, and payments correctly.
-   **[Supplier contact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/supplier-contact.md)**  
Field descriptions for the \[vm\_vdr\_contact\] table, which stores supplier contact details used in the Supplier Collaboration Portal.
-   **[Legal entity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/legal-entity.md)**  
Field descriptions for the \[sn\_fin\_legal\_entity\] table, which stores internal legal entities that request purchases.
-   **[Cost center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/cost-center.md)**  
Field descriptions for the Cost Center \[cmn\_cost\_center\] table used to create and manage cost center records that link financial systems to IT services.
-   **[Ledger account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/ledger-account.md)**  
Field descriptions for the \[sn\_fin\_gl\_account\] table, which stores ledger account data fetched from an ERP system, and used when viewing or updating general ledger account records associated with invoice generation.
-   **[Payment terms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/payment-terms.md)**  
Field descriptions for the \[sn\_shop\_payment\_term\] table, which stores payment terms that apply to invoice transactions.
-   **[Tax code fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/create-tax-code-fields.md)**  
Field descriptions for the Tax code form used to create and review tax codes applied to invoices.
-   **[Tax type fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/tax-type-fields.md)**  
Field descriptions for the Tax type form used to define and apply tax types to invoices.
-   **[Organization tax details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/organization-tax-details.md)**  
Field descriptions for the organization tax table \[sn\_fin\_org\_tax\_detail\], which stores supplier tax registration details used when reviewing or configuring supplier tax information in Accounts Payable.

**Parent Topic:**[Accounts Payable Operations reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/acc-pay-reference.md)

**Related topics**  


[Accounts Payable Operations properties]()

[Create New Invoice Line form]()

[Create invoice cost allocation form]()

[Outbound cost allocation staging table]()

[Distribution set form]()

[Create New Invoice case form]()

[Create New Invoice task form]()

[Invoice processing case form]()

[Tax lines]()

[Invoice exception form]()

[Request Help form]()

[Invoice exception definition form]()

[Approval Rule form]()

[Approval Plan form]()

[Accounts Payable Operations glossary]()

