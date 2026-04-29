---
title: Outbound message IDoc status for IDoc log tab fields
description: The outbound message IDoc status for IDoc log tab in Zero Copy Connector for ERP contains detailed information about an individual message.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, outbound, message, idoc, status, log]
breadcrumb: [Zero Copy Connector for ERP field descriptions, Reference, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Outbound message IDoc status for IDoc log tab fields

The outbound message IDoc status for IDoc log tab in Zero Copy Connector for ERP contains detailed information about an individual message.

For process details, see [View and troubleshoot IDoc messages](../task/view-and-troubleshoot-idoc-messages.md).

Explore the API for interacting with Zero Copy Connector for ERP models. For detailed information and examples for using the API, see [sn\_erp\_integration API - Scoped, Global](https://www.servicenow.com/docs/access?context=sn_erp_integrationBothAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US).

<table id="table_c51_mfb_ghc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Message ID

</td><td>

Unique ID number when an error or event occurs during IDoc processing.

</td></tr><tr><td>

Message number

</td><td>

Unique number within a message class, for example, 099.

</td></tr><tr><td>

Message type

</td><td>

The type of business document in an SAP system, for example, ORDERS.

</td></tr><tr><td>

Status

</td><td>

Processing state of outbound message sent via IDoc at a specific time.

</td></tr><tr><td>

Status code

</td><td>

Numerical value stored in IDoc status record, for example:-   03: Data passed to port \(outbound success\)
-   20: Delivery to external system failure \(outbound error\)

</td></tr><tr><td>

Status code text

</td><td>

Text description of the current state of the IDoc.

</td></tr><tr><td>

Parameter 1

</td><td>

Specified parameter to filter information, such as No filters, No conversion, or No version change.

</td></tr><tr><td>

Parameter 2

</td><td>

An additional specified parameter.

</td></tr><tr><td>

Parameter 3

</td><td>

An additional specified parameter.

</td></tr><tr><td>

Parameter 4

</td><td>

An additional specified parameter.

</td></tr><tr><td>

Created

</td><td>

Date and time the message was created.

</td></tr></tbody>
</table>**Parent Topic:**[Zero Copy Connector for ERP field descriptions](erp-canvas-field-descriptions.md)

