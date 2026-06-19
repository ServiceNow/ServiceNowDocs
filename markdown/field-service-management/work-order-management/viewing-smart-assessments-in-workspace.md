---
title: View and complete smart assessments in workspace
description: Technicians can use the configurable workspace to view, complete, and submit questionnaires partially completed in the mobile application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/work-order-management/viewing-smart-assessments-in-workspace.html
release: australia
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing Smart Assessment in Configurable Workspace, Completing work orders on the web interface, Use, Field Service Management]
---

# View and complete smart assessments in workspace

Technicians can use the configurable workspace to view, complete, and submit questionnaires partially completed in the mobile application.

## Before you begin

-   Users with the questionnaire\_reader role can view smart assessment questionnaires related to work order tasks, but cannot edit them.
-   The questionnaire\_user role is part of the wm\_agent role. Technicians who have the wm\_agent role and the category role can view and update Smart Assessment questionnaires associated with the category role.

Role required: wm\_agent

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  In the **CSM and FSM Configurable Workspace Foundation Landing Page** screen, select the List icon to view the assigned work order tasks.

3.  Select the **Work Order Tasks** option to view the related work items.

    You can create and save different filters by using the **condition**, **Number**, and **Group by** options to filter and sort your search results.

4.  Select the work order task to open it.

5.  In the details screen, select **More**.

6.  Select **Smart Assessment Instances** to view the related list of smart assessment questionnaires.

7.  Select the required questionnaire to open and view it.

    The questionnaire details screen displays the total number of questions, number of questions completed, and percentage completed.

8.  Select the **All questions** filter and select **Unanswered questions** to view and answer only the pending questions.

9.  Fill in the questionnaire details.

10. Select **Submit** to save and submit the questionnaire responses.

11. In the **Submit** prompt, select the check box and select **Submit**.

    The responses submitted in the questionnaire in the workspace are automatically saved. Unless the questionnaire is submitted, all the information provided in it is retained and can be edited. After the questionnaire is submitted, responses cannot be modified. Questionnaires that are already submitted through mobile cannot be edited in the workspace.


## Result

Submitting the questionnaire changes its state from **Work In Progress** to **Completed**, and the workspace is updated.

