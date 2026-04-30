---
title: Add a supplier contact from the Source-to-Pay Workspace
description: Add supplier contacts so that they can access the Supplier Collaboration Portal and start working on the most important tasks.
locale: en-US
release: yokohama
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage supplier contacts from the Source-to-Pay Workspace, Using Source-to-Pay Workspace, Using Supplier Lifecycle Operations, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Add a supplier contact from the Source-to-Pay Workspace

Add supplier contacts so that they can access the Supplier Collaboration Portal and start working on the most important tasks.

## Before you begin

Before performing this task, ensure that you do the following:

-   Configure self-registration for external users. For more information, see [Configure self-registration for external users](config-reg-for-external-users-slm.md).
-   Configure the sn\_supplier.external\_registration\_profile\_id system property to ensure that registration emails are sent to external users. For more information, see [Configure system property to send registration emails to external users](sys-prop-reg-email.md).

Role required: sn\_slm.owner, sn\_slm.manager, sn\_slm.admin

**Note:** Users with the sn\_slm.owner role can add contacts only for the suppliers that they manage. Users with sn\_slm.manager and sn\_slm.admin roles can add supplier contacts for any supplier.

## Procedure

1.  Navigate to **All** &gt; **Supplier Lifecycle Operations** &gt; **Source-to-Pay Workspace**.

2.  Under **Quick Actions**, select **Manage my suppliers**.

3.  Select the legal name of the supplier for which you want to add a supplier contact.

    The supplier details page is displayed.

4.  Navigate to the **Stakeholders** tab, and then select **Supplier contacts**.

5.  Select **Add**.

    **Note:** The **Add** button is visible only after the external user configuration is completed.

6.  In the **Contact emails** field, enter the email address of the contact that you want to invite.

    You can invite more than one contact by entering multiple email addresses separated by a comma.

7.  Select **Add**.

8.  From the **Role** drop down list, select one of the following options:

    -   **Contact**: Supplier contact role is assigned to the selected user.
    -   **Primary**: Primary contact role is assigned to the selected user.
9.  Select **Send invites**.![Add Supplier contacts dialog box.](../image/add-supplier-contact.png)

    A confirmation message stating that an email containing the registration link is sent to the email address is displayed.


## What to do next

[Register to the Supplier Collaboration Portal as an invited member](register-invited-member-supp-central.md).

**Parent Topic:**[Manage supplier contacts from the Source-to-Pay Workspace](../concept/managing-contacts-smw.md)

**Related topics**  


[Remove a supplier contact from the Source-to-Pay Workspace](remove-supp-contact-ws.md)

[Elevate a contact to the primary contact role from the Source-to-Pay Workspace](elevate-contact-ws.md)

[Restrict the primary contact role for a contact from the Source-to-Pay Workspace](restrict-contact-ws.md)

