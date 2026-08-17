---
title: Transfer a primary ticket in Service Operations Workspace
description: You can transfer a primary ticket to Universal Request, service set \(department\), or service either with resolution or without resolution.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/service-operations-workspace/transfer-primary-task-ur-sow.html
release: zurich
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Universal Request in Service Operations Workspace, Manage, Service Operations Workspace for ITSM, IT Service Management]
---

# Transfer a primary ticket in Service Operations Workspace

You can transfer a primary ticket to Universal Request, service set \(department\), or service either with resolution or without resolution.

## Before you begin

A primary task is the ticket \(such as an incident, change request or interaction\) that is linked to a Universal Request. When you open a task from the Universal Request list, and select **Transfer**, the ticket is routed to the selected department or service.

The **Transfer** button appears in the record action bar at the top of the primary task form. If the button is not visible, verify that the Universal Request plugin \(com.snc.universal\_request\) is installed and you have the itil role.

Role required: itil

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **Service Operations Workspace**.

2.  From the navigation list, select **List**.

3.  From the navigation list, select **Universal Request** &gt; **Open**.

4.  Open the primary task that you want to route to a Universal Request.

5.  Select **Transfer**.

6.  In the **Transfer Ticket** dialog, provide the following details.

    -   **Department**: Select the department from the list.
    -   **Service**: Select the specific service of the chosen department.
    -   **Transfer reason**: Select the reason from the list.
    -   **Transfer notes**: A brief description for routing the primary ticket that you want to pass to the agent.
    -   **Copy additional comments and attachments**: Deselect if you do not want to transfer the ticket with additional comments and attachments. By default, all attachments and comments are transferred.

        **Note:** Work notes aren't copied while transferring.

7.  Select **Transfer**.


## Result

After you select **Transfer**, the primary task is routed to the selected department or service. A new ticket is created for the target department, and the original primary task is linked to it in the Universal Request record under the **Associated Requests** related list.

**Parent Topic:**[Universal Request in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/service-operations-workspace/using-ur-sow.md)

