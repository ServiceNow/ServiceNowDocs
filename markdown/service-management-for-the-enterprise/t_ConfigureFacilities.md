---
title: Configure Facilities Service Management
description: Facilities administrators can set facilities configurations to determine how the system handles daily operations.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Activate Facilities Service Management, Facilities Service Management overview, Facilities Service Management, Service Management]
---

# Configure Facilities Service Management

Facilities administrators can set facilities configurations to determine how the system handles daily operations.

## Before you begin

Role required: facilities\_admin

## About this task

Facilities Service Management defaults to the request-driven processing method for handling tasks. For information about both processing methods, see [Task vs. request driven processing](../../planning-and-policy/concept/c_TaskVsRequestDrivenProcessing.md).

## Procedure

1.  Navigate to **All** &gt; **Facilities** &gt; **Administration** &gt; **Configuration**.

    **Note:** Administrators in domains lower than the global domain can view the Configurations screen, but cannot modify the settings.

    The options on the configuration screen are arranged in a multiple-tabbed layout, as follows:

    -   The **Business Process** tab contains options for setting up the request life cycle, creating catalogs and requests, and configuring notifications.
    -   The **Assignment** tab contains options for setting up manual and auto-assignment.
    -   The **Add-ons** tab contains options for enabling the knowledge base, managed documents, and task activities.
2.  Fill in the fields on the **Business process** tab.

    **Note:** The Configuration screen contains many configuration options. An option is enabled when the switch appears green and is toggled to the right. All configuration options listed in the **Dependency** must be enabled in order for the option to be displayed.

<table id="table_h44_tnx_5r"><thead><tr><th>

Field

</th><th>

Description

</th><th>

Dependency

</th></tr><tr><th class="sub-head" colspan="2">

Lifecycle

</th><th>

 

</th></tr></thead><tbody><tr><td>

Enable state flows

</td><td>

Enable state flows consistent with all [service management applications](../../it-services/concept/c_ServiceManagement.md). If you prefer to create your own state flows using business rules, client scripts, and UI actions, disable the option. A confirmation box displays and includes a link to a help article that describes the implications of disabling state flows. It is highly recommended that you read the article before proceeding.

 If you disable state flows and save, this configuration option is removed from the screen and state flows cannot be re-enabled from the user interface.

</td><td>

 

</td></tr><tr><td>

Process life cycle

</td><td>

Select **request driven \(subtasks are optional\)** if you do not want to require tasks to fulfill requests. When the request life cycle is request driven, requests can be directly assigned to users in an assignment group. Users can still add tasks to requests. However, closing all tasks does not automatically close the request. **Note:** If the **Enable state flows** option is not selected, the process life cycle becomes**request-driven** and this field is not displayed.

</td><td>

**Enable state flows** is turned on.

</td></tr><tr><td>

Agent must accept or reject the assigned task

</td><td>

Enable to require the assigned agent to accept or reject the task.

</td><td>

**Enable state flows** is turned on.

</td></tr><tr><td>

Work notes are required to close or cancel a request or task

</td><td>

Enable if work notes are required when closing, completing, or canceling requests and tasks. If it is disabled, work notes are not needed when closing, completing, or canceling.

</td><td>

 

</td></tr><tr><td>

Copy task work notes to request

</td><td>

Enable to synchronize task work notes with the work notes on the order or request. When work notes are added in the task, the same work notes appear in the order or request.

</td><td>

**Enable state flows** is turned on.

</td></tr><tr class="sub-head"><td class="sub-head" colspan="3">

**Catalog and Request Creation**

</td></tr><tr><td>

Create or update requests by inbound email.

</td><td>

Enable this option to allow inbound email messages to create or update requests. This option must be enabled to allow requests to be marked as spam.

</td><td>

 

</td></tr><tr><td>

Requests are created using

</td><td>

Select **catalog or regular form** to install the catalog and enable automatic publishing of request templates to the catalog.Select **regular form only** to uninstall the catalog and disable automatic publishing of request templates to the catalog.

</td><td>

 

</td></tr><tr><td>

Templates create a dedicated catalog item

</td><td>

Enable this option to allow automatic publishing of catalog items for the application.

</td><td>

 

</td></tr><tr class="sub-head"><td colspan="3">

**Notifications**

</td></tr><tr><td>

Send a notification when a field changes for a task or request.

</td><td>

Configure notifications to be sent to specific recipients when selected fields in requests and/or tasks change. 1.  From **Table**, select **Request** or **Task**.
2.  From **Field**, select the field to use for generating notifications. When a change is made to the selected field, a notification is sent to the recipients identified.
3.  From **Recipients**, select one or more recipients
4.  If **a specific user** or **a specific group**, is selected, the user is prompted to select a user or group.
5.  To define more notifications using other fields or recipients, repeat the steps on the next line.
6.  To remove a notification, click the ![delete notification symbol](../../planning-and-policy/image/DeleteNotification.png) symbol to the right of the notification.


</td><td>

 

</td></tr></tbody>
</table>3.  Click the **Assignment** tab and fill in the fields.

<table id="table_yl5_vns_5r"><thead><tr><th>

Field

</th><th>

Description

</th><th>

Dependency

</th></tr></thead><tbody><tr class="sub-head"><td class="sub-head" colspan="3">

Assignment method for tasks: Manually

</td></tr><tr><td>

Assign requests or tasks based on assignment group coverage areas

</td><td>

Enable this option to limit the selection of groups from the **Dispatch group** and **Assignment group** fields to groups that cover the location of the task.

</td><td>

 

</td></tr><tr class="sub-head"><td colspan="3">

**Scheduling**

</td></tr><tr><td>

Use agent or task scheduling

</td><td>

Enable this option to allow agent auto-assignment and agent auto-selection.

</td><td>

 

</td></tr><tr><td>

Auto-selection of agents will consider time zone for tasks

</td><td>

Enable this option to consider the time zone of the agent when assigning a task.

</td><td>

**Enable state flows** is turned on.

</td></tr><tr><td>

Enable priority assignment

</td><td>

Enable this option to use priority assignment for auto-assigning agents.

</td><td>

-   **Enable state flows** is turned on.
-   **Process life cycle: Life cycle is task driven**.
-   **Auto-selection of agents will consider agent or task schedules**.
 **Note:** The **Process life cycle** option is not available in all service management applications.

</td></tr><tr><td>

Select priorities for priority assignment

</td><td>

Select priorities for assignment.

</td><td>

-   **Use agent or task scheduling** is turned on.
-   **Enable priority assignment** is turned on.


</td></tr><tr class="sub-head"><td colspan="3">

**Additional Factors**

</td></tr><tr><td>

Auto-selection of agents will consider location of agents

</td><td>

Enable this option to use the agent and location when determining who to assign the task to. Agents closer to the task location receive preference.

</td><td>

-   **Enable state flows** is turned on.
-   If using **Process life cycle: Life cycle is task driven**, then **Assignment method for tasks: using auto-assignment**.
-   If using **Process life cycle: Life cycle is request driven**, then **Assignment method for requests: using auto-assignment**.


</td></tr><tr><td>

Auto-selection of agents for tasks requires them to have skills

</td><td>

This option determines the degree to which skills must be matched to a task when determining auto-assignment. -   Select **all** to require that an assigned agent has all the skills to perform the task. An agent who lacks one skill is eliminated.
-   Select **some** if you want agents who have most of the skills to perform the task.
-   Select **none** if you want to auto-assign agents without considering skills.


</td><td>

-   **Enable state flows** is turned on.
-   If using **Process life cycle: Life cycle is task driven**, then **Assignment method for tasks: using auto-assignment**.
-   If using **Process life cycle: Life cycle is request driven**, then **Assignment method for requests: using auto-assignment**.


</td></tr></tbody>
</table>4.  Click the **Add-ons** tab and fill in the fields.

    |Field|Description|Dependency|
|Part Requirements|
    |-----|-----------|----------|
    |-----------------|
    |Part requirements are needed by agents|Enable this option to require agents to specify parts for the task.| |
    |Edit associated models|Click **add** and select the part model to be used for this task. Click **more** to select more part models.|**Part requirements are needed by agents.**|
    |**Documentation**|
    |Enable a dedicated knowledge base|Enable this option to install the knowledge base for the application.| |
    |Enable managed documents|Enable this option to add a related list to managed documents.| |
    |Enable task activities|Enable this option to log the task interactions and communications, such as phone calls and email messages.| |
    |**Associated Task Tables**|
    |Select associated tables|Click **Add** to select more tables.| |
    |**Maps**|
    |Enable maps|Enable this option to use maps.| |

5.  Click **Save**.

    **Warning:** When the **Enable state flows** option is disabled, a confirmation box with a link to documentation appears, explaining the consequences of disabling state flows. It is highly recommended that you read the documentation before making this change, as the action of disabling service management state flows cannot be reversed.


-   **[Task vs. request driven processing](../../planning-and-policy/concept/c_TaskVsRequestDrivenProcessing.md)**  
All applications use either task-driven or request-driven processes for handling tasks.

**Parent Topic:**[Activate Facilities Service Management](t_ActivateFacilitiesSM.md)

