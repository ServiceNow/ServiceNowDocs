---
title: Working lifecycle event cases in HR Service Delivery Agent Workspace
description: Manage lifecycle event cases using HR Service Delivery Agent Workspace.You can show all lifecycle event cases by using lists.There are multiple ways to create a Lifecycle Event case.Monitor the status of a lifecycle event case with the Activity Set Status tab. You can also monitor the state of each activity set and activities in a lifecycle event case.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using the HR Service Delivery Agent Workspace, HR Service Delivery Agent Workspace \(Classic\), HR Service Delivery, Employee Service Management]
---

# Working lifecycle event cases in HR Service Delivery Agent Workspace

Manage lifecycle event cases using HR Service Delivery Agent Workspace.

A lifecycle event case is an HR case fulfilled by a lifecycle event. For example, the HR service for New Hire Onboarding fulfills the lifecycle event for New Hire Onboarding.

**Note:** This section assumes you have Enterprise Onboarding and Transitions activated. For more information, see [Understanding Lifecyle events for enterprise](understanding-enterprise-onboarding-and-transitions.md).

## List lifecycle event cases using HR Service Delivery Agent Workspace

You can show all lifecycle event cases by using lists.

### Before you begin

Role required: sn\_hr\_le.case\_writer

### Procedure

1.  Navigate to **All** &gt; **HR Case Management** &gt; **HR Agent Workspace**.

2.  Select the ![HR Agent Workspace - Lists icon](../reference/images/IconList.png) Lists icon.

3.  Select **Lifecycle Events**.

4.  Select **Lifecycle Events Cases**.

    ![HR Agent Workspace - Lifecycle Event Lists](../image/agent-ws-hr-le-lists.png)


## Create a lifecycle event case using HR Service Delivery Agent Workspace

There are multiple ways to create a Lifecycle Event case.

### Before you begin

Role required: sn\_hr\_le.case\_writer

### Procedure

1.  Navigate to **All** &gt; **HR Case Management** &gt; **HR Agent Workspace**.

2.  From the HR Service Delivery Agent Workspace landing page, select the ![HR Agent Workspace - Add New icon](../image/IconCreateRecordMenu.png) Add New icon.

3.  Select **HR Case**.

4.  From the Lifecycle Events Cases list, select the ![HR Agent Workspace - Add New icon](../image/IconCreateRecordMenu.png) Add New icon or the **New** button.

    ![HR Agent Workspace - Create LE case](../image/agent-ws-hr-create-le.png)

5.  Enter an employee name or case number.

    ![HR Agent Workspace search for employee or case](../image/agent-ws-hr-search-no.png)

6.  Verify that the employee is the correct person for the case.

    ![HR Agent Workspace verify employee](../image/agent-ws-hr-verify-empl.png)

7.  Enter **New Hire Onboarding** in the **HR service** field.

8.  Select **Create Case**.

9.  Select **Ready for Work**.

    The **State** changes to **Ready**. In the Details section, the **Assignment group** and **Assigned to** fields populate based on your case assignment rules or HR case template. For more information, see [Assignment and matching rules in HR](c_UseAssignmentRules-1.md) and [HR templates](hr-template-configuration.md).


## View activity set status in HR Service Delivery Agent Workspace

Monitor the status of a lifecycle event case with the **Activity Set Status** tab. You can also monitor the state of each activity set and activities in a lifecycle event case.

### Before you begin

Role required: sn\_hr\_le.case\_writer

### Procedure

1.  Navigate to **All** &gt; **HR Case Management** &gt; **HR Agent Workspace**.

2.  Locate and display a lifecycle event case that is in progress.

    For more information, see [List lifecycle event cases using HR Service Delivery Agent Workspace](agent-ws-hr-le-cases.md#).

3.  Select the **Activity Set Status** tab.

4.  Select **Activity Set Status**.

    ![HR Agent Workspace - Activity Set Status tab](../image/agent-ws-hr-act-set-stat.png)


