---
title: Customizing UI actions for the Now Mobile Agent application
description: Make it easier for your end users to get things done faster with the Field Service mobile application by creating custom UI actions.
locale: en-US
release: zurich
product: Mobile Experience for Field Service Management
classification: mobile-experience-for-field-service-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure the Now Mobile Agent application, Setting up Field Service Mobile Agent, Configure, Field Service Management]
---

# Customizing UI actions for the Now Mobile Agent application

Make it easier for your end users to get things done faster with the Field Service mobile application by creating custom UI actions.

The configurations for UI action conditions are different in Field Service mobile applications than those in the desktop application. Unlike the desktop application, the UI action conditions on mobile don’t execute any database queries and therefore don’t take up mobile resources. On the mobile application, instead of performing a system check on whether a Field Service configuration is enabled, you can configure the button to be active or inactive.

As an administrator, you can review the mobile UI actions and disable the ones that aren’t being used to use less mobile resources.

The following image shows the Now Mobile Agent application open in Studio. The Now Mobile Agent application open in Studio is where you can configure UI actions.

Here's a sample UI action configuration for accepting a work order task.

The **Accept** button on the desktop application has the following UI action conditions:

```
current.state == 16 && (new StateFlow().validFlow(current, '53d0aea8d7230100fceaa6859e610326', 'manual'));
```

The system checks these state flow conditions:

1.  The `SMconfiguration` record to see if the **accept\_reject** UI action is enabled or disabled using this script:

    ```
    (new sn_sm.SMConfiguration()).isEnabled(current, "accept_reject", false)
    ```

2.  If the task has been self-assigned

To modify the UI action for the corresponding button on your mobile device:

1.  Don’t change the `current.state == 16` condition. It checks for information on the current record.
2.  If this condition:

    ```
    (new sn_sm.SMConfiguration()).isEnabled(current, "accept_reject", false)
    ```

    is set to **false**, drop this condition and disable the corresponding mobile UI actions on the mobile application.

3.  Set the value for the **current tasks assigned to** field parameter to the logged-in user as shown here: `current.assigned_to == gs.getUserID()`

Based on the preceding example, here’s the modified condition for the UI action in the mobile application:

```
current.state == 16 && current.assigned_to == gs.getUserID()
```

Here’s another sample configuration for self-assigning a task.

The **Assign to Me** function on the desktop application has the following UI action conditions:

```
(new SMTask()).canAssignToSelf(current)
```

The `SMTask.canAssignToSelf(task)` script include method performs a system check for these conditions:

1.  State of the task
2.  Value of the scheduled start time
3.  If the task has been self-assigned
4.  If the user has the basic and agent roles as defined in the SM Configuration record
5.  Whether the user is part of a group handled by the task dispatch group

On the mobile application, the following UI script condition performs a check for the first three conditions listed before:

```
current.assigned_to != gs.getUserID() && !(current.expected_start.nil()) && (current.state == 10 || current.state == 16) 
```

For the fourth condition, you can add a specific role to the **Roles** field.

For the fifth condition, perform the following validation in the `wot_assign_to_me` write-back action item:

```
if (smTask.canAssignToSelf(wotGR)) 
smTask.assignToMe(gs.getUserID(), input.sys_id); 
else
gs.addErrorMessage(gs.getMessage("Not a valid task assignment."));
```

