---
title: Manage contacts from Business Portal
description: Create and update customer contacts, assign roles to contacts, and enable or disable contact login from the business portal.Use the Create Contact catalog item to create a customer contact from the business portal.Update the contact information for a user from the business portal.Enable or disable the login for a contact from the business portal to control user access to the portal.Assign one or more user roles to a contact from the business portal.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Business Portal, Customer communication, Use, Customer Service Management]
---

# Manage contacts from Business Portal

Create and update customer contacts, assign roles to contacts, and enable or disable contact login from the business portal.

## Create a customer contact

Use the **Create Contact** catalog item to create a customer contact from the business portal.

### Before you begin

Role required: sn\_customerservice.customer\_admin, sn\_customerservice.partner\_admin, or admin

### About this task

By selecting the **Create Contact** catalog item, you can add the details for a contact and create the contact record. After saving the record, you can perform the following actions depending on your role.

-   Users with the sn\_customerservice.customer\_admin or sn\_customerservice.partner\_admin can update the contact's user ID and enable or disable notifications.
-   Users with the admin role can set a password for the contact and require the contact to reset their password.

**Note:** These actions are available while you’re creating the contact record.

### Procedure

1.  Navigate to the business portal.

2.  Select **My company** &gt; **Create a contact** in the portal header.

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

4.  Select **Submit**.

    The system creates the contact and updates the Contact form.

5.  Update the information in the following fields.

    |Field|Description|
    |-----|-----------|
    |Notification|Enable or disable notifications for this customer.|
    |User ID|A unique identifier for this user. The user ID should follow this format: **firstname.lastname**|

6.  With the admin role, you can update the password information for the contact.

    |Field|Description|
    |-----|-----------|
    |Password|Set a password for the contact.|
    |Password needs reset|Requires the contacts to reset their password when they log in to the portal.|

7.  Select **Save** to update the record.


## Update contact information for a user

Update the contact information for a user from the business portal.

### Before you begin

Role required: sn\_customerservice.customer\_admin, sn\_customerservice.partner\_admin, or admin

### Procedure

1.  Navigate to the business portal.

2.  Select **My company** &gt; **Manage contacts**.

3.  Select the desired contact from the Contacts list.

4.  Select **Edit details**.

5.  Make the desired changes on the Contact form.

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

6.  Select **Save**.


## Enable or disable the login for a contact

Enable or disable the login for a contact from the business portal to control user access to the portal.

### Before you begin

Role required: sn\_customerservice.customer\_admin, sn\_customerservice.partner\_admin, or admin

### Procedure

1.  Navigate to the business portal.

2.  Select **My company** &gt; **Manage contacts** in the portal header.

3.  Select a contact from the Contacts list.

4.  In the Actions list, select one of the following links, as required.

<table id="choicetable_fnc_gct_lrb"><thead><tr><th align="left" id="d177600e762">

Choice

</th><th align="left" id="d177600e765">

Description

</th></tr></thead><tbody><tr><td id="d177600e771">

**Disable login**

</td><td>

Disables the login for this contact. When the login is inactive, the contact can’t access the business portal.This link is displayed if the login is enabled.

</td></tr><tr><td id="d177600e783">

**Enable login**

</td><td>

Enables the login for this contact.This link is displayed if the login is disabled.

</td></tr></tbody>
</table>
## Assign user roles to a contact

Assign one or more user roles to a contact from the business portal.

### Before you begin

Role required: sn\_customerservice.customer\_admin, sn\_customerservice.partner\_admin, or admin

### About this task

Use the Edit Role pop-up window to manage the roles for a contact. Contacts must have at least one assigned user role. If there are no roles in the **Selected** column on the pop-up window, you can’t update the record.

**Note:** The roles available in the Edit Role pop-up window are configured using the **sn\_customerservice.contact\_role\_assignment** property.

### Procedure

1.  Navigate to the business portal.

2.  Select **My company** &gt; **Manage contacts** in the portal header.

3.  Select a contact from the Contacts list.

4.  In the Actions list, select the **Edit Roles** link.

5.  In the Edit Role pop-up window, select a role in the **Available** column and move it to the **Selected** column.

6.  Select **Update** on the Edit Role pop-up window.

    **Note:** If there are no roles in the **Selected** column, the system displays an error message and the column resets to display the originally assigned roles.


