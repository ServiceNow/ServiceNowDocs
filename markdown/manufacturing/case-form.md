---
title: Case form
description: The Case form enables an agent to associate and store the related information, such as the customer's name, phone number, and company; account information; product and asset information; service contract and entitlement details.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Manufacturing Commercial Operations reference, Manufacturing Commercial Operations]
---

# Case form

The Case form enables an agent to associate and store the related information, such as the customer's name, phone number, and company; account information; product and asset information; service contract and entitlement details.

## Agent view

The agent view of the Case form includes the following components:

-   A timeline that provides a visual display of case activities.
-   Referenced entities for the case, including account and contact information, product and asset information, service contract and service entitlement details.

Agents and managers can view a Case form by navigating to **Customer Support** &gt; **Cases** and selecting one of the following menu options:

-   **My Cases**
-   **All**
-   **Open**
-   **Unassigned**
-   **Escalated**

From the Case list, select a case number to display the Case form.

<table id="table_czw_ftc_nr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Automatically assigned case number.

</td></tr><tr><td>

Channel

</td><td>

Method by which the customer-initiated contact and the case were opened. -   Web \(default\)
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

Name of the contact's company. This field is automatically filled if the information is available in the contact record.

</td></tr><tr><td>

Contact

</td><td>

Name of the customer contact for this case.

</td></tr><tr><td>

Service Organization

</td><td>

Name of business location.

</td></tr><tr><td>

Requesting Service Organization

</td><td>

Service organization for which this case is being requested.

</td></tr><tr><td>

Product

</td><td>

Product model of the asset. A model is a specific version or configuration of an asset. For example, Apple Mac Book Pro. If you select an asset in the **Asset** field and the asset has an associated product, the **Product** field is automatically updated. A product can be associated with multiple assets.

</td></tr><tr><td>

Asset

</td><td>

Asset tag number or the serial number of the asset involved in this case.

</td></tr><tr><td>

Install base

</td><td>

The Install base field helps you track of:-   which products and services have been purchased by a customer
-   how they’ve been installed or provisioned
-   detailed configuration for each installed item.

</td></tr><tr><td>

Partner Contact

</td><td>

Name of the partner contact for this case.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the issue or problem.

</td></tr><tr><td>

Opened

</td><td>

Date and time when the case was opened.

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

Assigned customer service agent group.

</td></tr><tr><td>

Assigned to

</td><td>

Assigned agent. If a group is selected in the **Assignment group** field, the assigned agent must belong to this group.

</td></tr><tr><td>

Contract

</td><td>

Contract number associated with this case.

</td></tr><tr><td>

Entitlement

</td><td>

Entitlement associated with this case. The entitlements available for selection in the reference list channel matches the case creation channel. The available entitlements are filtered by the settings in the **Account**, **Contract**, **Product**, **Asset** fields.If only one entitlement is available for this case, it’s automatically added to the **Entitlement** field.

</td></tr><tr><td>

Partner

</td><td>

Name of the partner company.

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

 To enable notifications for users in the **Work notes list** field, do the following:

1.  Navigate to the Notifications \(sys\_notification\) table.
2.  Select Case Action Status.
3.  In the **Who will receive** tab, do one of the following:
    -   Add a user in the **Users** field.
    -   In the **Recipients listed in fields** field, add the **Work notes list** field.
4.  Select **Update**.

</td></tr><tr><td>

Contributor Users

</td><td>

When a user with the case task agent role is assigned to a case task, the user is added to the **Contributor Users** field.If this user is removed from the **Assigned to** field on the Case Task form, and they aren’t assigned to any other tasks for the case, then they’re also removed from the **Contributor Users** field.

</td></tr><tr><td>

Contributor Groups

</td><td>

When a user with the case task agent role is assigned to a case task, the user's assignment group is added to the **Contributor Groups** field.If this user is removed from the **Assigned to** field on the Case Task form, and no other member of their assignment group is assigned to any task for the case, then the assignment group is removed from the **Contributor Groups** field.

If a group is removed from the **Assignment group** field on the Case Task form, and the group isn’t assigned to any other tasks for the case, then the assignment group is removed from the **Contributor Groups** field.

</td></tr><tr><td>

Additional comments

</td><td>

Customer-viewable comments. Each comment is inserted into the **Activity** field when the user selects the **Post** button.

</td></tr><tr><td>

Work notes \(Private\)

</td><td>

Information about how to resolve the case, or steps taken to resolve it, if applicable.

 Internal users who have been added to the Work notes list receive the Case work notes added notification containing the work notes when added.

 You can configure the notification, as required. The notes are viewable by the admin, agent, and agent manager.

</td></tr><tr><td class="sub-head" colspan="2">

Resolution Information

</td></tr><tr><td>

Closed by

</td><td>

Name of the user who closed the case.

</td></tr><tr><td>

Resolution Code

</td><td>

List indicating the resolution states for the case.This field is required when an agent proposes a solution for a case.

</td></tr><tr><td>

Cause

</td><td>

Details about the cause of the resolution.

</td></tr><tr><td>

Resolution notes

</td><td>

Details about how the case was closed. This field is required if a customer service agent or agent manager closes a case. If a customer closes a case, it isn’t required.

</td></tr><tr><td>

Add resolution notes to comments

</td><td>

Option to determine if the resolution notes are added to customer-viewable comments when the case is resolved. If selected, the resolution notes are added to the **Additional comments** \(customer-visible\) field.

</td></tr><tr><td>

Closed

</td><td>

Date and time that the case was closed.

</td></tr></tbody>
</table>