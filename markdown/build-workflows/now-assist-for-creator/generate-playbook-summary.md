---
title: Generate a playbook summary
description: Generate an AI-generated summary of the stages, activities, triggers, and inputs of a playbook from the Workflow Studio canvas.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/build-workflows/now-assist-for-creator/generate-playbook-summary.html
release: zurich
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: task
last_updated: "2026-05-26"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Playbook summarization, ServiceNow Otto for Creator, Build workflows]
---

# Generate a playbook summary

Generate an AI-generated summary of the stages, activities, triggers, and inputs of a playbook from the Workflow Studio canvas.

## Before you begin

Verify that the ServiceNow Otto for Creator plugin is installed and the **Playbook Summarization** skill is active.

**Note:** The skill is available in **Admin** &gt; **Now Assist Admin** &gt; **Now Assist Skills** &gt; **Creator**. If you don't see **Creator** under **Now Assist Skills**, the plugin is not installed.

\[Omitted image "now-assist-creator-skills.png"\] Alt text: Now assist for creator skills page.

For information about installing ServiceNow Otto for Creator, see [Install ServiceNow Otto for Creator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/now-assist-for-creator/install-now-assist-for-creator.md).

The playbook must have at least one stage and activity before a summary can be generated.

Role required: pd\_author

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Open the playbook for which you want to generate the summary.

3.  From the More Actions menu \[Omitted image "triggers-more-actions.png"\] Alt text:, select **Summarize**.

    The Playbook Summary pane displays.

4.  On the Playbook Summary panel, select **Summarize playbook**.

    \[Omitted image "playbook-summary-otto.png"\] Alt text: Generate a playbook summary from the summarize playbook button.

5.  Select a summary format: **Standard**, **Short**, or **Elaborate**.

    The summary is generated and displayed in the panel. The first paragraph provides a brief overview of the playbook, followed by a description of each stage.


## What to do next

After generating a summary, you can perform the following actions:

-   To refine the summary, enter a custom instruction in the AI chat field.
-   To copy the summary to the playbook description field, select **Set as description**, then select **Save and close**.
-   To regenerate the summary after playbook changes, select **Refresh**. If the playbook structure has changed since the last summary was generated, a warning appears prompting you to refresh.

**Related topics**  


[Playbook summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/now-assist-for-creator/playbook-summarization.md)

