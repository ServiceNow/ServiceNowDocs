---
title: Now Assist Guardian analytics
description: Monitor the performance of guardrails enabled through Now Assist Guardian.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/enable-ai-experiences/now-assist-guardian-analytics.html
release: australia
product: Enable AI Experiences
classification: enable-ai-experiences
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Now Assist Analytics, Analyzing Now Assist performance, Exploring Now Assist Admin, Now Assist, Enable AI experiences]
---

# Now Assist Guardian analytics

Monitor the performance of guardrails enabled through Now Assist Guardian.

The Now Assist Guardian analytics dashboard helps admins monitor and evaluate the effectiveness of offensive content and prompt injection guardrails in tracking and analyzing requests sent to large language models \(LLM\) and their responses.

\[Omitted image "naa-nag-offensive-content.png"\] Alt text: Prompt injection dashboard page

The indicators on the Now Assist Guardian dashboard page provide the following insights.

-   Average latency as a result of active offensive content and prompt injection guardrails. High latency could mean increased guardrail activity in the period.
-   Count and percentage of offensive content and prompt injection occurrences.
-   Skills where offensive content and prompt injection occurrences were detected.

Apply the filters on the dashboard to view guardrail activity for skills in a date range. See [Now Assist Analytics dashboard indicator details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/now-assist-analytics-dashboard-indicators.md) for information on the data and calculations behind each indicator.

## Offensive content indicators

-   **Guardrail-added latency**

    This area of the dashboard shows the average latency as a result of the active offensive content guardrail for the selected skills and date range.

    \[Omitted image "naa-nag-guardrail-latency-offensive-content.png"\] Alt text: Guardrail latency for prompt injection.

-   **Percentage flagged as offensive**

    This area of the dashboard shows the percentage of requests and responses to and from the LLM service that are flagged for offensive content.

    \[Omitted image "naa-nag-percentage-offensive-content.png"\] Alt text: Percentage of offensive content occurrences.

-   **Total offensive content occurrences**

    This area of the dashboard shows the total number of offensive content occurrences for the selected skills and date range.

    \[Omitted image "naa-nag-total-offensive-content.png"\] Alt text: Total offensive content occurrences.

-   **Categories of offensive content**

    This area of the dashboard shows a breakdown of offensive content occurrences by the categories. If content is deemed to be offensive under more than one category, for example, toxic and defamatory, the occurrence is counted individually toward both the categories. For more information on offensive content categories, see [Now Assist Guardian](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/servicenow-ai-platform-security/now-assist-guardian.md).

    \[Omitted image "naa-nag-categories-offensive-content.png"\] Alt text: Categories of offensive content indicator.

-   **Offensive content occurrences by skill**

    This area of the dashboard shows the number of offensive content occurrences over time by the skills in which the content is detected.

    \[Omitted image "naa-nag-offensive-content-occurrences-by-skill.png"\] Alt text: Offensive content occurrences by skill.


## Prompt injection indicators

-   **Guardrail-added latency**

    This area of the dashboard shows the average latency as a result of the active prompt injection guardrail for the selected skills and date range.

    \[Omitted image "naa-nag-guardrail-latency-prompt-injection.png"\] Alt text: Guardrail-added latency indicator.

-   **Percentage flagged as prompt injection**

    This area of the dashboard shows the percentage of requests and responses to and from the LLM service that are flagged for offensive content.

    \[Omitted image "naa-nag-percentage-prompt-injection.png"\] Alt text: Percentage flagged as prompt injection indicator.

-   **Total prompt injection occurrences**

    This area of the dashboard shows the total number of offensive content occurrences for the selected skills and date range.

    \[Omitted image "naa-nag-total-prompt-injection.png"\] Alt text: Total prompt injection occurrences

-   **Prompt injection occurrences by skill**

    This area of the dashboard shows the number of prompt injection occurrences over time by the skills where prompt injection attempts were detected.

    \[Omitted image "naa-nag-prompt-injection-by-skill.png"\] Alt text: Prompt injection occurrences by skill indicator.


**Parent Topic:**[Using Now Assist Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/using-now-assist-analytics.md)

