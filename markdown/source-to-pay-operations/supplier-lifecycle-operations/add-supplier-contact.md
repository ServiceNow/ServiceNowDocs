---
title: Add a supplier contact from the Source-to-Pay Workspace
description: Add the supplier contacts so that they can access the Supplier Collaboration Portal and start working on the most important tasks.
locale: en-US
release: xanadu
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Managing supplier contacts from the Source-to-Pay Workspace, Using Source-to-Pay Workspace, Using Supplier Lifecycle Operations, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Add a supplier contact from the Source-to-Pay Workspace

Add the supplier contacts so that they can access the Supplier Collaboration Portal and start working on the most important tasks.

## Before you begin

Before performing this task, ensure that you do the following:

-   Configure self-registration for external users. For more information, see [Configure self-registration for external users](config-reg-for-external-users-slm.md).
-   Configure the sn\_supplier.external\_registration\_profile\_id system property to ensure that registration emails are sent to external users. For more information, see [Configure system property to send registration emails to external users](sys-prop-reg-email.md).

Role required: sn\_slm.owner

**Note:** The sn\_slm.owner role can add contacts only for the suppliers that they own.

## Procedure

1.  Navigate to **All** &gt; **Supplier Lifecycle Operations** &gt; **Source-to-Pay Workspace**.

2.  Under My suppliers, select the legal name of the supplier that you want to add a supplier contact for.

    The supplier details page is displayed.

3.  On the **About** tab, under Supplier Contacts, select the add supplier contact icon \(![Add supplier contact icon](../image/add-key-contacts.png)\) or select **Add a Supplier Contact**.

    **Note:** The **Add a Supplier Contact** option is displayed only when you add your first contact for a supplier. This option is not displayed when you add subsequent contacts for a supplier.

4.  In the Invite contacts dialog box, in the **Contact emails** field, enter the email address of the contact that you want to invite.

    You can invite more than one contact by entering multiple email addresses separated by a comma.

5.  Select **Add**.

6.  From the Role list next to each email address, select one of the following options:

    -   **Contact**: The contact is assigned the secondary contact role.
    -   **Admin**: The contact is assigned the primary contact role.
7.  Select **Send invites**.

    An email containing the registration link is sent to the email address.


## What to do next

[Register to the Supplier Collaboration Portal as an invited member](register-invited-member-supp-central.md).

**Parent Topic:**[Managing supplier contacts from the Source-to-Pay Workspace](../concept/managing-contacts-smw.md)

