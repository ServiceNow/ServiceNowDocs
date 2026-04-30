---
title: Purchase Requisition staging table
description: The Purchase requisition \[sn\_spend\_intg\_purchase\_requisition\] staging table temporarily stores important data about purchase requests before this data is sent to the primary table.
locale: en-US
release: zurich
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Inbound staging tables for Sourcing and Procurement Operations, Inbound staging tables, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Purchase Requisition staging table

The Purchase requisition \[sn\_spend\_intg\_purchase\_requisition\] staging table temporarily stores important data about purchase requests before this data is sent to the primary table.

|Field|Data type|Description|
|-----|---------|-----------|
|Accounting period|String|Financial period during which expenses related to the purchase requisition are recorded.|
|Actual end|String|End date of a purchase requisition \(PR\) process.|
|Actual start|String|Start date or initiation date of a purchase requisition \(PR\) process.|
|Additional comments|String|Supplementary information or notes added to a purchase requisition \(PR\).|
|After the fact|String|Actions or processes related to a purchase requisition \(PR\) that are handled or documented after a requisition is approved.|
|Assigned to|String|Individual or department responsible for reviewing, approving, and processing the purchase requisition \(PR\).|
|Assignment group|String|Team responsible for managing a Purchase Requisition \(PR\) within an organization.|
|Business owner|String|Individual or entity that has legal ownership and control over a business.|
|Cost center|String|Department, unit, or segment within an organization that is responsible for managing its own budget and expenses related to purchase requisitions.|
|Description|String|Description of the purchase requisition.|
|ERP Source|String|It is a field or attribute associated with a purchase requisition that indicates the specific ERP module, system, or process from which the requisition was generated.|
|Group Id|String|Unique identifier assigned to a group of purchase requisitions. This identifier groups together related requisitions for easier management, tracking, and processing.|
|Handling fee|String|Additional charge associated with the processing of a Purchase Requisition \(PR\).|
|Legal entity|String|Legal entity within an organization that is responsible for the purchase requisition.|
|Location|String|Location of the legal entity.|
|Number|String|Unique identifier assigned to a purchase requisition document within the procurement system.|
|Order type|String|Classification of orders based on their nature, purpose, or processing requirements.|
|Payment term|String|Specific terms and conditions under which payment is to be made for the goods or services requested in a Purchase Requisition \(PR\).|
|Preferred currency|String|Currency that is preferred or required for processing a Purchase Requisition \(PR\).|
|Primary contact|String|Individual responsible for managing the Purchase Requisition \(PR\) process.|
|Priority|String|Level of urgency assigned to a Purchase Requisition \(PR\) within an organization's procurement process.|
|Purchase|String|Purchase order associated with the purchase requisition.|
|Purchase order|String|Official purchase order issued to the supplier.|
|Purchasing entity|String|Organization or department that is responsible for procurement of goods or services within a company.|
|Requested delivery|String|Date by which the requester of a purchase requisition \(PR\) expects the goods or services to be delivered.|
|Requisition type|String|Classification of a purchase requisition based on the nature or purpose of the requested goods or services.|
|Short description|String|Brief description of the purchase order.|
|State|String|Current state of the purchase requisition.|
|Submitted by|String|Individual or entity that created the purchase requisition request.|
|Supplier|String|Vendor or supplier from whom the requested goods or services are intended to be purchased.|
|Total amount|String|Total cost or value of all items or services requested in a requisition.|
|Total estimated shipping|String|Estimated cost associated with the shipping of goods or services.|
|Total estimated tax|String|Estimated amount of tax applicable to the goods or services requested in a Purchase Requisition \(PR\).|

**Parent Topic:**[Inbound staging tables for Sourcing and Procurement Operations](../concept/spo-inbound-staging-tables.md)

**Related topics**  


[CMDB Model Category Stage inbound staging table](spo-prod-cate-inbound-table.md)

[CMDB Service Model Stage inbound staging table](spo-serv-mod-inbound-table.md)

[CMN Location Stage inbound staging table](spo-loc-inbound-table.md)

[Catalog Import staging table](catalog-import-staging-table.md)

[Catalog Error staging table](catalog-error.md)

[Cost Center Stage inbound staging table](spo-cost-center-inbound-table.md)

[Department Stage inbound staging table](spo-dept-inbound-table.md)

[ERP Plant Address Mapping Stage inbound staging table](spo-erp-plant-address-inbound-table.md)

[FX Currency Stage inbound staging table](spo-fx-currency-inbound-table.md)

[FX Rate Stage inbound staging table](spo-fx-rate-inbound-table.md)

[Fixed asset details stage inbound table](fixed-asset-details-stage-inbound-table.md)

[GL Account Stage inbound staging table](spo-gl-account-inbound-table.md)

[Import Availability Updates inbound staging table](spo-import-avail-inbound-table.md)

[Availability Error staging table](availability-error-staging-table.md)

[Cost Allocation inbound staging table \(Deprecated\)](spo-cost-alloc-inbound-table.md)

[Invoice inbound staging table](spo-inbound-invoice-table.md)

[Purchase Order inbound staging table](spo-inbound-pur-order-table.md)

[Purchase Order Line inbound staging table](spo-inbound-pol-table.md)

[Receipt inbound staging table](spo-inbound-receipt-table.md)

[Legal Entity Stage inbound staging table](spo-legal-entity-inbound-table.md)

[Office Location Stage inbound staging table](spo-office-loc-inbound-table.md)

[Order Acknowledgement staging table](order-acknowledgement-staging-table.md)

[Order Acknowledgement Error staging table](order-acknowledgement-error.md)

[Payment Terms Stage inbound staging table](spo-pay-terms-inbound-table.md)

[Price Import staging table](price-import-staging-table.md)

[Price Error outbound staging table](price-error-staging-table.md)

[Product Model Stage inbound staging table](spo-prod-mod-inbound-table.md)

[Purchase Entity Stage inbound staging table](spo-purch-entity-inbound-table.md)

[Purchase Line Stage inbound staging table](spo-purch-line-stage-inbound-table.md)

[Spend Shipment Import inbound staging table](spend-shipment-import-inbound-table.md)

[Shipment Error staging table](shipment-error-staging-table.md)

[Supplier Product Stage inbound staging table](spo-supp-prod-inbound-table.md)

[Third Party Sourcing Registration staging table](third-party-sourcing-registration-staging-table.md)

[Third Party Unit Mapping staging table](third-party-unit-mapping-staging-table.md)

[Third Party Unit staging table](third-party-unit-staging-table.md)

[Unit of Measure inbound staging table](unit-measure-inbound-staging-table.md)

