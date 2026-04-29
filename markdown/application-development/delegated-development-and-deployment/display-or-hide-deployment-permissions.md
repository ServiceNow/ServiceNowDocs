---
title: Display or hide update set deployment permissions
description: Display or hide deployment permissions for update sets from the Manage Developers dialog.
locale: en-US
release: australia
product: Delegated Development and Deployment
classification: delegated-development-and-deployment
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Delegated Development, Planning your application, Building applications]
---

# Display or hide update set deployment permissions

Display or hide deployment permissions for update sets from the Manage Developers dialog.

## Before you begin

Role required: admin

## About this task

System properties control the visibility of the **Publish To Update Set** and **Manage Update Sets** permissions. By default, both deployment permissions for update sets are hidden.

## Procedure

1.  In the Navigation filter, enter `sys_properties.list`.

    The entire list of properties in the System Properties \[sys\_properties\] table appears.

    **Note:** For details on how to add and enable system properties, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

2.  Enable or disable specific deployment permissions by adding or updating the following system properties.

<table id="table_rng_dtq_jdb"><thead><tr><th>

System property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

com.snc.dd.manage\_update\_set\_enabled

</td><td>

Enables or disables display of the **Manage Update Set** permission.The default value of this system property is **false**. To enable the display of this permission, set this value to **true**.

</td></tr><tr><td>

com.snc.dd.publish\_to\_app\_repo\_enabled

</td><td>

Enables or disables display of the **Publish To App Repo** permission.The default value for this system property is **true**. To disable display of this permission, set this value to **false**.

</td></tr><tr><td>

com.snc.dd.publish\_to\_app\_store\_enabled

</td><td>

Enables or disables display of the **Publish To App Store** permission. The default value for this system property is **true**. To disable display of this permission, set this value to **false**.

</td></tr><tr><td>

com.snc.dd.publish\_to\_update\_set\_enabled

</td><td>

Enables or disables display of the **Publish To Update Set** permission. The default value for this system property is **false** by default, which disables display of this permission. To enable the display of this permission, set this value to **true**.

</td></tr><tr><td>

com.snc.dd.upgrade\_app\_enabled

</td><td>

Enables or disables display of the **Upgrade App** permission. The default value for this system property is **true**. To disable display of this permission, set this value to **false**.

</td></tr></tbody>
</table>
