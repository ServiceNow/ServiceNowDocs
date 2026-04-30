---
title: Create an agentic workflow
description: Create an agentic workflow in AI Agent Studio so that AI agents can coordinate to solve complex problems.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-09-17"
reading_time_minutes: 11
breadcrumb: [Now Assist AI agents, Enable AI experiences]
---

# Create an agentic workflow

Create an agentic workflow in AI Agent Studio so that AI agents can coordinate to solve complex problems.

## Before you begin

Role required: sn\_aia.admin

## About this task

Agentic workflows solve business problems with agentic AI. In AI Agent Studio, you must define an agentic workflow and connect it with an AI agent to execute complex goals involving variable data or other factors that traditional automation can struggle with.

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage** &gt; **Agentic workflows** and select **New**.

    You’re directed to the New agentic workflow page on the Describe and connect step.

    ![Agentic workflow Guided Setup showcasing the different stages of configuring a new agentic workflow.](../image/create-agentic-workflow-latest.png)

2.  If you want to use AI to help you with the agentic workflow setup, select **Generate description and steps** to create a draft of an agentic workflow description and instructions with Now Assist.

    On the Generate a description and list of steps with Now Assist pop-up window, you can select **Generate** to write the name, description, and instructions fields for you. You can make changes to those fields after the text has been generated or try again with new instructions.

3.  Describe the business outcome that this agentic workflow targets and connect the AI agents to the agentic workflow based on your requirements.

    **Note:** If you have generated an agentic workflow by using Now Assist, the name, description, and list of steps fields are automatically filled in for you. You can still make changes!

    1.  Give the agentic workflow a name, description, and list of steps to complete.

        For examples on writing successful descriptions and instructions for the large language model \(LLM\), see [General guidelines for creating AI agents and agentic workflows](../concept/gg-creating-aia.md). The guidelines explain some factors to consider when writing your description and list of steps and offer some examples.

<table id="table_ifz_ttg_22c"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Wokflow Name

</td><td>

Name of your agentic workflow. Provide a name for the business challenge that you want to solve.Example: Issue Resolution

</td></tr><tr><td>

Workflow description

</td><td>

Brief summary of what business problem that your agentic workflow is going to solve. This description is given to the LLM to understand the overall objective.

</td></tr><tr><td>

List of steps

</td><td>

Guided action plan to be followed by your AI agents in the agentic workflow. These steps should be a detailed numbered list that includes specific instructions for as many cases as possible, including potential errors.

</td></tr></tbody>
</table>    2.  Assign one or more AI agents to execute the instructions for the agentic workflow.

        1.  In the Add AI agents that can perform these steps section, select **Add AI agent** and fill in the name of the AI agent in the **AI agent** field.
        2.  Select **Add**.
        3.  If you want to create an AI agent for your agentic workflow, then in the Add AI Agent drop-down list, select **Create new AI agent**.

            For more information, see [Create an AI agent](configure-next-best-action-agent.md).

            **Note:** If no AI agents are available for selection, the **Add AI agent** button is inactive.

        The selected AI agent is added to the agentic workflow.

    3.  Configure Access Control Lists \(ACLs\) for the agentic workflow.

        **Note:** The ACLs determine who has access to discover and execute the agentic workflow. To learn more about the ACLs you can create in AI Agent Studio and how to add more advanced security configurations, see [Implement access control in Now Assist AI agents](../concept/aia-security-implementation.md).

        This is a required step. If you have previously configured an agentic workflow without creating an ACL, you must generate an ACL before you can make other modifications.

        If you have already created an ACL for the agentic workflow, then it will appear in a list in this section. You can double-click the role pills to edit the roles.

<table id="table_rlv_bgr_hgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User access

</td><td>

The type of users whose access for the agentic workflow is defined by the following options:-   **Any authenticated user**: Any user who is logged in can access the agentic workflow.
-   **Users with specific roles**: Users that have at least one of the assigned roles to them can access the agentic workflow. This is the default option.

**Note:** If a user doesn't have access to an agentic workflow or if the user doesn't have access to at least one of the AI agents in the respective agentic workflow execution, then the whole execution aborts before the first AI agent is initiated.

-   **Public**: Any user can access the agentic workflow even without logging in. Use this option only when you want guests to be able to access the agentic workflow.


</td></tr><tr><td>

Role

</td><td>

Assign one or more specific roles from the drop-down.**Note:** Selecting the role is possible only when you chose the **Users with specific roles** user access.

</td></tr></tbody>
</table>    4.  Define the type of sys\_user the agentic workflow will run as.

        -   For more information about understanding the user identities that will execute the agentic workflow, see [User identity](../concept/aia-security-implementation.md#section_rch_xgg_hgc).
        -   For more information about understanding the rules for Access Control Lists \(ACLs\) in ServiceNow AI Platform®, see [Access Control List Rules](https://www.servicenow.com/docs/access?context=access-control-rules&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).
<table id="table_vjm_kpr_hgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Run as

</td><td>

The user identity with which the agentic workflow runs.Select one of the following entity types that your agentic workflow should run as:

1.  **Dynamic user**: The logged in user \(sys\_user\) who invokes the execution of an agentic workflow.

The dynamic user can be the sys\_user of a trigger, agentic workflow, or human user that passes its roles to this agentic workflow \(the upstream component/entity that invoked the agentic workflow\).

Any execution run by a dynamic user is recorded in the name of the logged in user. For example, if an incident is created by a Dynamic user, then the incident created is recorded in the name of the currently logged in user.

**Note:** The Dynamic user is the default setting for all agentic workflows unless there is a specific need that justifies an AI user. Generally, most agentic workflow can run as dynamic users.

2.  **AI user**: The agentic workflow runs and executes as a preconfigured, static user identity with assigned roles that will not change regardless of who or how the execution is invoked.

The AI user is a type of sys\_user record of type AI agents. Any actions performed by an agentic workflow running as an AI user are logged in the name of the AI user for that action or execution. For example, if an incident is created by an AI user, then the caller for that execution is recorded as the assigned AI user.

The AI user is a sys\_user with predefined roles.

**Warning:** Allowing public users to invoke AI users will give them elevated permissions to what data is accessible to them. Agentic workflows very rarely need to run as AI users.

 If you do not have an AI user but want to use the **AI user** identity, you need to create a new record on the User table. See [Create a user](https://www.servicenow.com/docs/access?context=t_CreateAUser&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US). Select **AI user** as the identity type.

</td></tr><tr><td>

AI user

</td><td>

Select a specific AI user from the drop-down menu.

</td></tr></tbody>
</table>        **Note:** When determining these security settings, be sure to consider the security settings for all aspects of the agentic flow, from agentic workflow, AI agents, and tools.

    5.  In the Ask Now Assist to suggest AI agents section, select **Recommend AI Agents** to explore the suggested recommendations for the AI agents.

    6.  Specify which AI providers this agentic workflow does not support.

        Some AI models may perform your specific agentic workflow tasks better than others. You can choose an unsupported LLM from the **Select unsupported LLMs** drop-down if you do not want an agentic workflow to be available if a certain default AI model provider is active.

    7.  Select **Save and continue**.

        Once you select **Save and continue**, Now Assist runs a check to try to identify if the agentic workflow is a potential duplicate of an existing one. If you see the Possible duplications found pop-up window, you can review the flagged agentic workflows and verify that the one you're creating is unique.

        If there’s an existing similar agentic workflow, it’s possible for the wrong one to run when a user attempts to trigger it. Try to make your description and list of steps as unique as possible to avoid duplicates.

        You must select **Save and continue** to create the ACL for the AI agent on the ACL table. If you want to create additional or **Deny-Unless** ACLs or add Security Attributes for the AI agent, a user with the correct elevated privileges can create them on the ACL table directly. Additional ACLs cannot be configured in AI Agent Studio.

        If you selected **Users with specific roles** for your ACL, after you've selected Save and continue, you can still edit the roles of the ACL. Return to the first page of the guided setup and double-click the role pills in the ACL section to make changes.

        You’re directed to the Add a preferred trigger page.

4.  Define a preferred trigger and the conditions for activating your agentic workflow.

    **Note:** Triggers are optional. If you only want your AI agent to be discoverable in chats in the Now Assist panel, you don't need to set a trigger.

    ![Agentic workflow Guided Setup showcasing the Add trigger page.](../image/agentic-wrkflow-add-trigger.png)

    1.  Select **Add Trigger**.

    2.  On the form, fill in the fields.

        Trigger conditions for the agentic workflows set the conditions required for a user to execute an agentic workflow.

        ![The Add trigger form of an agentic workflow.](../image/agentic-wrkflow-trigger-form.png)

<table id="table_dw3_czl_zcc"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Select trigger

</td><td>

List of triggers that are available in the instance.

</td></tr><tr><td>

Name

</td><td>

Name of the trigger.

</td></tr><tr><td>

Active

</td><td>

Option to keep your trigger conditions active.

</td></tr><tr><td>

Table

</td><td>

Name of the applicable table for your agentic workflow.Example for the Issue Auto Resolution agentic workflow: Incident

</td></tr><tr><td>

Conditions

</td><td>

Conditions that you can add to control the trigger configuration.Select **+ Add condition set** to add conditions to your agentic workflow trigger.

</td></tr><tr><td>

Method of defining sys\_user

</td><td>

-   Use an existing table
-   Use a new custom script


</td></tr><tr><td>

Sys\_user

</td><td>

The user that the AI agent runs as.

 If you select a table, then the choices could include the Caller, Resolved by, Closed by, or another user field. You can also create a custom script to generate and return the sys\_id of the user.

</td></tr><tr><td>

Objective template

</td><td>

Template instruction for an AI agent to follow during its execution.

 For some trigger types, you can also select additional fields in your template instructions.

</td></tr><tr><td>

Channel

</td><td>

Medium for the agentic workflow output: Now Assist panel or Virtual Agent.

 **Note:** To view the output from a triggered agentic workflow in the Now Assist panel, you need the now\_assist\_panel\_user role.

</td></tr><tr><td>

Show notification

</td><td>

Select the **Show Notification** option to enable notifications for your triggers.

 If there are multiple triggers with notifications enabled for the same table, only one notification is shown.

</td></tr></tbody>
</table>        If you choose a scheduled trigger, additional options are available, such as the day of the week and time when you want the trigger to run.

        **Note:** When running a scheduled trigger, not every record is included in the execution. By default, the value is 10. If you want to change this number, you must set the **sn\_aia.max\_scheduled\_trigger\_query** system property to a different value.

        If you choose an email trigger, the target emails must exist on the Reply \[sys\_reply\] table. New emails aren’t available as triggers.

    3.  Select **Add**.

        You’re directed to the Define trigger page.

    4.  Select **Save and continue**.

        You’re directed to the Select a UI display page.

5.  Configure the display and access for your agentic workflow from the Select a UI display page.

    1.  Turn on the Display toggle to display your agentic workflow output on the selected channel.

        **Note:** You must toggle the **Status** to activate your agentic workflow, but selecting Now Assist panel is optional. Only enable it if you want your agentic workflow to be discoverable in that channel. If you only plan to trigger your agentic workflow by other means, you don't need to enable it.

        ![Select display page showing the Now Assist panel as the output option for agentic workflow execution.](../image/agentic-wrkflw-display.png)

        **Note:** If the Now Assist panel display option isn’t available, you must enable the panel first. For more information, see [Turn on the Now Assist panel](../../now-assist-admin/task/activate-now-assist-panel.md). You must have the now\_assist\_panel\_role to view the output from a triggered agentic workflow in the Now Assist panel.

    2.  You can select the next icon \(![Next icon.](../../../reuse/icons/product-icons/chevron-right-fill-24.svg)\) to access the User roles drop-down list and select a user role for who should be accessing the agentic workflow.

    3.  Select **Save and test**.

        You’re directed to the agentic workflow testing page. For more information about testing an agentic workflow, see [Test an agentic workflow](test-aia-use-case.md).

        To test the agentic workflow, you must have the sn\_aia.admin role and any roles the ACL configured for the agentic workflow requires, if applicable.


## Result

An agentic workflow is created and can be seen in the agentic workflow list in the Create and manage page.

If you selected **Users with specific roles** for your ACL, you can change roles at any point. Return to the guided setup and double-click the pills to make changes. All other security changes must be done on the ACL \[sys\_security\_acl\] table by a user with elevated permissions.

