---
title: Outbound message configuration fields
description: The add new outbound message configuration record in Zero Copy Connector for ERP contains information that defines IDoc outbound messages.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, erp data, connect, outbound, message]
breadcrumb: [Zero Copy Connector for ERP field descriptions, Reference, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Outbound message configuration fields

The add new outbound message configuration record in Zero Copy Connector for ERP contains information that defines IDoc outbound messages.

For process details, see [Create an IDoc outbound message configuration in Zero Copy Connector for ERP](../task/create-an-idoc-outbound-message-configuration.md).

<table id="table_xxc_pk4_bhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the new outbound message configuration.

</td></tr><tr><td>

Operation

</td><td>

The action, function, or process used to send data.

</td></tr><tr><td>

Receiver partner number

</td><td>

Number for which a master record is created in a system application, for example, S4LOCAL.

</td></tr><tr><td>

Receiver partner type

</td><td>

Partner role or function. Common types include:-   LS: Logical System
-   KU: Customer \(for outbound messages\)
-   LI: Vendor \(for outbound messages\)

</td></tr><tr><td>

System

</td><td>

Name of the ERP system on which the new configuration should be stored.

</td></tr><tr><td>

Partner Profile

</td><td>

Identifies the partner. Automatically added based on the specified system.

</td></tr><tr><td>

Message type

</td><td>

The IDoc message type, for example, ORDERS.

</td></tr></tbody>
</table>**Parent Topic:**[Zero Copy Connector for ERP field descriptions](erp-canvas-field-descriptions.md)

