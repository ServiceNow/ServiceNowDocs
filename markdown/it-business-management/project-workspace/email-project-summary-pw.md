---
title: Schedule the project summary emails with Email project summary skill
description: Schedule the project summary emails to prioritize and track the most important changes in the project in Project Workspace.
locale: en-US
release: xanadu
product: Project Workspace
classification: project-workspace
topic_type: task
last_updated: "2024-10-24"
reading_time_minutes: 3
breadcrumb: [Manage Projects, Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Schedule the project summary emails with Email project summary skill

Schedule the project summary emails to prioritize and track the most important changes in the project in Project Workspace.

Demo of an email project summary skill in Project Workspace. 

## Before you begin

Ensure that the Email project summary skill is active.

Role required: it\_project\_manager

## About this task

By using the Email project summary skill, you can generate a concise project summary. The project summary is shared through email. Project managers can monitor key elements such as milestones, resource assignments, projects, and project tasks. They can also prioritize their projects and decide the cadence of receiving these project summary emails.

## Procedure

1.  Navigate to **Workspaces** &gt; **Project Workspace** and open any project.

2.  From the planning page, select the more actions icon \(![More actions icon.](../../innovation-management/image/more-options-icon.png)\) and then select **Email project summary**.

3.  From the Email project summary modal, select the **Cadence** as Weekly, Bi-weekly, or Monthly according to your requirement.

4.  Select **On this day**, as days for weekly or bi-weekly or dates for monthly cadence.

    **Note:** The email ID of the project manager is required before you can send the summary over the email.

    You can disable email summary by selecting **Disable email summary** check box.

5.  Select **Users** from the list.

    -   The project manager is automatically set as the default email recipient for the project.
    -   You can select one or multiple users. Only users with sn\_ppm\_read role or have read or view access to project information appear for selection in the users list.
    -   When an email is sent to recipients, the project manager is placed in the To list, while all other recipients are included in the Cc list.
    -   For confidential projects, recipients are required to be included in the list of users authorized to view the project.
6.  Select the **Include critical path task changes** to enable project task monitor AI agent directly from email project summary modal.

    You can receive notifications when changes to critical path tasks may delay your project timelines. These AI-driven alerts help you take action before risks escalate.

7.  Select **Schedule** to schedule the email cadence for the project.

    **Note:** Because the information in these fields is AI generated, it's a good idea to review the text and make sure it's accurate.

    The Email project summary skill captures different snapshots of your project at different times. For example, if you choose a weekly schedule, the skill captures a snapshot of the project this week and then another one next week. These snapshots are saved in the back end. The Now LLM Service then compares the two snapshots and highlight the important changes you must focus on \(like a delay in a milestone or an increased budget\). The skill then creates a summary of these key updates and sends an email to the project manager with links to project records. The project summary keeps the project managers informed on important updates without having to review changes manually.

8.  Select **Schedule and send** to schedule and send instant summary for the project.

    When you select Schedule and send, you receive a project summary instantly and also receive summaries based on the selected cadence. The email would go to the recipients selected along with the Project Manager.


## Schedule a project summary mail

Let's assume that you have selected a weekly cadence and chosen Monday \(which falls on 2025-07-07\). After adding recipients, you have selected the Critical Path Task Changes check box to enable the Project Task Monitor AI agent.

-   If you select Schedule, the project summary is emailed to you and the recipients weekly on Mondays, starting from 2025-07-07 and continuing until the project becomes inactive.
-   If you select Schedule and send, you will receive an initial summary email immediately and will also receive summaries according to the selected cadence and day.

**Parent Topic:**[Managing projects with Project Workspace](../concept/use-projects-pw.md)

**Related topics**  


[Configure the Monitor project tasks agentic workflow in AI Agent Studio](../../now-assist-spm/task/configure-agents-project-task-monitoring.md)

