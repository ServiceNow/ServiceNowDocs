---
title: View and troubleshoot IDoc messages
description: When working with SAP business entities that can only be created or changed using IDoc, view outbound messages for details and troubleshooting information in Zero Copy Connector for ERP \(Enterprise Resource Planning\).
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, idoc, outbound, message, details, information, troubleshoot]
breadcrumb: [Create and change SAP business entities with IDoc, Add an entity to a model, Building models, Use, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# View and troubleshoot IDoc messages

When working with SAP business entities that can only be created or changed using IDoc, view outbound messages for details and troubleshooting information in Zero Copy Connector for ERP \(Enterprise Resource Planning\).

## Before you begin

Role required: sn\_erp\_integration.erp\_admin

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the outbound messages list by selecting the outbound messages icon ![](../image/erp-outbound-messages-icon.png) in the side panel.

3.  Select an outbound message.

4.  Select the **Messages** tab.

5.  Select a **Message ID** to view details about a specific message.

6.  View transaction details.

    For example:

    -   Check the **Status** field to see if the message was successful.
    -   Check the **IDoc payload** field if the message was not successful and you need to troubleshoot. Also, see sn\_erp\_integration API - Scoped, Global for detailed information and examples using the API.
    -   The **IDoc number** can also be useful.
    For a detailed description of the field values, see [Outbound message transaction details tab fields](../reference/erp-canvas-outbound-message-transaction-details-tab-fields.md).

7.  Select the **Errors** tab to view information about any message errors that have occurred.

    For a detailed description of the field values, see [Outbound message errors tab fields](../reference/erp-canvas-outbound-message-errors-tab-columns.md).

8.  Select the **IDoc status for IDoc log** tab for technical information about the message.

    For a detailed description of the column values, see [Outbound message IDoc status for IDoc log tab fields](../reference/erp-canvas-outbound-message-idoc-status-for-idoc-log-tab-columns.md).


**Parent Topic:**[Create and change SAP business entities with IDoc](../concept/create-and-change-sap-business-entities-with-idoc.md)

