---
title: Schedule the project insights email
description: Schedule the project insights email to prioritize and track the most important changes in the project in Project Workspace.
locale: en-US
release: zurich
product: Project Workspace
classification: project-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Manage Projects, Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Schedule the project insights email

Schedule the project insights email to prioritize and track the most important changes in the project in Project Workspace.

Demonstration of project summary generation skill in Project Workspace. 

## Before you begin

**Important:** This Now Assist skill is now turned on by default. The skill will be automatically available to appropriate role users for the application. This change simply activates the skill and does not touch the roles that are needed to use the skill. The new default behavior works as follows:

-   **New customers**

    When you install a Now Assist product, designated skills will turn on automatically.

-   **Existing customers who are upgrading**

    Any previously unconfigured skill will turn on automatically \(the skill was never turned on, then off again\).

    There is no change to Now Assist skills that are currently enabled and customized.

    Previously configured skills that were turned on, then off, will remain inactive.


If you have users with custom roles that need access to this skill, you must update ACLs for those roles.

Role required: it\_project\_manager

## About this task

By using the Project insights generation skill, you can generate a concise project insights. The project insights are shared through email. Project managers can monitor key elements such as project, project task, milestone, resource assignment, ridac, and financial. They can also prioritize their projects and decide the cadence of receiving these project insights email.

When a project is created in the work in progress state, the project insight generation skill is automatically enabled. This ensures that projects begin generating insights early in the execution phase without requiring manual setup. In addition, all existing projects in the work in progress state are automatically enabled for email‑based project insights.

## Procedure

1.  Navigate to **Workspaces** &gt; **Project Workspace** and open any project.

2.  From the planning page, select the more actions icon \(![More actions icon.](../../innovation-management/image/more-options-icon.png)\) and then select **Configure project insights**.

    From Project insights generation skill card, select **Edit** to modify the email conditions. From project insights configuration screen, select **Switch scope** and then select **Edit conditions**. Administrators can control insight generation through admin‑level configuration. From Email condition modal, admins can define which projects should generate insights and trigger email notifications, providing flexibility over when and for which projects insights are sent.

    **Note:** To add user access, you need to edit Access control lists \(ACLs\). Users with it\_project\_manager role only can turn on this skill.

3.  From the Configure project insights modal, in Choose topics step, select **Next**.

    You can select or deselect the project, project task, milestone, resource assignment, ridac, and financial card to customize what information is displayed in the Project insights email.

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

    When you select Send preview, you receive a project insights instantly and also receive insights based on the selected cadence. The email would go to the recipients selected along with the Project Manager.


## Schedule a project insight email

Let's assume that you have selected a weekly cadence and chosen Monday \(which falls on 2025-07-07\). After adding recipients:

-   If you select **Schedule**, the project insights are emailed to you and the recipients weekly on Mondays, starting from 2025-07-07 and continues until the project becomes inactive.
-   If you select **Send preview**, you will receive an initial insights email immediately and will also receive insights according to the selected cadence and day.

**Parent Topic:**[Managing projects with Project Workspace](../concept/use-projects-pw.md)

**Related topics**  


[Configure the Monitor project tasks AI agent in AI Agent Studio](../../now-assist-spm/task/configure-agents-project-task-monitoring.md)

