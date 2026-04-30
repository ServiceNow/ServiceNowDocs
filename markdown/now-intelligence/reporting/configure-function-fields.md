---
title: Configuring function fields
description: You can configure up to 20 active function fields per table using the Report Designer. When you configure a function field on a table, you can group or stack by the results of the function calculation.
locale: en-US
release: yokohama
product: Reporting
classification: reporting
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Report on function fields, Advanced reporting topics, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Configuring function fields

You can configure up to 20 active function fields per table using the Report Designer. When you configure a function field on a table, you can group or stack by the results of the function calculation.

Role required: admin, function\_field\_admin.

While regular fields store a value in the database, a function field displays the results of a database query. The function field generates the value based on computations of other fields and constants. You can use these fields in reports and data visualizations as you would other fields.

Limitations:

-   Function fields in reporting do not support dot walking.
-   Security is evaluated on the components of the function and on the calculated value of the field. When used in visualizations, sections that contain information that the user is not allowed to see are hidden from the user.
-   Only the creator of a function field or a platform admin can edit or deactivate that field. Platform admins can deactivate any function field.
-   Field function names must be unique.
-   Only 20 function fields can be active on a table at any one time. To add function fields, you must deactivate others. See [Deactivate a function field](delete-function-field.md).

**Parent Topic:**[Report on function fields](../concept/function-fields-reporting.md)

