---
title: Create contacts for emergency notifications
description: Use the ServiceNow users list to create contacts manually and synchronize the contacts with Everbridge to send emergency notifications.
locale: en-US
release: australia
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Setup steps for emergency notification, Integrating Crisis Management with Everbridge, Using BCM Classic Workspace, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Create contacts for emergency notifications

Use the ServiceNow users list to create contacts manually and synchronize the contacts with Everbridge to send emergency notifications.

## Before you begin

Role required: BCM admin \(sn\_bcm.admin\)

## About this task

After creating the contact from the user list, you can update the contacts and synchronize them with Everbridge.

Delivery channels are imported from Everbridge to the delivery channels table. Using the imported delivery channels, you can manually create contact delivery details or the system administrator can do an easy import.

## Procedure

1.  Navigate to **Business Continuity** &gt; **Everbridge Contact Configuration** &gt; **Contacts**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_u1t_44f_ppb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source

</td><td>

-   If you created the contact manually from the users list, then it is Manual.
-   If you had used the sync rule to create contact, then it is Sync rule.


</td></tr><tr><td>

Last sync on

</td><td>

Auto-populates the date on which the contact was last synchronized with Everbridge.

</td></tr><tr><td>

Contact ID

</td><td>

Unique ID of the contact.

</td></tr><tr><td>

Sync status

</td><td>

Defaults to **New** when the contact is created. The status can also be:-   **Success**: When the contact is successfully synced with Everbridge.
-   **Error**: If there is an error in syncing.
-   **Updated**: If the contact or the delivery details were modified.


</td></tr><tr><td>

User

</td><td>

User reference from the Users table \[sys\_user\].

</td></tr><tr><td>

External contact ID

</td><td>

Contact ID in Everbridge.

</td></tr><tr><td>

Sync error

</td><td>

Error in syncing the contact with Everbridge.

</td></tr></tbody>
</table>    You can delete a contact that you created manually from the User table. However, the contact must be in **New** state. If the referenced user record is deleted, then a scheduled job that runs weekly deletes the contact from the Contacts table.

4.  Click **Submit**.

5.  To create delivery details for the contact you created, click **New** in the **Delivery details** related list.

    1.  Select the Delivery channel from the list that you imported.

    2.  Enter a value.

        If the delivery channel is email, then enter an email ID.

    3.  Enter the order of preference in which the delivery channels are prioritized to send notifications.

    4.  Click **Submit**.

6.  To import contacts using a sync rule, you must first [create a contact import rule](contact-import-sync-rule.md).

7.  To import contacts based on contact sync rules, click **Import users** button.

    Refresh the form page to get the imported list of users.

    **Import users** action reads the Users table \[sys\_user\] based on the contact sync rules and creates a record in the Contacts table.

8.  To synchronize your list of contacts with that of Everbridge, click the **Sync with Everbridge** button.

    After the contacts are synchronized with Everbridge, the status of the sync action is recorded in the **Sync status** field. The unique ID of the contacts that are synced successfully in Everbridge are recorded as the **External contact ID** of the Contacts table.


