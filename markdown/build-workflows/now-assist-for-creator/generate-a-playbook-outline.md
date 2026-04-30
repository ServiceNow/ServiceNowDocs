---
title: Generate a playbook
description: Provide text directions to Now Assist to generate a playbook outline with placeholder activities.
locale: en-US
release: zurich
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Playbook generation, Now Assist for Creator, Build workflows]
---

# Generate a playbook

Provide text directions to Now Assist to generate a playbook outline with placeholder activities.

Generate a playbook outline and get recommendations for placeholder activities 

## Before you begin

Learn how to write prompts to generate better playbooks. For more information, see [Writing prompts and reviewing playbook outlines](../concept/playbook-assist.md#writing-playbook-prompts).

Role required:

-   admin, playbook.admin, pd\_author, or a delegated developer permission

## Procedure

1.  Navigate to **All** &gt; **Workflow Studio**.

    The Workflow Studio landing page appears. Playbooks is shown by default, but you can toggle to flows, subflows, actions, and decisions.

2.  Open the **New** drop-down menu and select **Playbook**.

    The new playbook opens in a Workflow Studio tab. **Build with Now Assist** is the default method, but you can switch to **Build from scratch**.

3.  On the **Build with Now Assist** tab, fill in the following fields.

<table id="table_ubj_vbf_dbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Label**

</td><td>

Unique, user-facing name for your playbook. This name also appears to agents and fulfillers during runtime.

</td></tr><tr><td>

**Now Assist directions**

</td><td>

Directions for the playbook that you want outlined.-   **Be precise and descriptive in the directions.**
    -   Describe each stage and activity in as much detail as you can.

    -   Specify the order that stages and activities run in.

    -   Specify if any stages or activities run at the same time.

</td></tr><tr><td>

**Application**

</td><td>

Application scope that you want your playbook to run in. Selecting **Global** lets your playbook run in any application scope. For more information, see [Application scope](https://www.servicenow.com/docs/access?context=c_ApplicationScope&version=zurich&pubname=zurich-application-development&ft:locale=en-US).**Important:** You can't change the application scope of a playbook after you've generated a preview for it.

</td></tr></tbody>
</table>4.  Select **Generate playbook preview**.

    Workflow Studio uses your text directions to build a playbook outline. If successful, Workflow Studio displays a preview of the playbook in diagramming view.

    ![Generated playbook preview](../images/playbook-preview.png)

5.  Scroll horizontally in the preview, and zoom in and out as needed.

6.  Review the preview of the playbook for accuracy.

7.  If the playbook outline doesn’t meet your requirements, try rephrasing your prompt according to [Writing prompts and reviewing playbook outlines](../concept/playbook-assist.md#writing-playbook-prompts), and select **Regenerate preview**.

8.  If you're ready to generate your playbook outline, select **Save and edit playbook**.

    **Note:** Generating or regenerating a playbook preview counts as 10 assists. To track your Now Assist usage, see [Monitoring Now Assist usage in Subscription Management](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US). Opening a playbook does not count as an assist.

9.  To view the prompt that was used to generate a playbook, navigate to **More actions menu** &gt; **Properties** &gt; **General** &gt; **Now Assist directions**.

    ![Playbook properties in the More actions menu.](../images/playbook-properties-menu.png)

    ![Prompt that was used to generate a playbook.](../images/playbook-prompt-properties.png)

10. Configure your trigger.

    For more information about triggers, see [Configure your trigger.](add-configure-trigger.md)

11. Configure placeholder activities by manually selecting the placeholder activity.

    **Tip:** To generate recommendations for activity definitions from Now Assist instead, see [Generate playbook recommendations](generate-playbook-recommendations.md).

    1.  Select a placeholder activity that you want to configure \( ![Placeholder activity icon.](../images/placeholder-activity-icon.png)\).

        You can also hover over the placeholder activity and select the **replace activity** icon \(![Icon for replacing an activity](../images/replace-activity-icon.png) in the mini-picker to directly open the activity picker.

    2.  Update the **Label** and **Description**, if needed.

    3.  Under the **Activity definition** field, select the edit button \(![Edit icon in the playbook builder.](../images/playbook-edit-button.png)\).

        The activity picker is displayed.

    4.  In the activity picker, search for the activity, subflow, or action to add.

        **Note:** Select the application first, and then the activity from the resulting list. For more information about subflows or actions, see [subflow, or action](../concept/automation-assets.md).

    5.  Configure the activity inputs.

        For more information about common activities and their inputs, see [Playbooks reference](../reference/process-automation-designer-reference.md).

12. If you don't see the activity that you want to add in the activity picker, create an activity definition.

    For more information, see [create an activity definition](create-activity-definition.md).

13. After you configure all your stages and activities, select **Activate** in the header.

    Activating your playbook publishes it so that it runs when triggered.

14. **Note:** When you change your playbook after activating it, the system saves your changes but deactivates your playbook.

    To publish any new changes to your playbook, select **Activate** again.

    For more information, see [Playbook statuses and activation states](../reference/process-status-activation-state.md).


## Result

When your playbook's trigger conditions are met, your playbook runs. As a result, the system creates a Process Execution record and renders user-facing configurations for Playbook Experience. For an example of how to digitize a manual business process that renders as a playbook, see [Design an automated process](design-automated-process.md).

## What to do next

Design the Playbook Experience for your agents and fulfillers in UI Builder. To learn how to design and customize the runtime playbook experience in UI Builder, see [Customize the Playbook Experience](../../workspace/concept/playbook-customize-playbook.md).

