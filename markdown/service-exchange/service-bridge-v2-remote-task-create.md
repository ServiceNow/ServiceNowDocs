---
title: Create remote tasks to sync data
description: Remote tasks provide linked tasks across multiple instances and enable business workflows without any custom integrations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/service-exchange/service-bridge-v2-remote-task-create.html
release: zurich
product: Service Exchange
classification: service-exchange
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Install and configure for consumers, Service Exchange for Consumers, Service Exchange]
---

# Create remote tasks to sync data

Remote tasks provide linked tasks across multiple instances and enable business workflows without any custom integrations.

## Before you begin

-   A remote task definition must already exist.
-   Role required: sn\_sb.remote\_task\_creator.

## About this task

As a consumer, you can integrate tasks like incidents, cases, and service requests bi-directionally with your providers using remote tasks.

## Procedure

1.  Navigate to **All** &gt; **Incidents** &gt; **Open**.

2.  Select the **Number** related link to open an incident.

3.  In the Related Links section, select the **Create Remote Task for Provider** related link.

    **Note:** The **Create Task for Provider** related link appears in this section only if at least one active and valid remote task definition is available for the provider table associated with the task.

4.  The Remote Task page appears.

    The **Parent** field is populated with the task record and the **Status** field is set to **New**.

5.  In the **Remote task definition** field, enter or search for a remote task definition.

    **Note:**

    -   Only active and valid remote task definitions associated with the parent task are displayed.
    -   The **Provider Connection** field is automatically filled in based on the remote task definition selected.
    -   If only one remote task definition is available, the **Remote Task Definition** field is automatically populated.
6.  Select **Submit**.

    When you navigate back to the parent task, the newly created remote task appears in the Remote Tasks related list.

    **Note:** The remote task is created asynchronously and may not show initially if the parent task form is quickly loaded. Refresh the form to see the newly created remote task.

7.  Navigate to **Service Exchange Consumer** &gt; **Remote Tasks**.

    The list of remote tasks is displayed. When the newly created remote task is received in the provider instance, a new parent task based on the remote task is created.

8.  Select the newly created task, then select the **Remote Tasks** tab in the Related Links section.

    The **Status** field is set to **Connected** and the description has been updated.

9.  Navigate back to the parent task.

10. Update the **Short Description** field for the parent task and select **Save**.

11. Log into the consumer instance and open the task.

    The data is synced and the **Short Description** field is updated in the consumer instance. A work note indicates that the **Short Description** field was updated by the provider.

    **Note:**

    -   You can create a remote task on the provider instance by following the same steps. Data is synced between the consumer and provider instances and any changes you make in the consumer instance are automatically updated in the provider instance.
    -   When data, such as an attachment or task, is shared with another instance through Service Exchange, it becomes part of that instance’s data. Service Exchange does not delete data on remote instances; the receiving instance must handle the deletion if required.
    -   When you create a remote task on the consumer instance, the **Provider Connection** field is automatically populated when you select a remote task definition.

