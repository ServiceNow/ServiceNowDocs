---
title: Schedule the project summary emails with Email project summary skill
description: Schedule the project summary email to prioritize and track the most important changes in the project in Project Workspace.
locale: en-US
release: yokohama
product: Project Workspace
classification: project-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Manage Projects, Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Schedule the project summary emails with Email project summary skill

Schedule the project summary email to prioritize and track the most important changes in the project in Project Workspace.

## Before you begin

Make sure that the Email project summary skill is active.

If you have users with custom roles that need access to this skill, you must update ACLs for those roles.

Role required: it\_project\_manager

## About this task

By using the Project summary generation skill, you can generate a concise project insights. The project summary is shared through email. Project managers can monitor key elements such as milestones, resources, projects, RIDAC, and project tasks. They can also prioritize their projects and decide the cadence of receiving these project insights email.

## Procedure

1.  Navigate to **Workspaces** &gt; **Project Workspace** and open any project.

2.  From the planning page, select the more actions icon \(![More actions icon.](../../innovation-management/image/more-options-icon.png)\) and then select **Configure project insights**.

    You can view the configure project insights option only when the project summary generation skill is turned on.

    To turn on the skill, navigate to **Admin** &gt; **Now Assist Admin**. From Now Assist Skills tab, select **SPM** category. From Project summary generation skill card, select **Turn on**. From Turn on Project insights generation modal, select **Turn on**.

    From Project summary generation skill card, select **Deactivate skill** to deactivate the skill. From Deactivate skill modal, select the reason of deactivation and select **Deactivate**.

    **Note:** To add user access, you need to edit Access control lists \(ACLs\). Users with it\_project\_manager role only can turn on this skill.

3.  From the Configure project insights modal, in Choose topics step, select **Next**.

    You can select or deselect the Project tasks, Milestones, or Resources cards to customize what information is displayed in the Project insights email.

4.  In Personalize content step, add your requirements and select **Next**.

    You can define your tone, writing style, and priority entities. For example, identify risks of this project. Please provide a formal summary in bullet points.

5.  In Set frequency step, select the **Cadence** as Weekly, Bi-weekly, or Monthly according to your requirement.

6.  Select **On this day**, as days for weekly or bi-weekly or dates for monthly cadence.

7.  Select **Users** from the list.

    -   The project manager is automatically set as the default email recipient for the project.
    -   You can select one or multiple users. Only users with sn\_ppm\_read role or have read or view access to project information appear for selection in the users list.
    -   When an email is sent to recipients, the project manager is placed in the To list, while all other recipients are included in the Cc list.
    -   For confidential projects, recipients are required to be included in the list of users authorized to view the project.
8.  Select **Send preview** to generate and send a preview of the insights email instantly.

    When you select Send preview, you receive a project summary instantly and also receive insights based on the selected cadence. The email would go to the recipients selected along with the Project Manager.


## Schedule a project summary email

Let's assume that you have selected a weekly cadence and chosen Monday \(which falls on 2025-07-07\). After adding recipients:

-   If you select **Schedule**, the project summary is emailed to you and the recipients weekly on Mondays, starting from 2025-07-07 and continues until the project becomes inactive.
-   If you select **Send preview**, you will receive an initial summary email immediately and will also receive summary according to the selected cadence and day.

**Parent Topic:**[Managing projects with Project Workspace](../concept/use-projects-pw.md)

**Related topics**  


[Configure the Monitor project tasks AI agent in AI Agent Studio](../../now-assist-spm/task/configure-agents-project-task-monitoring.md)

