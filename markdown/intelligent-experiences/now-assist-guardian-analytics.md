---
title: Now Assist Guardian analytics
description: Monitor the performance of guardrails enabled through Now Assist Guardian.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-02-07"
reading_time_minutes: 2
breadcrumb: [Using Now Assist Analytics, Analyzing Now Assist performance, Now Assist, Enable AI experiences]
---

# Now Assist Guardian analytics

Monitor the performance of guardrails enabled through Now Assist Guardian.

The Now Assist Guardian analytics dashboard helps admins monitor and evaluate the effectiveness of offensive content and prompt injection guardrails in tracking and analyzing requests sent to large language models \(LLM\) and their responses.

![Prompt injection dashboard page](../image/naa-nag-offensive-content.png "Now Assist Guardian dashboard page")

The indicators on the Now Assist Guardian dashboard page provide the following insights.

-   Average latency as a result of active offensive content and prompt injection guardrails. High latency could mean increased guardrail activity in the period.
-   Count and percentage of offensive content and prompt injection occurrences.
-   Skills where offensive content and prompt injection occurrences were detected.

Apply the filters on the dashboard to view guardrail activity for skills in a date range. See [Now Assist Analytics dashboard indicator details](now-assist-analytics-dashboard-indicators.md) for information on the data and calculations behind each indicator.

## Offensive content indicators

-   **Guardrail-added latency**

    This area of the dashboard shows the average latency as a result of the active offensive content guardrail for the selected skills and date range.

    ![Guardrail latency for prompt injection.](../image/naa-nag-guardrail-latency-offensive-content.png "Guardrail-added latency indicator")

-   **Percentage flagged as offensive**

    This area of the dashboard shows the percentage of requests and responses to and from the LLM service that are flagged for offensive content.

    ![Percentage of offensive content occurrences.](../image/naa-nag-percentage-offensive-content.png "Percentage flagged as offensive indicator")

-   **Total offensive content occurrences**

    This area of the dashboard shows the total number of offensive content occurrences for the selected skills and date range.

    ![Total offensive content occurrences.](../image/naa-nag-total-offensive-content.png "Total offensive content occurrences indicator")

-   **Categories of offensive content**

    This area of the dashboard shows a breakdown of offensive content occurrences by the categories. If content is deemed to be offensive under more than one category, for example, toxic and defamatory, the occurrence is counted individually toward both the categories. For more information on offensive content categories, see [Now Assist Guardian](../../now-assist-platform/concept/now-assist-guardian.md#).

    ![Categories of offensive content indicator.](../image/naa-nag-categories-offensive-content.png "Categories of offensive content indicator")

-   **Offensive content occurrences by skill**

    This area of the dashboard shows the number of offensive content occurrences over time by the skills in which the content is detected.

    ![Offensive content occurrences by skill.](../image/naa-nag-offensive-content-occurrences-by-skill.png "Offensive content occurrences by skill indicator")


## Prompt injection indicators

-   **Guardrail-added latency**

    This area of the dashboard shows the average latency as a result of the active prompt injection guardrail for the selected skills and date range.

    ![Guardrail-added latency indicator.](../image/naa-nag-guardrail-latency-prompt-injection.png "Guardrail-added latency indicator")

-   **Percentage flagged as prompt injection**

    This area of the dashboard shows the percentage of requests and responses to and from the LLM service that are flagged for offensive content.

    ![Percentage flagged as prompt injection indicator.](../image/naa-nag-percentage-prompt-injection.png "Percentage flagged as prompt injection indicator")

-   **Total prompt injection occurrences**

    This area of the dashboard shows the total number of offensive content occurrences for the selected skills and date range.

    ![Total prompt injection occurrences](../image/naa-nag-total-prompt-injection.png "Total prompt injection occurrences indicator")

-   **Prompt injection occurrences by skill**

    This area of the dashboard shows the number of prompt injection occurrences over time by the skills where prompt injection attempts were detected.

    ![Prompt injection occurrences by skill indicator.](../image/naa-nag-prompt-injection-by-skill.png "Prompt injection occurrences by skill indicator")


**Parent Topic:**[Using Now Assist Analytics](using-now-assist-analytics.md)

