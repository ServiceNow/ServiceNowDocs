---
title: Configure system property to send registration emails to external users
description: Configure the sn\_supplier.external\_registration\_profile\_id system property to ensure that registration emails are sent to external users for accessing the Supplier Collaboration Portal.
locale: en-US
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure self-registration for external users, Install Supplier Collaboration Portal, Configure, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Configure system property to send registration emails to external users

Configure the sn\_supplier.external\_registration\_profile\_id system property to ensure that registration emails are sent to external users for accessing the Supplier Collaboration Portal.

## Before you begin

[Configure self-registration for external users](config-reg-for-external-users-slm.md).

Role required: admin

## Procedure

1.  Navigate to **External User Self-Registration** &gt; **User Registration Configurations**.

2.  Open the record for the user registration configuration.

3.  Select the context menu icon \(![Context menu icon](../image/context-menu.png)\), and then select **Copy sys\_id**.

4.  In the navigation filter, enter `sys_properties.list`.

    The entire list of properties in the System Properties \[sys\_properties\] table appears.

5.  In the **Name** search field, enter `sn_supplier.external_registration_profile_id`.

6.  Select the **sn\_supplier.external\_registration\_profile\_id** system property.

7.  In the **Value** field, paste the sys ID of the user registration configuration.

8.  Select **Update**.

    On the Supplier Case Management Properties page, the **Sys Id of the External User Registration Configuration for Onboarding a contact for a supplier** field is auto-populated with the sys ID of the user registration configuration you specified in the **Value** field of the **sn\_supplier.external\_registration\_profile\_id** system property.


**Parent Topic:**[Configure self-registration for external users](config-reg-for-external-users-slm.md)

**Related topics**  


[Configure the Vendor Contact table to send invitation emails during self-registration](config-vendor-contact-table.md)

[Enable notifications about self-registration errors](enable-supp-admin-emails.md)

