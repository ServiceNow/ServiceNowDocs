---
title: Assign the workplace user role to employees
description: Set rules in Workplace Core to assign the workplace user role to employees in only the specific countries where you are starting a return to office operations.
locale: en-US
release: xanadu
product: Safe Workplace
classification: safe-workplace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Workplace Core, Safe Workplace, Health and Safety, Employee Service Management]
---

# Assign the workplace user role to employees

Set rules in Workplace Core to assign the workplace user role to employees in only the specific countries where you are starting a return to office operations.

## Before you begin

Ensure that the user profiles of all your employees have required details. You can review the employee user profiles by navigating to **User Administration** &gt; **Users**.

Role required: admin or sn\_wsd\_core.admin

## Procedure

1.  Navigate to **Workplace Safety Management** &gt; **Administration**.

2.  Select **Client Role Assignment Rules**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Unique name for this assignment rule.|
    |Role|This value is auto-generated with the workplace user role \(sn\_wsd\_core.workplace\_user\).|
    |Active|Option for indicating whether this assignment rule is active.|
    |Condition|Option to add filter conditions that a user profile must match. To add a condition, select **Add filter condition**. To add a OR clause, select **Add "OR" clause**.|
    |Table|Table on which the conditions must be built. The field is automatically selected as `sys_user`.|

4.  Select **Submit**.


## Result

The workplace user roles are assigned. If a record is created or updated on this table, a role assignment process is triggered in the background.

