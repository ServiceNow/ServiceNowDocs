---
title: Create remote tasks to sync data
description: Remote tasks provide linked tasks across multiple instances and enable business workflows without any custom integrations.
locale: en-US
release: australia
product: Service Bridge
classification: service-bridge
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use for consumers, Service Exchange for Consumers, Service Exchange]
---

# Create remote tasks to sync data

Remote tasks provide linked tasks across multiple instances and enable business workflows without any custom integrations.

## Before you begin

-   Role required: admin
-   Remote task definition must already exist.

## About this task

As a consumer, you can integrate tasks like incidents, cases, and service requests bi-directionally with your providers using remote tasks.

## Procedure

1.  Navigate to **All** &gt; **Incidents** &gt; **Open**.

2.  Click on the **Number** link to open an incident.

3.  Click **Create Remote Task for Provider** in the Related Links section.

    **Note:** The **Create Task for Provider** link appears in this section only if at least one active and valid remote task definition is available for the provider table associated with the task.

4.  The Remote Task page appears.

    In the Remote Task page, the Parent field is populated with the task record and the Status field is set to New.

5.  Select a Remote Task Definition from the list.

    **Note:**

    -   Only active and valid remote task definitions associated with the parent task are displayed.
    -   The Provider Connection field is automatically filled in based on the Remote Task Definition selected.
    -   If only one Remote Task Definition is available, the Remote Task Definition field is automatically populated.
6.  Click **Submit**.

    When you navigate back to the parent task, you can see the newly created remote task in the Remote Tasks related list.

    **Note:** The Remote Task is created asynchronously and may not show initially if the parent task form is quickly loaded. You may need to refresh the form to see the newly created Remote Task.

7.  Navigate to **Service Exchange Consumer** &gt; **Remote Tasks**.

    The list of remote tasks is displayed. When the newly created Remote Task is received in the provider instance, a new parent task based on the Remote Task is created.

8.  Click on the newly created task and then click on the remote task under the Remote Tasks tab in the Related Links section.

    You can see the Status field is set to Connected and that the description has been updated.

9.  Navigate back to the parent task.

10. Update the Short Description for the parent task and click **Save**.

11. Log into the consumer instance and open the task.

    You can see that the data has been synced and Short Description field has been updated in the consumer instance. You can also see a work note indicating that the Short Description has been updated by the provider.

    **Note:**

    -   You can create a remote task on the provider instance by following the same steps. Data is synced between the consumer and provider instances and any changes you make in the consumer instance are automatically updated in the provider instance.
    -   Once an attachment is shared with another instance through Service Exchange using a remote task or a provider task, it becomes part of that instance’s data. Service Exchange does not delete attachments on remote instances — the receiving instance must handle deletion.
    -   When you create a remote task on the consumer instance, the Provider Connection field is automatically populated when you select a Remote Task Definition.

