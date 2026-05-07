---
title: Create contacts for emergency notifications
description: Create the contacts manually to send out an emergency notification and synchronize them with the Everbridge instance.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Setup for Everbridge notifications, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Create contacts for emergency notifications

Create the contacts manually to send out an emergency notification and synchronize them with the Everbridge instance.

## Before you begin

Role required: sn\_bcm.admin

## About this task

After creating the contacts from the user list, you can update and synchronize them with the Everbridge instance.

Delivery channels are imported from the Everbridge instance to the delivery channels table. By using the imported delivery channels, you can manually create the contact delivery details.

## Procedure

1.  Navigate to **Business Continuity** &gt; **Everbridge Contact Configuration** &gt; **Contacts**.

    The contacts are displayed in the list view as shown in the example.![Contacts in the list view.](../image/ebn-contacts-list-view.png)

2.  Select **New**.

    The Contact form is shown in the example.![Contact form.](../image/contacts-ebn.png)

3.  On the form, fill in the fields.

    You can delete a contact that you created manually from the User table. However, the contact must be in **New** state. If the referenced user record is deleted, then a scheduled job that runs weekly deletes the contact from the Contacts table.

    For more information on the fields, see [Contact form](../reference/contact-form.md).

4.  Select **Submit**.

5.  To import contacts based on contact sync rules, select the **Import users** button.

    To import the contacts using a sync rule, you must first [Create the contact import rules](create-contact-import-rules.md). Refresh the form page to get the imported list of users.

    **Import users** action reads the Users table \[sys\_user\] based on the contact sync rules and creates a record in the Contacts table.

6.  To synchronize your list of contacts with that of Everbridge, select the **Sync with Everbridge** button.

    After the contacts are synchronized with Everbridge, the status of the sync action is recorded in the **Sync status** field. The unique ID of the contacts that are synced successfully in Everbridge are recorded as the **External contact ID** of the Contacts table.


-   **[Contact form](../reference/contact-form.md)**  
Use the Contact form to create the contacts manually and then synchronize the contacts with Everbridge.
-   **[Create the contact import rules](create-contact-import-rules.md)**  
Create a contact import rule to apply on the User table. You can then filter out the users as the contacts for emergency notifications.

**Parent Topic:**[Setup for Everbridge notifications](../concept/setup-steps-for-emergency-notification-uib-ws.md)

