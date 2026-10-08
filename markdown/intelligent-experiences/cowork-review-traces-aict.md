---
title: Review Cowork traces in AI Control Tower
description: Check the quality and safety scores of Cowork sessions in AI Control Tower, then open a session or trace to see which metric scores and details.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/cowork-review-traces-aict.html
release: zurich
topic_type: task
last_updated: "2026-09-30"
reading_time_minutes: 3
keywords: [AI Control Tower, traces, Monitor tab, sample rate]
breadcrumb: [Trace evaluation for Cowork in AI Control Tower, Configure, ServiceNow Cowork, Enable AI experiences]
---

# Review Cowork traces in AI Control Tower

Check the quality and safety scores of Cowork sessions in AI Control Tower, then open a session or trace to see which metric scores and details.

## Before you begin

Role required: sn\_app\_cowork.admin and sn\_ai\_governance.ai\_steward

## About this task

In AI Control Tower, each AI system is tracked as an asset in the Inventory Cowork appears as the ServiceNow CoworkAgent asset, which AI Control Tower creates when a user connects Cowork to the instance. The asset starts in the Unmanaged state, with limited functionality, and shows traces only after you move it to the Managed state. Nothing else needs to be configured to receive traces. For more on asset states, see [Managed and unmanaged AI assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/disc-ai-managed-unmanaged.md).

Review traces to see how users work with Cowork and to catch a drop in quality or safety scores, or a security issue in a response.

For how AI Control Tower scores traces, see [Trace evaluation for Cowork in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/cowork-trace-evaluation.md).

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home**,

2.  Select **Inventory**.

3.  In the search field, enter `Cowork`.

4.  Select **ServiceNow Cowork Agent**.

5.  Select **Move to Managed** to move the asset to **Managed**.

    The asset shows Managed, and the **Monitor** tab appears.

    To move several assets at once from the Inventory list, see [Move AI assets to managed](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/disc-move-assets-to-managed.md).

6.  Select the **Monitor** tab.

    The tab shows the average overall quality and safety scores, the metrics evaluated and their sample rate, average latency and tokens per session, and agent activity over time.

    **Note:** Scores appear only after evaluation finishes, which takes some time after a trace arrives. Until then, the score cards show no data. Refresh the page to see new scores.

7.  Scroll to **Recent evaluated sessions** and review the quality and safety score for each session.

8.  Select a session.

    The session page lists the lowest scoring metrics, a score and reason for each metric, and the traces in the session.

9.  Select a trace, then select a span.

    The span details show each metric score and the reason behind it.

    To trace a low score to its cause, see [Investigate a low-scoring session](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mon-ai-investigate-session-task.md).

10. To change which metrics run on this asset, select the gear icon on the **Metrics evaluated** card.

    Select the metrics in **Edit metrics evaluated for this asset**, then select **Save metric**.

    For the available metrics, see [Evaluation metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mon-ai-evaluation-metrics-reference.md).

    For more options, including sample rates for this asset, see [Configure asset-specific metrics for external AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mon-ai-configure-asset-metrics-external.md).

11. To score more traces, navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Settings** &gt; **Rules and templates** &gt; **Evaluation**, and raise the **Sample rate** on the **AI evaluations** sub tab.

    Select **Update** to save the change.

    For more about evaluation settings, see [Activate evaluation scoring for external AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mon-ai-monitor-external-ai-system.md).

    To set the sample rate for each metric, see [Configure global metrics for external AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mon-ai-configure-global-metrics-external.md).


**Parent Topic:**[Trace evaluation for Cowork in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/cowork-trace-evaluation.md)

