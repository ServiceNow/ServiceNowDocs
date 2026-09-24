---
title: Template item condition form
description: The Template item condition form displays displays the conditions that apply to a that template item.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/task-plan-template-item-condition-form.html
release: brazil
topic_type: reference
last_updated: "2026-09-04"
reading_time_minutes: 2
breadcrumb: [Customer Service forms, Reference, Customer Service Management]
---

# Template item condition form

The Template item condition form displays displays the conditions that apply to a that template item.

The Template item condition form includes the following fields on the Details tab.

<table id="table_vyg_gzg_lvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Short description

</td><td>

A brief description of the template item condition.

</td></tr><tr><td>

Template item

</td><td>

The number of the parent template item.

</td></tr><tr><td>

Condition table

</td><td>

The table on which the condition is applied.By default \(when **Advanced** is unchecked\), you select one of the following:

-   The same table as the **Target record** in the task plan template.
-   The parent template item's table.

When **Advanced** is selected, this field instead lists tables that share the reference selected in the **Base table mapping field**.

</td></tr><tr><td>

Condition

</td><td>

Use this field to add the conditions for the template item. Each condition contains a field, operator, and value\(s\).Select **Set conditions** to display the Condition pop-up window.

-   Add a condition for the template item that contains a field, operator, and value.
-   Select **+New condition set** to add a new condition.
-   Select **x** to remove a condition.
-   Select **Set** to save the conditions and close the pop-up window

</td></tr><tr><td>

Advanced

</td><td>

Select this check box to instead configure the condition on a table that shares a reference with the target table or parent template item table, rather than on that table directly. When **Advanced** is selected, the **Condition table** field lists tables that share the reference selected in **Base table mapping field**. Three additional fields appear and are mandatory: **Base table**, **Base table mapping field**, and **Condition table mapping field**.

Selecting or clearing this check box displays a **Change Advanced settings?** confirmation dialog before the change takes effect. See [Create a template item condition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/create-task-plan-template-item-condition.md) for the exact behavior.

</td></tr><tr><td>

Base table

</td><td>

Displayed when **Advanced** is selected. Select the parent template item's table or the task plan template's target record table. This is the table that the related table in **Condition table** must share a reference with.

</td></tr><tr><td>

Base table mapping field

</td><td>

Displayed when **Advanced** is selected. Select a reference field on the **Base table**. The **Condition table** field then lists tables that share this same reference.

</td></tr><tr><td>

Condition table mapping field

</td><td>

Displayed when **Advanced** is selected. Select the field on the **Condition table** that matches the reference selected in **Base table mapping field**.

</td></tr></tbody>
</table>