---
title: Generate a playbook
description: Generate a playbook with Now Assist by providing text directions or image.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/build-workflows/now-assist-for-creator/generate-a-playbook-outline.html
release: zurich
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: task
last_updated: "2026-06-01"
reading_time_minutes: 5
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Playbook generation, Now Assist for Creator, Build workflows]
---

# Generate a playbook

Generate a playbook with Now Assist by providing text directions or image.

Generate a playbook outline and get recommendations for placeholder activities 

## Before you begin

Learn how to write prompts to generate better playbooks. For more information, see [Writing prompts and reviewing playbook outlines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/now-assist-for-creator/playbook-assist.md).

Role required:

-   admin, playbook.admin, pd\_author, or a delegated developer permission

## Procedure

1.  Navigate to **All** &gt; **Workflow Studio**.

2.  From the **New** drop-down menu, select **Playbook**.

3.  On the **Build with Now Assist** tab, fill in the following fields.

    \[Omitted image "new-playbook-now-assist.png"\] Alt text: Build a new playbook with Now Assist.

<table id="table_ubj_vbf_dbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Type**

</td><td>

Type of the playbook you want to create.Select **Standard playbook**.

</td></tr><tr><td>

**Playbook name**

</td><td>

Unique, user-facing name for your playbook. This name also appears to agents and fulfillers during runtime.

</td></tr><tr><td>

**Application**

</td><td>

Application scope that you want your playbook to run in. Selecting **Global** lets your playbook run in any application scope. For more information, see [Application scope](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/building-applications/c_ApplicationScope.md).**Important:** You can't change the application scope of a playbook after you've generated a preview for it.

</td></tr><tr><td>

**Describe the playbook using these inputs**

</td><td>

Directions for the playbook that you want to create.-   **Instructions only**

Provide only text instructions to generate the playbook.

    -   Describe each stage and activity in as much detail as you can.

    -   Specify the order that stages and activities run in.

    -   Specify if any stages or activities run at the same time.

-   **Image**

Attach a high quality, clear image of the process. You can compliment the image with text instructions as well. For example, if you attach an image of a flow chart, you can add additional information about the process as text directions.

</td></tr><tr><td>

**Execution type**

</td><td>

The type of playbook you want to create.-   **Record driven**

The playbook is tied to a record. It is triggered on demands, or automatically based on the record operations. Any data that comes from the playbook will also be stored on that record.

-   **Standalone**

Single session playbook that don't store data to a record. These must be manually triggered or called from another playbook.

</td></tr><tr><td>

**Parent table**

</td><td>

In case of a record driven playbook, the table where the record resides. This option is not relevant for a standalone playbook.

</td></tr><tr><td>

**Additional properties**

</td><td>

Option to allow the playbook to be publicly accessible. Once embedded it is set to available to unauthenticated users, as long as there aren’t additional restrictions preventing the user from accessing the playbook. **Note:** Playbooks must be tied to a public parent table for unauthenticated users to see it in runtime.

</td></tr></tbody>
</table>4.  Select **Generate playbook preview**.

    Based on your instructions, Now Assist generates a preview of the playbook with all the elements and displays the preview in the diagramming view. Now Assist adds a placeholder activity wherever it's unable to find a relevant activity.

5.  Review the generated playbook preview for accuracy.

    If the generated playbook doesn’t meet your requirements, try rephrasing your prompt according to [Writing prompts and reviewing playbook outlines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/now-assist-for-creator/playbook-assist.md), and select **Regenerate preview**.

6.  If you're ready to generate your playbook, select **Save and edit playbook**.

7.  Configure your trigger.

    For more information about triggers, see [Configure your trigger.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-studio/add-configure-trigger.md)

8.  Configure placeholder activities by manually selecting the placeholder activity.

    **Tip:** To generate recommendations for activity definitions from Now Assist instead, see [Generate playbook recommendations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/now-assist-for-creator/generate-playbook-recommendations.md).

    1.  Select a placeholder activity that you want to configure \( \[Omitted image "placeholder-activity-icon.png"\] Alt text: Placeholder activity icon.\).

        You can also hover over the placeholder activity and select the **replace activity** icon \(\[Omitted image "replace-activity-icon.png"\] Alt text: Icon for replacing an activity in the mini-picker to directly open the activity picker.

    2.  Update the **Label** and **Description**, if needed.

    3.  Under the **Activity definition** field, select the edit button \(\[Omitted image "playbook-edit-button.png"\] Alt text: Edit icon in the playbook builder.\).

        The activity picker is displayed.

    4.  In the activity picker, search for the activity, subflow, or action to add.

        **Note:** Select the application first, and then the activity from the resulting list. For more information about subflows or actions, see [subflow, or action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-studio/automation-assets.md).

    5.  Configure the activity inputs.

        For more information about common activities and their inputs, see [Playbooks reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-studio/process-automation-designer-reference.md).

9.  If you don't see the activity that you want to add in the activity picker, create an activity definition.

    For more information, see [create an activity definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-studio/create-activity-definition.md).

10. After you configure all your stages and activities, test the playbook.

11. Select **Activate** in the header.

    Activating your playbook publishes it so that it runs when triggered.

    **Note:** When you change your playbook after activating it, the system saves your changes but deactivates your playbook.

    To publish any new changes to your playbook, you must activate the playbook again. For more information, see [Playbook statuses and activation states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-studio/process-status-activation-state.md).


## Result

When your playbook's trigger conditions are met, your playbook runs. As a result, the system creates a Process Execution record and renders user-facing configurations for Playbook Experience. For an example of how to digitize a manual business process that renders as a playbook, see [Design an automated process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-studio/design-automated-process.md).

## What to do next

Design the Playbook Experience for your agents and fulfillers in UI Builder. To learn how to design and customize the runtime playbook experience in UI Builder, see [Customize the Playbook Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-studio/playbook-customize-playbook.md).

