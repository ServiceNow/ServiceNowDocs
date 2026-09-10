---
title: Preview an AI specialist in the new AI Agent Studio
description: Run a preview of your AI specialist in the new AI Agent Studio on a single record to preview how it works and verify it matches your intentions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/test-aiw-ais-new.html
release: australia
topic_type: task
last_updated: "2026-05-26"
reading_time_minutes: 1
breadcrumb: [Configure in AI Agent Studio, Configure, Autonomous Workforce, Enable AI experiences]
---

# Preview an AI specialist in the new AI Agent Studio

Run a preview of your AI specialist in the new AI Agent Studio on a single record to preview how it works and verify it matches your intentions.

## Before you begin

Role required: sn\_aia.admin

## About this task

You can test an execution of the AI specialist on a single record to preview its capabilities.

**Note:** Previewing an AI specialist, depending on the tasks configured, can actually make changes to the record. Previews aren't simulations.

## Procedure

1.  Navigate to the **All** &gt; **AI Agent Studio** &gt; **Agentic solutions**.

2.  Select the AI specialist you want to preview.

3.  In the node view, select the first node of the AI specialist.

    The first node contains the main configuration settings for the AI specialist. The other nodes represent the individual agents that comprise the underlying architecture and do not require modification to preview an AI specialist.

4.  Scroll down to the **Test** section in the AI specialist guided setup.

5.  In the dropdown menu, select a record you want to preview the AI specialist on.

    Once a record is chosen, you can select the open link button to open the record in a new browser tab to check the details.

    **Note:** Choose records that you can safely make changes to. The work is actually being done on the record during the preview.

6.  Select **Run** to begin the preview.

    The test begins on the record. You can watch what fields it updates and any comments or work notes it generates.

    When the test is complete, you can review all the changes made.

7.  Verify that the AI specialist's performance meets your expectations.

    See the Testing section in [General guidelines for AI specialists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gg-ai-workforce.md) for more information about how to test your AI specialist.


## Result

Your AI specialist has worked on a specific record or records of your choice.

## What to do next

You can return to the **Profile** or **Tasks** sections by scrolling up in the guided setup to make changes if necessary. Once the changes are made, you can preview the AI specialist again.

If you're satisfied with the AI specialist's performance after making changes, you can select **Save** to save changes or **Activate** to let the AI begin work.

