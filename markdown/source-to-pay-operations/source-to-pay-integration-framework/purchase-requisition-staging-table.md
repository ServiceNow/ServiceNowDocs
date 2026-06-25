---
title: Purchase Requisition staging table
description: The Purchase requisition \[sn\_spend\_intg\_purchase\_requisition\] staging table temporarily stores important data about purchase requests before this data is sent to the primary table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/purchase-requisition-staging-table.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Inbound staging tables Sourcing Procurement, Inbound staging tables, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
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

**Parent Topic:**[Inbound staging tables for Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/spo-inbound-staging-tables.md)

**Related topics**  


[CMDB Model Category Stage inbound staging table]()

[CMDB Service Model Stage inbound staging table]()

[CMN Location Stage inbound staging table]()

[Catalog Import staging table]()

[Catalog Error staging table]()

[Cost Center Stage inbound staging table]()

[Department Stage inbound staging table]()

[ERP Plant Address Mapping Stage inbound staging table]()

[FX Currency Stage inbound staging table]()

[FX Rate Stage inbound staging table]()

[Fixed asset details stage inbound table]()

[GL Account Stage inbound staging table]()

[Import Availability Updates inbound staging table]()

[Availability Error staging table]()

[Cost Allocation inbound staging table \(Deprecated\)]()

[Invoice inbound staging table]()

[Purchase Order inbound staging table]()

[Purchase Order Line inbound staging table]()

[Receipt inbound staging table]()

[Legal Entity Stage inbound staging table]()

[Office Location Stage inbound staging table]()

[Order Acknowledgement staging table]()

[Order Acknowledgement Error staging table]()

[Payment Terms Stage inbound staging table]()

[Price Import staging table]()

[Price Error outbound staging table]()

[Product Model Stage inbound staging table]()

[Purchase Entity Stage inbound staging table]()

[Purchase Line Stage inbound staging table]()

[Spend Shipment Import inbound staging table]()

[Shipment Error staging table]()

[Supplier Product Stage inbound staging table]()

[Third Party Sourcing Registration staging table]()

[Third Party Unit Mapping staging table]()

[Third Party Unit staging table]()

[Unit of Measure inbound staging table]()

