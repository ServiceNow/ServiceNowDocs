---
title: Configure the Vendor Contact table to send invitation emails during self-registration
description: Configure the Vendor Contact \[vm\_vdr\_contact\] table to send invitation emails to supplier contacts during the self-registration process.
locale: en-US
release: zurich
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure self-registration for external users, Install Supplier Collaboration Portal, Configure, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Configure the Vendor Contact table to send invitation emails during self-registration

Configure the Vendor Contact \[vm\_vdr\_contact\] table to send invitation emails to supplier contacts during the self-registration process.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All**.

2.  In the left navigation pane, enter `vm_vdr_contact_list.do`.

3.  On the Vendor Contacts page, right-click any column header and select **Configure** &gt; **Notifications**.

4.  In the Name column, select **Vendor Contact Invited**.

5.  On the **When to send** tab, add the condition: "Source is not supplier\_registration".![Condition added to send invitation emails to supplier contacts during the self-registration process.](../image/configure-vendor-contact-table-invitation.png)

6.  From the form header, right-click and select **Save**.


**Parent Topic:**[Configure self-registration for external users](config-reg-for-external-users-slm.md)

**Related topics**  


[Configure system property to send registration emails to external users](sys-prop-reg-email.md)

[Enable notifications about self-registration errors](enable-supp-admin-emails.md)

