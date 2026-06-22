---
title: Health tab in AI Control Tower
description: Monitor the performance of guardrails enabled through Now Assist Guardian.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-control-tower/aict-health-tab.html
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Health, Now Assist Guardian]
breadcrumb: [AI Control Tower Home, AI Control Tower dashboard, Explore, AI Control Tower, Enable AI experiences]
---

# Health tab in AI Control Tower

Monitor the performance of guardrails enabled through Now Assist Guardian.

The Health tab in the AI Control Tower dashboard helps you monitor and evaluate the effectiveness of offensive content and prompt injection guardrails active on your ServiceNow AI assets.

\[Omitted image "aict-health-tab.png"\] Alt text: Health tab showing the metrics for offensive content and prompt injection guardrails.

The visualizations on the Health tab provide the following insights.

-   Average latency as a result of active offensive content and prompt injection guardrails. High latency could mean increased guardrail activity in the period.
-   Count and percentage of offensive content and prompt injection occurrences.
-   Skills where offensive content and prompt injection occurrences were detected.

The dashboard does not consider historical data for Health metrics.

Apply the filters on the dashboard to view guardrail activity for skills in a date range.

## Content guardrail effectiveness

-   **Number of content items flagged**

    This area of the dashboard shows the number of offensive content and prompt injection occurrences in the selected date range.

    \[Omitted image "aict-health-total-content-flagged.png"\] Alt text: Visualization showing the total number of content items flagged for offensiveness and prompt injection.

-   **Percentage of content items flagged of total use**

    This area of the dashboard shows the percentage of requests and responses to and from the large language model \(LLM\) service that are flagged for offensiveness and prompt injection.

    \[Omitted image "aict-health-total-percentage-content-flagged.png"\] Alt text: Visualization showing the percent of content items flagged for offensiveness and prompt injection.


## Offensive content visualizations

-   **Guardrail-added latency**

    This area of the dashboard shows the average latency as a result of the active offensive content guardrail for the selected skills and date range.

    \[Omitted image "aict-health-guardrail-latency-offensive-content.png"\] Alt text: Guardrail latency for offensiveness guardrail.

-   **Percentage flagged as offensive**

    This area of the dashboard shows the percentage of requests and responses to and from the large language model \(LLM\) service that are flagged for offensive content.

    \[Omitted image "aict-health-percentage-offensive-content.png"\] Alt text: Percentage of offensive content occurrences.

-   **Total offensive content occurrences**

    This area of the dashboard shows the total number of offensive content occurrences for the selected skills and date range.

    \[Omitted image "aict-health-total-offensive-content.png"\] Alt text: Total number of offensive content occurrences.

-   **Categories of offensive content**

    This area of the dashboard shows a breakdown of offensive content occurrences by the categories. If content is deemed to be offensive under more than one category, for example, toxic and defamatory, the occurrence is counted individually toward both the categories. For more information on offensive content categories, see [Now Assist Guardian](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/servicenow-ai-platform-security/now-assist-guardian.md).

    \[Omitted image "aict-health-categories-offensive-content.png"\] Alt text: Visualization showing the categories of offensive content.

-   **Offensive content occurrences by skill**

    This area of the dashboard shows the number of offensive content occurrences over time by the skills in which the content is detected.

    \[Omitted image "aict-health-offensive-content-occurrences-by-skill.png"\] Alt text: Offensive content occurrences by skill.


## Prompt injection visualizations

-   **Guardrail-added latency**

    This area of the dashboard shows the average latency as a result of the active prompt injection guardrail for the selected skills and date range.

    \[Omitted image "aict-health-guardrail-latency-prompt-injection.png"\] Alt text: Visualization showing the guardrail-added latency

-   **Percentage flagged as prompt injection**

    This area of the dashboard shows the percentage of requests and responses to and from the LLM service that are flagged for offensive content.

    \[Omitted image "aict-health-percentage-prompt-injection.png"\] Alt text: Visualization showing the percentage of requests and responses flagged as prompt injection.

-   **Total prompt injection occurrences**

    This area of the dashboard shows the total number of offensive content occurrences for the selected skills and date range.

    \[Omitted image "aict-health-total-prompt-injection.png"\] Alt text: Total prompt injection occurrences.

-   **Prompt injection occurrences by skill**

    This area of the dashboard shows the number of prompt injection occurrences over time by the skills where prompt injection attempts were detected.

    \[Omitted image "aict-health-prompt-injection-by-skill.png"\] Alt text: Visualization showing the number of prompt injection occurrences by skill.


