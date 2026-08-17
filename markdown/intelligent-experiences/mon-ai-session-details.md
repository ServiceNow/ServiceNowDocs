---
title: Session details
description: View metric breakdowns, the judge's reasoning, and trace and span data for a specific evaluated session.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/mon-ai-session-details.html
release: australia
topic_type: concept
last_updated: "2026-06-30"
reading_time_minutes: 5
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Investigate sessions, Monitor and evaluate AI systems, Monitor AI assets, AI Control Tower, Enable AI experiences]
---

# Session details

View metric breakdowns, the judge's reasoning, and trace and span data for a specific evaluated session.

## Key benefits

-   Understand which metrics are pulling a session's quality or safety score up or down by reviewing the scoring breakdown.
-   Read the judge's reasoning for each metric to understand why a score was assigned.
-   Identify the exact trace and span where an issue occurred by following the score indicators in the span timeline.
-   Compare the AI system's input and output at each step to determine whether the issue originated in the data the system received or the response it produced.

\[Omitted image "mon-ai-session-details.png"\] Alt text: The session detail page showing quality and safety score cards, session scores, and a list of traces.

## Viewing session information

The session details page shows the AI system, its type, session duration, and token usage. Duration is measured from the first interaction to session close or timeout \(10 minutes of inactivity\). Total runtime tokens reflect the cost of running the interaction, not the cost of evaluating it.

## Quality and safety score cards

Review the overall quality and safety of the session by reviewing the score cards. View a breakdown of the score by selecting the side panel icon. The side panel is filtered to show only the metrics that apply to this session, along with each metric's weight, score, and explanatory notes about how the score is calculated.

## Session scores and aggregate scores

Understand what's driving a session's quality and safety scores by reviewing all of its evaluated metrics in one place. Metrics scored at the session, trace, or span level all roll up to this section, so you don't have to open each trace or span to see an individual score.

Session-level metrics such as Task completion assess the entire conversation rather than individual traces or spans, so a low session-level score often means the agent didn't accomplish the user's overall goal, even when individual steps were executed correctly. To see whether a metric was evaluated at the session, trace, or span level, check the Level column.

For a metric evaluated at the trace or span level, the score shown is an aggregate, meaning the average of that metric's scores across the traces or spans where it was evaluated. To understand any score, read the Reason column. For an aggregated metric, the reason notes that the score is an average and points you to open an individual span or trace to read the judge's reasoning for each one.

## Traces

Sort the traces to focus your investigation by selecting Lowest quality score, Lowest safety score, Highest latency, or other criteria from the list. Select a trace to open the trace detail.

A trace shows N/A for its Quality or Safety score when no metrics in your corresponding metric template apply to that trace. This happens when all metrics in the template are evaluated at the session or span level only, or when the metrics that do apply to the trace level weren't evaluated for that particular trace. An N/A score doesn't indicate a problem with the trace. Rather, it indicates that your template's formula has nothing to calculate at the trace level. To see scores for that trace, either:

-   Add a trace-level metric to your template. See [Configure an evaluation metric template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-configure-metric-templates.md).
-   Review span-level scores by expanding the trace and selecting individual spans in the timeline.

## Trace detail

Identify which trace in the session is responsible for the low score by reviewing the traces list. View the span timeline and evaluation data by selecting a trace.

-   **Span timeline**

    Visualizes the trace as a waterfall where each span appears as a horizontal bar showing its duration. Nested spans are indented under their parent. Quality and safety indicators on individual spans highlight which spans scored highest or lowest, so you can focus your investigation on the right span without reviewing each one individually.

-   **Evaluation scores**

    Lists each evaluation metric scored for this trace, along with the score and the judge's reasoning. Select a reason to open the full reasoning in a modal. Use this table to understand which metrics drove the trace's score before selecting individual spans.

-   **Details**

    Shows what the AI system received and what it produced for this trace. Select the **Input** tab to view the user's request or the data passed to the agent. Select the **Output** tab to view the agent's response. Select **Open details** to view the full content in a modal when the preview is truncated.


Navigate between traces without returning to the session detail page by selecting **Previous trace** or **Next trace**.

## Span detail

Identify the root cause of an issue at the most granular level by selecting a span in the timeline and viewing the details.

-   **Duration**

    Time the span took to execute. Unusually high duration can indicate a slow external service call or a timeout that affected the agent's response.

-   **Tokens \(input, output, total\)**

    Number of tokens consumed by the span. Compare input and output token counts to assess whether the response is proportional to the prompt. A high input token count relative to other spans may indicate the agent is sending excessive context to an LLM call.

-   **Quality**

    Quality score for this span. A low quality score on a specific span helps you pinpoint which step in the agent's reasoning or tool usage produced an incorrect or incomplete result.

-   **Safety**

    Safety score for this span. A low safety score on a specific span helps you isolate which step in the agent's execution produced inappropriate content.


**Note:** The token counts reflect the cost of running the AI system's actual interaction, not the cost of evaluating it. Evaluation scoring consumes separate tokens that aren't displayed here.

Learn why a span scored the way it did by reviewing the evaluation metric scores and the judge's reasoning. For example, a Tool choice accuracy score of 54% with reasoning that says "the agent selected a knowledge base search when a CMDB lookup was more appropriate" tells you exactly what decision the agent made incorrectly.

Determine whether the issue originated in the input or the output by viewing the Details section. The **Input** tab shows the data or prompt passed to the span. The **Output** tab shows what the span returned. For example, a correctly formatted request paired with an incorrect tool call tells you the issue is in the agent's logic, not the incoming data. Select **Open details** to view the full content when the preview is truncated.

**Parent Topic:**[Investigating low-scoring sessions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-investigating-low-scoring-sessions.md)

