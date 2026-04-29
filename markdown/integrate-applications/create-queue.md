---
title: Create a queue in RPA Hub
description: Create a queue in RPA Hub to manage the work items that you want the robot to process.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Queue implementation, Use, RPA Hub, Workflow Data Fabric]
---

# Create a queue in RPA Hub

Create a queue in RPA Hub to manage the work items that you want the robot to process.

## Before you begin

To access a queue, an RPA business user or a support user must be a part of **Managed by Group** and must have relevant roles such as RPA business user, RPA developer, RPA support user.

\(Optional\) Configure the system properties related to **Activity Stream**, to add or remove the fields. The changes to these fields are captured in the work notes. For more information, see [Configure the system properties for an activity stream in RPA Hub](configure-sys-properties-activity.md).

Role required: sn\_rpa\_fdn.rpa\_release\_manager or sn\_rpa\_fdn.rpa\_admin

## About this task

Queues are used in automations to distribute transactional data or the workload among different robots.

A queue is a repository that can hold a number of work items. Work items can store multiple types of data, such as transaction information, customer details, or information from a document.

You can't delete a queue that is associated to a published bot process.

For more information on queues implementation in RPA Hub, see [Queue implementation in RPA Hub](../concept/queues-implement-rpa.md).

You can use the guided tour to get instructions on how to create a queue in the classic environment. For more information, see [Use Guided Tours in RPA Hub](use-guided-tour-rpa-hub.md).

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  On the **Lists** tab, under **Build**, select **Queues**.

4.  Select **New**.

5.  On the form, fill in the fields.

6.  Select **Save**.

7.  In the **Activity** and **Compose** fields, view the activity of the form, work notes, and additional comments.

8.  To delete a queue, select the three-dot icon next to the **Save** button and select **Delete**.

    **Note:** Verify that the queue is not associated to any bot process. You can delete a queue which is associated to a retired bot process. Deleting a queue also deletes the associated work items.


-   **[Queue form in RPA Hub](../reference/queue-form.md)**  
Use the Work Queue form to create a queue. A queue lists the work items that you want the robot to process.

**Parent Topic:**[Queue implementation in RPA Hub](../concept/queues-implement-rpa.md)

**Related topics**  


[Assign a bot process to a queue from Queues menu in RPA Hub](assign-botprocess-queue.md)

[Unassign a bot process from a queue in RPA Hub](unassign-botprocess-queue.md)

[View Audit History](https://www.servicenow.com/docs/access?context=c_HistorySets&version=australia&pubname=australia-platform-security&ft:locale=en-US)

