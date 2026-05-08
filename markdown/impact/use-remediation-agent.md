---
title: Use Real-time prevention monitoring to fix a general guidelines finding
description: Navigate the AI-Eligible Findings dashboard, generate an AI fix for an existing finding, review the code comparison, and apply the fix to your instance.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-05-07"
reading_time_minutes: 2
breadcrumb: [Real-time prevention monitoring for Scan Engine, Scan Engine, Platform Health, Using Impact, Impact]
---

# Use Real-time prevention monitoring to fix a general guidelines finding

Navigate the AI-Eligible Findings dashboard, generate an AI fix for an existing finding, review the code comparison, and apply the fix to your instance.

## Before you begin

Role required: gen\_ai\_ai\_fix\_user

## About this task

When a Scan Engine run detects findings in your instance, Real-time prevention monitoring surfaces those that are eligible for AI-generated fixes. You review the proposed code change side-by-side with the original code, then accept or reject it. Fixes are applied within your active update set so your change management process stays intact.

The diagram indicates the overall flow of the steps to fix a general guidelines finding.

![Flow chart to fix a general guidelines finding outlining the required steps.](../image/real-time-agent-fix-code-flow.png)

## Procedure

1.  Navigate to **All** &gt; **Impact** &gt; **Platform Health**.

    This is the control center for instance quality. Diagnostics, analytics trending, and findings are all accessible from here.

2.  Navigate to **Platform Health** &gt; **Findings** &gt; **Open findings**.

    -   This opens the AI-Eligible Findings dashboard which is the developer's landing page.
    -   Every finding displayed is already AI-eligible and Now Assist can generate a fix for it. The view is intentionally scoped so developers only see what AI can act on.
    -   There are three available tabs.
    |Tab|Description|
    |---|-----------|
    |Open findings|AI-eligible issues available to be addressed|
    |AI fixes ready to review|Fixes that are generated, awaiting your approval|
    |Resolved|Your complete history of closed findings|

    **Note:** Next, generate a fix.

3.  Select a finding and request to generate an AI fix.

    1.  In the **Open findings** list, select any finding using its check box.

    2.  Select **Fix with Now Assist**.

    3.  Select **Generate**.

        -   Now Assist reads the specific script and writes a corrected version, not a template, but a fix tailored to the exact code.
        -   The status will update from Pending to Ready when the fix is complete.
    **Tip:** If you do not want to wait for generation during the exercise, move to the **AI fixes ready to review** tab, as a fix may already be available from a prior run.

4.  Navigate to **AI fixes ready to review** &gt; **Review AI fixes** to evaluate the AI-generated fix.

    The review screen opens with a list of scanned records that have fixes available on the first panel.

5.  Select an entry to load and examine the Code Comparison.

    -   Original code appears on the first panel.
    -   AI-generated fixes appear on the second panel.
6.  Review the specific Now Assist suggested change and confirm the finding is addressed correctly.

    Common fix types you may see:

    -   Replacing deprecated API calls, for example, `gs.log` → `gs.error`
    -   Adding missing error handlers
    -   Correcting scoped APP API usage
7.  Select **AI Finding Details**.

    This panel provides a less technical explanation of what the general guideline is, why this specific code violates it, what changed, and why the fix is correct.

8.  Select **Accept all** to initiate acceptance of all AI fixes.

9.  Review the confirmation dialog carefully, then select **Accept and fix code**.

    **Note:** The fix is applied in your current scope and update set. A full audit trail is created, including who approved the fix, when it was applied, and exactly what changed. The original code is preserved in the update set. If necessary, you can reverse the operation.

10. Navigate to the **Resolved** tab to confirm.

    Your finding should now appear there, confirming the fix was accepted and applied successfully. If the fix status does not change from Pending, check the **AI fixes ready to review** tab for a previously generated fix or wait and refresh the page.


## Result

The finding no longer appears in **Open findings** and is listed under the **Resolved** tab.

