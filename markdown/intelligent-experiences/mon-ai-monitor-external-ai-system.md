---
title: Activate evaluation scoring for external AI systems
description: Assess the quality and safety of your external AI systems by connecting them to AI Control Tower and activating evaluation scoring.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/mon-ai-monitor-external-ai-system.html
release: australia
topic_type: task
last_updated: "2026-07-13"
reading_time_minutes: 5
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, Monitor and evaluate AI systems, Monitor AI assets, AI Control Tower, Enable AI experiences]
---

# Activate evaluation scoring for external AI systems

Assess the quality and safety of your external AI systems by connecting them to AI Control Tower and activating evaluation scoring.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward

## About this task

External AI systems require trace data to be scored by the evaluation engine. Unlike AI systems on the ServiceNow AI Platform, which are automatically instrumented, external AI systems must be connected to send trace data to AI Control Tower. There are two ways to establish this connection:

-   **SDK instrumentation**: Instrument your AI agent code using the Traceloop SDK and authenticate with an API key. Use this method for any AI agent framework that is not hosted on a supported cloud platform or monitoring service.
-   **Trace connection**: Connect to a supported cloud platform or monitoring service through your cloud credentials and a MID Server. Use this method when your AI agents already run on or send traces to a supported platform. No API key or code instrumentation is required.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Settings** &gt; **Rules and templates** &gt; **Evaluation**.

2.  On the **AI evaluations** sub-tab, select **External AI systems**.

3.  Set the **Activate** toggle to on.

4.  Connect your external AI system to send trace data to AI Control Tower using SDK instrumentation or a trace connection.

<table id="choicetable_connection_method"><thead><tr><th align="left" id="d33899e143">

Connection method

</th><th align="left" id="d33899e146">

Description

</th></tr></thead><tbody><tr><td id="d33899e152">

**SDK instrumentation**

</td><td>

Use for any third-party AI agent framework \(CrewAI, LangChain, AWS Agent Core, and others\) not connected through a trace connection. Requires generating an API key and configuring the Traceloop SDK in your agent code.

 1.  Generate an API key to authenticate trace data requests from your external AI system.

**Note:** Multiple API keys can exist, but only one is active at a time.

    1.  In the **API key for external AI system evaluation** section, select **Create API key**.

The API Key record page opens on a new browser tab.

    2.  On the form, fill in the fields.

<table id="table_api_key_fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the API key.

</td></tr><tr><td>

Description

</td><td>

Purpose of the API key.

</td></tr><tr><td>

User

</td><td>

User associated with this API key.Select a user with the `sn_ai_observe.ai_data_sender` role. Use a dedicated service account rather than a user with elevated permissions. This role is installed with the AI Control Tower Evaluations plugin and grants permission to send observability data without granting read or write access to AI Control Tower configuration. If the service account does not already have this role, assign it before creating the API key.

</td></tr><tr><td>

Active

</td><td>

Whether the API key is active.

</td></tr><tr><td>

Auth Scope

</td><td>

Scope that controls the API key's authority at runtime.

</td></tr><tr><td>

Expiry

</td><td>

Date when the API key expires. Leave empty for no expiration.

</td></tr></tbody>
</table>    3.  Select **Submit**.

    4.  Copy the generated token and store it securely.

The token is displayed only once. If you lose it, generate a new key, which deactivates the previous one.

    5.  Return to the AI Control Tower browser tab and refresh the page.

The new API key appears in the **API key for external AI system evaluation** section.

2.  Instrument your AI agent to send trace data to your ServiceNow instance.

For instrumentation steps using the Traceloop SDK, see [Instrument a third-party AI agent with the Traceloop SDK for AI Control Tower Evaluations](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3144255).

</td></tr><tr><td id="d33899e340">

**Trace connection**

</td><td>

Use when your AI agents run on a supported cloud platform or already send traces to a supported monitoring service. The ServiceNow AI Platform collects trace data through your cloud credentials and a MID Server. No API key or SDK instrumentation is required.

 See [Configuring trace connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-configuring-trace-connections.md).

</td></tr></tbody>
</table>5.  Review the quality and safety metrics that are included by default.

    The following quality and safety metrics are evaluated for external AI systems with a 5% sample rate by default.

    -   **Task completion**

        Whether the agent decision path and output satisfy the user's request.

    -   **Answer relevancy**

        Whether the response addresses the query and remains on topic.

    -   **Secrets detection**

        Whether the response contains leaked credentials, API keys, or other sensitive secrets.

    -   **Instruction adherence**

        How closely the response follows the given instructions.

    For a complete list of available metrics and their descriptions, see [Evaluation metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-evaluation-metrics-reference.md).

6.  Add or remove metrics that you want to evaluate.

    **Important:** Adding more metrics increases the visibility you gain into each session, but also increases the processing performed to evaluate it. Select the metrics that give you the insight you need.

<table id="choicetable_add_remove_metrics_ext"><thead><tr><th align="left" id="d33899e443">

Option

</th><th align="left" id="d33899e446">

Description

</th></tr></thead><tbody><tr><td id="d33899e452">

**Add metrics**

</td><td>

1.  Select **+ Add metrics**.
2.  In the Add evaluation metrics panel, find or search for the metric that you want to add.
3.  Select the metric.
4.  Select **Done**.


</td></tr><tr><td id="d33899e482">

**Remove metrics**

</td><td>

1.  In the Included Agentic AI metrics table, find the metric that you want to remove.
2.  Select the remove icon.
3.  Select **Remove** to confirm.


</td></tr></tbody>
</table>7.  Update the sample rate for one or more included metrics.

    The sample rate determines what percentage of AI executions a metric evaluates. For external AI systems, each metric has its own sample rate, so you can evaluate the metrics that matter most on more executions and sample the rest to limit processing.

    **Note:** When metrics that contribute to the same quality or safety score use different sample rates, the metric with the higher rate evaluates more executions and can skew that score toward its results.

    1.  In the Agentic AI metrics table, select the edit icon next to the sample rate that you want to update.

    2.  Enter the new sample rate.

    3.  Select **Apply**.


## Result

Evaluation scoring is active for external AI systems. Scores appear on the monitoring Overview page as new sessions are evaluated.

## What to do next

To have a metric contribute to your quality or safety scores, add it to a metric template and assign a weight. See [Configure an evaluation metric template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-configure-metric-templates.md).

To start evaluating a managed external AI system, you must turn on evaluation at the asset level. See [Enable evaluation for an AI system](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/disc-enable-evaluation.md).

**Parent Topic:**[Configuring monitoring and evaluations in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-configuring-aict-evaluations.md)

