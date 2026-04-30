---
title: Edit a function field
description: The user who created a function field or a user with the admin or function\_field\_admin role can edit the definition of a saved function field. It isn’t possible to edit the label or the return type of a saved function field.
locale: en-US
release: xanadu
product: Reporting
classification: reporting
topic_type: task
last_updated: "2025-07-18"
reading_time_minutes: 1
breadcrumb: [Report on function fields, Advanced reporting topics, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Edit a function field

The user who created a function field or a user with the admin or function\_field\_admin role can edit the definition of a saved function field. It isn’t possible to edit the label or the return type of a saved function field.

## Before you begin

Role required: admin, function\_field\_admin

## Procedure

1.  Perform one of the following actions:

    -   On an upgraded instance that has not been fully migrated to Platform Analytics, navigate to **All** &gt; **Reports** &gt; **Create New**.
    -   On a new instance or one that has been fully migrated to Platform Analytics, navigate to **All** &gt; **Platform Analytics Administration** &gt; **Usage and governance** &gt; **Reports** and select **New**.
2.  Select a report based on the table that you want to add a function field to.

    When you configure a function field, it is available in any report on the same table. For example, a function field that calculates how long incidents have been open is available for all reports on the incident table.

3.  Open the **Configure** tab and select **Configure function field**.

4.  Enter text in the **Search functions** box to find the function field you want to edit.

    Search functionality searches on the Label of the field, the name of the field, and the function definition.

5.  Select a new operation, new fields the function operates on, or both.

    Validation of the edited function may indicate that it returns an invalid result.

6.  Select **Save**.

    If one or more reports use the function field, you see a link to a list of those reports. You can review the list, select **Save anyway**, or select **Cancel**.


## Result

The results of the edited function field replace the old results in all reports in which the function field is used.

**Parent Topic:**[Report on function fields](../concept/function-fields-reporting.md)

