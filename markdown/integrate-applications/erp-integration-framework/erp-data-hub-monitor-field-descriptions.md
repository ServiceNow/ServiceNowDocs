---
title: Zero Copy Connector for ERP Monitor field descriptions
description: The Zero Copy Connector for ERP \(Enterprise Resource Planning\) Monitor enables you to track ERP transactions and their progress.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, monitor, transaction, action, log, status]
breadcrumb: [Zero Copy Connector for ERP field descriptions, Reference, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Zero Copy Connector for ERP Monitor field descriptions

The Zero Copy Connector for ERP \(Enterprise Resource Planning\) Monitor enables you to track ERP transactions and their progress.

For process details, see [Monitor Zero Copy Connector for ERP transactions and logged errors](../task/monitor-erp-data-hub-logged-extraction-and-remote-lookup-transactions.md).

<table id="table_uk4_144_2dc"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Transaction log

</td><td>

A unique, system-assigned transaction log identification number. Select the number for details.

</td></tr><tr><td>

Flow engine context

</td><td>

If the transaction occurs in a flow, the specific flow is logged and displayed here. Select the context name to open the flow in Workflow Studio and obtain more information.

 **Note:** System-provided flows are logged. Custom flows aren't logged.

</td></tr><tr><td>

Status

</td><td>

Extraction or remote lookup state: Started, Success, or Error.

</td></tr><tr><td>

Source

</td><td>

Source table in Zero Copy Connector for ERP. For example, sn\_erp\_integration\_remote\_table.

</td></tr><tr><td>

Source Name

</td><td>

System ID of the source identified in the **Source** field. Select the name to obtain more information.

</td></tr><tr><td>

Display name

</td><td>

The ERP model operation.

</td></tr><tr><td>

System

</td><td>

ERP system on which the transaction took place.

</td></tr><tr><td>

Caller scope

</td><td>

The application that performed the transaction. For ERP transactions, the caller scope is sn\_erp\_integration.

</td></tr><tr><td>

Duration \(ms\)

</td><td>

Amount of time \(in milliseconds\) that the transaction took to process.

</td></tr><tr><td>

Response item count

</td><td>

The number of records that were read.

</td></tr><tr><td>

Updated

</td><td>

The date and time the transaction was last changed.

</td></tr></tbody>
</table>**Parent Topic:**[Zero Copy Connector for ERP field descriptions](erp-canvas-field-descriptions.md)

