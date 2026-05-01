---
title: Duplicate an agentic workflow
description: Duplicate an existing agentic workflow in AI Agent Studio to save time by not having to manually configure or create agentic workflows.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-05-01"
reading_time_minutes: 2
breadcrumb: [Create an agentic workflow, Now Assist AI agents, Enable AI experiences]
---

# Duplicate an agentic workflow

Duplicate an existing agentic workflow in AI Agent Studio to save time by not having to manually configure or create agentic workflows.

## Before you begin

Role required: sn\_aia.admin

## About this task

Duplicate the agentic workflows to do the following tasks:

-   Duplicate the record.
-   Disallow any agentic workflows with existing names.

Custom columns, such as the Tools and Knowledge sources, Status, and a column with the Duplicate icon \(![Duplicate icon.](../image/ai-agents-clone-icon.png)\) are available for agentic workflows list.

**Note:** Selecting the Duplicate icon duplicates the selected agentic workflow.

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage** &gt; **Agentic workflows** and open the AI agents list in AI Agent Studio.

2.  Duplicate the agentic workflow from either the Manage agentic workflows and AI agents page or the AI agent form.

    |Current location|Navigation option|
    |----------------|-----------------|
    |**Manage agentic workflows and AI agents page**|On the agentic workflows list, select the duplicate icon \(![Duplicate icon.)](../image/ai-agents-clone-icon.png)\) for the agentic workflow that you would like to duplicate.|
    |**AI agent form**|Open the agentic workflow that you want to duplicate, select the menu icon \(![Menu icon.](../image/three-dots-icon.png)\) next to **Exit** on the Describe and instruct form, and select **Duplicate**.|

    You see a confirmation message in a pop-up window.

    ![Confirmation pop-up window that asks you to either duplicate the agentic workflow or cancel the action.](../image/clone-use-case-confirm.png)

3.  Create a copy of the agentic workflow with the same information from the original agentic workflow's record by selecting **Duplicate**.

    **Note:**

    -   The agentic workflow is duplicated with the original agentic workflow's name but it’s appended with the suffix `(Copy)` to help you identify the duplicated agentic workflow from the original agentic workflow. For example, `Steps for Issue Resolution (Copy)`. You can rename it and also edit the other information that is duplicated.
    -   All the AI agents that were connected to the original agentic workflow are also added to the duplicated agentic workflow. You can edit these AI agents and add more agents for your own requirements.
4.  After editing the details in the Describe and instruct section, select **Save and continue**.

5.  In the Define Trigger section, activate any triggers that are duplicated from the original agentic workflow if you need them and select **Save and continue**.

    **Note:** The triggers that you see in the duplicated agentic workflows are from the original agentic workflow. They aren’t active by default but you can activate them if necessary.

6.  In the Toggle display section, turn on the Display toggle for the duplicated agentic workflow to be visible in the Now Assist panel and select **Save and test**.


## Result

You’re redirected to the AI Agent Studio home page. In the Manage and configure AI agents to solve agentic workflow section on the **Agentic workflows** tab, you see the duplicated agentic workflow.

