---
title: Generate a playbook summary
description: Generate an AI-generated summary of the stages, activities, triggers, and inputs of a playbook from the Workflow Studio canvas.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/build-workflows/workflow-studio/generate-playbook-summary.html
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-05-26"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Playbook summarization, Playbooks in Workflow Studio, Building playbooks, Use, Workflow Studio, Build workflows]
---

# Generate a playbook summary

Generate an AI-generated summary of the stages, activities, triggers, and inputs of a playbook from the Workflow Studio canvas.

## Before you begin

The playbook must have at least one stage and activity before a summary can be generated.

Role required: pd\_author

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Open the playbook for which you want to generate the summary.

3.  From the More Actions menu \( \[Omitted image "triggers-more-actions.png"\] Alt text:\), select **Summarize**.

4.  On the Playbook Summary panel, select **Summarize playbook**.

5.  Select a summary format: **Standard**, **Short**, or **Elaborate**.

    The summary is generated and displayed in the panel. The first paragraph provides a brief overview of the playbook, followed by a description of each stage.


## What to do next

After generating a summary, you can perform the following actions:

-   To refine the summary, use the **Refine** options to elaborate, shorten, or change the tone, or enter a custom instruction in the open prompt field.
-   To regenerate the summary after playbook changes, select **Refresh**. If the playbook structure has changed since the last summary was generated, a warning appears prompting you to refresh.
-   To copy the summary to the playbook description field, select **Set as description**, then select **Save and close**.

**Parent Topic:**[Playbook summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-studio/playbook-summarization.md)

