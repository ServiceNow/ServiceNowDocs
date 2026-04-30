---
title: Configure knowledge generation
description: Configure the Knowledge Generation skill to draft knowledge articles on resolving case tasks for agents to review and edit before publishing.
locale: en-US
release: zurich
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Activate Now Assist Skills, Configure, Now Assist for CSM, Customer Service Management]
---

# Configure knowledge generation

Configure the Knowledge Generation skill to draft knowledge articles on resolving case tasks for agents to review and edit before publishing.

## Before you begin

Ensure that the following is set up before you activate the skill:

1.  Install the Required Plugin- Now Assist for CSM plugin.
2.  Enable KCS system properties: The visibility of the **Create Knowledge** action in CSM Configurable Workspace depends on specific system properties and differs from its implementation in the Core UI UI.

    -   In Core UI, the action is implemented as a UI Action.
    -   In CSM Configurable Workspace, it is implemented as a Declarative Action.
    The visibility and behavior of the **Create Knowledge** button in the CSM Configurable Workspace depends on two system properties:

    -   sn\_customerservice.enable\_knowledge\_kcs: If this property is true, the button appears in the CSM Configurable Workspace.
    -   sn\_customerservice.kcs.enable\_template\_on\_case\_workspace
        -   If this property is false, the button is a UI Action and clicking it does not open a template selector.
        -   If this property is true, the button is a Declarative Action and clicking it opens a template selector modal.
    If either property is disabled, the action will not appear in CSM Configurable Workspace—even if it is visible in Core UI.

3.  Activate the KCS template.
    1.  Navigate to **All** &gt; **Knowledge** &gt; **Administration** &gt; **Article Template**.
    2.  Locate the **KCS Article**.
    3.  Set its status to **Active**.

        **Important:**

        -   -   For Now Assist panel, if property sn\_customerservice.enable\_knowledge\_kcs and KCS Article Template is not enabled then it will create article using standard template for cases.
-   For Core UI / Workspace, if sn\_customerservice.enable\_knowledge\_kcs and KCS Article Template is not enabled then it will not show **Create Knowledge** button on case form.

Role required: admin

The knowledge generation skill incorporates information that you enter in the following fields:

-   Short Description
-   Description
-   Resolution Notes
-   Work Notes
-   Comments

Any modifications to the names or labels of these fields can quality the generation and quality of knowledge generation articles.

**Note:** It is recommended to revert to the default field name and field label for the affected fields. To remove incompatible fields from generation, ensure a copy of the skill has been created, as not all fields are removable/configurable. Additionally, ensure that the Knowledge Management advanced installer plugin is enabled and the following system properties are set to TRUE:

-   sn\_customerservice.enable\_knowledge\_kcs
-   kcs.enable\_template\_on\_case\_workspace

## Procedure

1.  Navigate to **Admin &gt; Now Assist Admin &gt;Skills**.

2.  Select the **Customer** workflow, and **CSM** as the product.

3.  Activate Skill for the **KB Generation** skill.

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
-   Resolution notes \(for cases and incidents\)
-   Work notes
-   Comments


</td></tr></tbody>
</table>5.  Select **Define Availability** to customize how and when the skill capability is active and accessible.

    -   Select **Skill is always available** so no restrictions are placed on when a skill is available.
    -   Select **Customize skill availability** to define conditions and use the condition builder to configure fields and values.
6.  Select **Define access** to determine who can access this skill.

    By selecting specific roles, you're controlling who can use it. The roles you choose will also be available in the next step **Select display**.

    Default and Custom Roles:

    -   If no changes are made, the default roles sn\_customerservice\_agent and sn\_customerservice.consumer\_agent will automatically appear in **Define Access** and **Select Display**.
    -   If custom roles were added before the upgrade, they’ll be updated automatically by a script.
    -   If new roles are created after the upgrade, you’ll need to manually add them in both the **Define Access** and **Select Display**.

        **Note:** In the **Select Display** step, you can only choose roles that were added in the **Define Access** step. If you add a role in **Define Access**, you still need to manually select it in **Select Display** to make it active.

7.  Select **Display** to determine where the KB generation appears.

    -   Select In-product desktop to display Now Assist skills on forms and workspaces.
    -   Select Now Assist panel to display Now Assist skills in the Now Assist panel.
8.  After selecting **Review and Activate** to examine changes, select **Done** to close the KB generation settings.

9.  Select **Activate** to turn on the skill for agents and complete the configuration.


