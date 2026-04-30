---
title: Create a questionnaire
description: Create and insert a new questionnaire for agents to respond to.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Questionnaire activity, Stages and activities, Building playbooks, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Create a questionnaire

Create and insert a new questionnaire for agents to respond to.

## Before you begin

Role required: admin, playbook\_admin, playbook\_author, or playbook\_content\_author

Familiarize yourself with the [questionnaire activity inputs and outputs](../reference/questionnaire-activity.md).

## Procedure

1.  In diagram view, hover on the object that you want to insert a questionnaire activity next to, and select the **+** icon to add an activity.

    The mini-picker displays.

2.  Select the questionnaire icon \[insert inline icon image\] to add a questionnaire.

    A questionnaire activity is added and the side panel opens for configuration.

3.  Under the **Details** tab, fill in the following fields.

<table><tbody><tr><td>

**Label**

</td><td>

Enter a unique name for your activity. This name appears in your playbook during runtime.

</td></tr><tr><td>

**Description**

</td><td>

Optionally, enter some descriptive details about your activity.

</td></tr><tr><td>

**Start Rule**

</td><td>

Choose when you want your activity to start running. Options include:-   **When stage starts**: Your activity starts running as soon as its stage starts running. Your stage starts running when your playbook is triggered.
-   **After specific activities**: Your activity starts running after specified activities have finished running.


</td></tr><tr><td>

**Display order**

</td><td>

Define the order in which this activity will appear during a playbook run.

</td></tr><tr><td>

**Run condition**

</td><td>

After the activity starts, the activity runs only if specific conditions are met.

</td></tr><tr><td>

**Start with delay**

</td><td>

Specify a duration of time to wait before running an activity whose start rule and conditions have been met. Give users a specific amount of time to complete actions. For more information, see [Start with delay input properties](../reference/start-with-delay-properties.md).

</td></tr><tr><td>

**Restart rules**

</td><td>

Choose what this activity does when a playbook is restarted:-   **Skip on restart**: Skip this activity when the playbook run is due to a restart.
-   **Run always**: Always run this activity, including first runs.
-   **Skip on first run**: Skip this activity during the first run.
For more information, see [Restart a playbook](restart-a-playbook.md).

</td></tr></tbody>
</table>4.  Under the **Questionnaire** tab, select **New questionnaire**.

5.  Add questions.

    **Note:** In the canvas, hover over the activity to see additional actions to edit a questionnaire.


**Parent Topic:**[Questionnaire activity](../reference/questionnaire-activity.md)

