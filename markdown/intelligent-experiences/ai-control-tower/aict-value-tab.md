---
title: Value tab in AI Control Tower
description: Use the Value dashboard page to gain insights into the value realized from multiple types of AI systems, view data about user engagement and feedback, and adoption of every type of AI system in your organization.
locale: en-US
release: yokohama
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [AI Control Tower Home, AI Control Tower dashboard, Exploring AI Control Tower, AI Control Tower, Enable AI experiences]
---

# Value tab in AI Control Tower

Use the Value dashboard page to gain insights into the value realized from multiple types of AI systems, view data about user engagement and feedback, and adoption of every type of AI system in your organization.

The Value dashboard page contains visualizations that help you assess the value of your AI systems. Creator skills are included in the Value dashboard page. Value metrics for creator skills are aggregated across non-production and production instances. You need to have the AI steward role to view this dashboard.

![Value tab in AI Control Tower.](../image/value-tab-aict.png "Value tab in AI Control Tower")

The indicators on the dashboard are based on the value templates associated with each AI system. See [Using value templates](using-value-templates.md) for more information.

## Track the overall value

-   **Total productivity gained**

    This area of the dashboard shows the estimated productivity gains \(in hours\) in the selected period as a result of using various AI systems, including third-party AI systems.

    ![Total productivity gained.](../image/aict-value-productivity.png "Total productivity gained")

-   **Average AI users**

    This area of the dashboard shows the average unique users who used a ServiceNow AI system in the selected date range. The chart does not include users of third-party AI systems.

    ![Average AI users.](../image/aict-value-avg-ai-users.png "Average AI users")

-   **Top 5 AI systems by value \(in hrs\)**

    This area of the dashboard shows the top 5 AI systems that delivered the most value to the users in the selected date range. The data includes both ServiceNow and third-party AI systems.

    ![Top 5 AI systems by value in hours.](../image/aict-value-top-5-systems-by-value.png "Top 5 AI systems by value (in hrs)")


## Productivity indicators

-   **Task closure efficiency gain using AI system**

    This area of the dashboard shows the percentage improvement in task completion time using AI systems versus manual tasks in the selected date range. This data includes only ServiceNow AI actions.

    ![Task closure efficiency gain using AI system indicator](../image/aict-value-task-closure-efficiency-ai.png "Task closure efficiency gain using AI system indicator")

-   **Top 10 AI systems consuming assists**

    This area of the dashboard shows the top 10 AI systems with the highest consumption of assists in the selected date range. This data includes only ServiceNow AI actions.

    ![Top 10 AI systems consuming assists indicator.](../image/aict-value-top-10-ai-systems-consuming-assists.png "Top 10 AI systems consuming assists indicator")

-   **AI systems with no usage**

    This area of the dashboard shows the list of deployed AI systems which are not used in the selected date range. The data includes both ServiceNow and third-party AI actions.

    ![AI systems with no usage indicator.](../image/aict-value-ai-systems-no-usage.png "AI systems with no usage indicator")

-   **System summary**

    This area of the dashboard lists all the AI systems along with details of users and productivity gained. The data includes both ServiceNow and third-party AI actions.

    ![AI systems summary indicator.](../image/aict-value-system-summary.png "System summary indicator")


## Engagement indicators

-   **Total AI actions**

    This area of the dashboard shows the total number of LLM related actions across all skills in the selected date range. The data includes both ServiceNow and third-party AI actions.

    ![Total AI actions indicator.](../image/aict-value-total-ai-actions.png "Total AI actions indicator")

-   **Usage by department**

    This area of the dashboard shows the top 5 departments with the highest usage of AI systems in the selected date range. For more detailed analysis of AI systems usage by all the departments, select **See all**. The data includes both ServiceNow and third-party AI actions.

    ![Usage of AI systems by departments indicator.](../image/aict-value-ai-usage-by-department.png "Usage of AI systems by departments indicator")

    **Note:** Usage of AI systems by **Others** indicate the AI actions by users with empty department.

-   **Countries with highest AI adoption**

    This area of the dashboard shows the top 5 countries with the most usage of AI systems in the selected date range. The data includes both ServiceNow and third-party AI actions.

    ![Countries with highest AI adoption indicator.](../image/aict-value-countries-highest-ai-adoption.png "Countries with highest AI adoption indicator")

-   **Countries with lowest AI adoption**

    This area of the dashboard shows the top 5 countries with the least usage of AI systems in the selected date range. The data includes both ServiceNow and third-party AI actions.

    ![Countries with lowest AI adoption indicator.](../image/aict-value-countries-lowest-ai-adoption.png "Countries with lowest AI adoption indicator")

-   **AI actions comparison by user department**

    This area of the dashboard shows the number and type of AI actions executed by up to 5 departments in the selected date range.

    ![AI actions comparison by user department indicator.](../image/aict-value-ai-actions-comparison-department.png "AI actions comparison by user department indicator")


## Quality indicators

-   **Positive feedback**

    This area of the dashboard shows the summary of positive feedback received for all AI executions in the selected date range. This data includes only ServiceNow AI actions.

    ![Positive feedback indicator.](../image/aict-value-quality-positive-feedback.png "Positive feedback indicator")

-   **% of task closed using AI system**

    This area of the dashboard shows the percentage of tasks completed with an associated AI system execution plan. Tasks represent the record in task tables, such as incident, problem, change, case, and request. This data includes only ServiceNow AI actions.

    ![Percentage of tasks closed using AI system indicator.](../image/aict-value-quality-percentage-task-closed.png "% of task closed using AI system indicator")

-   **Success rate**

    This area of the dashboard indicates the percentage of successful AI executions across all AI systems. This data includes only ServiceNow AI actions.

    ![Success rate indicator.](../image/aict-value-quality-success-rate.png "Success rate indicator")

-   **Success rate summary**

    This area of the dashboard lists all the AI systems with successful executions and its details.

    ![Success rate summary indicator.](../image/aict-value-quality-success-rate-summary.png "Success rate summary indicator")


## Creator skills indicators

-   **Highest instance usage**

    This area of the dashboard displays the highest percentage of instance usage. This data includes only ServiceNow AI actions.

    ![Highest instance usage indicator.](../image/aict-value-creator-highest-instance-usage.png "Highest instance usage indicator")

-   **Highest skill usage**

    This area of the dashboard displays the highest percentage of assists usage by one skill. This data includes only ServiceNow AI actions.

    ![Highest skill usage indicator.](../image/aict-value-creator-highest-skill-usage.png "Highest skill usage indicator")

-   **Total creator calls**

    This area of the dashboard displays the total calls for creator skills across the instance. This data includes only ServiceNow AI actions.

    ![Total creator calls indicator.](../image/aict-value-creator-total-creator-calls.png "Total creator calls indicator")

-   **Accepted creator calls**

    This area of the dashboard displays the total accepted creator calls. This data includes only ServiceNow AI actions.

    ![Accepted creator calls indicator.](../image/aict-value-creator-accepted-creator-calls.png "Accepted creator calls indicator")

-   **Skill satisfaction**

    This area of the dashboard displays the skill satisfaction by measuring both usage and approvals. This data includes only ServiceNow AI actions.

    ![Skill satisfaction indicator.](../image/aict-value-creator-skill-satisfaction.png "Skill satisfaction indicator")

-   **Designation with highest creator calls**

    This area of the dashboard displays the designation with the highest usage of creator skill. This data includes only ServiceNow AI actions.

    ![Designation with highest creator calls indicator.](../image/aict-value-creator-desgn-highest-creator-calls.png "Designation with highest creator calls indicator")

-   **Creator calls by skill**

    This area of the dashboard displays the number of creator calls by skills. This data includes only ServiceNow AI actions.

    ![Creator calls by skill indicator.](../image/aict-value-creator-creator-calls-by-skill.png "Creator calls by skill indicator")

-   **Creator calls by instance name**

    This are of the dashboard displays the number of creator calls by instance names. This data includes only ServiceNow AI actions.

    ![Creator calls by instance name indicator.](../image/aict-value-creator-creator-calls-by-instance-name.png "Creator calls by instance name indicator")

-   **Creator calls by code environment**

    This area of the dashboard displays the most used code environment for creator skills. This data includes only ServiceNow AI actions.

    ![Creator calls by code environment indicator.](../image/aict-value-creator-creator-calls-by-code-environment.png "Creator calls by code environment indicator")

-   **Creator call by title/designation**

    This area of the dashboard displays the number of creator calls by designations. This data includes only ServiceNow AI actions.

    ![Creator call by title/designation indicator.](../image/aict-value-creator-creator-calls-by-title.png "Creator call by title/designation indicator")


