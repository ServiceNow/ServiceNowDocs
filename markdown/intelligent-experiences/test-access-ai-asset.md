---
title: Test access to an AI asset
description: Verify whether a user has access to an agentic AI asset \(an AI agent or an agentic workflow\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/test-access-ai-asset.html
release: australia
topic_type: task
last_updated: "2026-10-15"
reading_time_minutes: 1
keywords: [Access analyzer, Test access to AI asset]
breadcrumb: [Implement access control in AI Agent Studio, Configure AI Agent Studio, AI Agent Studio, Enable AI experiences]
---

# Test access to an AI asset

Verify whether a user has access to an agentic AI asset \(an AI agent or an agentic workflow\).

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

    If a test fails because of ACL issues, the reason for the failure appears in the Chat window in the node map view. In the Trace Log tab, you can see the test status and the relevant links to understand more details about the failure:

    \[Omitted image "test-access-ai-asset.png"\] Alt text: Test Access page of an AI asset in the node map view with the trace log open showing an error that access is denied to the user.

    -   Select **Access Analyzer**: You can go to Access Analyzer for more details.

        This opens the Permission for Explain SLA page in Access Management, where you can see the access results for the executed AI asset.

    -   Select **Access rules**: You can revisit the access rules for the selected AI asset.

