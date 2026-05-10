---
title: Manage contacts from the customer service portal
description: Create and update customer contacts, assign roles to contacts, and enable or disable contact logins from the customer portal.Use the Create Contact catalog item to create a contact from the customer portal.Update the contact information for a user from the customer portal.Enable or disable the login for a contact from the customer portal.Assign one or more user roles to a contact from the customer portal.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use Customer Service Portal, Customer communication, Use, Customer Service Management]
---

# Manage contacts from the customer service portal

Create and update customer contacts, assign roles to contacts, and enable or disable contact logins from the customer portal.

## Create a customer contact

Use the **Create Contact** catalog item to create a contact from the customer portal.

### Before you begin

Role required: sn\_customerservice.customer\_admin, sn\_customerservice.partner\_admin, or admin

### About this task

By selecting the **Create Contact** catalog item, you can add the details for a contact and create the contact record. After saving the record, you can perform the following actions depending on your role.

-   Users with the sn\_customerservice.customer\_admin or sn\_customerservice.partner\_admin can update the contact's user ID and enable or disable notifications.
-   Users with the admin role can set a password for the contact and require the contact to reset their password.

**Note:** These actions are available while you are creating the contact record.

### Procedure

1.  Click **Requests** &gt; **Request Something** in the portal header.

2.  In the Categories list, click **Services** and then click the **Create Contact** catalog item to display the Create Contact form.

3.  Fill in the fields on the Create Contact form.

    |Field|Description|
    |-----|-----------|
    |First name|The customer's first name.|
    |Last name|The customer's last name.|
    |Title|The customer's job title.|
    |Language|The customer's preferred language.|
    |Account|The customer's account.|
    |Email|The customer's email address.|
    |Business phone|The customer's business phone.|
    |Mobile phone|The customer's mobile phone.|

4.  Click **Submit**.

    The system creates the contact and updates the Contact form.

5.  Update the information in the following fields.

    |Field|Description|
    |-----|-----------|
    |Notification|Enable or disable notifications for this customer.|
    |User ID|A unique identifier for this user. The user ID should follow this format: **firstname.lastname**|

6.  With the admin role, you can update password information for the contact.

    |Field|Description|
    |-----|-----------|
    |Password|Set a password for the contact.|
    |Password needs reset|Requires the contact to reset their password when they log in to the portal.|

7.  Click **Save** to update the record.


## Update contact information for a user

Update the contact information for a user from the customer portal.

### Before you begin

Role required: sn\_customerservice.customer\_admin, sn\_customerservice.partner\_admin, or admin

### Procedure

1.  Click **Support** &gt; **Contacts** in the portal header.

2.  Select a contact from the Contacts list.

3.  Make the desired changes to the fields on the Contact form.

    |Field|Description|
    |-----|-----------|
    |First name|The customer's first name.|
    |Last name|The customer's last name.|
    |Title|The customer's job title.|
    |Language|The customer's preferred language.|
    |Time zone|The time zone for this customer's location.|
    |Account|The customer's account.|
    |Email|The customer's email address|
    |Business phone|The customer's business phone.|
    |Mobile phone|The customer's mobile phone.|
    |Notification|Enable or disable notifications for this customer.|
    |User ID|A unique identifier for this user. The user ID should follow the format **firstname.lastname**.|

4.  Click **Save**.


## Enable or disable the login for a contact

Enable or disable the login for a contact from the customer portal.

### Before you begin

Role required: sn\_customerservice.customer\_admin, sn\_customerservice.partner\_admin, or admin

### Procedure

1.  Select **Support** &gt; **Contacts** in the portal header.

2.  Select a contact from the Contacts list.

3.  In the Actions list, select one of the following links.

<table id="choicetable_fnc_gct_lrb"><thead><tr><th align="left" id="d236961e734">

Choice

</th><th align="left" id="d236961e737">

Description

</th></tr></thead><tbody><tr><td id="d236961e743">

**Disable login**

</td><td>

Disables the login for this contact. When the login is disabled, the contact can’t access the customer portal.This link is displayed if the login is enabled.

</td></tr><tr><td id="d236961e755">

**Enable login**

</td><td>

Enables the login for this contact.This link is displayed if the login is disabled.

</td></tr></tbody>
</table>
## Assign a user role to a contact

Assign one or more user roles to a contact from the customer portal.

### Before you begin

Role required: sn\_customerservice.customer\_admin, sn\_customerservice.partner\_admin, or admin

### About this task

Use the Edit Role pop-up window to manage the roles for a contact. Contacts must have at least one assigned user role. If there are no roles in the **Selected** column on the pop-up window, you cannot update the record.

**Note:** The roles available in the Edit Role pop-up window are configured using the **sn\_customerservice.contact\_role\_assignment** property.

### Procedure

1.  Click **Support** &gt; **Contacts** in the portal header.

2.  Select a contact from the Contacts list.

3.  In the Actions list, click the **Edit Roles** link.

4.  In the Edit Role pop-up window, select a role in the **Available** column and move it to the **Selected** column.

5.  Click **Update** on the Edit Role pop-up window.

    **Note:** If there are no roles in the **Selected** column, the system displays an error message and the column resets to display the originally assigned roles.

6.  Click **Save** on the Contact form.


