---
title: Highlight alerts by condition in Express List
description: Learn how to apply color-coded highlights to alerts in the Express List based on conditions such as severity, state, and priority, so you can quickly spot critical signals.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/event-management/el-highlight-field-values.html
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-07-27"
reading_time_minutes: 1
breadcrumb: [Assign and manage alerts, Express List in SOW for ITOM, Event Management, ITOM AIOps, IT Operations Management]
---

# Highlight alerts by condition in Express List

Learn how to apply color-coded highlights to alerts in the Express List based on conditions such as severity, state, and priority, so you can quickly spot critical signals.

## Before you begin

Role required: admin

## About this task

To turn on this feature, enable the system property \[sn\_sow\_exp\_app.express\_list\_conditional\_highlighting\]. This property is disabled by default.

## Procedure

1.  Navigate to **All** and search for `sys_highlighted_value_list.do`.

    The Highlighted Values page opens.

2.  In the Highlighted Values filter, set **for text** = `em_alert`.

3.  Select **New** to create a record where you add the highlight conditions.

4.  In the **Table** field, select **Alert\[em\_alert\]**.

5.  In the **Field** field, select the field from the drop-down list.

6.  Right-click the form header and select **Save**.

7.  In the **Highlighted Value Condition** tab, select **New**.

8.  In the Highlighted Value Condition form, fill in only these fields.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Conditions

</td><td>

Define the criteria that trigger the highlight. Select **Add Filter Condition** to add a condition, or Add OR Clause to add an alternative set of conditions. Use **AND** or **OR** to combine multiple conditions, and the red **X** to remove one.

</td></tr><tr><td>

Color

</td><td>

Select the highlight color applied to rows that match the condition \(for example, yellow\).

</td></tr><tr><td>

Application

</td><td>

The application scope in which the condition applies \(for example, Global\).

</td></tr><tr><td>

Order

</td><td>

The sequence in which the condition is evaluated when multiple conditions exist. Lower numbers are evaluated first.

</td></tr><tr><td>

Show Icon

</td><td>

Select this check box to display an icon with the highlight.

</td></tr><tr><td>

Icon

</td><td>

Icon to display \(for example, check-circle-fill\).

</td></tr><tr><td>

Variant

</td><td>

Controls the visual style and emphasis of the highlighted text, including the icon \(for example, primary, secondary, or tertiary\), determining how prominently it appears.

</td></tr><tr><td>

Value Override

</td><td>

Enter a string value to display in place of the field's actual value.

</td></tr><tr><td>

Size

</td><td>

Select the size of the highlight or icon \(for example, Small or Medium\). Medium is the default. **Note:** This is available only from the Australia release.

</td></tr></tbody>
</table>9.  Select **Submit**.

    You return to the Highlighted Values page.

10. In the **UX Highlighted Values Configurations** tab, select **Edit**.

11. In the Collection list, select **SOW Highlighted Value Config** and use the arrow button to move it to the **UX Highlighted Values Configurations** List.

12. Select **Save**.

    The highlight conditions appear on the alerts in the Express List.


