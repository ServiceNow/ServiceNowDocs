---
title: Configure sentiment analysis case
description: Configure Sentiment Analysis to evaluate case sentiment, trends, and reasoning from case inputs, helping agents resolve cases more efficiently.
locale: en-US
release: yokohama
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2025-06-10"
reading_time_minutes: 2
breadcrumb: [Activate Now Assist Skills, Configure, Now Assist for Customer Service Management \(CSM\), Customer Service Management]
---

# Configure sentiment analysis case

Configure Sentiment Analysis to evaluate case sentiment, trends, and reasoning from case inputs, helping agents resolve cases more efficiently.

## Before you begin

Role required: admin

Sentiment analysis is generated from the information that you enter in the following fields:

-   Description
-   Short Description
-   State
-   Priority
-   Additional Comments

Any modifications to the names or labels of these fields can result in issues with sentiment analysis.

The Sentiment Reasoning field in the record provides details on which factors were considered for reasoning. This includes:

-   Exact tone in the given inputs.
-   Feedback in recent comment.
-   Task priority.
-   SLA consideration.

## Procedure

1.  Navigate to **Admin &gt; Now Assist Admin &gt; Skills**.

2.  Select the **Customer** workflow, and **CSM** as the product.

3.  Activate Skill for the **Sentiment Analysis Case** skill.

    Each skill has a guided setup with multiple steps. A check symbol next to each step indicates whether its setup is complete, partially complete, or incomplete. After configuring a step, select **Save and continue** to move forward, or **Back** to return to a previous step.

4.  Select **Define Trigger** and edit the job schedule period to configure how often the skill will be implemented.

5.  Select **General details** and edit name and description of the skill.

    Additional information regarding details of the skill are displayed, but cannot be edited.

6.  Select **Choose Input** and review the tables and fields to create prompts that determines where data is pulled from.

    **Note:** You cannot modify the input data source.

<table id="id_xlz_fhc_4fc"><thead><tr><th>

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

-   Description
-   Short Description
-   State
-   Priority
-   Additional Comments


</td></tr></tbody>
</table>7.  Select **Role attribution**

    **Note:** You cannot modify the input data source.

<table id="table_erm_mzt_pfc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Case \[sn\_customerservice\_case\]

</td></tr><tr><td>

Requestor fields

</td><td>

-   Consumer
-   Contact
-   Created by
-   Opened by


</td></tr></tbody>
</table>8.  Select **Define Availability** to customize how and when the skill capability is active and accessible.

    -   Select **Skill is always available** so no restrictions are placed on when a skill is available.
    -   Select **Customize skill availability** to define conditions and use the condition builder to configure fields and values.
9.  Select **Enable dashboard** to see sentiment analysis across cases.

10. Select **Define access** to determine who can access this skill.

    By selecting specific roles, you're controlling who can use it. The roles you choose will also be available in the next step **Select display**.

    Default and Custom Roles:

    -   If no changes are made, the default role sn\_esm\_agent will automatically appear in **Define Access** and **Select Display**.
    -   If custom roles were added before the upgrade, they’ll be updated automatically by a script.
    -   If new roles are created after the upgrade, you’ll need to manually add them in both the **Define Access** and **Select Display**.

        **Note:** In the **Select Display** step, you can only choose roles that were added in the **Define Access** step. If you add a role in **Define Access**, you still need to manually select it in **Select Display** to make it active.

11. Toggle **Display** to determine if chat recommendation appears in In-product desktop, displaying Now Assist skills on forms and workspaces.

12. After selecting **Review and Activate** to examine changes, select **Done** to close the Sentiment Analysis generation settings.

13. Select **Activate** to turn on the skill for agents and complete the configuration.


