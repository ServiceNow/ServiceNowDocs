---
title: Skill details
description: Use the Skill details page to view usage and performance indicators of a skill.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-10-17"
reading_time_minutes: 3
breadcrumb: [Skills performance, Using Now Assist Analytics, Analyzing Now Assist performance, Now Assist, Enable AI experiences]
---

# Skill details

Use the Skill details page to view usage and performance indicators of a skill.

The Skill details dashboard page contains indicators pertaining to a specific skill. The indicators provide insight into skill usage and performance. Select a skill from the drop-down to view the indicators. The drop-down lists both active and inactive skills. Each skill has a subtitle that identifies the skill family it belongs to, for example, ITSM, HR, and so on. Use the date range filter to view skill usage and performance over a certain period. The date range filter selection applies to all visualizations on the page.

![Flow generation skill details dashboard](../image/naa-flow-generation-skill-details-dashboard.png)

The indicators on the Skill details dashboard page provide the following insights.

-   Skill usage trend visualization for a selected period can reveal patterns in skill usage
-   Acceptance rate visualization shows how well the skill met the requirements of users who used the skill. A high acceptance rate for a skill is an indicator of good performance. A low acceptance rate among skill users indicates that the skill doesn’t meet the requirements either fully or partially.
-   The number of actions visualization for a selected period can reveal the scale of the skill executions. The trend line comparison shows the increasing or decreasing trend from the previous period.
-   The daily active users visualizations show a breakdown of daily active users by skill to help you see user activity on the skill.

## Skill details indicators

The indicators on skill details pages might differ based on the skill selected. For example, summarization skills might have different set of indicators compared to generation skills. This is because each skill is mapped to its own dashboard that contains a set of indicators related to the skill.

Now Assist Analytics dashboard comes with some default skill-to-dashboard mappings to get you started. The default dashboards are visible to users with Now Assist Analytics Viewer \[sn\_na\_analytics.viewer\] role. You can create your own dashboards and map them to skills. See [Create a dashboard with the in-line editor](https://www.servicenow.com/docs/access?context=create-db-in-ac&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US) and [Map a skill to a dashboard](map-a-skill-to-a-dashboard.md) for more information on creating custom dashboards and mapping them to skills respectively.

The following indicators are for the Flow Generation skill.

-   **Skill usage trend indicator**

    This area of the dashboard shows the Flow Generation skill usage in a trend chart for the selected filters. The visualization is interactive. Hover over the trend lines to see the number of times the Flow Generation skill was used.

    ![Flow generation skill usage trend](../image/naa-flow-generation-skill-usage-trend.png "Skill usage trend indicator")

-   **Total Flow Generation actions indicator**

    This area of the dashboard shows the number of flow generation actions for the selected date range. A single use of the Flow Generation skill represents an action. The headline number is an indicator of the scale of flow generation skill usage across products. The trend line comparison shows the increase or decrease in number of actions from the previous period.

    ![Total flow generation actions indicator](../image/naa-total-flow-generation-actions.png "Total flow generation actions indicator")

-   **Accepted flow generation actions indicator**

    This area of the dashboard shows the number of flow generation actions, that is, the number of flow generation skill executions that resulted in flows which were accepted by the users.

    ![Number of accepted flow generation actions indicator](../image/naa-accepted-flow-generation-actions.png "Accepted flow generation actions indicator")

-   **Acceptance rate indicator**

    This area of the dashboard shows the acceptance rate of Flow Generation skill based on user acceptance of the flow. The percentage is calculated using the formula: \(Total number of accepted flow generation actions/Total number of flow generation actions\) x 100.

    ![Acceptance rate indicator](../image/naa-flow-generation-acceptance-rate.png "Acceptance rate indicator")


**Parent Topic:**[Skills performance](skill-usage.md)

