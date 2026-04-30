---
title: Configure email recommendation
description: Configure email reply recommendation to help agents generate and refine efficient email responses based on conversation context.
locale: en-US
release: yokohama
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2025-06-02"
reading_time_minutes: 2
breadcrumb: [Activate Now Assist Skills, Configure, Now Assist for Customer Service Management \(CSM\), Customer Service Management]
---

# Configure email recommendation

Configure email reply recommendation to help agents generate and refine efficient email responses based on conversation context.

Configure email recommendation skill 

## Before you begin

Role required: admin

Email reply recommendations are generated from the information that you enter in the following fields:

-   Short description
-   Description
-   All journal fields
-   Emails

## Procedure

1.  Navigate to **Admin &gt; Now Assist Admin &gt; Skills**.

2.  Select the **Customer** workflow, and **CSM** as the product.

3.  Activate Skill for the **Email Recommendation** skill.

    Each skill has a guided setup with multiple steps. A check symbol next to each step indicates whether its setup is complete, partially complete, or incomplete. After configuring a step, select **Save and continue** to move forward, or **Back** to return to a previous step.

4.  Select **Choose Input** and review the tables and fields to create prompts that determines where data is pulled from.

    **Note:** You cannot modify the input data source.

<table id="table_mnf_45q_1bc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Case \[sn\_customerservice\_case\]

</td></tr><tr><td>

Input fields

</td><td>

-   Short description
-   Description
-   Emails
-   Additional Comments
-   Work Notes
-   Activity


</td></tr></tbody>
</table>5.  Select **Define Availability** to customize how and when the skill capability is active and accessible.

    -   Select **Skill is always available** so no restrictions are placed on when a skill is available.
    -   Select **Customize skill availability** to define conditions and use the condition builder to configure fields and values.
6.  Select **Define access** to determine who can access this skill.

    By selecting specific roles, you're controlling who can use it. The roles you choose will also be available in the next step **Select display**.

    Default and Custom Roles:

    -   If no changes are made, the default role sn\_esm\_agent will automatically appear in **Define Access** and **Select Display**.
    -   If custom roles were added before the upgrade, they’ll be updated automatically by a script.
    -   If new roles are created after the upgrade, you’ll need to manually add them in both the **Define Access** and **Select Display**.

        **Note:** In the **Select Display** step, you can only choose roles that were added in the **Define Access** step. If you add a role in **Define Access**, you still need to manually select it in **Select Display** to make it active.

7.  Toggle **Display** to determine if email recommendation appears in In-product desktop, displaying Now Assist skills on forms and workspaces.

8.  After selecting **Review and Activate** to examine changes, select **Done** to close the Email Reply generation settings.

9.  Select **Activate** to turn on the skill for agents and complete configuration.


