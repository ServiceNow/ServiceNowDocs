---
title: ERP Data Hub Monitor field descriptions
description: The ERP Data Hub Monitor enables you to track ERP transactions and their progress.
locale: en-US
release: xanadu
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2024-10-27"
reading_time_minutes: 1
breadcrumb: [ERP Data Hub field descriptions, ERP Data Hub reference, ERP Data Hub, Building low-code applications, Developing your application, Building applications]
---

# ERP Data Hub Monitor field descriptions

The ERP Data Hub Monitor enables you to track ERP transactions and their progress.

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

Source table in ERP Data Hub. For example, sn\_erp\_integration\_etl\_extraction\_task or sn\_erp\_integration\_remote\_table.

</td></tr><tr><td>

Source Name

</td><td>

System ID of the source identified in the **Source** field. Select the name to obtain more information.

</td></tr><tr><td>

System

</td><td>

ERP system on which the transaction took place.

</td></tr><tr><td>

ERP Model Operation

</td><td>

Operation called by the transaction. For example, if you're creating an ERP model with a read operation and call it, the model's read operation is displayed here.

</td></tr><tr><td>

Duration \(ms\)

</td><td>

Amount of time \(in milliseconds\) that the transaction took to process.

</td></tr><tr><td>

Created

</td><td>

The date and time the transaction completed.

</td></tr><tr><td>

Async

</td><td>

If Async is true, the job runs in the background, for example, extractions are asynchronous. If Async is false, the user initiates the job, for example, remote lookup is synchronous.

</td></tr><tr><td>

Encoded query

</td><td>

Encoded query being used for the specific transaction.

 For more information, see [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

Logged on

</td><td>

UNIX timestamp for transaction start time.

</td></tr><tr><td>

Response item count

</td><td>

The number of records that were read.

</td></tr></tbody>
</table>**Parent Topic:**[ERP Data Hub field descriptions](erp-canvas-field-descriptions.md)

