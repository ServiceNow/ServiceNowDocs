---
title: Set up Employee Health and Safety Status properties
description: Set up Employee Health and Safety Status properties to configure the email notifications that are sent to visitors.
locale: en-US
release: yokohama
product: Employee Readiness Core
classification: employee-readiness-core
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Employee Health and Safety Status, Employee Readiness Core, Safe Workplace, Health and Safety, Employee Service Management]
---

# Set up Employee Health and Safety Status properties

Set up Employee Health and Safety Status properties to configure the email notifications that are sent to visitors.

## Before you begin

Role required: sn\_imt\_core.admin

## Procedure

1.  Navigate to **All** &gt; **Employee Health and Safety Status** &gt; **Properties**.

2.  Set the following property values.

    |Property|Description|
    |--------|-----------|
    |sn\_imt\_core.send\_email\_to\_visitor|When enabled, the **Notify about scheduled visit** email notification is sent to the visitor when an employee invites them to the workplace. The email is sent immediately after the employee submits the invitation. The email contains a brief confirmation of the scheduled visit, including information about the date of the visit and the name of the employee who invited them.|
    |sn\_imt\_core.days\_to\_ask\_for\_health\_data|Sets the number of days before the scheduled visit that the **Ask for health related data from visitor** email notification is sent to the visitor. The email contains information about safety requirements and policies that the visitor must agree to follow. The visitor must respond `Yes` to the email to complete the [Visitor Invitation Requirement](../reference/included-health-safety-requirements.md).|

    For more information about the email notifications used by the properties, see [Modify visitor notification emails](../../employee-health-screening/task/configure-health-screening.md#).

3.  Click **Save**.


**Parent Topic:**[Employee Health and Safety Status](../concept/employee-health-safety-status.md)

