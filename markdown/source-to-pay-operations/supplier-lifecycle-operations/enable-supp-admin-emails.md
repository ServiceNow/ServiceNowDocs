---
title: Enable notifications about self-registration errors
description: Add the sn\_slm.admin role to the groups to enable supplier admins to receive an email if a supplier contact encounters an error during self-registration.
locale: en-US
release: zurich
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure self-registration for external users, Install Supplier Collaboration Portal, Configure, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Enable notifications about self-registration errors

Add the sn\_slm.admin role to the groups to enable supplier admins to receive an email if a supplier contact encounters an error during self-registration.

## Before you begin

Role required: sn\_slm.admin

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Users and Groups** &gt; **Groups**.

2.  Search for and select the **Supplier Administrators** group.

3.  On the **Roles** tab, select **Edit**.

4.  In the Collection list, search for and double-click the **sn\_slm.admin** role to move it to the Role list.![Added sn_slm.admin role to the Supplier Administrators group.](../image/enable-supplier-admin-self-registration.png)

5.  Select **Save**.


**Parent Topic:**[Configure self-registration for external users](config-reg-for-external-users-slm.md)

**Related topics**  


[Configure system property to send registration emails to external users](sys-prop-reg-email.md)

[Configure the Vendor Contact table to send invitation emails during self-registration](config-vendor-contact-table.md)

