---
title: Delegated Development System Properties
description: The update-set deployment permissions are hidden by default and require a system administrator to enable them with system properties.
locale: en-US
release: zurich
product: Delegated Development and Deployment
classification: delegated-development-and-deployment
topic_type: reference
last_updated: "2025-08-20"
reading_time_minutes: 1
breadcrumb: [Delegated Development reference, Delegated Development, Planning your application, Building applications]
---

# Delegated Development System Properties

The update-set deployment permissions are hidden by default and require a system administrator to enable them with system properties.

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
</table>**Parent Topic:**[Delegated Development reference](delegated-development-reference.md)

