---
title: Zero Copy Connector for ERP partner profile field descriptions
description: The partner profile record in Zero Copy Connector for ERP contains information that defines inbound and outbound communications with a partner.
locale: en-US
release: zurich
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2025-10-22"
reading_time_minutes: 1
breadcrumb: [Zero Copy Connector for ERP field descriptions, Reference, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Zero Copy Connector for ERP partner profile field descriptions

The partner profile record in Zero Copy Connector for ERP contains information that defines inbound and outbound communications with a partner.

For process details, see [View Zero Copy Connector for ERP partner profile information](../task/view-erp-system-partner-profile-information.md).

This feature is available starting with the Zurich Patch 4 release.

<table id="table_nfm_dcz_1hc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Partner class

</td><td>

An optional field that can be used to group partners.

</td></tr><tr><td>

Partner status

</td><td>

Indicates if the partner profile is active or inactive and most often contains **A** for active.

</td></tr><tr><td>

Language

</td><td>

Specifies the language for the person who receives messages about technical problems with IDoc creation. For example, an **E** indicates English and **S** indicates Spanish.

</td></tr><tr><td>

Partner number

</td><td>

Number for which a master record is created in a system application, for example, S4LOCAL.

</td></tr><tr><td>

Partner type

</td><td>

Partner role or function. Common types include:-   LS: Logical System
-   KU: Customer \(for outbound messages\)
-   LI: Vendor \(for outbound messages\)

</td></tr><tr><td>

User type

</td><td>

Most often contains **US** \(for user\) to indicate that you want the system to notify a specific person when the inbound message arrives.

</td></tr><tr><td>

Message type \(Allowed message types column\)

</td><td>

Type of business document allowed to be sent or received, for example, an order or invoice.

</td></tr><tr><td>

Message function \(Allowed message types column\)

</td><td>

A second level of differentiation of message type to assign additional process codes or actions.

</td></tr><tr><td>

Message code \(Allowed message types column\)

</td><td>

A third level of differentiation of message type.

</td></tr></tbody>
</table>**Parent Topic:**[Zero Copy Connector for ERP field descriptions](erp-canvas-field-descriptions.md)

