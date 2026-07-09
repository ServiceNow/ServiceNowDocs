---
title: Data required for invoice processing
description: Reference information for the key tables and required data used to process invoices in Accounts Payable Operations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/accounts-payable-operations/master-data-table-apo.html
release: zurich
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

-   [Purchase order](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/purchase-order-table.md)
-   [Purchase order lines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/purchase-order-lines.md)
-   [Supplier](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/supplier.md)
-   [Supplier Legal Entity Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/supplier-legal-entity-mapping.md)
-   [Supplier contact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/supplier-contact.md)
-   [Legal entity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/legal-entity.md)
-   [Cost center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/cost-center.md)
-   [Ledger account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/ledger-account.md)
-   [Payment terms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/payment-terms.md)
-   [Tax code fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/create-tax-code-fields.md)
-   [Tax type fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/tax-type-fields.md)
-   [Organization tax details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/organization-tax-details.md)

-   **[Cost center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/cost-center.md)**  
Cost centers are a commonly used reference between financial systems and IT. Cost center records represent business entities and have a related list of CI Cost Center Relationships that measure the cost center's consumption of business services.
-   **[Tax code fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/create-tax-code-fields.md)**  
As a Tax manager, you can create tax codes to be applied in an invoice.
-   **[Legal entity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/legal-entity.md)**  
View the legal entity corresponding to a purchase.
-   **[Ledger account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/ledger-account.md)**  
A reference field for the account used to generate the  invoice.​
-   **[Organization tax details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/organization-tax-details.md)**  
Accounts Payable specialist uses the organization tax table to view the supplier's tax registration details.
-   **[Payment terms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/payment-terms.md)**  
Specify the terms and conditions that apply to customers while paying for an invoice. These are usually imposed by suppliers during the purchase.
-   **[Purchase order](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/purchase-order-table.md)**  
A purchase order is a binding contract between a buyer and a supplier that authorizes a purchasing transaction. It contains the descriptions, quantities, prices, applicable discounts, payment terms, delivery dates, and other associated terms and conditions with the supplier.
-   **[Purchase order lines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/purchase-order-lines.md)**  
Purchase order lines provide information of the individual lines under a purchase requisition or a sourcing request for the referenced supplier.
-   **[Supplier](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/supplier.md)**  
You can add a supplier to the primary data and add products related to that supplier. The supplier data is managed effortlessly and enhance productivity of the teams that engage with suppliers.
-   **[Supplier Legal Entity Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/supplier-legal-entity-mapping.md)**  
The linking of supplier registered legal entity to the customer's corresponding legal entity within APO is referred as Supplier legal entity mapping. Mapping ensures that invoices, purchase orders, and payments are correctly routed, validated, and processed across systems.
-   **[Supplier contact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/supplier-contact.md)**  
You can add the supplier contacts allowing them to access the  Supplier Collaboration Portal  and start working on the most important tasks. You can view information about the supplier contacts and also indicates which user is the primary contact.
-   **[Tax type fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/tax-type-fields.md)**  
As a Tax manager, you can create tax types to be applied to an invoice.

**Parent Topic:**[Accounts Payable Operations reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/acc-pay-reference.md)

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

