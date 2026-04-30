---
title: Ad hoc cases and tasks for lifecycle event cases
description: You can add an ad hoc task or case to an active lifecycle event case and associate it to a specific activity set. When tasks are added they appear for the subject person under My Tasks or the Review your work in the Employee Center or Employee Center Pro.You can create a case or task and add it to a stage \(bundle\) while a lifecycle event is in progress.
locale: en-US
release: yokohama
product: Lifecycle Events
classification: lifecycle-events
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Create an HR case for a lifecycle event, Using Lifecycle Events, Lifecycle Events, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Ad hoc cases and tasks for lifecycle event cases

You can add an ad hoc task or case to an active lifecycle event case and associate it to a specific activity set. When tasks are added they appear for the subject person under **My Tasks** or the **Review your work** in the Employee Center or Employee Center Pro.

Lifecycle events are a collection of activities \(services, tasks, requests, notifications, etc.\) that are organized to provide an employee experience. Examples of an employee experience are new hire onboarding or when an employee takes parental leave. In a lifecycle event, all employees that are part of a specific audience go through the same experience.

Ad hoc tasks or cases are not part of an original lifecycle event configuration. Ad hoc tasks or cases can be added to an existing stage or bundle of a lifecycle event that is in progress and active.

**Note:** You cannot add a task or case to a closed or completed activity set.

When an agent adds an ad hoc task or case, it also becomes visible to the Subject person in the Employee Center or their mobile device. This allows the Subject person of a case to perform a task or respond to a request.

Adding an ad hoc case or task to an active lifecycle event case provides agents with flexibility that does not disturb the original structure.

Examples of when an ad hoc task or case are useful:

-   **Extend family leave**

    An employee is on parental leave, but wants to extend their leave.

    An agent can add a new case to the employee's parental leave lifecycle event that extends their leave.

    Adding a new case that extends an employee's parental leave becomes a child case of the parent lifecycle event case.

-   **Changing personal information during onboarding**

    Another example is when a new hire is going through the onboarding process of a lifecycle event.

    A new hire wants to change personal information, but there is no way to do this while onboarding.

    An agent can create a new task for the new hire that appears in the current activity set as a to-do.

-   **Required plugins**

    To use the lifecycle event ad hoc feature, the following plugins are required:

    -   Human Resources Scoped App: Core \[com.sn\_hr\_core\]
    -   Human Resources Scoped App: Lifecycle Events \[com.sn\_hr\_lifecycle\_events\]
-   **Optional plugins**

    The following plugins are optional that allows you to create or view ad hoc tasks or case in alternative places:

    -   Human Resources Scoped App: Workspace \[com.sn\_hr\_agent\_workspace\]
    -   Playbook Experience \[com.playbook\_experience\]

## Create an ad hoc case or task

You can create a case or task and add it to a stage \(bundle\) while a lifecycle event is in progress.

### Before you begin

Role required: sn\_hr\_le.case\_writer

### Procedure

1.  Navigate to **All** &gt; **Lifecycle Events** &gt; **Lifecycle Events Cases**.

2.  Select a case that has a state that is active \(for ad hoc tasks only\).

    **Note:** To add an ad hoc case, the lifecycle event case cannot be in the Closed Complete, Closed Incomplete, or Cancelled, states.

3.  Scroll down to the Related Links section of the case form.

4.  Select **Add a child case** or **Add task**.

    For more information, see [Create an HR case for a lifecycle event](../task/create-hr-lifecycle-event-case.md) and [Adding an HR task to an HR case](../task/t_ViewAnHRTask.md).

5.  After filling in the required fields, ensure you select a value from the **Stage** field.

    For an HR case, the **Stage** field is located in the Case Details section. For an HR task, the **Stage** field is between the **Template** and **Display order** fields.

    If you do not associate a task or case with a stage in the lifecycle event, the task or case becomes a child of the parent case, but is not included in the lifecycle event.

    **Note:** Stage is also known as an activity set or bundle. For more information, see [Configure a lifecycle event activity set](../task/configure-hr-lifecycle-event-activity-set.md).


