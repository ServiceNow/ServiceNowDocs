---
title: Configuring the log protection plugin
description: Configure the protection rules for each table and operation to complete the configuration of the log protection plugin.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Avoid log tampering, System logs, Logs, Platform Security]
---

# Configuring the log protection plugin

Configure the protection rules for each table and operation to complete the configuration of the log protection plugin.

## Before you begin

Role required: security\_admin

## Procedure

1.  Navigate to **All** &gt; **Protected Tables** &gt; **Log Protection**.

    The Admin Panel page is displayed.

    **Note:** Starting in the Utah release, the Protected Tables plugin is installed by default, but disabled.

2.  Elevate your role to security\_admin in order to continue configuring the plugin.

    1.  Select **System Administrator**.

    2.  Select **Elevate role**.

        The Elevate role modal shows up.

    3.  Select the security\_admin option to elevate your role and select **Update**.

3.  Configure the protection rules for each table and operation. The protection rules apply to update, insert and delete. The protection levels can't be changed for some tables. The syslog and syslog\_app\_scope tables have fixed values for update and delete protections. The protected\_table\_configuration table has fixed protection values for all three operations.

    **Note:** For sysevent table, insert protections can't be set to block.

    If you had **Apply to Child Tables** turned on for syslog in the previous release, the child tables are added to Log Protection with the same protection rules as syslog upon upgrade to the Utah release. This only happens for syslog, not for any other tables.

4.  Enable the feature by selecting the **Enable Log Protection** toggle.

    **Note:** You can disable this plugin only by changing the com.glide.security.protected\_table.enabled property in the sys\_properties table.


