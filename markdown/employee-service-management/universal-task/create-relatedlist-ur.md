---
title: Add a Universal Task related list
description: Add a Universal Task related list to a service-specific form in both the ServiceNow AI Platform and Agent Workspace to let agents view a universal task for the request.
locale: en-US
release: australia
product: Universal Task
classification: universal-task
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring your service, Setting up and configuring Universal Task, Universal Task, Employee Service Management]
---

# Add a Universal Task related list

Add a Universal Task related list to a service-specific form in both the ServiceNow AI Platform and Agent Workspace to let agents view a universal task for the request.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to the table that the related list must be added to.

2.  Open a service-specific form.

3.  Right-click the additional actions context menu ![Context menu](../images/context-menu.png).

4.  Navigate to **Configure** &gt; **Related Lists**.

5.  On the form, select the **Universal Task-&gt;Parent**.

6.  Select a view name:

    -   Default view: To add the Universal Task related list in the ServiceNow AI Platform form.
    -   Workspace: To add the Universal Task related list in the Agent Workspace form.
7.  Click **Save**.

    **Note:** Due to access control list \(ACL\) restrictions, the **New** button might not work while you are creating a task. You can hide the **New** button on the related list and use the UI action to create a universal task.

    ![Disable the New tab.](../images/ut-relatdlst-new-tab.png)

    For more information on adding related lists, see [Related lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_RelatedLists.md).


**Parent Topic:**[Configuring your service for Universal Task](../concept/config-service-for-ut.md)

**Previous topic:**[Create UI actions for your service with Universal Task](config-uiactions-for-ut.md)

**Next topic:**[Add a Task tab on the Standard Ticket page](config-stdtktpage-for-ut.md)

