---
title: Create a customer service case
description: Customer service agents and agent managers can create cases using the Customer Service Management application.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Manage cases, Using Customer Service Management, Customer Service Management]
---

# Create a customer service case

Customer service agents and agent managers can create cases using the Customer Service Management application.

## Before you begin

Role required: sn\_customerservice\_agent, sn\_customerservice\_manager, or admin

## Procedure

1.  Create a case.

<table id="choicetable_dw2_1w3_3kb"><thead><tr><th align="left" id="d202703e64">

Option

</th><th align="left" id="d202703e67">

Description

</th></tr></thead><tbody><tr><td id="d202703e73">

**CSM Configurable Workspace**

</td><td>

From the Interaction form, click **Create Case**.

</td></tr><tr><td id="d202703e86">

**Platform interface**

</td><td>

Navigate to **Customer Service** &gt; **Cases** &gt; **Create New**.You can also create cases by:

-   Clicking **New** in the Customer Service Cases list.
-   Clicking the **Create New Case** related link from any of the entities that can be associated with a case, such as accounts or products.


</td></tr></tbody>
</table>2.  Fill in the fields on the Create Case form.

<table id="table_czw_ftc_nr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

The automatically assigned case number.

</td></tr><tr><td>

Channel

</td><td>

The method by which the customer initiated contact and the case was opened. -   Web \(default\)
-   Phone
-   Email
-   Chat
-   Social


</td></tr><tr><td>

Contact Local Time

</td><td>

The local time of the contact assigned to the case. It is automatically filled according to the time zone set on the Contact form. If no time zone is set on the Contact form, it is filled according to the **Contact Timezone** set on the case itself.

 If no time zone is set on the Contact form or in the case, the field is left blank and is read-only.

 If a case is closed or canceled, the **Contact Local Time** field is hidden.

 **Note:** Configure the form layout to add this field to the Case form.

</td></tr><tr><td>

Contact time zone

</td><td>

The contact time zone if the customer is working in a different time zone for the case. It overrides the Contact form time zone.If no contact local time or contact time zone is set, the instance time zone is displayed.

 Once the case is created, the field is read-only.

 **Note:** Configure the form layout to add this field to the Case form.

</td></tr><tr><td>

Account

</td><td>

The name of the company associated with this case. If you select a contact in the **Contact** field, this field is auto-filled if the account information is available in the contact record.

</td></tr><tr><td>

Contact

</td><td>

The name of the customer contact for this case.

</td></tr><tr><td>

Consumer

</td><td>

The name of the consumer for this case. **Note:** This field is active only when the Customer Data Models for B2B2C plugin \(com.sn\_csm\_b2b\_consumers\) is [installed](activate-customer-data-models-b2b2c.md). Once Account is selected, only consumers belonging to the account are displayed.

</td></tr><tr><td>

Service Organization

</td><td>

Internal or external entity that is involved in providing service to the requester.

</td></tr><tr><td>

Requesting Service Organization

</td><td>

The name of the service organization requesting assistance.

</td></tr><tr><td>

Product

</td><td>

The product model of the asset. A model is a specific version or configuration of an asset \(for example, Apple Mac Book Pro\). If you select an asset in the **Asset** field, this field is auto-filled if the associated product information is available in the asset record. A product may be associated with multiple assets.

</td></tr><tr><td>

Asset

</td><td>

The asset tag number or the serial number of the asset associated with this case.

</td></tr><tr><td>

Partner Contact

</td><td>

The name of the partner contact for this case. If you select a partner in the **Partner** field, the list of available partner contacts is based on this selection.

</td></tr><tr><td>

Follow the sun

</td><td>

A check box to indicate that a case should be handed-off for global follow-up. If a customer enters additional comments on a **Priority 1 - Critical** or a**Priority 2 - High** case, or if the case is escalated, the flag is automatically selected.

 You can also manually select the check box.

 The activity stream on the case form is updated with any changes.

 **Note:** Enable the **Follow the sun** check box on the Customer Service case form by setting the value of the property **sn\_customerservice.FTS\_flag\_enabled** to **true**. Configure the form layout to add this field to the Case form.

</td></tr><tr><td>

Short description

</td><td>

A brief description of the customer question, issue, or problem.

</td></tr><tr><td>

Opened

</td><td>

The date and time that the case was opened.

</td></tr><tr><td>

Priority

</td><td>

The assigned priority:-   1 - Critical
-   2 - High
-   3 - Moderate
-   4 - Low \(default\)


</td></tr><tr><td>

Assignment group

</td><td>

The assigned customer service agent group.

</td></tr><tr><td>

Assigned to

</td><td>

The assigned agent. This field displays all users with the sn\_customerservice\_manager and sn\_customerservice\_agent roles.If a group is selected in the **Assignment group** field, the assigned agent must belong to this group.

</td></tr><tr><td>

Assigned on

</td><td>

The data and time when the case is assigned. This field is updated when a user is added or changed in the **Assigned to** field.

</td></tr><tr><td>

Contract

</td><td>

The contract number associated with this case. If you selected an asset in the **Asset** field, the **Contract** field displays those contracts that include a line item for that asset.

</td></tr><tr><td>

Entitlement

</td><td>

The service entitlement associated with this case. The available entitlements are filtered by the settings in the **Account**, **Contract**, **Product**, **Asset**, and **Channel** fields.

 If only one entitlement is available for this case, it is automatically added to the **Entitlement** field.

</td></tr><tr><td>

Partner

</td><td>

The name of the partner for this case.

</td></tr></tbody>
</table>3.  Click **Submit**.

    If available, the following information is associated with a newly created case:

    -   The name of the contact and the contact's company
    -   The product and contract details
    -   The SLA and entitlements

