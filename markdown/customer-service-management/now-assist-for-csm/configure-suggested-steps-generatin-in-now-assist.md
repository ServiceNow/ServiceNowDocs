---
title: Configure Suggested Steps Generation
description: Configure suggested steps generation to analyze clusters of similar cases and suggest next steps for case resolution for accelerated and consistent agent case troubleshooting.Learn how to enable the suggested steps generation in the CSM Workspace after skill activation.Replace the default sn\_esm\_agent role with a custom role.
locale: en-US
release: yokohama
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2025-08-18"
reading_time_minutes: 3
keywords: [generative AI, generative AI for Customer Service Management, generative AI for customer service agents, generative AI, generative AI for Customer Service Management, generative AI for customer service agents, generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Activate Now Assist Skills, Configure, Now Assist for Customer Service Management \(CSM\), Customer Service Management]
---

# Configure Suggested Steps Generation

Configure suggested steps generation to analyze clusters of similar cases and suggest next steps for case resolution for accelerated and consistent agent case troubleshooting.

## Before you begin

Role required: admin

Suggested steps are generated from the records identified based on the information that you enter in the following fields:

-   Short Description
-   Edited Conditions

## Procedure

1.  Navigate to **Admin &gt; Now Assist Admin &gt; Skills**.

2.  Select the **Customer** workflow, and **CSM** as the product.

3.  Activate Skill for the **Suggested Steps Generation** skill.

    Each skill has a guided setup with multiple steps. A check symbol next to each step indicates whether its setup is complete, partially complete, or incomplete. After configuring a step, select **Save and continue** to move forward, or **Back** to return to a previous step.

4.  Select **Choose Inputs** and review the tables and fields to create prompts that determines where data is pulled from.

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

-   Short description
-   Edited Conditions: Edit the conditions to update the filter and ensure that only relevant and up-to-date records are used.


</td></tr></tbody>
</table>5.  Select **Record Clustering** to group records by similarity based on the adjusted inputs in the previous step.

    **Note:** Record clustering allows you to add the job in the queue, providing you with the ability to leave the page while the task is running in the background. You will be notified when the task is complete.

6.  Select **Define access** to determine who can access this skill.

    By selecting specific roles, you're controlling who can use it. The roles you choose will also be available in the next step **Select display**.

    Default and Custom Roles:

    -   If no changes are made, the default role sn\_esm\_agent will automatically appear in **Define Access** and **Select Display**.
    -   If custom roles were added before the upgrade, they’ll be updated automatically by a script.
    -   If new roles are created after the upgrade, you’ll need to manually add them in both the **Define Access** and **Select Display**.

        **Note:** In the **Select Display** step, you can only choose roles that were added in the **Define Access** step. If you add a role in **Define Access**, you still need to manually select it in **Select Display** to make it active.

    -   For customizing access control, see [Customize access control for suggested steps](configure-suggested-steps-generatin-in-now-assist.md#)
7.  Toggle **Display** to determine if suggested step recommendations appear in In-product desktop, displaying Now Assist skills on forms and workspaces.

8.  After selecting **Review and Activate** to examine changes, select **Done** to close the Suggested Steps Generation settings.

9.  Select **Activate** to turn on the skill for agents and complete the configuration.


## Make suggested steps available on CSM Workspace

Learn how to enable the suggested steps generation in the CSM Workspace after skill activation.

### Before you begin

Role required: admin

After activating the Suggested steps generation feature in the Now Assist Admin console, follow the steps outlined to make the skill available in CSM Configurable Workspace.

### Procedure

1.  Navigate to **All** &gt; **UI Builder**.

2.  Go to **Experiences** &gt; **CSM/FSM Configurable Workspace** &gt; **Record** &gt; **Front-line Case Page**.![Front-line Case page location under CSM/FSM Configurable Workspace](../image/csm-fsm-configurable-workspace.png)

3.  In the left content navigation pane, scroll down and select **Recommended Action 1**.

4.  In the right pane, clear the checkbox **Hide recommended actions**.![Image shows the Hide recommended actions checkbox unchecked](../image/recommended-actions1-tab.png)

5.  Select **Save** to apply the changes.


### Result

Recommended Actions will be displayed in the CSM/FSM Configurable Workspace and you can see the Suggested steps generation skill under it.

## Customize access control for suggested steps

Replace the default sn\_esm\_agent role with a custom role.

### Before you begin

Role required: admin

### Procedure

1.  Update role permissions

    In the sys\_user\_role table, open your custom role and add sn\_gaf.data\_writer to the Contains Role related list.

2.  Update ACLs

    In the sys\_security\_acl table, filter for ACL names starting with gaf\_suggested\_steps\_csm. Add your custom role to each of the four matching records.

3.  Configure skill access

    In Now Assist Admin, complete the setup for the CSM Suggested Steps Generation skill:

    -   Add your custom role in the **Define Access** step.
    -   Add the same role in the **Select Display** step.

### Result

By default, the sn\_esm\_agent role is used. These steps allow you to configure a custom role if needed.

