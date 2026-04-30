---
title: Configure activity response generation
description: Set up the activity response generation skill in the Now Assist Admin console to enable automated responses in comments and work notes.
locale: en-US
release: yokohama
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2025-11-05"
reading_time_minutes: 2
keywords: [Generative AI, Generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Activate Now Assist Skills, Configure, Now Assist for Customer Service Management \(CSM\), Customer Service Management]
---

# Configure activity response generation

Set up the activity response generation skill in the Now Assist Admin console to enable automated responses in comments and work notes.

## Before you begin

Role required: admin

## About this task

Use the Now Assist Admin console for configuring the activity response generation skill by selecting inputs, defining access, and activating the skill.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills**.

    Access the skills configuration page.

    Verify you have admin role.

2.  Select the **Customer** workflow and choose **CSM**

    This determines the product context for the skill.

    Workflow and product must match your configuration requirements.

3.  Activate skill for the activity response generation skill.

    Each skill has a guided setup with multiple steps.

    A check symbol next to each step indicates whether its setup is complete, partially complete, or incomplete. After configuring a step, select **Save and continue** to move forward, or **Back** to return to a previous step.

4.  Select **General details** and edit name and description of the skill.

    Additional information regarding details of the skill are displayed, but can’t be edited.

5.  Select **Choose Input** and review the tables and fields to create prompts that determine where data is pulled from.

    **Note:** You can’t modify the input data source.

    |Input|Description|
    |-----|-----------|
    |Input table|Case \[sn\_customerservice\_case\]|
    |Input fields|Description, Short Description, Additional comments, Work notes, State, Priority. |

6.  Select **Define access** to determine who can access this skill.

    By selecting specific roles, you’re controlling who can use it. The roles you choose will also be available in the next step **Select display**.

    Default and Custom Roles:

    -   If no changes are made, the default role sn\_esm\_agent automatically appear in **Define Access** and **Select Display**.
    -   If custom roles were added before the upgrade, they’re updated automatically by a script.
    -   If new roles are created after the upgrade, you can manually add them in both the **Define Access** and **Select Display**.

        **Note:** In the **Select Display** step, you can only choose roles that were added in the **Define Access** step. If you add a role in **Define Access**, you still must manually select it in **Select Display** to make it active.

7.  Toggle **Select display** to determine if activity response generation skill appears in In-product desktop, displaying Now Assist skills on forms and workspaces.

8.  After selecting **Review and Activate** to examine changes, select **Done** to close the activity response generation settings.

9.  Select **Activate** to turn on the skill for agents and complete the configuration.

    Skill is activated for agents and a success modal shows up with the option to **Return to CSM** and to **Go to Now Assist content menu**.

10. Select **Go to Now Assist context menu** to [configure](customize-now-assist-context-menu-for-skills.md) the activity response generation skill's Now Assist Context Menu in Now Assist Experience.


**Related topics**  


[Generate activity stream responses](generate-a-recommendation-to-respond-to-an-activity.md)

