---
title: Apply a work order template
description: Work order templates enable users with the proper roles to automatically create work orders, tasks, and part requirements.
locale: en-US
release: yokohama
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Manage work orders, Prepare work orders, Using Field Service Management, Field Service Management]
---

# Apply a work order template

Work order templates enable users with the proper roles to automatically create work orders, tasks, and part requirements.

## Before you begin

Role required: wm\_admin or model\_manager

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Work Order** &gt; **Create New**.

2.  Select the desired work order template from the **Template** field and save the form.

    The template information is used to:

    -   Copy the short description, priority, and billable status to the work order. The system also copies the qualification group to the work order form if this field is present. Qualification groups are not required when [automatic qualification](../../planning-and-policy/concept/c_QualifyWorkOrders.md#AutomaticConfiguration) is configured. Work orders created from an incident, problem, or change request display the short description from the source task, even when a template is selected. Tasks for work orders created from templates always display the short description from the task template.
    -   Create work orders tasks, using the information from the work task templates.

        **Note:** The fields such as **Territory** and **Dispatch Group** are automatically populated based on the selected **Location** irrespective of the work order template or state only if the **Field\_Service\_Territories** territory model is enabled. For more information, see [Enable the Field Service territory model](../../field-service-management/task/enable-territory-model.md).

    -   Create the parts requirements. If a part specified is out of stock, the system displays a message naming the part.

**Parent Topic:**[Manage work orders](../../planning-and-policy/concept/c_ManageWorkOrders.md)

