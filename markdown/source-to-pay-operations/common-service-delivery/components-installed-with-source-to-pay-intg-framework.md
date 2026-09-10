---
title: Components installed with Source-to-Pay Integration Framework
description: Several types of components are installed with the installation of the Source-to-Pay Integration Framework application, including tables and user roles.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/common-service-delivery/components-installed-with-source-to-pay-intg-framework.html
release: australia
product: Common Service Delivery
classification: common-service-delivery
topic_type: reference
last_updated: "2026-08-06"
reading_time_minutes: 5
breadcrumb: [Learn about FSC common applications, Common applications, Finance and Supply Chain applications, Finance and Supply Chain]
---

# Components installed with Source-to-Pay Integration Framework

Several types of components are installed with the installation of the Source-to-Pay Integration Framework application, including tables and user roles.

## Roles installed

<table id="table_u1t_gb1_wdc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Integration Admin\[sn\_spend\_intg.admin\]

</td><td>

Full administrative access to the Source-to-Pay Integration Framework application, including all outbound integration and tax integration records.

</td><td>

None

</td></tr><tr><td>

Procurement Integrator\[sn\_spend\_intg.procurement\_integrator\]

</td><td>

Access to create and process outbound procurement integration records exchanged with external third-party systems.

</td><td>

External User \[snc\_external\]

</td></tr></tbody>
</table>## Tables installed

<table id="table_fbz_45z_wdc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Availability Error\[sn\_spend\_intg\_availability\_error\]

</td><td>

Extends the Import Error table and stores the supplier part number for a failed availability import record.

</td></tr><tr><td>

Availability Import\[sn\_spend\_intg\_imp\_availability\]

</td><td>

Extends the Import Set Row table and stages inbound product availability data, including the supplier, catalog, part number, and available units, received from a third-party system.

</td></tr><tr><td>

Awarded Supplier Outbound Queue\[sn\_spend\_intg\_awarded\_supplier\_out\_queue\]

</td><td>

Stores the awarded supplier details for a sourcing request line, including the supplier number, quantity, integration status, and third-party RFx tool information, sent to an external sourcing tool.

</td></tr><tr><td>

Catalog Error\[sn\_spend\_intg\_catalog\_error\]

</td><td>

Extends the Import Error table and stores the supplier and manufacturer part numbers for a failed catalog import record.

</td></tr><tr><td>

Catalog Import\[sn\_spend\_intg\_imp\_catalog\]

</td><td>

Extends the Import Set Row table and stages inbound supplier catalog data, including product identifiers, category, pricing, and contract details, received from a third-party system.

</td></tr><tr><td>

Consolidated product\[sn\_spend\_intg\_consolidated\_product\]

</td><td>

Stores a supplier product consolidated with its third-party catalog product, including product category, model, pricing range, delivery time, and sourcing requirements.

</td></tr><tr><td>

Import Error\[sn\_spend\_intg\_import\_error\]

</td><td>

Stores the error message for a failed outbound integration record, with a reference to the corresponding outbound status record.

</td></tr><tr><td>

Order Acknowledgement\[sn\_spend\_intg\_imp\_purchase\_order\_ack\]

</td><td>

Extends the Import Set Row table and stages inbound purchase order and sales order acknowledgement data, including status codes and estimated arrival date, received from a supplier.

</td></tr><tr><td>

Order Acknowledgement Error\[sn\_spend\_intg\_order\_ack\_error\]

</td><td>

Extends the Import Error table and stores the sales order number and line number for a failed order acknowledgement record.

</td></tr><tr><td>

Outbound Cost Allocation\[sn\_spend\_intg\_outbound\_cost\_allocation\]

</td><td>

Stores the cost center, GL account, and allocation amount or percentage for a purchase or order line sent to an external ERP system.

</td></tr><tr><td>

Outbound Order\[sn\_spend\_intg\_outbound\_purchase\_order\]

</td><td>

Stores outbound purchase order details, including the order number, amount, supplier, legal entity, and integration status, sent to an external ERP system.

</td></tr><tr><td>

Outbound Order Line\[sn\_spend\_intg\_outbound\_purchase\_order\_line\]

</td><td>

References the Outbound Order table and stores the line-level product, quantity, pricing, and delivery details sent to an external ERP system.

</td></tr><tr><td>

Outbound Purchase Requisition\[sn\_spend\_intg\_outbound\_purchase\_requisition\]

</td><td>

Stores outbound purchase requisition details, including the requisition number, product, total amount, and integration status, sent to an external ERP system.

</td></tr><tr><td>

Outbound Receipt\[sn\_spend\_intg\_outbound\_receipt\]

</td><td>

Stores outbound receipt details, including the receipt number, quantity received, and purchase order line reference, sent to an external ERP system.

</td></tr><tr><td>

Outbound Status\[sn\_spend\_intg\_outbound\_status\]

</td><td>

Stores the status of outbound records sent to a third-party import set, including the state, status code, and status message returned by the supplier or customer system.

</td></tr><tr><td>

Price Break Stage\[sn\_spend\_intg\_price\_break\_stage\]

</td><td>

Extends the Import Set Row table and stages inbound price break data, including the quantity range, price, currency, and contract number, received from a third-party system.

</td></tr><tr><td>

Price Error\[sn\_spend\_intg\_price\_error\]

</td><td>

Extends the Import Error table and stores the supplier part number for a failed price import record.

</td></tr><tr><td>

Price Import\[sn\_spend\_intg\_imp\_price\]

</td><td>

Extends the Import Set Row table and stages inbound negotiated pricing and contract data for a supplier product, received from a third-party system.

</td></tr><tr><td>

Pricing Stage\[sn\_spend\_intg\_pricing\_stage\]

</td><td>

Extends the Import Set Row table and stages inbound contractual pricing data, including the contract number, price, and price type, for a supplier product.

</td></tr><tr><td>

Purchase Line Outbound\[sn\_spend\_intg\_purchase\_line\_outbound\]

</td><td>

Stores outbound purchase line details, including account assignment, cost center, supplier, and delivery location, sent to an external ERP system.

</td></tr><tr><td>

Purchase line stage\[sn\_spend\_intg\_purchase\_line\]

</td><td>

Extends the Import Set Row table and stages inbound purchase line data, including the supplier product, cost allocation, delivery location, and account assignment details.

</td></tr><tr><td>

Purchase requisition stage\[sn\_spend\_intg\_purchase\_requisition\]

</td><td>

Extends the Import Set Row table and stages inbound purchase requisition data, including the requisition type, supplier, business owner, and total amount.

</td></tr><tr><td>

S2P Integration outbound\[sn\_spend\_intg\_outbound\]

</td><td>

Stores outbound integration requests and responses exchanged with external systems, including the associated document, integration status, and ERP source.

</td></tr><tr><td>

Shipment Error\[sn\_spend\_intg\_shipment\_error\]

</td><td>

Extends the Import Error table and stores the supplier shipment number and sales order details for a failed shipment import record.

</td></tr><tr><td>

Shipment Import\[sn\_spend\_intg\_imp\_shipment\]

</td><td>

Extends the Import Set Row table and stages inbound shipment data, including the tracking number, carrier, delivery address, and shipment quantity, received from a supplier.

</td></tr><tr><td>

Sourcing Bid Stage\[sn\_spend\_intg\_sourcing\_bid\_stage\]

</td><td>

Extends the Import Set Row table and stages inbound supplier bid data for a sourcing request, including the quote price, supplier contact details, and delivery lead time.

</td></tr><tr><td>

Sourcing Event Outbound Queue\[sn\_spend\_intg\_ne\_out\_queue\]

</td><td>

Stores outbound negotiation event details, including the negotiation objectives, type, and integration status, sent to an external sourcing or negotiation tool.

</td></tr><tr><td>

Sourcing Inbound Stage\[sn\_spend\_intg\_inbound\_sourcing\_request\]

</td><td>

Extends the Import Set Row table and stages inbound sourcing request data, including the product model, category, and requested delivery dates, received from a third-party system.

</td></tr><tr><td>

Sourcing Line Outbound Queue\[sn\_spend\_intg\_prl\_out\_queue\]

</td><td>

References the Sourcing Outbound Queue table and stores the line-level supplier part number and integration status sent to an external sourcing tool.

</td></tr><tr><td>

Sourcing Outbound Queue\[sn\_spend\_intg\_sourcing\_out\_queue\]

</td><td>

References the Sourcing Event Outbound Queue table and stores outbound sourcing request details, including the product, quantity, budget, and delivery address, sent to an external sourcing tool.

</td></tr><tr><td>

Supplier Product Stage\[sn\_spend\_intg\_supplier\_product\_stage\]

</td><td>

Extends the Import Set Row table and stages inbound supplier product data, including the product model, category, accounting fields, and sourcing requirements.

</td></tr><tr><td>

Tax integration field mapping\[sn\_spend\_intg\_tax\_field\_map\]

</td><td>

Extends the Mapping Configuration table and stores the field, value, and JSON mappings used to translate transactions between ServiceNow and a target tax engine.

</td></tr><tr><td>

Tax integration staging\[sn\_spend\_intg\_tax\_staging\]

</td><td>

Stores tax integration requests and responses exchanged with an external tax engine, including the integration status and tax response status for each transaction.

</td></tr><tr><td>

Third party - API connections\[sn\_spend\_intg\_third\_party\_apis\]

</td><td>

References the Third-Party Registration table and stores the API endpoint URLs used to search products, retrieve order details, and place orders with a supplier.

</td></tr><tr><td>

Third party - cXML connections\[sn\_spend\_intg\_third\_party\_cxmls\]

</td><td>

References the Third-Party Registration table and stores the punchout start URL, order request URL, and inbound and outbound credentials used for a cXML punchout connection.

</td></tr><tr><td>

Third-Party Catalog\[sn\_spend\_intg\_third\_party\_catalog\]

</td><td>

Stores third-party supplier catalog data, including the product identifiers, category, unit of measure, negotiated price, and available countries.

</td></tr><tr><td>

Third-Party Category\[sn\_spend\_intg\_third\_party\_category\]

</td><td>

References the Third-Party Registration and CMDB Model Category tables and maps a third-party category name to a ServiceNow product model category.

</td></tr><tr><td>

Third-Party Model Mapping\[sn\_spend\_intg\_third\_party\_category\_map\]

</td><td>

References the Product Model and Third-Party Category tables and maps a product model to its corresponding third-party category.

</td></tr><tr><td>

Third-Party Registration\[sn\_spend\_intg\_third\_party\_registration\]

</td><td>

References the Supplier table and stores the provider name, cXML punchout and API exchange settings, and catalog index file used to register a third-party integration.

</td></tr><tr><td>

Third-Party Sourcing Registration\[sn\_spend\_intg\_sourcing\_vendor\]

</td><td>

Stores the name and code of a third-party sourcing vendor to be integrated with ServiceNow.

</td></tr><tr><td>

Third-Party Unit\[sn\_spend\_intg\_third\_party\_uom\]

</td><td>

References the Third-Party Registration and CMDB Model Unit tables and maps a third-party unit of measure to a ServiceNow unit, per provider.

</td></tr><tr><td>

Third-Party Unit Mapping\[sn\_spend\_intg\_third\_party\_uom\_map\]

</td><td>

References the Supplier Product and Third-Party Unit tables and maps a supplier product to its corresponding third-party unit of measure.

</td></tr></tbody>
</table>