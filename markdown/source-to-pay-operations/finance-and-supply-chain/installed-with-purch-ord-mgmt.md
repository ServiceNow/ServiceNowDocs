---
title: Components installed with Purchase Order Management
description: Several types of components are installed with the activation of the Purchase Order Management plugin, including roles and tables.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/finance-and-supply-chain/installed-with-purch-ord-mgmt.html
release: zurich
product: Finance and Supply Chain
classification: finance-and-supply-chain
topic_type: reference
last_updated: "2025-11-24"
reading_time_minutes: 1
keywords: [installation, components, purchase order management installation, purchase order management roles, purchase order management tables]
breadcrumb: [Install Purchase Order Management, Configure, Purchase Order Management, Source-to-Pay Operations, Finance and Supply Chain]
---

# Components installed with Purchase Order Management

Several types of components are installed with the activation of the Purchase Order Management plugin, including roles and tables.

## Roles installed

The following roles are installed with Purchase Order Management.

<table id="table_n2y_by1_q2c"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Purchase Order Management Administrator \[sn\_poem\_core.admin\]

</td><td>

Can access all the features and capabilities of the Purchase Order Management application

</td><td>

-   sn\_shop.procurement\_administrator
-   sn\_poem\_core.operational\_buyer

</td></tr><tr><td>

Operational Buyer \[sn\_poem\_core.operational\_buyer\]

</td><td>

Can be assigned purchase orders \(PO\) and also update assigned POs.

</td><td>

-   sn\_poem\_core.viewer
-   sn\_shop.procurement\_specialist

</td></tr><tr><td>

Purchase Order Management Viewer \[sn\_poem\_core.viewer\]

</td><td>

Can view purchase orders

</td><td>

sn\_fin.procurement\_user

</td></tr><tr><td>

Purchase Order Management Collaborator \[sn\_poem\_core.collaborator\]

</td><td>

Can view, edit, and resolve assigned purchase order exception tasks

</td><td>

sn\_poem\_core.viewer

</td></tr></tbody>
</table>## Tables installed

The following tables are installed with Purchase Order Management.

|Table|Description|
|-----|-----------|
|Purchase Order Exception Task \[sn\_poem\_exception\_task\]|Stores the purchase order exception tasks.|
|Purchase Order Exception \[sn\_poem\_exception\]|Stores the purchase order exception details.|
|Purchase Order Exception Split Line \[sn\_poem\_exception\_split\_line\]|Stores the details of split lines when a supplier submits a purchase order exception.|
|Purchase Order Confirmation \[sn\_poem\_po\_confirmation\]|Stores the purchase order confirmation details.|
|Purchase Order Confirmation Line \[sn\_poem\_po\_confirmation\_line\]|Stores the details of purchase order confirmation lines.|

**Parent Topic:**[Install Purchase Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/finance-and-supply-chain/install-purch-order-mgmt.md)

