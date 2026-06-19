---
title: Custom skill details
description: Use the Custom skill details dashboard page to view usage and performance indicators of custom skills.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/enable-ai-experiences/custom-skill-details.html
release: zurich
product: Enable AI Experiences
classification: enable-ai-experiences
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
keywords: [Now Assist, Analytics, skills details, dashboard, generative AI, Gen AI, sn\_na\_analytics\_viewer]
breadcrumb: [Using Now Assist Analytics, Analyzing Now Assist performance, Exploring Now Assist Admin, Now Assist, Enable AI experiences]
---

# Custom skill details

Use the Custom skill details dashboard page to view usage and performance indicators of custom skills.

The Custom skill details dashboard page contains indicators pertaining to a custom skill. The indicators provide insight into skill usage and performance. Select a skill from the Skills drop-down list to view the indicators. The drop-down lists both active and inactive skills. Each skill has a subtitle that identifies the skill family that it belongs to, for example, ITSM, HR, and so on. Use the date range filter to view skill usage and performance over a certain period. The date range filter selection applies to all visualizations on the page. See [Now Assist Analytics dashboard indicator details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/now-assist-analytics-dashboard-indicators.md) for information on the data and calculations behind each indicator.

\[Omitted image "naa-custom-skill-details.png"\] Alt text: Custom skill details dashboard page.

The indicators on the Custom skill details dashboard page provide the following insights. See [Now Assist Analytics dashboard indicator details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/now-assist-analytics-dashboard-indicators.md) for information on the data and calculations behind each indicator.

-   Skill engagement trend visualizations for a selected period can reveal patterns in skill usage across workflows, products, and features.
-   The daily unique users visualization shows a breakdown of daily unique users by the selected skill to help you see user activity and engagement with the skill.
-   Acceptance rate visualization shows how well the skill met the requirements of users who used the skill. A high acceptance rate for a skill is an indicator of good performance. A low acceptance rate among skill users indicates that the skill doesn’t meet the requirements either fully or partially.
-   Skills feedback visualization shows that the feedback recorded based on user response to each skill execution in the selected date range.

## Skill details indicators

The Custom skill details page contains a common set of indicators that give you insights into custom skills. Only those skills where the skill family is Other or the category is Custom are shown in the skills filter on the page.

The following indicators are common across all custom skills.

-   **Number of custom skills created**

    This area of the dashboard shows the number of custom skills created by the users in the selected date range.

    \[Omitted image "naa-number-of-custom-skill-created.png"\] Alt text: Number of custom skills created indicator.

-   **Number of custom skills activated**

    This area of the dashboard shows the number of custom skills activated by the users in the selected date range.

    \[Omitted image "naa-number-of-custom-skill-activated.png"\] Alt text: Number of custom skills activated indicator.

-   **Number of prompts in active custom skills**

    This area of the dashboard shows the number of prompts in active custom skills in the selected date range.

    \[Omitted image "naa-number-of-prompts-active-custom-skills.png"\] Alt text: Number of prompts in active custom skills indicator.

-   **Number of Assists consumed by custom skills**

    This area of the dashboard shows the number of Assists consumed by custom skills in the selected date range.

    \[Omitted image "naa-number-of-assists-consumed-custom-skills.png"\] Alt text: Number of Assists consumed by custom skills indicator.

-   **Count of invocations**

    This area of the dashboard shows the count of invocations for the custom skills in the selected date range.

    \[Omitted image "naa-number-of-count-invocations.png"\] Alt text: Count of invocations indicator.

-   **Daily unique users engaging with the skill**

    This area of the dashboard shows the number of unique users per day who engaged with the skill in the selected date range. The bar chart shows a trend of increase or decrease in the number of unique users to help you understand periods of high and low skill engagement.

    \[Omitted image "naa-daily-custom-skill-unique-users.png"\] Alt text: Daily unique users engaging with the skill indicator.

-   **Skill engagement trend by workflows**

    This area of the dashboard shows the skill usage across workflows in a bar chart for the selected date range. The visualization is interactive. Hover over the bars to see the number of times the skill was used in each of the workflows.

    \[Omitted image "naa-skill-engagement-trend-by-workflows.png"\] Alt text: Skill engagement trend by workflows indicator.

-   **Skill engagement trend by products**

    This area of the dashboard shows the skill usage across Now Assist products in a bar chart for the selected date range. The visualization is interactive. Hover over the bars to see the number of times the skill was used in each of the products.

    \[Omitted image "naa-skill-engagement-trend-by-products.png"\] Alt text: Skill engagement trend by products.

-   **Skill engagement trend by features**

    This area of the dashboard shows the skill usage across Now Assist features in a bar chart for the selected date range. The visualization is interactive. Hover over the bars to see the number of times the skill was used in each of the features.

    \[Omitted image "naa-skill-engagement-trend-by-features.png"\] Alt text: Skill engagement trend by features indicator.

-   **Executed successfully**

    This area of the dashboard shows the acceptance rate of the selected skill based on user feedback. The percentage is calculated using the formula: \(Total number of accepted skill executions/Total number of skill executions\) x 100.

    \[Omitted image "naa-executed-successfully.png"\] Alt text: Executed successfully indicator.

-   **Skills feedback**

    This area of the dashboard shows the feedback recorded for each execution of the selected skill. User feedback is categorized into the following:

    -   Accepted \(edited &amp; non-edited\): The user accepted the skill output with or without further edits to the output.
    -   Rejected: The user rejected the skill output.
    -   Canceled: The user canceled the skill execution.
    -   Ignored: The user didn't take any action based on the skill output.
    \[Omitted image "naa-skills-feedback.png"\] Alt text: Skills feedback indicator.


**Parent Topic:**[Using Now Assist Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/using-now-assist-analytics.md)

