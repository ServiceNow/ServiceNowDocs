---
title: Deactivate a function field
description: The user who created a function field or a user with the admin role can deactivate it. If there are more than 20 function fields on a table, you can’t create a new function field without deactivating one or more existing ones.
locale: en-US
release: xanadu
product: Reporting
classification: reporting
topic_type: task
last_updated: "2025-09-09"
reading_time_minutes: 1
breadcrumb: [Report on function fields, Advanced reporting topics, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Deactivate a function field

The user who created a function field or a user with the admin role can deactivate it. If there are more than 20 function fields on a table, you can’t create a new function field without deactivating one or more existing ones.

## Before you begin

Role required: admin

## Procedure

1.  Perform one of the following actions:

    -   On an upgraded instance that has not been fully migrated to Platform Analytics, navigate to **All** &gt; **Reports** &gt; **Create New**.
    -   On a new instance or one that has been fully migrated to Platform Analytics, navigate to **All** &gt; **Platform Analytics Administration** &gt; **Usage and governance** &gt; **Reports** and select **New**.
2.  Select the report with the function field to deactivate.

3.  Open the **Configure** tab and select **Configure function field**.

4.  Enter text in the **Search functions** box to find the function field you want to deactivate.

5.  Select the function field and choose **Deactivate**.

    If one or more reports use the function field, you see a link to a list of those reports. You can review the list, choose **Deactivate anyway**, or select **Cancel**.

6.  Confirm the deactivation or cancel.


## Result

The deactivated function field is no longer available for use in the reports on the table that it was based on.

**Note:** When you deactivate a field, the user list preference is deleted.

**Parent Topic:**[Report on function fields](../concept/function-fields-reporting.md)

