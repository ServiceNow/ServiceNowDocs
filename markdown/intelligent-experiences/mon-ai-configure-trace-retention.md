---
title: Configure trace data retention and access
description: Control how long session, trace, and span data is stored to reduce storage usage, and choose whether that data stays available for analysis.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/mon-ai-configure-trace-retention.html
release: zurich
topic_type: task
last_updated: "2026-08-18"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, Monitoring and evaluating AI systems, Monitor AI assets, AI Control Tower, Enable AI experiences]
---

# Configure trace data retention and access

Control how long session, trace, and span data is stored to reduce storage usage, and choose whether that data stays available for analysis.

## Before you begin

Role required: admin

## About this task

By default, session, trace, and span data is retained for 30 days. If your organization has strict data-minimization requirements, a system administrator can shorten that window or stop retaining trace data altogether. Aggregate quality and safety scores remain available either way; only the underlying trace-level detail is affected.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Settings** &gt; **Rules and templates** &gt; **Evaluation**.

2.  Select the **Trace data retention and access** sub-tab.

3.  Choose a trace retention option.

<table id="choicetable_xh1_qdf_hkc"><thead><tr><th align="left" id="d131372e106">

Option

</th><th align="left" id="d131372e109">

Description

</th></tr></thead><tbody><tr><td id="d131372e115">

**Don't keep traces**

</td><td>

Permanently delete session, trace, and span data after approximately 1 day, once scoring is complete, by selecting **Don't keep traces**.After selecting this option, no session data is displayed in AI Control Tower.

-   Evaluated sessions views on the monitoring overview and on each AI system's **Monitor** tab are hidden.
-   Actionable insights from AI Skill Kit are turned off.


</td></tr><tr><td id="d131372e146">

**Keep traces for scoring**

</td><td>

1.  Retain data for analysis and re-scoring by selecting **Keep traces for scoring**.
2.  Specify the number of days to keep the data from 1 to 30.


</td></tr></tbody>
</table>4.  Select **Save**.

    **Warning:** If the new setting would delete data you're currently storing, a confirmation dialog shows how many traces would be deleted and how many AI systems are affected. Type the exact trace count shown, then select **Deletion** to confirm. This action can't be undone.


## Result

A confirmation message shows the retention period now in effect. The setting applies instance-wide, across all AI evaluation pipelines.

