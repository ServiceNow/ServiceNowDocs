---
title: Create a case task to follow up with an exposed employee
description: As a case manager, create case tasks for potentially exposed employees. Assign these tasks to contact tracers to follow up with them to evaluate their health status.
locale: en-US
release: zurich
product: Contact Tracing
classification: contact-tracing
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Managing cases to follow up with potentially exposed contacts, Contact Tracing, Safe Workplace, Health and Safety, Employee Service Management]
---

# Create a case task to follow up with an exposed employee

As a case manager, create case tasks for potentially exposed employees. Assign these tasks to contact tracers to follow up with them to evaluate their health status.

## Before you begin

Role required: sn\_imt\_tracing.case\_manager

## About this task

The [**sn\_imt\_tracing.auto\_create\_case\_tasks**](configure-contact-tracing-properties.md#sysprop_auto_case_task) property, enabled by default, and the **Create case tasks for exposed contacts** workflow cause automatic creation of case tasks when potentially exposed employees are added to a case. If the admin has set the property to No, you must add a case task for potentially exposed employees added to a case.

## Procedure

1.  Navigate to **All** &gt; **Contact Tracing** &gt; **Case Management** &gt; **Cases Assigned to Me**.

2.  Open a case to create case tasks for the potentially exposed contacts.

3.  In the Exposed Contacts related list, select employees for whom you want to create case tasks.

4.  In the Actions on selected rows list, select **Create Task**.

    A task for each selected exposed contact is created and available in the Case Tasks related list. To add a case task for a user not in the exposed contacts list, click **New** in the Case Tasks related list. After creation of the task, the user is added to the Exposed Contacts related list.

5.  In the Case Tasks related list, update the following fields:

    1.  Double-click the **Due date** field and select the date that the task should be completed by.
    2.  Double-click the **Assigned to** field and select a user to work on the task.

        If notifications are enabled, the contact tracers are notified via email.

    **Note:** To update multiple tasks in the list, click in a field, hold the Shift key, and press the Down Arrow or the Up Arrow key. Press the Enter key to open the list editor and enter appropriate values.


## Result

The case tasks are created and assigned to the contact tracers to follow up about the health status of the exposed employees.

## What to do next

The contact tracers can start working on the tasks by [following up with the exposed contacts](contact-exposed-contacts.md) about their health status.

**Parent Topic:**[Managing cases to follow up with potentially exposed contacts](../concept/exposure-case-management.md)

