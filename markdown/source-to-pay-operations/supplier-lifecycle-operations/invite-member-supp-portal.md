---
title: Invite a member to access the Supplier Collaboration Portal
description: Invite supplier contacts to access the Supplier Collaboration Portal so that they can raise requests and start working on their assigned tasks.
locale: en-US
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Supplier Collaboration Portal, Use, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Invite a member to access the Supplier Collaboration Portal

Invite supplier contacts to access the Supplier Collaboration Portal so that they can raise requests and start working on their assigned tasks.

## Before you begin

Before performing this task, ensure that you do the following:

-   Configure self-registration for external users. For more information, see [Configure self-registration for external users](config-reg-for-external-users-slm.md).
-   Map the external user registration configuration to the Supplier Collaboration Portal. For more information, see [Map the self-registration configuration to Supplier Collaboration Portal](map-ext-user-to-supp-central.md).
-   Configure the **sn\_supplier.external\_registration\_profile\_id** system property to ensure that registration emails are sent to external users. For more information, see [Configure system property to send registration emails to external users](sys-prop-reg-email.md).

Role required: sn\_slm.contact

## About this task

The **Invite** option in the Contacts widget is available only to the primary supplier contact and the supplier administrator. Only the primary supplier contact and the supplier administrator can invite new members to access the Supplier Collaboration Portal.

## Procedure

1.  Navigate to the Supplier Collaboration Portal home page by accessing your instance URL and adding a /supplier suffix.

    For example, `https://example.com/supplier`.

2.  In the My contacts widget, select **Invite**.

    The Invite contacts dialog box is displayed.

3.  In the **Contact emails** field, enter the email address of the contact that you want to invite.

    You can invite more than one contact by entering multiple email addresses separated by a comma.

4.  Select **Add**.

5.  From the **Role** list next to each email address, select one of the following options:

    -   **Contact**: Manages assigned files
    -   **Primary**: Manages all contacts and files
6.  Select **Send invites**.

    A registration email is sent to the email addresses.


## What to do next

The invited member receives an email with the registration link to the Supplier Collaboration Portal. For more information, see [Register to the Supplier Collaboration Portal as an invited member](register-invited-member-supp-central.md).

**Note:**

After Xanadu December 2024 release, you can also invite contacts from other email domains, provided they are part of the hierarchy.

**Related topics**  


[Using Supplier Collaboration Portal](../concept/use-supp-central.md)

[Register to the Supplier Collaboration Portal as an invited member](register-invited-member-supp-central.md)

