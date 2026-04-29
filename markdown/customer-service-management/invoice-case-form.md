---
title: Invoice case form
description: The invoice case form displays details about an invoice case.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Case Management for Invoice Operations, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Invoice case form

The invoice case form displays details about an invoice case.

<table id="table_vyg_gzg_lvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Invoice Case

</td></tr><tr><td>

Number

</td><td>

The automatically generated record number. The prefix for numbers from the Invoice Case table is **INVCS**.

</td></tr><tr><td>

Channel

</td><td>

The method by which the customer initiated contact and the case was opened.-   Web \(default\)
-   Phone
-   Email
-   Chat
-   Social
-   Community
-   Alert
-   Virtual Agent

</td></tr><tr><td>

Account

</td><td>

The name of the company that the invoice case is opened for.

</td></tr><tr><td>

Contact

</td><td>

The name of the customer contact for the invoice case.

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

Partner Contact

</td><td>

The name of the partner contact for this invoice case.

</td></tr><tr><td>

Parent

</td><td>

The parent record for the invoice case.

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

The date and time that the invoice case was opened.

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

The contract number associated with the invoice case.

</td></tr><tr><td>

Entitlement

</td><td>

The entitlement associated with the invoice case. The entitlements available for selection in the reference list channel matches the case creation channel. The available entitlements are filtered by the settings in the **Account**, **Contract**, **Product**, and **Asset** fields.If only one entitlement is available for this case, it is automatically added to the **Entitlement** field.

</td></tr><tr><td>

Partner

</td><td>

The name of the partner company.

</td></tr><tr><td>

Request source

</td><td>

The source of the invoice case. Invoice cases can be created from the following sources:-   Specific invoice lines, single invoice
-   Invoice header details, multiple invoices

</td></tr><tr><td>

Invoice

</td><td>

The invoice that the invoice case is created for.

</td></tr><tr><td class="sub-head" colspan="2">

Notes

</td></tr><tr><td>

Watch list

</td><td>

Users who receive notifications about this case when additional comments are added or if the state of a case is changed to Resolved or Closed.

</td></tr><tr><td>

Work notes list

</td><td>

Internal users who receive a notification about this case when work notes are added. You can only add internal users to the work notes list.

</td></tr><tr><td>

Additional comments \(Customer visible\)

</td><td>

Customer-viewable comments. Each comment is inserted into the Activity field when the user saves the record.

</td></tr><tr><td>

Work notes \(Private\)

</td><td>

Information about how to resolve the case, or steps taken to resolve it, if applicable.

 Internal users who have been added to the Work notes list receive notifications when work notes are added to the invoice case.

</td></tr><tr><td class="sub-head" colspan="2">

Closure Information

</td></tr><tr><td>

Closed by

</td><td>

The name of the user who closed the case.

</td></tr><tr><td>

Closed

</td><td>

 

</td></tr><tr><td>

Resolution code

</td><td>

The resolution provided for the invoice case:

</td></tr><tr><td>

Cause

</td><td>

Details about the cause of the issue or problem.

</td></tr><tr><td>

Resolution notes

</td><td>

Details about how the case was resolved.

</td></tr><tr><td>

Add resolution notes to comments

</td><td>

A check box to determine if the resolution notes are added to customer-viewable comments when the case is resolved.If selected, the resolution notes are added to the **Additional comments** \(customer-visible\) field.

By default, the check box is cleared.

</td></tr><tr><td class="sub-head" colspan="2">

Related Records

</td></tr><tr><td>

Incident

</td><td>

Displays the number of the incident record associated with this invoice record.

</td></tr><tr><td>

Problem

</td><td>

Displays the number of the problem record associated with this invoice record.

</td></tr><tr><td>

Change Request

</td><td>

Displays the number of the change request record associated with this invoice record.

</td></tr><tr><td>

Caused by Change

</td><td>

If a case is the result of a change, this field displays the associated change request record.

</td></tr></tbody>
</table>