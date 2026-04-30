---
title: Data source table information
description: The following information can help you with the FTP import and export data.
locale: en-US
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Procurement File Transfer Framework, Integrate, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Data source table information

The following information can help you with the FTP import and export data.

## Data source types

Data sources are used to create an import set so that data can be processed, if necessary, prior to being mapped onto a production table.

|Label|Name|
|-----|----|
|File|Data is in a recognized file format, accessible locally or remotely through several file retrieval methods.|
|JDBC|Data is in a database, accessible using JDBC. ServiceNow Technical Support supports Oracle, MySQL, Sybase, DB2 Universal, and MS SQL Server drivers.|
|LDAP|Data is in an LDAP server, accessible through the LDAP or LDAPS ports, 389 and 636 respectively.|
|OIDC|Data is accessible via OIDC.|
|REST \(IntegrationHub\)|Data is in a REST API, accessible through IntegrationHub.|
|Data Stream IntegrationHub|Data is loaded from a Data Stream Action, accessible through IntegrationHub.|
|Custom \(Load by Script\)|Data is obtained using a custom script.|

## Folder structure

See the following folder structure. You can use the `<type>.request` for taking the data and `<type>.response` for posting the data back to the FTP server:

```
catalog.request
catalog.response

invoice.request
invoice.response

orders.request
orders.response

shipment.request
shipment.response
```

## Associated Table Transform Map

To import data, define a data source and transform map, and schedule or run an import at some regular interval.

Table transform map is associated with the table to transform the `File Based Catalog Import [sn_spend_ftp_intg_catalog_stage]` data into `Catalog Import [sn_spend_intg_imp_catalog]`. See the following table transform labels and associated table information.

|Label|Name|
|-----|----|
|Invoice Import|sn\_spend\_intg\_imp\_invoice|
|Catalog Import|sn\_spend\_intg\_imp\_catalog|
|Availability Import|sn\_spend\_intg\_imp\_availability|
|Shipment Import|sn\_spend\_intg\_imp\_shipment|
|Order Acknowledgment|sn\_spend\_intg\_imp\_purchase\_order\_ack|
|Price Import|sn\_spend\_intg\_imp\_price|

-   **[Payloads samples and errors](payloads-information.md)**  
Use the following sample payloads to enable procurement data import and export.

**Parent Topic:**[Procurement File Transfer Framework](../concept/procurement-file-transfer-framework.md)

