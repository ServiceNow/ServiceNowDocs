---
title: Assign PPE to employees
description: You can assign PPE directly to an employee without them submitting a request.
locale: en-US
release: zurich
product: Safe Workplace
classification: safe-workplace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Workplace PPE Inventory Management, Safe Workplace, Health and Safety, Employee Service Management]
---

# Assign PPE to employees

You can assign PPE directly to an employee without them submitting a request.

## Before you begin

Role required: sn\_imt\_ppe.ppe\_admin

## About this task

If an employee submits a request for PPE, follow the steps to [Fulfill a request for PPE](fulfill-ppe-request.md) instead.

When you assign hardware PPE to an employee, the state changes from **In stock** to **In use**. The state can be updated and the item can be reassigned to another employee.

When you assign consumable PPE to an employee, a consumable record is created with the quantity allocated to the employee. The state is set to **Consumed** and is read-only. Consumable PPE cannot be reassigned to another employee.

**Note:** Don't use the **Consume** button on consumable records to assign PPE. Instead, use the following steps.

## Procedure

1.  Navigate to **PPE Inventory Management** and select **Assign Consumable** or **Assign Hardware**.

    **Note:** To assign PPE in the Now Mobile app, navigate to **Health** &gt; **Manage PPE Inventory** and select **Assign Consumable** or **Assign Hardware**.

2.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Model|The model to assign.|
    |Issuing stockroom|The stockroom where the PPE is located.|
    |Assigned to|The employee that you're assigning PPE to.|
    |Quantity|The number of items to assign. This field is only available for consumable models.|
    |Hardware|The specific item to assign, with a unique asset tag or serial number. This field is only available for hardware models.|

3.  Click **Submit**.

    The assignment log is updated with the PPE you assigned. To view the assignment log, navigate to **PPE Inventory Management** &gt; **Assignment Log**.


## What to do next

After assigning PPE to employees, you can view all assigned PPE by navigating to **PPE Inventory Management** &gt; **Inventory** and selecting **Assigned Hardware** or **Consumed**.

**Note:** The **Assigned Hardware** and **Consumed** pages have a **New** button. Do not assign PPE using the **New** button. Using this button does not update the assignment log.

**Parent Topic:**[Workplace PPE Inventory Management](../concept/ppe-inventory-management.md)

