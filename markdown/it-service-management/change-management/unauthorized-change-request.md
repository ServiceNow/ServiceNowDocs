---
title: Unauthorized change request
description: Understand how an unauthorized change activity on a configuration item \(CI\) is captured and managed, so that you can review and take timely action on this change.
locale: en-US
release: zurich
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Create a change request, Use, Change Management, IT Service Management]
---

# Unauthorized change request

Understand how an unauthorized change activity on a configuration item \(CI\) is captured and managed, so that you can review and take timely action on this change.

As part of the ServiceNow® Service Mapping integration with ServiceNow® ITSM, the Change Management application receives an event notification when an unauthorized change activity is detected. As a result, an emergency unauthorized change request is created for the relevant CI. You can review and approve or reject the unauthorized change from the Change Management application.

**Note:** Unauthorized change requests are created only for the CIs that are part of the application services. Also, there is a flapper algorithm that uses a learning pattern to minimize false positives.

At times, the discovery process \(horizontal or top-down discovery\) identifies a change on a CI property that may not be an actual change by definition. This identification is due to a measurement error or just a different representation of the same value, such as case sensitivity. The learning pattern identifies the false positives \(flapper changes\) and prevents triggering the recomputation and time-line updates as an emergency change request is a critical action. You want to avoid false positives and report only real changes.

The learning pattern identifies the false positives as follows:

1.  When a CI property associated with a service changes, the new value \(CI and field pair\) is logged in the flapper’s data table.
2.  The system runs a nightly job and executes various algorithms on the data that is collected to identify patterns that point to false positives.
3.  The system runs all the relevant strategy predicates for the changed CI fields with a confidence level greater than 90%. This step determines whether all the new values are false positives or not. If all the new values are false positives, then the change is ignored, and the model is not updated.

    **Note:** If the CI is associated with an active change request, then this step is skipped.


An unauthorized change request is created when an unplanned CI change activity occurs, and the system triggers the following checks:

-   The system checks to see if the CI is part of the allowed CI classes. If it is allowed, then the system checks to see if this specific CI has been flagged previously. If it was flagged and the previously created unauthorized change was within the notification ignore period, then no further action is taken. If not, then further checks are made to see whether this CI is associated to a change request that matches the condition stated in the properties. If not, then the change to the CI that was detected is flagged as unauthorized and a **ci.change.unplanned** event is raised.
-   On receipt of the **ci.change.unplanned** event, the script checks to see if the **Enable event processing** field is **true**. If it is **true**, then an unauthorized change request is created. By default, this property is **false**.

The **ci.change.unplanned** event that is generated automatically triggers the creation of an Emergency type change request.

With the help of the following details that are pre-populated on the form, you can identify and review the unauthorized change:

-   The **Unauthorized** option is selected. This option indicates that the change is an unauthorized change.
-   The **Assignment group** field is populated with **Change Management**.
-   The **Configuration item** field is populated with the item that the unauthorized change was made for.
-   The **Description** field is populated with the information on the changed fields of the change request.

An email notification is sent to the Assignment group, CI Item managed by, Owned by, and Assigned to members for review and approval. However, if there are many CI changes and there are no open change requests created to include the CIs, the system creates unauthorized change requests on these CIs. When this event occurs, the members receive numerous unauthorized change notification emails. In such a case, you can choose to disable these notifications. For more information, see [Disable unauthorized change notification](../task/disable-unauth-notification.md).

**Note:** Email notifications are sent only when there is an unplanned change on the CI that is part of an application service \(discovered or manual service\).

After this change request is approved, the state changes to **Review** and the regular process is followed to close the request.

## Assign post-implementation review

When a change is implemented without approval, post-implementation review is necessary to evaluate the risk and impact of the unauthorized change.

After the unauthorized change is approved, a change task is created with **State** field as **Review**. This change task is assigned to the Change Management group with the **Short description** field as **Post Implementation Review**. The assigned members who receive the notification can review and close the change task.

## Modify the unauthorized change setting

As a change manager, you can clear the **Unauthorized** check box to convert the unauthorized change request to an emergency change request. When you clear the check box, enter the reason for this modification in the **Work notes** field.

If you are an ITIL user, clear the **Unauthorized** check box by creating an outage from the task record with the **Type** field specified as `Outage`. For more information, see [Create an outage from a task](../../task-outage/task/t_CreateAnOutageFromATask.md).

**Note:** When there is an unauthorized change without an outage record associated, then the state flow moves from **Authorize** to **Review** and skips the schedule or implement state. The state changes because the implementation has already happened for this change.

-   **[Disable the creation of an unauthorized change request](../task/disable-unauth-notification.md)**  
You can choose to disable the generation of unauthorized change requests that you receive on any unauthorized change event. When a configuration item \(CI\) that is part of an application service is updated, the system identifies this update and verifies whether the updated CI is part of an open change request.
-   **[Unauthorized change properties](../reference/unauth-change-properties.md)**  
Use the Unauthorized Change Properties page to enable or disable the unauthorized change capability, and to configure the criteria for additional unauthorized change properties.

**Parent Topic:**[Create a change request](../task/t_CreateAChange.md)

**Related topics**  


[Create a change request from a configuration item \(CI\)](../task/t_CreateAChangeFromACI.md)

[Create a standard change request from the catalog](../task/t_RaiseNewStdCngeFmTempl.md)

[Copy a change request](../task/copy-a-change-request.md)

[Create a change task](../task/create-a-change-task.md)

