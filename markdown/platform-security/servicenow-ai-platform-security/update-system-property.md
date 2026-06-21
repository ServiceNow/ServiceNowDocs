---
title: Update system property
description: Update the glide.les.disable\_logs\_forwarding system property within the Log Export Service application to control log forwarding during migration or database reseeding operations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/servicenow-ai-platform-security/update-system-property.html
release: australia
product: ServiceNow AI Platform Security
classification: servicenow-ai-platform-security
topic_type: task
last_updated: "2026-06-21"
reading_time_minutes: 1
breadcrumb: [Administer, Log Export Service \(LES\), Platform Security]
---

# Update system property

Update the glide.les.disable\_logs\_forwarding system property within the Log Export Service application to control log forwarding during migration or database reseeding operations.

## Before you begin

Role required: admin

## About this task

This property controls whether log forwarding is active in Log Export Service. By default, the value is set to **false**, meaning logs are forwarded normally. During database reseeding or migration, historical log records can be replayed or reprocessed, which may result in duplicate log exports to downstream systems. To prevent duplicate logs from being sent, set this property to **true** to temporarily pause LES forwarding. After the migration is complete, revert the value to **false** to resume normal operation.

## Procedure

1.  Navigate to **All** &gt; **Log Export Service** &gt; **Sources**.

2.  In the workspace filter navigator, enter **sys\_properties.list** to access the system properties list.

    This opens the full list of system properties.

3.  In the Name column, search for **glide.les.disable\_logs\_forwarding**.

    In case you do not find the property **glide.les.disable\_logs\_forwarding**, you can create a new system property by following these steps:

    1.  Select **New** on the top-right corner of your screen to create new system property.

    2.  In the **Name** field enter **glide.les.disable\_logs\_forwarding**.

    3.  In the **Type** field, select **true \| false**.

        Only the **Name** and **Type** fields are required. All other fields are optional and can be left empty.

4.  Open the record.

5.  The default value is **false**, which means log forwarding is active.

6.  In the **Value** field, set the value based on your requirement:

<table><tbody><tr><td>

**Property**

</td><td>

**Value**

</td><td>

**When to use**

</td></tr><tr><td>

**glide.les.disable\_logs\_forwarding**

</td><td>

**true**

</td><td>

During migration or DB reseeding, this disables log forwarding.

</td></tr><tr><td>

**glide.les.disable\_logs\_forwarding**

</td><td>

**false**

</td><td>

Default. After migration is complete, this re-enables log forwarding.

</td></tr></tbody>
</table>7.  Select **Update** to save the change.


## Result

When the property is set to **true**, Log Export Service stops forwarding logs, ensuring no data is sent during a migration or DB reseeding event. Once the operation is complete and the value is reverted to **false**, log forwarding resumes automatically. This configuration allows administrators to safely pause log forwarding during maintenance windows without affecting the underlying LES configuration.

**Warning:** After migration or database reseeding is complete, revert the property value to **false**. If you do not revert this setting, log forwarding stops permanently and may result in missing log data in downstream systems.

**Parent Topic:**[Administering Log Export Service \(LES\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/servicenow-ai-platform-security/les-administer.md)

