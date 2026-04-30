---
title: Configure trending topics dashboard
description: Configure the trending topic dashboard to identify clusters of related records, visualize their volume and sentiment over time, and leverage AI-generated insights to proactively resolve issues and improve operational efficiency.
locale: en-US
release: yokohama
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2025-11-05"
reading_time_minutes: 2
keywords: [Generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Activate Now Assist Skills, Configure, Now Assist for Customer Service Management \(CSM\), Customer Service Management]
---

# Configure trending topics dashboard

Configure the trending topic dashboard to identify clusters of related records, visualize their volume and sentiment over time, and leverage AI-generated insights to proactively resolve issues and improve operational efficiency.

## Before you begin

Role required: admin

Trending topics dashboard is generated from the information that you enter in the short description field.

**Note:** Any modifications to the names or labels of these fields can result in issues with trending topics in the dashboard.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills**.

2.  Select the **Customer** workflow, and **CSM** as the product.

3.  Activate skill for the **Trending topics dashboard** skill.

    Each skill has a guided setup with multiple steps. A check symbol next to each step indicates whether its setup is complete, partially complete, or incomplete. After configuring a step, select **Save and continue** to move forward, or **Back** to return to a previous step.

4.  Select **General details** and edit name and description of the skill.

    Additional information regarding details of the skill are displayed, but can’t be edited.

5.  Select **Cluster Input** and review the tables and fields to create prompts that determine the source from which the data is pulled.

    You can’t modify the input data source.

    |Input|Description|
    |-----|-----------|
    |Input table|Case \[sn\_customerservice\_case\]|
    |Input fields|Short description|

6.  Select **Record clustering** to group records by similarity based on the adjusted inputs in the previous step.

    Record clustering enables you to add the job in the queue, providing you with the ability to leave the page while the task is running in the background. You are notified when the task is complete.

7.  Select **Define access** to determine who can access this skill.

    By selecting specific roles, you’re controlling who can use it. The roles you choose will also be available in the next step **Select display**.

    Default and Custom Roles:

    -   If no changes are made, the default role sn\_customerservice\_manager automatically appear in **Define Access** and **Select Display**.
    -   If custom roles were added before the upgrade, they’re updated automatically by a script.
    -   If new roles are created after the upgrade, you can manually add them in both the **Define Access** and **Select Display**.

        **Note:** In the **Select Display** step, you can only choose roles that were added in the **Define Access** step. If you add a role in **Define Access**, you still must manually select it in **Select Display** to make it active.

8.  Toggle **Select display** to determine if trending topics dashboard skill appears in In-product desktop, displaying Now Assist skills on forms and workspaces.

9.  Select roles for whom trending topics dashboard are displayed.

    The user roles added in the **Define access** step for each ACL\(access control list\) can be selected in this step.

10. After selecting **Review and Activate** to examine changes, select **Done** to close the activity response generation settings.

11. Select **Activate** to turn on the skill for agents and complete the configuration.

    Skill is activated for agents.


**Related topics**  


[View trending topics dashboard](../concept/view-trending-topics-dashboard.md)

