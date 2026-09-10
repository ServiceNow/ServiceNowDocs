---
title: Outbound message transaction details tab fields
description: The outbound message transaction details tab in Zero Copy Connector for ERP contains information about the transaction, including ID numbers, transaction time, and source.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/erp-canvas-outbound-message-transaction-details-tab-fields.html
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2026-08-06"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, outbound, message, transaction, detail]
breadcrumb: [Field descriptions, Reference, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Outbound message transaction details tab fields

The outbound message transaction details tab in Zero Copy Connector for ERP contains information about the transaction, including ID numbers, transaction time, and source.

For process details, see [View and troubleshoot IDoc messages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/view-and-troubleshoot-idoc-messages.md).

Explore the API for interacting with Zero Copy Connector for ERP models. For details and examples of using the API, see [sn\_erp\_integration API - Scoped, Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/sn_erp_integrationBothAPI.md).

<table id="table_ist_gfb_ghc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Transaction log

</td><td>

Unique, system-assigned transaction log identification number. Select the number for details.

</td></tr><tr><td>

Flow engine context

</td><td>

If the transaction occurs in a flow, the specific flow is logged and displayed here. Select the context name to open the flow in Workflow Studio and obtain more information.**Note:** System-provided flows are logged. Custom flows aren't logged.

</td></tr><tr><td>

Source

</td><td>

Source of the transaction.

</td></tr><tr><td>

ERP system

</td><td>

ERP system on which the transaction took place.

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

Application that performed the transaction. For ERP transactions, the caller scope is sn\_erp\_integration.

</td></tr><tr><td>

Encoded query

</td><td>

Filter for obtaining the IDoc information, for example, idoc\_type=ORDERS01.

</td></tr><tr><td>

EDI transaction ID

</td><td>

Unique ID for an electronic exchange of a business document.

</td></tr><tr><td>

IDOC message parameter 1

</td><td>

Specified parameter to filter information.

</td></tr><tr><td>

SAP Document

</td><td>

Document sent via IDoc.

</td></tr><tr><td>

IDOC status

</td><td>

Processing state of an outbound message sent via IDoc at a specific time.

</td></tr><tr><td>

IDOC message parameter 2

</td><td>

Specified parameter to filter information.

</td></tr><tr><td>

IDOC payload

</td><td>

Data sent from the SAP system via IDoc.

</td></tr><tr><td>

IDOC message type

</td><td>

Type of business document in an SAP system, for example, ORDERS.

</td></tr><tr><td>

IDOC number

</td><td>

Unique number identifying the specific message.

</td></tr><tr><td>

IDOC message parameter 3

</td><td>

Specified parameter to filter information.

</td></tr><tr><td>

IDOC message parameter 4

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
</table>