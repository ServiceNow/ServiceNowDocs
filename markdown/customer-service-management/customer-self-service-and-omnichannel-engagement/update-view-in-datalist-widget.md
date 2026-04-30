---
title: Modify view in the Data List widget
description: Create a condition script to modify views in the Portal Data List widget.
locale: en-US
release: zurich
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2026-01-31"
reading_time_minutes: 1
breadcrumb: [Portal Data List widget, Set up Configurable Portal widgets, Set up self-service, Configure, Customer Service Management]
---

# Modify view in the Data List widget

Create a condition script to modify views in the Portal Data List widget.

## Before you begin

The UI Components for Customer Portals plugin must have been activated. For more information, see [Activate the UI Components for Customer Portals plugin](activate-config-portal-widget.md)

Role required: sp\_admin

## About this task

<table id="table_k4r_1s5_c3c"><thead><tr><th>

Priority

</th><th>

Source

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1 \(Highest\)

</td><td>

Script

</td><td>

If a Views Condition Script is configured and returns a view name, that view is used. Scripts have the most flexibility since they can apply custom logic using the parameters - `categoryId`, `params`.

</td></tr><tr><td>

2

</td><td>

role\_based\_views / guest\_view

</td><td>

If no script is configured or the script doesn’t return a view, the system checks the JSON instance options. -   For logged-in users, it checks `role_based_views` to find a view matching the user's roles.
-   For non-logged-in users, it uses `guest_view`

.

</td></tr><tr><td>

3

</td><td>

view

</td><td>

The widget uses the view JSON instance option if the script or role based view/guest view mappings doesn’t apply.

</td></tr><tr><td>

4 \(Lowest\)

</td><td>

Default View on Platform

</td><td>

If no other configuration applies, the widget uses the platform’s default view for the table.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **System Extensions Points** &gt; **Scripted Extensions Points**.

2.  On the Extension Points page, in the **API Name column** search field, enter `*datalist`.

3.  Select the **sn\_ciwf\_ui\_cmpnt.DatalistCategoryConditionScript** in the **API Name** column.

    If a message appears about the application scope, select **here** to be able to edit the record.

4.  On the DatalistCategoryConditionScript page, in the Related links, select **Create implementation**.

5.  In the **Script** field, paste the following CSS code:

    ```
    
    getView: function(category_id, params) {
        return "case"; // view
    }
    
    ```

<table id="table_r5r_kyx_13c"><thead><tr><th>

Parameters

</th><th>

Description

</th></tr></thead><tbody><tr><td>

category\_id

</td><td>

Portal Data list category id.

</td></tr><tr><td>

params

</td><td>

JSON containing url\_params and related\_table. For example,```

{
  "url_params": {
    "table": "customer_contact",
    "sys_id": "60beb5e7d7600200e5982cf65e6103ad",
    "view": "sp"
  },
  "related_table": "sn_customerservice_case"
}

```

</td></tr></tbody>
</table>6.  Copy the name of a condition script from the **Name** field.

7.  Select **Update**.

8.  Navigate to your portal home page.

9.  On the Data List widget, press Control+right-click.

10. Select **Instance Options**.

11. In the Behavior section, paste the name that you copied into the **Data List condition script** field.

12. Select the condition script from the list.

13. Select **Save**.


