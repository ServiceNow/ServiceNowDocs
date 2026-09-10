---
title: Create a questionnaire
description: Create and insert a new questionnaire for agents to respond to.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/create-questionnaire.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Questionnaire activity, Stages and activities, Understanding the playbook components, Build Playbooks, Playbooks, Workflow Studio, Build workflows]
---

# Create a questionnaire

Create and insert a new questionnaire for agents to respond to.

## Before you begin

Role required: admin, playbook\_admin, playbook\_author, or playbook\_content\_author

Familiarize yourself with the [questionnaire activity inputs and outputs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/questionnaire-activity.md).

## Procedure

1.  In diagram view, hover on the object that you want to insert a questionnaire activity next to, and select the **+** icon to add an activity.

2.  In the mini-picker, select the square icon \[Omitted image "diagram-activity-icon.png"\] to add an activity.

3.  Under **Interactive**, select **Questionnaire**.

    \[Omitted image "pb-questionnaire-pb.png"\] Alt text: Screenshot showing the Questionnaire option in the activity menu.

    A questionnaire activity is added and the side panel opens for configuration.

4.  Under the **Details** tab, select the More Menu icon \[Omitted image "dec-table-menu-options.png"\], and **Show additional options** to view all fields.

    **Note:** **Display order**, **Start with delay**, and **Run condition** fields are hidden by default.

    \[Omitted image "pb-questionnaire-pb-3.png"\] Alt text: Screenshot showing Show additional options.

5.  Fill in the following fields.

<table id="table_ugr_4v5_3kc"><tbody><tr><td>

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

Define the order in which this activity will appear during a playbook run. This field is hidden by default.

</td></tr><tr><td>

**Start with delay**

</td><td>

Specify a duration of time to wait before running an activity whose start rule and conditions have been met. Give users a specific amount of time to complete actions. This field is hidden by default. For more information, see [Start with delay input properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/start-with-delay-properties.md).

</td></tr><tr><td>

**Run condition**

</td><td>

After the activity starts, the activity runs only if specific conditions are met. This field is hidden by default.

</td></tr><tr><td>

**Restart rules**

</td><td>

Choose what this activity does when a playbook is restarted:-   **Skip on restart**: Skip this activity when the playbook run is due to a restart.
-   **Run always**: Always run this activity, including first runs.
-   **Skip on first run**: Skip this activity during the first run.
For more information, see [Restart a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/restart-a-playbook.md).

</td></tr></tbody>
</table>6.  Under the **Questionnaire** tab, select **Create questionnaire**.

    \[Omitted image "pb-questionnaire-pb-1.png"\] Alt text: Screenshot showing the Create questionnaire button.

7.  Add questions to the questionnaire one at a time.

    1.  Select **Add question**.

    2.  Enter your **Question**.

    3.  Toggle the **Required question** to make the question optional.

        **Note:** Marking a question as required means the user must answer it before submitting the questionnaire. It doesn't prevent the user from skipping the activity. For more information, see [Questionnaire activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/questionnaire-activity.md).

    4.  Select a **Type of answer** for this question.

        Each answer type may have its own specific additional required configurations.

    5.  Enter a **Max answer length** to set the maximum number of characters a user can enter for their answer during runtime.

    6.  Repeat step 5 for all the questions you want to add.

    \[Omitted image "pb-questionnaire-pb-2.png"\] Alt text: Screenshot showing the question fields.

8.  Select **Save and close** to complete the questionnaire.

9.  In the canvas, hover over the questionnaire activity and select the Edit icon \[Omitted image "workspace-icon-edit.png"\] Alt text: Edit credentials icon..

    You can add, reorder, and remove questions, and change the options available on a question.

    **Note:**

    Editing a questionnaire changes the activity definition. Playbook executions already in progress continue to use the questionnaire as it was when the execution started.


**Parent Topic:**[Questionnaire activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/questionnaire-activity.md)

