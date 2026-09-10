---
title: Test access to an AI asset
description: Verify whether a user has access to an agentic AI asset - AI agent and agentic workflow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/test-access-ai-asset.html
release: australia
topic_type: task
last_updated: "2026-09-03"
reading_time_minutes: 1
keywords: [Access analyzer, Test access to AI asset]
breadcrumb: [Implement access control in AI Agent Studio, Configure AI Agent Studio, AI Agent Studio, Enable AI experiences]
---

# Test access to an AI asset

Verify whether a user has access to an agentic AI asset - AI agent and agentic workflow.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Agentic Solutions**.

2.  Select an AI asset you want to test access to.

    You can test access to an AI agent and agentic workflow. Select one of them from the Agentic solution page.

3.  In the node map view or guided setup, select **Run test**.

4.  On the Run a test pop up, select **Single test** as the test type and choose a test objective from the auto-populated objectives.

5.  Select **Run Single test**.

6.  Review the test results.

    If there is a failed test due to ACL issues, you will see in the node map view, the reason for the failed test in the Chat window. In the Trace Log tab, you will see the test status along with the relevant links to understand more details about the failure:

    \[Omitted image "test-access-ai-asset.png"\] Alt text: The test access page of an AI asset in mode map view.

    -   Select **Access Analyzer**: You can go to Access Analyzer for more details.

        This opens the Permission for Explain SLA page in Access Management, where you can see the access results for the executed AI asset.

    -   Select **Access rules**: You can revisit the access rules for the selected AI asset.

