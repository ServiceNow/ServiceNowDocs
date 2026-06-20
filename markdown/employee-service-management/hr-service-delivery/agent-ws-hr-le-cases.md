---
title: Working lifecycle event cases in HR Service Delivery Agent Workspace
description: Manage lifecycle event cases using HR Service Delivery Agent Workspace.You can show all lifecycle event cases by using lists.There are multiple ways to create a Lifecycle Event case.Monitor the status of a lifecycle event case with the Activity Set Status tab. You can also monitor the state of each activity set and activities in a lifecycle event case.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/employee-service-management/hr-service-delivery/agent-ws-hr-le-cases.html
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

**Note:** This section assumes you have Enterprise Onboarding and Transitions activated. For more information, see [Understanding Lifecyle events for enterprise](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/hr-service-delivery/understanding-enterprise-onboarding-and-transitions.md).

## List lifecycle event cases using HR Service Delivery Agent Workspace

You can show all lifecycle event cases by using lists.

### Before you begin

Role required: sn\_hr\_le.case\_writer

### Procedure

1.  Navigate to **All** &gt; **HR Case Management** &gt; **HR Agent Workspace**.

2.  Select the \[Omitted image "IconList.png"\] Alt text: HR Agent Workspace - Lists icon Lists icon.

3.  Select **Lifecycle Events**.

4.  Select **Lifecycle Events Cases**.

    \[Omitted image "agent-ws-hr-le-lists.png"\] Alt text: HR Agent Workspace - Lifecycle Event Lists


## Create a lifecycle event case using HR Service Delivery Agent Workspace

There are multiple ways to create a Lifecycle Event case.

### Before you begin

Role required: sn\_hr\_le.case\_writer

### Procedure

1.  Navigate to **All** &gt; **HR Case Management** &gt; **HR Agent Workspace**.

2.  From the HR Service Delivery Agent Workspace landing page, select the \[Omitted image "IconCreateRecordMenu.png"\] Alt text: HR Agent Workspace - Add New icon Add New icon.

3.  Select **HR Case**.

4.  From the Lifecycle Events Cases list, select the \[Omitted image "IconCreateRecordMenu.png"\] Alt text: HR Agent Workspace - Add New icon Add New icon or the **New** button.

    \[Omitted image "agent-ws-hr-create-le.png"\] Alt text: HR Agent Workspace - Create LE case

5.  Enter an employee name or case number.

    \[Omitted image "agent-ws-hr-search-no.png"\] Alt text: HR Agent Workspace search for employee or case

6.  Verify that the employee is the correct person for the case.

    \[Omitted image "agent-ws-hr-verify-empl.png"\] Alt text: HR Agent Workspace verify employee

7.  Enter **New Hire Onboarding** in the **HR service** field.

8.  Select **Create Case**.

9.  Select **Ready for Work**.

    The **State** changes to **Ready**. In the Details section, the **Assignment group** and **Assigned to** fields populate based on your case assignment rules or HR case template. For more information, see [Assignment and matching rules in HR](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown) and [HR templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/hr-service-delivery/hr-template-configuration.md).


## View activity set status in HR Service Delivery Agent Workspace

Monitor the status of a lifecycle event case with the **Activity Set Status** tab. You can also monitor the state of each activity set and activities in a lifecycle event case.

### Before you begin

Role required: sn\_hr\_le.case\_writer

### Procedure

1.  Navigate to **All** &gt; **HR Case Management** &gt; **HR Agent Workspace**.

2.  Locate and display a lifecycle event case that is in progress.

    For more information, see [List lifecycle event cases using HR Service Delivery Agent Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/hr-service-delivery/agent-ws-hr-le-cases.md).

3.  Select the **Activity Set Status** tab.

4.  Select **Activity Set Status**.

    \[Omitted image "agent-ws-hr-act-set-stat.png"\] Alt text: HR Agent Workspace - Activity Set Status tab


