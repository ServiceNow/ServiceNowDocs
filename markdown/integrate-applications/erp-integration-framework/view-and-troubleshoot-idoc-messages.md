---
title: View and troubleshoot IDoc messages
description: When working with SAP business entities that can only be created or changed using IDoc, view outbound messages for details and troubleshooting information.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/erp-integration-framework/view-and-troubleshoot-idoc-messages.html
release: zurich
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, idoc, outbound, message, details, information, troubleshoot]
breadcrumb: [Create and change SAP business entities with IDoc, Add an entity to a model, Building models, Use, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# View and troubleshoot IDoc messages

When working with SAP business entities that can only be created or changed using IDoc, view outbound messages for details and troubleshooting information.

## Before you begin

Role required: sn\_erp\_integration.erp\_admin

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the outbound messages list by selecting the outbound messages icon \[Omitted image "erp-outbound-messages-icon.png"\] Alt text: in the side panel.

3.  Select an outbound message.

4.  Select the **Messages** tab.

5.  Select a **Message ID** to view details about a specific message.

6.  View transaction details.

    For example:

    -   Check the **Status** field to see if the message was successful.
    -   Check the **IDoc payload** field if the message was not successful and you need to troubleshoot. Also, see  for detailed information and examples using the API.
    -   The **IDoc number** can also be useful.
    For a detailed description of the field values, see [Outbound message transaction details tab fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/erp-canvas-outbound-message-transaction-details-tab-fields.md).

7.  Select the **Errors** tab to view information about any message errors that have occurred.

    For a detailed description of the field values, see [Outbound message errors tab fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/erp-canvas-outbound-message-errors-tab-columns.md).

8.  Select the **IDoc status for IDoc log** tab for technical information about the message.

    For a detailed description of the column values, see [Outbound message IDoc status for IDoc log tab fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/erp-canvas-outbound-message-idoc-status-for-idoc-log-tab-columns.md).


**Parent Topic:**[Create and change SAP business entities with IDoc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/create-and-change-sap-business-entities-with-idoc.md)

