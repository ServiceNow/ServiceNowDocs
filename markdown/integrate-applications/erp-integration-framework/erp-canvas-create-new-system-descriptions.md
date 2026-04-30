---
title: Zero Copy Connector for ERP new system field descriptions
description: The new system form in Zero Copy Connector for ERP contains information on connection details for the ERP \(Enterprise Resource Planning\) system.
locale: en-US
release: zurich
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, system]
breadcrumb: [Zero Copy Connector for ERP field descriptions, Reference, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Zero Copy Connector for ERP new system field descriptions

The new system form in Zero Copy Connector for ERP contains information on connection details for the ERP \(Enterprise Resource Planning\) system.

For process details, see [Create an ERP system in Zero Copy Connector for ERP](../task/create-an-erp-system.md).

|Field|Description|
|-----|-----------|
|ERP system|Name of the ERP system to help identify the business area.|
|Short description|Brief description of what the ERP system is for.|
|Connection|Alias of the connection credential that you configured to connect to the system of record. You can select only from connections in the Zero Copy Connector for ERP scope.|
|ERP software|The supported ERP software on the system. Select one or more options from the list, for example, ECC 7.5 and SAP S/4HANA 2021. The list contains major SAP versions and doesn't include patch versions.|
|KB link \(on heartbeat tabs after system record is first saved\)|If there's an error and a relevant knowledge base article is available, a link to the article is provided.|
|Status \(on heartbeat tabs after system record is first saved\)|State of the heartbeat: **Success**, **Failed**, or **Not connected**.|
|Error text \(on heartbeat tabs after system record is first saved\)|Details about any errors that have occurred.|
|Updated \(on heartbeat tabs after system record is first saved\)|Date and time when the heartbeat was last changed.|

**Parent Topic:**[Zero Copy Connector for ERP field descriptions](erp-canvas-field-descriptions.md)

