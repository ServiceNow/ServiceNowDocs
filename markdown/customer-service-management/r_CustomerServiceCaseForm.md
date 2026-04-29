---
title: Case form
description: The Case form displays detailed information about a customer issue or problem.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Customer Service forms, Reference, Customer Service Management]
---

# Case form

The Case form displays detailed information about a customer issue or problem.

A customer service agent creates a case to identify a customer's question or issue and to track the activities related to resolving the issue. An agent also uses a case to track communication to and from the customer, including the communication channels being used.

Case activities include any action that is taken to resolve an issue. This can include phone calls or emails, knowledge base research, conversations with subject matter experts, and dispatch requests to field service agents, as well as other activities.

From the Case form, an agent can associate and store the related information, such as the customer's name, phone number, and company; account information; product and asset information; service contract and entitlement details, and any associated service level agreements \(SLAs\).

There are several key features to a case.

-   Communication between an agent and the customer or an agent and other employees within the organization. Details of all internal and external communication are recorded on the Case form.
-   Any additional tasks that result from a case, such as a work order. Tasks are tracked from a related list on the Case form. These tasks may be internal to the organization or they may involve the customer.
-   Information from the case that can be included in the knowledge base and used to help resolve other cases.

There are two different Case form views: a detailed view that is available to agents and agent managers in the Customer Service Management application and a simplified view that is available to external customers from the Customer and Consumer Service Portals.

## Agent view

The agent view of the Case form includes the following components:

-   A timeline that provides a visual display of case activities.
-   Referenced entities for the case including account and contact information, product and asset information, service contract and service entitlement details, and any pertinent SLAs. Except for SLAs, this information exists in the system and can be associated with the case by the agent or agent manager.
-   All communication about the case, both external and internal. This information is stored in the **Additional comments** field \(external communication\), the **Work notes** field \(internal communication\), the **Resolution notes** field. The **Resolution notes** field stores details about the case resolution, and the **Activity** field, which stores all communication in a chronological list.

Agents and managers can view a Case form by navigating to **Customer Support** &gt; **Cases** and selecting one of the following menu options:

-   **My Cases**
-   **All**
-   **Open**
-   **Unassigned**

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

Method by which the customer initiated contact and the case was opened. -   Web \(default\)
-   Phone
-   Email
-   Chat
-   Social

</td></tr><tr><td>

Contact Local Time

</td><td>

Local time of the contact assigned to the case. This is automatically filled according to the time zone set on the Contact form. If no time zone is set on the Contact form, it is filled according to the **Contact Timezone** set on the case itself.

 If no time zone is set on the Contact form or in the Case form, the field is left blank and is read-only.

 If a case is closed or canceled, the **Contact Local Time** field is hidden.

 **Note:** Configure the form layout to add this field to the Case form.

</td></tr><tr><td>

Contact time zone

</td><td>

Contact time zone if the customer is working in a different time zone for the case. This field overrides the Contact form time zone.If no contact local time or contact time zone is set, the instance time zone is displayed.

 After the case is created, the field is read-only.

 **Note:** Configure the form layout to add this field to the Case form.

</td></tr><tr><td>

Account

</td><td>

Name of the contact's company. This field is filled in automatically if the information is available in the contact record.

</td></tr><tr><td>

Contact

</td><td>

Name of the customer contact for this case.

</td></tr><tr><td>

Consumer

</td><td>

Name of the consumer for this case.

</td></tr><tr><td>

Provider Organization

</td><td>

Organization resolving the cases.

</td></tr><tr><td>

Requestor Organization

</td><td>

Organization requesting the omni-channel interactions.

</td></tr><tr><td>

Product

</td><td>

Product model of the asset. A model is a specific version or configuration of an asset \(for example, Apple Mac Book Pro\). If you select an asset in the **Asset** field and the asset has an associated product, the **Product** field is automatically updated. A product can be associated with multiple assets.

</td></tr><tr><td>

Asset

</td><td>

Asset tag number or the serial number of the asset involved in this case.

</td></tr><tr><td>

Install base

</td><td>

The Install base field helps you track which products and services have been purchased by a customer, how they have been installed or provisioned, along with the detailed configuration for each installed item.

</td></tr><tr><td>

Partner Contact

</td><td>

Name of the partner contact for this case.

</td></tr><tr><td>

Follow the sun

</td><td>

Option to indicate that a case should be handed-off for global follow-up. If a customer enters additional comments on a **Priority 1 - Critical** or a**Priority 2 - High** case, or if the case is escalated, the flag is automatically selected.

 The activity stream on the case form is updated with any changes.

 **Note:** Enable the **Follow the sun** check box on the Customer Service case form by setting the value of the property **sn\_customerservice.FTS\_flag\_enabled** to **true**. Configure the form layout to add this field to the Case form.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the issue or problem.

</td></tr><tr><td>

Opened

</td><td>

Date and time that the case was opened.

</td></tr><tr><td>

Priority

</td><td>

The assigned priority:-   1 — Critical
-   2 — High
-   3 — Moderate
-   4 — Low \(default\)

</td></tr><tr><td>

State

</td><td>

Customer service case states:-   New
-   Open
-   Awaiting Info
-   Resolved
-   Closed
-   Canceled

 **Note:** Configure the form layout to add this field to the Case form

</td></tr><tr><td>

Assignment group

</td><td>

Assigned customer service agent group.

</td></tr><tr><td>

Assigned to

</td><td>

Assigned agent. If a group is selected in the **Assignment group** field, the assigned agent must belong to this group.

</td></tr><tr><td>

Assigned on

</td><td>

Date and time when the case is assigned. This field is updated when a user is added or changed in the **Assigned to** field.

</td></tr><tr><td>

Contract

</td><td>

Contract number associated with this case.

</td></tr><tr><td>

Entitlement

</td><td>

Entitlement associated with this case. The entitlements available for selection in the reference list channel matches the case creation channel. The available entitlements are filtered by the settings in the **Account**, **Consumer**, and **Contract** fields.If only one entitlement is available for this case, it is automatically added to the **Entitlement** field.

Starting with the Zurich release, agents can add multiple entitlements to a case. If the **sn\_customerservice.advanced\_entitlements** system property is set to true, the Case Entitlements related list is visible on the Case form and the **Entitlement** field is hidden. For more information, see the following topics:

-   [Add an entitlement to a case](../task/add-entitlement-to-case.md)
-   [Properties installed with Customer Service Management](r_PropInstallWcustServ.md)

</td></tr><tr><td>

Partner

</td><td>

Name of the partner company.

</td></tr><tr><td class="sub-head" colspan="2">

Notes

</td></tr><tr><td>

Watch list

</td><td>

Users who receive notifications about this case when additional comments are added or if the state of a case is changed to **Resolved** or **Closed**. Select the add me icon to add yourself to the watch list.

</td></tr><tr><td>

Work notes list

</td><td>

Internal users who receive a notification about this case when work notes are added. You can only add internal users to the work notes list.

 Select the add me icon to add yourself to the work notes list.

 To enable notifications for users in the **Work notes list** field:

1.  Navigate to the Notifications \(sys\_notification\) table.
2.  Select Case Action Status.
3.  In the **Who will receive** tab, do one of the following:
    -   Add a user in the **Users** field.
    -   In the **Recipients listed in fields** field, add the **Work notes list** field.
4.  Select **Update**.

</td></tr><tr><td>

Contributor Users

</td><td>

When a user with the case task agent role \(sn\_customerservice.case\_task\_agent\) is assigned to a case task, the user is added to the **Contributor Users** field.If this user is removed from the **Assigned to** field on the Case Task form, and they are not assigned to any other tasks for the case, thenn they are also removed from the **Contributor Users** field.

</td></tr><tr><td>

Contributor Groups

</td><td>

When a user with the case task agent role \(sn\_customerservice.case\_task\_agent\) is assigned to a case task, the user's assignment group is added to the **Contributor Groups** field.If this user is removed from the **Assigned to** field on the Case Task form, and no other member of their assignment group is assigned to any other tasks for the case, then the assignment group is removed from the **Contributor Groups** field.

 If a group is removed from the **Assignment group** field on the Case Task form, and the group is not assigned to any other tasks for the case, then the assignment group is removed from the **Contributor Groups** field.

</td></tr><tr><td>

Additional comments

</td><td>

Customer-viewable comments. Each comment is inserted into the **Activity** field when the user selects the **Post** button.

</td></tr><tr><td>

Work notes

</td><td>

Information about how to resolve the case, or steps taken to resolve it, if applicable.

 Internal users who have been added to the Work notes list receive the Case work notes added notification containing the work notes when added.

 You can configure the notification, as required. The notes are viewable by the admin, agent, and agent manager.

</td></tr><tr><td>

Activities

</td><td>

Records all activity associated with this case.

</td></tr><tr><td class="sub-head" colspan="2">

Resolution Information

</td></tr><tr><td>

Resolved by

</td><td>

Agent to whom the case is assigned when the case is resolved.

</td></tr><tr><td>

Closed by

</td><td>

Name of the user who closed the case.

</td></tr><tr><td>

Resolution Code

</td><td>

Choice list indicating the resolution states for the case.This field is mandatory when an agent proposes a solution for a case.

</td></tr><tr><td>

Cause

</td><td>

Details about the cause of the resolution.

</td></tr><tr><td>

Resolution notes

</td><td>

Details about how the case was closed. This field is mandatory if a customer service agent or agent manager closes a case. If a customer closes a case, it is not mandatory.

</td></tr><tr><td>

Add resolution notes to comments

</td><td>

Option to determine if the resolution notes are added to customer-viewable comments when the case is resolved. If selected, the resolution notes are added to the **Additional comments** \(customer-visible\) field.

</td></tr><tr><td>

Resolved

</td><td>

Date and time that the case was resolved.

</td></tr><tr><td>

Closed

</td><td>

Date and time that the case was closed.

</td></tr></tbody>
</table>## Customer view

Customers can view a Case form by selecting **My Cases** on the customer portal and then selecting a case number from their Case list.

The customer view of the Case form includes the following components:

-   A process flow formatter that indicates the current state of the case.
-   The related entity information, including account and contact information, product and asset information, and service contract information.
-   An **Activity** field that stores all communication for the case in a chronological list.

