---
title: Order case form
description: The order case form displays details about an order case.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Order Operations Case Management, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Order case form

The order case form displays details about an order case.

<table id="table_vyg_gzg_lvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

The automatically generated record number. The prefix for numbers from the Order Case table is ORDCS.

</td></tr><tr><td>

Account

</td><td>

The name of the company that the order case is opened for.

</td></tr><tr><td>

Contact

</td><td>

The name of the customer contact for the order case.

</td></tr><tr><td>

Scope of request

</td><td>

Identifies the scope of the change for an order caseAgents can use this field to select the type of change for an order case.

-   **Specific line items, Single order**: Sets one or more order line items as the source for case line items.
-   **Multiple orders**: Sets one or more complete orders as the source for case line items.

Selecting **Specific line items, Single order** sets the **Origin table** field to "Order Line Item" and makes the **Order number** field mandatory.

When the user selects the order number in the **Order number** field and selects **Add** on the Order Case form, the system displays the Add order lines to case modal. This modal lists the order lines for the specified order number.

Selecting **Multiple orders** sets the **Origin table** field to "Customer Order".

</td></tr><tr><td>

Order number

</td><td>

Reference to the customer order.If the **Scope of request** field is set to "Specific Line Items, Single Order" then this field becomes mandatory.

</td></tr><tr><td>

Channel

</td><td>

The method by which the customer initiated contact and the case was opened.-   Web \(default\)
-   Phone
-   Email
-   Chat
-   Social

</td></tr><tr><td>

Service

</td><td>

The service that was selected from the service selector when the order case was created.

</td></tr><tr><td>

Product

</td><td>

The product model of the asset. A model is a specific version or configuration of an asset \(for example, Apple Mac Book Pro\).If you select an asset in the **Asset** field and the asset has an associated product, the **Product** field is automatically updated. A product can be associated with multiple assets.

</td></tr><tr><td>

Asset

</td><td>

The asset tag number or the serial number of the asset involved in this case.

</td></tr><tr><td>

Install Base

</td><td>

The Install base field helps you track which products and services have been purchased by a customer, how they have been installed or provisioned, along with the detailed configuration for each installed item.

</td></tr><tr><td>

Origin table

</td><td>

Displays the table where the order case was initiated.

</td></tr><tr><td>

Short description

</td><td>

A brief description of the issue or request.

</td></tr><tr><td>

Needs attention

</td><td>

When checked, the system sends a notification to the agent in the **Assigned to** field. The notification includes the case number, state, priority, and short description.

</td></tr><tr><td>

Opened

</td><td>

The date and time that the case was opened.

</td></tr><tr><td>

Priority

</td><td>

The assigned priority:-   1 — Critical
-   2 — High
-   3 — Moderate
-   4 — Low \(default\)

</td></tr><tr><td>

Assignment group

</td><td>

The assigned customer service agent group.

</td></tr><tr><td>

Assigned to

</td><td>

The assigned agent. If a group is selected in the **Assignment group** field, the assigned agent must belong to this group.

</td></tr><tr><td>

Contract

</td><td>

The contract number associated with the order case.

</td></tr><tr><td>

Entitlement

</td><td>

The entitlement associated with this case. The entitlements available for selection in the reference list channel matches the case creation channel. The available entitlements are filtered by the settings in the **Account**, **Contract**, **Product**, and **Asset** fields.If only one entitlement is available for this case, it is automatically added to the **Entitlement** field.

</td></tr><tr><td>

Partner contact

</td><td>

The name of the partner contact.

</td></tr><tr><td>

Partner

</td><td>

The name of the partner company.

</td></tr><tr><td>

Parent

</td><td>

The parent record for the order case.

</td></tr><tr><td>

Resolution code

</td><td>

Choice list indicating the resolution states for the case. This field is mandatory when an agent proposes a solution for a case.The Order Operations Case Management application adds the following resolution codes to the **Resolution code** field:

-   Change approved
-   Added replacement product

</td></tr><tr><td>

Request reason code

</td><td>

-   Increase Demand
-   Change in Contract
-   Initial input incorrect
-   Other

</td></tr></tbody>
</table>