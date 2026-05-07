---
title: Install ServiceNow Vault
description: Install the ServiceNow Vault application and assign the required roles.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-16"
reading_time_minutes: 1
breadcrumb: [Configuring ServiceNow Vault, ServiceNow Vault]
---

# Install ServiceNow Vault

Install the ServiceNow Vault application and assign the required roles.

## Before you begin

Role required: admin

## About this task

When you first navigate to the Vault console on a new instance, the console is in preview-only mode. To activate full functionality, install the Vault console application from the ServiceNow Store or Application Manager. After installation, Data Discovery is available by default. All other tools require separate configuration.

## Procedure

1.  Install ServiceNow Vault by going to the [ServiceNow Store](https://store.servicenow.com/store/app/fcd8d60a1b47ae94c34d2135624bcb74) and selecting **Buy**.

    Alternatively, you can also complete installation by navigating to **All** &gt; **Application Manager** &gt; **Vault Console**.

2.  Elevate to the `security_admin` role by selecting your profile icon and then selecting **Elevate Roles**.

    A dialog box appears that contains available roles for elevation. In this case, you can check security\_admin and select **OK**.

3.  Assign the `sn_vault_console.vault_console_admin` role to the user that would need access to the Vault console by performing the following:

    1.  Navigate to **All** &gt; **User Administration** &gt; **Users** and then open a user record.

    2.  In the **Roles** related list, select **Edit**.

    3.  In the **Collection** list, select the sn\_vault\_console.vault\_console\_admin role, and then select **Add**.

    4.  Select **Save**.

4.  Based on organizational needs and functionality of each user, further additional tool-specific roles can be assigned to users.

    For more role related information, see [ServiceNow Vault roles](../concept/vault-roles.md).


