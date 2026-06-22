---
title: Add and configure a stage in a playbook
description: Add and configure a stage in your playbook.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/add-configure-stage.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Stages and activities, Understanding the playbook components, Build Playbooks, Playbooks, Workflow Studio, Build workflows]
---

# Add and configure a stage in a playbook

Add and configure a stage in your playbook.

## Before you begin

Role required: playbook.admin or pd\_author

Review [Stages and activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/process-automation-designer-lanes-activities.md).

## Procedure

1.  Add a stage.

<table id="choicetable_z1g_1yz_21c"><thead><tr><th align="left" id="d37916e75">

View

</th><th align="left" id="d37916e78">

Steps

</th></tr></thead><tbody><tr><td id="d37916e84">

**Diagram**

</td><td>

1.  Select the **+** icon after the trigger to add the first stage in your playbook.
2.  In the mini-picker, select the dotted square icon. \[Omitted image "diagram-stage-icon.png"\] Alt text: Square dotted stage icon in Diagram view mini-picker.


</td></tr><tr><td id="d37916e113">

**Board**

</td><td>

In Board view, click **+ Add stage**.

</td></tr></tbody>
</table>    Your new stage appears, and the Stage properties panel opens.

2.  Fill in the following fields.

    1.  Provide the basic details of the stage.

<table id="table_zcq_mfv_21c"><tbody><tr><td>

**Label**

</td><td>

Enter a unique, user-facing name for your stage. This name appears to agents and fulfillers during runtime of your playbook.

</td></tr><tr><td>

**Description**

</td><td>

Optionally, enter some descriptive details about your stage.

</td></tr><tr><td>

**Run condition**

</td><td>

After the stage starts, the stage runs only if specific conditions are met.

</td></tr><tr><td>

**Start Rule**

</td><td>

Choose when you want your stage to start running. Options include:-   **When playbook starts**: Your stage starts running as soon as the playbook starts.
-   **After specific stages**: Your stage starts running after specified stage\(s\) have finished running.


</td></tr></tbody>
</table>    2.  **Show additional options** in the activity for [even more granular control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/advanced-instruction-activity.md).

        **Warning:** Changing the advanced property fields of an activity can potentially break your automation. Make sure you understand how the playbook and its activities flow before you make changes.

<table id="choicetable_ffz_mct_vlb"><tbody><tr><td id="d37916e257">

**Display order**

</td><td>

When there are multiple stages running at the same time, define the order in which stages appear during a playbook run.**Note:** In Workflow Studio, this can also be helpful when viewing parallel activities in Diagram view.

</td></tr><tr><td id="d37916e277">

**Start with delay**

</td><td>

Specify a duration of time to wait before running an stage whose start rule and conditions have been met. For more information, see [Start with delay input properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/start-with-delay-properties.md).

</td></tr></tbody>
</table>3.  Under the **Runtime permissions** tab, add sets of users, user groups, user criteria and roles, and define whether they can add optional activities to the stage or restart the stage and its activities.

4.  Click **Save and close** to finish adding the stage to your playbook.

    You can continue to add more stages to your playbook and fill in fields as described in the previous steps. In the Board view, use the **Stage actions menu** \[Omitted image "icon-menu.png"\] Alt text: Stage actions menu to add stages between existing stages.

    Stages are created.


## What to do next

[Add and configure your activities.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/add-configure-activity.md)

**Parent Topic:**[Stages and activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/process-automation-designer-lanes-activities.md)

