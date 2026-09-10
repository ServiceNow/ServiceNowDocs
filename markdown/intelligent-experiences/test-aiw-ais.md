---
title: Preview an AI specialist in the legacy AI Agent Studio
description: Run a preview of your AI specialist in the legacy AI Agent Studio on a single record to preview how it works and verify it matches your intentions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/test-aiw-ais.html
release: zurich
topic_type: task
last_updated: "2026-08-11"
reading_time_minutes: 1
keywords: [test AI specialist, preview AI specialist]
breadcrumb: [Configure in the legacy AI Agent Studio, Configure, Autonomous Workforce, AI Agent Studio, Enable AI experiences]
---

# Preview an AI specialist inthe legacy AI Agent Studio

Run a preview of your AI specialist inthe legacy AI Agent Studio on a single record to preview how it works and verify it matches your intentions.

## Before you begin

Role required: sn\_aia.admin

## About this task

You can test an execution of the AI specialist on a single record to preview its capabilities.

**Note:** Previewing an AI specialist, depending on the tasks configured, can actually make changes to the record. Previews are not simulations.

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.

2.  In the **AI specialists** tab, select the AI specialist you want to preview.

3.  Navigate to the **Preview** tab in the AI specialist guided setup.

4.  Choose a record to run the preview on.

    Recommended records for preview are selected based on their relevance to the capabilities and tasks available to the AI specialist.

    Once a record is chosen, you can select the open link button to open the record in a new browser tab to check the details.

    **Note:** Choose records that you can safely make changes to. The work is actually being done on the record during the preview.

5.  Select **Run** to begin the preview.

    The test begins on the record. You can watch what fields it updates and any comments or work notes it generates.

    When the test is complete, you can review all the changes made.

6.  Verify that the AI specialist's performance meets your expectations.

    See the Testing section in [General guidelines for AI specialists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gg-ai-workforce.md) for more information about how to test your AI specialist.


## Result

Your AI specialist has worked on a specific record or records of your choice.

## What to do next

You can return to the **Profile** or **Tasks** tabs in the guided setup to make changes if necessary. Once the changes are made, you can preview the AI specialist again.

If you are satisfied with the AI specialist's performance after making changes, you can select **Save** to save changes or **Activate** to let the AI begin work.

