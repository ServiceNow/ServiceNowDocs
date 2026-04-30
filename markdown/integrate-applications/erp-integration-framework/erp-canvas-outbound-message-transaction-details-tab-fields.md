---
title: Outbound message transaction details tab fields
description: The outbound message transaction details tab in Zero Copy Connector for ERP contains information about the transaction including ID numbers, transaction time, and the source.
locale: en-US
release: zurich
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, outbound, message, transaction, detail]
breadcrumb: [Zero Copy Connector for ERP field descriptions, Reference, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Outbound message transaction details tab fields

The outbound message transaction details tab in Zero Copy Connector for ERP contains information about the transaction including ID numbers, transaction time, and the source.

For process details, see [View and troubleshoot IDoc messages](../task/view-and-troubleshoot-idoc-messages.md).

This feature is available starting with the Zurich Patch 4 release.

Explore the API for interacting with Zero Copy Connector for ERP models. For detailed information and examples for using the API, see [sn\_erp\_integration API - Scoped, Global](https://www.servicenow.com/docs/access?context=sn_erp_integrationBothAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).

<table id="table_ist_gfb_ghc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Transaction log

</td><td>

A unique, system-assigned transaction log identification number. Select the number for details.

</td></tr><tr><td>

Flow engine context

</td><td>

If the transaction occurs in a flow, the specific flow is logged and displayed here. Select the context name to open the flow in Workflow Studio and obtain more information.**Note:** System-provided flows are logged. Custom flows aren't logged.

</td></tr><tr><td>

Source

</td><td>

Source of the transaction, for example, an ETL extraction task.

</td></tr><tr><td>

ERP system

</td><td>

The ERP system on which the transaction took place.

</td></tr><tr><td>

Duration \(ms\)

</td><td>

Amount of time \(in milliseconds\) that the transaction took to process.

</td></tr><tr><td>

Status

</td><td>

State of an IDoc at a specific time, such as Started, Success, or Error.

</td></tr><tr><td>

Caller scope

</td><td>

The application that performed the transaction. For ERP transactions, the caller scope is sn\_erp\_integration.

</td></tr><tr><td>

Encoded query

</td><td>

A filter for obtaining the IDoc information, for example, idoc\_type=ORDERS01.

</td></tr><tr><td>

EDI transaction ID

</td><td>

A unique ID for an electronic exchange of a business document.

</td></tr><tr><td>

IDOC message parameter 2

</td><td>

Specified parameter to filter information.

</td></tr><tr><td>

SAP Document

</td><td>

Document sent via IDoc.

</td></tr><tr><td>

IDOC status

</td><td>

Processing state of outbound message sent via IDoc at a specific time.

</td></tr><tr><td>

IDOC message parameter 3

</td><td>

Specified parameter to filter information.

</td></tr><tr><td>

IDOC payload

</td><td>

Data sent from SAP system via IDoc.

</td></tr><tr><td>

IDOC message type

</td><td>

The type of business document in an SAP system, for example, ORDERS.

</td></tr><tr><td>

IDOC number

</td><td>

Unique number identifying the specific message.

</td></tr><tr><td>

IDOC message parameter 4

</td><td>

Specified parameter to filter information.

</td></tr><tr><td>

IDOC message parameter 1

</td><td>

Specified parameter to filter information.

</td></tr><tr><td>

IDOC status text

</td><td>

Text description from SAP enhanced with additional information to describe the current state of the IDoc.

</td></tr><tr><td>

IDOC create error

</td><td>

Not currently used.

</td></tr></tbody>
</table>**Parent Topic:**[Zero Copy Connector for ERP field descriptions](erp-canvas-field-descriptions.md)

