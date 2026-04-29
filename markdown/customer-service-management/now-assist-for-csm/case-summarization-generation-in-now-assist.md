---
title: Configure Case Summarization
description: Configure case summarization to generate and display case summaries for agents and control who can access them in production.
locale: en-US
release: australia
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Activate Now Assist Skills, Configure, Now Assist for CSM, Customer Service Management]
---

# Configure Case Summarization

Configure case summarization to generate and display case summaries for agents and control who can access them in production.

## Before you begin

Role required: admin

Case summarization relies on a base input table and its associated field inputs with descriptions to provide the context for a generated summary. Choose your base table, and view the associated base input fields within the provided input templates. Record state determines which input template is used when generating a summary.

Provided input templates:

-   Case new
-   Case work in progress
-   Case resolved

Any modifications to the names or labels of the fields within these templates can result in issues with notes generation.

## Procedure

1.  Navigate to **Admin &gt; Now Assist Admin &gt; Skills**.

2.  Select the **Customer** workflow, and **CSM** as the product.

3.  Activate skill for the **Case summarization** skill.

    Each skill has a guided setup with multiple steps. A check symbol next to each step indicates whether its setup is complete, partially complete, or incomplete. After configuring a step, select **Save and continue** to move forward, or **Back** to return to a previous step.

4.  Select **General details** and edit name and description of the skill.

    Additional information regarding details of the skill are displayed, but can’t be edited.

5.  Select **Choose Input** and review the tables and fields to define the prompts that determine where data is pulled from.

    You can modify the rule conditions to determine when the input template is used. Additional data sources can be added via related tables as well.

<table id="id_xlz_fhc_4fc"><thead><tr><th>

Input template data

</th><th>

Base input field

</th></tr></thead><tbody><tr><td>

Base input fields

</td><td>

-   Description
-   Short description
-   State
-   Work notes
-   Additional comments


</td></tr><tr><td>

Listed rule conditions to the input table

</td><td>

Default is determined by record state.

</td></tr><tr><td>

\#1 Additional data source: Related table

</td><td>

-   Task SLA -&gt; Task
-   SLA definition
-   Stage
-   Breach time


</td></tr><tr><td>

\#2 Additional data source: Related table

</td><td>

-   Case -&gt; Parent
-   Number
-   Short description
-   State
-   Assigned to
-   Additional comments
-   Work notes
-   Case lines


</td></tr><tr><td>

\#3 Additional data sources

</td><td>

Activity is listed as 'Email.'

</td></tr></tbody>
</table>6.  Select **Customize prompt** to evaluate the generated outputs of case summaries.

    Evaluate the prompt used for each of the input templates by selecting an existing record to test the output. The review and modify the prompt after evaluating the output results, edit it within the Now Assist Skill Kit.

7.  Select **Define availability** to customize how and when the skill capability is active and accessible.

    -   Select **Skill is always available** so no restrictions are placed on when a skill is available.
    -   Select **Customize skill availability** to define conditions and use the condition builder to configure fields and values.
8.  Select **Define triggers** to determine how the skill will be triggered.

    -   Select **Automatic** to see the case summary of a record automatically generated when the user lands on a record page.
    -   Select **User trigger** to create a case summary of a record when the user opens a record page and selects the **Summarize** button.
9.  Select **Define access** to determine who can access this skill.

    By selecting specific roles, you're controlling who can use it. The roles you choose will also be available in the next step **Select display**.

    Default and Custom Roles:

    -   If no changes are made, the default role sn\_customerservice\_agent or sn\_customerservice.consumer\_agent automatically appear in **Define access** and **Select display**.
    -   If custom roles were added before the upgrade, they’re updated automatically by a script.
    -   If new roles are created after the upgrade, you can manually add them in both the **Define access** and **Select display**.

        **Note:** In the **Select display** step, you can only choose roles that were added in the **Define access** step. If you add a role in **Define access**, you still must manually select it in **Select display** to make it active.

10. Select **Display** to determine where the skill appears.

    -   Select **In-product desktop** to display Now Assist skills on forms and workspaces. Then, select the roles for whom the skill will be displayed.
    -   Select **Now Assist panel** to display Now Assist skills in the Now Assist panel.
11. After selecting **Review and activate** to examine changes, select **Done** to close the case summarization generation settings.

12. Select **Activate** to turn on the skill for agents and complete the configuration.


**Related topics**  


[Summarize a call by using Now Assist for Customer Service Management \(CSM\)](summarize-a-call-by-using-now-assist-for-customer-service-management-csm.md)

