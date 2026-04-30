---
title: Client scripts installed with Customer Service Management
description: Client scripts are added with activation of Customer Service Management.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Components installed with Customer Service Management, Customer Service Management reference, Customer Service Management]
---

# Client scripts installed with Customer Service Management

Client scripts are added with activation of Customer Service Management.

<table id="table_gpt_myw_kt"><thead><tr><th>

Client script

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Channel and State readonly for customer

</td><td>

Case\[sn\_customerservice\_case\]

</td><td>

Sets the **Channel** and **State** fields to read-only on the Case form that the customer can view from the customer portal.

</td></tr><tr><td>

Check Contextual Security Installed

</td><td>

Contact \[customer\_contact\]

</td><td>

Checks if the Contextual Security plugin \(com.glide.role\_management\) is installed before creating a customer contact.

</td></tr><tr><td>

Customer Case View

</td><td>

Case\[sn\_customerservice\_case\]

</td><td>

Hides certain elements in the Case form for ESS view.

</td></tr><tr><td>

Empty Case form on Account Change

</td><td>

Case\[sn\_customerservice\_case\]

</td><td>

When a user makes a change to the value in the **Account** field on the Case form, the values in the following fields are cleared: **Partner**, **Partner contact**, **Asset**, **Entitlement**, **Contract**, and **Contact**.

</td></tr><tr><td>

Empty Partner Contact on Partner Change

</td><td>

Case\[sn\_customerservice\_case\]

</td><td>

When a user makes a change to the value in the **Partner** field on the Case form, the **Partner contact** field is also cleared.

</td></tr><tr><td>

Hide Activity Stream

</td><td>

Contact\[customer\_contact\]

</td><td>

Hides the activity stream on top of the form header.

</td></tr><tr><td>

Hide attachment icon

</td><td>

Registration Request \[sn\_customerservice\_registration\]

</td><td>

Hides the attachment icon on top of the form header.

</td></tr><tr><td>

Hide Icons Form Header

</td><td>

Case\[sn\_customerservice\_case\]

</td><td>

Hides the email icon from the more options menu and the activity stream icon at the top of the form header. Also hides the book icon next to the **Short Description** field on the form.

</td></tr><tr><td>

Hide Suggestion next to Short Description

</td><td>

Case\[sn\_customerservice\_case\]

</td><td>

Hides the suggestion icon next to the **Short description** field.

</td></tr><tr><td>

Make field readonly

</td><td>

Account Relationship Type \[sn\_customerservice\_account\_relationship\_type\]

</td><td>

Sets the **From** and **To** fields to read only once a record is created in the Account Relationship Type table \(sn\_customerservice\_account\_relationship\_type\).

</td></tr><tr><td>

Open the glide list for new appointment

</td><td>

Appointment\[sn\_customerservice\_appointment\]

</td><td>

Opens the glide list to select the user for an appointment for new records.

</td></tr><tr><td>

Populate Contact Company

</td><td>

Case\[sn\_customerservice\_case\]

</td><td>

When a user name is selected in the **Contact** field, the **Account** field is populated with the contact's account information.

</td></tr><tr><td>

Populate Contract

</td><td>

Case\[sn\_customerservice\_case\]

</td><td>

Populates the **Contract** field when the **Account** field is filled.

</td></tr><tr><td>

Populate contract and entitlement

</td><td>

Case\[sn\_customerservice\_case\]

</td><td>

Populates the **Contract** and **Entitlement** fields when the **Account** field is filled.

</td></tr><tr><td>

Populate Entitlement

</td><td>

Case\[sn\_customerservice\_case\]

</td><td>

Populates the **Entitlement** field when the **Account** field is filled.

</td></tr><tr><td>

Populate Product

</td><td>

Case\[sn\_customerservice\_case\]

</td><td>

When an asset is selected in the **Asset** field, the **Product** field is populated with the asset's product model.

</td></tr><tr><td>

Registration code read-only

</td><td>

Registration Request \[sn\_customerservice\_registration\]

</td><td>

Sets the **Registration code** field to read-only.

</td></tr><tr><td>

Set account read on load

</td><td>

Account Team Member \[sn\_customerservice\_team\_member\]

</td><td>

Sets the **Account** field to read only for a new record when the account is not empty on form load.

</td></tr><tr><td>

Set asset readonly

</td><td>

Asset Contact\[sn\_customerservice\_m2m\_asset\_contact\]

</td><td>

Set the **Asset** field to readonly for a new form when the asset value is not empty.

</td></tr><tr><td>

Show partner field

</td><td>

Case \[sn\_customerservice\_case\]

</td><td>

Shows the **Opened by** field on the Case form.

</td></tr><tr><td>

Special Handling Notes for Case

</td><td>

Case\[sn\_customerservice\_case\]

</td><td>

Shows all of the Special Handling Notes with display type alert related to the current record.

</td></tr><tr><td>

Validate Product Entitlement

</td><td>

Entitlement\[service\_entitlement\]

</td><td>

Displays a field warning message for the **Per unit** field if a product is selected but the **Asset**, **Contract**, and **Account** fields are empty.

</td></tr></tbody>
</table>**Parent Topic:**[Components installed with Customer Service Management](r_InstalledWithCustomerService.md)

