---
title: Investigate a low-scoring session
description: Determine the root cause of a low quality or safety score by working through the session detail, trace timeline, and span-level input and output data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/mon-ai-investigate-session-task.html
release: australia
topic_type: task
last_updated: "2026-04-08"
reading_time_minutes: 4
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Investigating sessions, Monitoring and evaluating AI systems, Monitor AI assets, Super Intelligence Control Tower, Enable AI experiences]
---

# Investigate a low-scoring session

Determine the root cause of a low quality or safety score by working through the session detail, trace timeline, and span-level input and output data.

## Before you begin

Role required: sn\_ai\_asset\_mgmt.ai\_asset\_owner or sn\_ai\_governance.ai\_steward

## About this task

Trace and span detail for a session is available only for a limited time. To review the judge's reasoning and the input and output for each trace and span, complete your investigation within 7 days for ServiceNow AI systems, or within 30 days for external AI systems. After that window, the session's quality and safety scores remain available, but the trace and span detail is removed.

## Procedure

1.  Navigate to **All** &gt; **Control Tower** &gt; **Home** &gt; **Insights** &gt; **Monitor** and select the **Evaluated sessions** tab.

2.  In the Evaluated sessions list, find the session that you want to investigate.

    For example, sort by score to identify the lowest-scoring sessions, search for a specific session by name, or filter the list to find the session.

3.  Select the session that you want to investigate.

4.  On the session detail page, determine which quality metrics are contributing to the low score by reviewing the Quality score card.

    1.  Open the quality scoring breakdown by selecting the side panel icon.

    2.  Review each metric's weight and score to determine which metric is affecting the score.

    3.  Close the side panel.

    For example, if the session quality score is 67%, the side panel might show that Answer relevancy scored 50% at 40% weight, while Answer completeness scored 91% at 35% weight. The low Answer relevancy score is the primary contributor to the low quality composite.

5.  On the session detail page, determine which safety metrics are contributing to the low score by reviewing the Safety score card.

    1.  Open the safety scoring breakdown by selecting the side panel icon.

    2.  Review each metric's weight and score to determine which metric is affecting the score.

    3.  Close the side panel.

    For example, a Profanity score of 0% at 49% weight would immediately explain a low safety composite.

6.  Identify which metrics are lowering the quality and safety scores by reviewing the lowest scoring metrics on each score card.

    Each card lists up to three of the metrics that contribute to the score, starting with the lowest. To learn more about any score, point to the information icon next to the metric name. When a score is an average, the reason points you to open an individual span or trace to read the judge's reasoning for each one.

7.  Identify which trace is responsible for the low score by sorting the traces list.

    -   Find the trace with the lowest quality score by selecting **Lowest quality score**.
    -   Find the trace with the lowest safety score by selecting **Lowest safety score**.
8.  Select the trace that you want to investigate.

9.  In the trace side panel, determine which metrics failed on that trace by reviewing the trace-level evaluation scores and the judge's reasoning.

    The evaluation scores table shows only the metrics applicable to this trace. Different metrics are evaluated at the trace level than at the span level.

    The judge's reasoning tells you what specifically went wrong. For example, an Answer completeness score of 50% with reasoning "The response covered only some of the relevant information in the retrieved context" tells you the agent's response was incomplete.

10. Determine whether the agent's response addressed the user's request by reviewing the trace-level input and output.

    The input and output show you the actual conversation between the user and the AI system.

    1.  Select the **Input** tab to see what the user asked or what data was passed to the agent.

    2.  Select the **Output** tab to see how the agent responded.

    3.  Select **Open details** to view the full content when the preview is truncated.

11. Identify and select the span that caused the issue using the quality and safety indicators in the span timeline.

12. Confirm the root cause by reviewing the span's evaluation scores and comparing its input and output data.

    1.  Review the evaluation metric scores and the judge's reasoning for this specific step.

    2.  Select the **Input** tab to see what data was passed to this span.

    3.  Select the **Output** tab to see what the span produced.

    4.  Select **Open details** to view the full content when the preview is truncated.

    At the span level, the input and output show the agent's internal execution, not the user-facing conversation. For example, the input might be a correctly formatted API request, while the output shows the agent called the wrong endpoint or passed a malformed parameter.

13. Review additional traces to determine whether the issue is isolated or recurring by selecting **Next trace** or **Previous trace** to navigate between traces.


## What to do next

After identifying the root cause, coordinate with the product owner to adjust the agent's configuration, prompts, or tool access. Monitor subsequent sessions to verify that the issue is resolved.

**Parent Topic:**[Investigating low-scoring sessions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/mon-ai-investigating-low-scoring-sessions.md)

