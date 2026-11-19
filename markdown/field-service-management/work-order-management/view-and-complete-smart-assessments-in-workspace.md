---
title: View and complete Smart Assessments in CSM/FSM Configurable Workspace
description: Technicians can use CSM/FSM Configurable Workspace to view, complete, and submit the Smart Assessment questionnaires that were partially completed in the mobile application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/field-service-management/work-order-management/view-and-complete-smart-assessments-in-workspace.html
release: yokohama
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-06-10"
reading_time_minutes: 1
breadcrumb: [Managing Smart Assessment questionnaires in CSM/FSM Configurable Workspace, Complete work orders on the web interface, Using Field Service Management, Field Service Management]
---

# View and complete Smart Assessments in CSM/FSM Configurable Workspace

Technicians can use CSM/FSM Configurable Workspace to view, complete, and submit the Smart Assessment questionnaires that were partially completed in the mobile application.

## Before you begin

-   If you have the questionnaire\_reader role, you can only view the Smart Assessment questionnaires related to work order tasks, but not edit them.
-   The questionnaire\_user role is part of the wm\_agent role. If you have the wm\_agent role and the category role, you can view and update Smart Assessment questionnaires associated with the category role.

Role required: wm\_agent

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  In the **CSM and FSM Configurable Workspace Foundation Landing Page** screen, select the List icon to view the assigned work order tasks.

3.  Select the **Work Order Tasks** option to view the related work items.

    You can create and save different filters by using the **Condition**, **Number**, and **Group by** options to filter and sort your search results.

4.  Select the work order task to open it.

5.  In the details screen, select **More**.

6.  Select **Smart Assessment Instances** to view the related list of smart assessment questionnaires.

7.  Select the required questionnaire to open and view it.

    The questionnaire details screen displays the total number of questions, number of questions completed, and the percentage completed.

8.  From the **All questions** filter, select **Unanswered** questions to view only the pending questions.

9.  Fill in the details, as needed.

10. Select **Submit** to save and submit the questionnaire responses.

    The responses submitted in the questionnaire from CSM/FSM Configurable Workspace are automatically saved. Unless the questionnaire is submitted, all the information provided in the questionnaire is retained and can be edited. After submission, the responses cannot be modified. Questionnaires that are already submitted through mobile cannot be edited from CSM/FSM Configurable Workspace.


## Result

Submitting the questionnaire changes its state from **Work In Progress** to **Completed**, and the Workspace displays the updated state.

**Parent Topic:**[Managing Smart Assessment questionnaires in CSM/FSM Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/field-service-management/work-order-management/managing-smart-assessment-questionnaires-in-csm-and-fsm-configurable-workspace.md)

