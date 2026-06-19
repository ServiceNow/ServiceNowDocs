---
title: Use an AI skill as an activity
description: Use an existing AI skill as an activity in your playbook to perform lightweight, focused AI tasks. When the playbook reaches the activity, the skill runs, produces structured outputs, and passes those outputs to subsequent activities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/use-ai-skill-as-activity.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-05-05"
reading_time_minutes: 2
breadcrumb: [Stages and activities, Understanding the playbook components, Build Playbooks, Playbooks, Workflow Studio, Build workflows]
---

# Use an AI skill as an activity

Use an existing AI skill as an activity in your playbook to perform lightweight, focused AI tasks. When the playbook reaches the activity, the skill runs, produces structured outputs, and passes those outputs to subsequent activities.

## Before you begin

Make sure that the ServiceNow Call Now Assist Skill Step Plugin is installed.

Role required: playbook\_admin or pd\_author

## About this task

AI skills handle lightweight, one-shot tasks such as sentiment analysis or text generation. Unlike AI agents, skills don't require full agentic orchestration. When you add a skill to an activity, the skill inputs load dynamically based on the skill you select. You can reference the skill output in downstream activities using the data pill picker.

You can add multiple **Use an AI skill** activities to the same playbook, each performing a different focused task. The outputs of each skill are available independently to subsequent steps.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Open the playbook where you want to add the Use an AI skill activity.

3.  In a new or an existing stage, select **Add an activity**.

4.  From the list of activities, under **Common activities**, select **Use an AI skill**.

5.  In the properties panel, configure the activity.

    1.  In the **Automation** tab, fill in the fields:

        -   **AI skill**: The AI skill that you want to add to the activity.
        -   **Inputs**: The input field loads dynamically based on the skill you select and is specific to that skill. For example, if it is a `Incident root cause analyzer` skill, provide a detailed description of the incident as input to the skill.
    2.  Select **Save and close**.

6.  Reference the skill output in subsequent activities.

    1.  Add an activity where you want to reference the output, for example an instruction activity.

    2.  In the activity's Automation tab, open the data pill picker.

    3.  Select the output produced by the Use an AI skill activity.

    You can chain multiple skill activities in the same playbook and reference each skill's output independently in the activities that follow them.

    Skill outputs can also drive decision branching. You can configure a branch condition or playbook variant based on the value produced by a Use an AI skill activity.


## What to do next

After authoring is complete, test and activate the playbook.

**Parent Topic:**[Stages and activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/process-automation-designer-lanes-activities.md)

