---
title: AI Agent Analytics dashboard
description: Track the AI agent use and efficiency gain on your instance through the AI Agent Analytics dashboard. The dashboard can reveal trends in how AI agents are used to improve the time to resolution and the number of tasks closed.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 14
breadcrumb: [Now Assist AI agents reference, Now Assist AI agents, Enable AI experiences]
---

# AI Agent Analytics dashboard

Track the AI agent use and efficiency gain on your instance through the AI Agent Analytics dashboard. The dashboard can reveal trends in how AI agents are used to improve the time to resolution and the number of tasks closed.



## Required ServiceNow AI Platform roles

To use the AI Agent Analytics dashboard, you must have either the sn\_aia.viewer or the sn\_aia.admin role.

If you want to change the dashboard, you must duplicate it and apply changes to the copy. You can redirect the Analytics page in AI Agent Studio to the new dashboard by replacing the dashboard sys\_id in the system property **sn\_aia.analytics\_dashboard\_sysid**.

## Accessing the AI Agent Analytics dashboard

To open the dashboard, navigate to **All** &gt; **AI Agent Studio** &gt; **Analytics**.

You can also access the dashboard from the AI Agent Studio overview page. Go to the Recent agentic workflows and AI agents activity section and select the **View analytics** link.

## Indicators

Most indicators are updated daily. The latency indicators are updated every 15 minutes.

Once you have installed Now Assist AI Agents, you can collect initial data by running the \[Now Assist AI Agents\] Historical Data Collection job. The other data collection jobs, \[Now Assist AI Agents\] Daily Data Collection and \[Now Assist AI Agents\] Periodic Data Collection, update the indicators.

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Agentic workflow latency

</td><td>

Time taken for an agentic workflow to complete.

</td></tr><tr><td>

AI agent execution plan P90 latency

</td><td>

Time taken for 90% of AI agent execution plans in a system to be processed.

</td></tr><tr><td>

AI agent execution plan P95 latency

</td><td>

Time taken for 95% of AI agent executions plans in a system to be processed.

</td></tr><tr><td>

AI agent execution plan P99 latency

</td><td>

Time taken for 99% of AI agent execution plans in a system to be processed.

</td></tr><tr><td>

AI agent latency

</td><td>

Time taken for an AI agent in a system to be processed.

</td></tr><tr><td>

All agentic workflows

</td><td>

Total number of agentic workflows created before today.

</td></tr><tr><td>

All AI agents

</td><td>

Total number of AI agents created before today.

</td></tr><tr><td>

All tools

</td><td>

Total number of tools created before today.

</td></tr><tr><td>

LLM P90 latency

</td><td>

Time taken for 90% of LLM requests in a system to be processed.

</td></tr><tr><td>

LLM P95 latency

</td><td>

Time taken for 95% of LLM requests in a system to be processed.

</td></tr><tr><td>

LLM P99 latency

</td><td>

Time taken for 95% of LLM requests in a system to be processed.

</td></tr><tr><td>

Number of closed tasks

</td><td>

Total number of tasks closed.

</td></tr><tr><td>

Number of closed tasks with AI agent assist

</td><td>

Total number of tasks closed today that were closed with agentic workflows or AI agents.

</td></tr><tr><td>

Summed duration of closed tasks

</td><td>

Total time taken to close tasks.

</td></tr><tr><td>

Summed duration of closed tasks with AI agent assist

</td><td>

Total time taken to close tasks today that were closed with agentic workflows or AI agents.

</td></tr><tr><td>

Tool execution P90 latency

</td><td>

Time taken for 90% of tool executions in a system to be processed.

</td></tr><tr><td>

Tool execution P95 latency

</td><td>

Time taken for 95% of tool executions in a system to be processed.

</td></tr><tr><td>

Tool execution P99 latency

</td><td>

Time taken for 99% of tool executions in a system to be processed.

</td></tr><tr><td>

Tool latency

</td><td>

Time taken for a tool in a system to be processed.

</td></tr><tr><td>

Total number of CS conversations

</td><td>

Total number of conversations in Now Assist panel or Virtual Agent.

</td></tr><tr><td>

Total number of execution plans

</td><td>

Total number of execution plans created by agentic workflows and AI agents today.

</td></tr><tr><td>

Total number of execution tasks

</td><td>

Total number of tasks executed by agentic workflows and AI agents today.

</td></tr><tr><td>

Total number of tool executions

</td><td>

Total number of tool executions in agentic workflows and AI agents today.

</td></tr><tr><td>

Use case execution plan P90 latency

</td><td>

Time taken for 90% of agentic workflows in a system to be processed.

</td></tr><tr><td>

Use case execution plan P95 latency

</td><td>

Time taken for 95% of agentic workflows in a system to be processed.

</td></tr><tr><td>

Use case execution plan P99 latency

</td><td>

Time taken for 99% of agentic workflows in a system to be processed.

</td></tr></tbody>
</table><table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

% of conversations with an AI agent or agentic workflow defined

</td><td>

Number of conversations in Now Assist panel or Virtual Agent with a defined AI agentic or agentic workflow divided by the total number of conversations.

</td></tr><tr><td>

Average time to close a task

</td><td>

Average time taken for a task to go from creation to closure.

</td></tr><tr><td>

Average time to close a task with AI agent assist

</td><td>

Average time taken for a task to go from creation to closure with an agentic workflow or AI agent involved.

</td></tr><tr><td>

Efficiency gain

</td><td>

Percentage efficiency gain comparing average time taken to close a task with AI agent assist against a task closed without AI agent assist.

</td></tr><tr><td>

Percentage of tasks closed using AI agents

</td><td>

Number of tasks closed using AI agents and agentic workflows divided by the total number of tasks.

</td></tr></tbody>
</table>## Breakdowns

Different breakdowns enable you to divide the data differently to track specific aspects of the AI agent usage. Not all breakdowns are available for all indicators.

-   Agentic workflow
-   AI agent
-   AI agent execution status
-   Latency metric
-   Tool
-   Tool latency metric

## Filters

You can filter data to review a subset of trends. The following table lists the available filters on the AI Agent Analytics dashboard.

<table id="table_hgz_ync_j2c"><thead><tr><th>

Page

</th><th>

Available filters

</th></tr></thead><tbody><tr><td>

Activity

</td><td>

Time created

</td></tr><tr><td>

Performance

</td><td>

-   Time created
-   Agentic workflow
-   AI agent
-   Tool

</td></tr><tr><td>

Troubleshooting

</td><td>

Time created

</td></tr></tbody>
</table>## Data visualizations

Visualizations are graphic elements that can be used to see data trends, percentages, and scores. The AI Agent Analytics dashboard includes the following visualizations.

<table><thead><tr><th>

Title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AI agent tool type

</td><td>

Pie chart

</td><td>

Tools divided by type. Example: Script, Flow action, Subflow, and so on.

</td></tr><tr><td>

AI agent tool execution mode

</td><td>

Pie chart

</td><td>

Tools divided by either autonomous or supervised execution mode.

</td></tr><tr><td>

Execution plans in last 7 days

</td><td>

Pie chart

</td><td>

Execution plans divided by status \(Completed, Terminated, Wrap Up, or In Progress\)

</td></tr><tr><td>

AI agent executions

</td><td>

List

</td><td>

List of AI agent executions. The list is broken down by AI agent and AI agent execution status. Columns span for multiple weeks, and there are change percentages and trend lines comparing the current against the previous week.

</td></tr><tr><td>

Execution tasks in last 7 days

</td><td>

Pie chart

</td><td>

Execution tasks divided by status \(Success, Ongoing, Cancelled, Queued\).

</td></tr><tr><td>

Number of agentic workflows

</td><td>

Trend line

</td><td>

Total number of agentic workflows. The agentic workflows created in the last day and a trend line are shown.

</td></tr><tr><td>

Number of AI agents

</td><td>

Trend line

</td><td>

Total number of AI agents. The AI agents created in the last day and a trend line are shown.

</td></tr><tr><td>

Number of tools

</td><td>

Trend line

</td><td>

Total number of tools. The tools created in the last day and a trend line are shown.

</td></tr><tr><td>

AI agent execution plans

</td><td>

List

</td><td>

List of AI agent execution plans. The list is broken down by agentic workflow. Columns span for multiple weeks, and there are change percentages and trend lines comparing the current against the previous week.

</td></tr></tbody>
</table><table><thead><tr><th>

Title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AI agent execution plans

</td><td>

Score cards

</td><td>

Four score cards, one for each execution plan status \(Ready, In progress right now, Completed, and Terminated\).

</td></tr><tr><td>

AI agent executions

</td><td>

Score cards

</td><td>

Four score cards, one for each execution plan status \(In progress right now, Completed, Successful, and Errors/Cancelled\).

</td></tr><tr><td>

AI agent/tool executions

</td><td>

List

</td><td>

List of AI agent and tool executions. The list is broken down by AI agent and tool, and there are columns for each status \(Cancelled, Ongoing, Queued, and Success\).

</td></tr></tbody>
</table><table><thead><tr><th>

Title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Tasks closed using AI agents

</td><td>

Trend line

</td><td>

Percentage of tasks closed using AI agents. Trend line is shown.

</td></tr><tr><td>

Efficiency gain using AI agents

</td><td>

Trend line

</td><td>

Percentage efficiency gained with agentic workflows and AI agents. Trend line is shown.

</td></tr><tr><td>

Average close time assisted by AI agents

</td><td>

Trend line

</td><td>

Average time taken for a task to go from creation to closure with the involvement of an AI agent or agentic workflow. Trend line is shown.

</td></tr><tr><td>

Efficiency gain supporting indicators

</td><td>

List

</td><td>

List of indicators. The list is broken down by indicator. Columns span across a time span.

</td></tr><tr><td>

AI agent conversations daily

</td><td>

Trend line

</td><td>

Total number of AI agent conversations in Now Assist panel or Virtual Agent. Trend line is shown.

</td></tr><tr><td>

% of conversations using AI agents

</td><td>

Trend line

</td><td>

Percentage of AI agent conversations in Now Assist panel or Virtual Agent that used agentic workflows or AI agents. Trend line is shown.

</td></tr></tbody>
</table><table><thead><tr><th>

Title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

P90 agentic workflow latency

</td><td>

Score card

</td><td>

Time in seconds of 90% of agentic workflows in a system to be processed.

</td></tr><tr><td>

P95 agentic workflow latency

</td><td>

Score card

</td><td>

Time in seconds of 95% of agentic workflows in a system to be processed.

</td></tr><tr><td>

P99 agentic workflow latency

</td><td>

Score card

</td><td>

Time in seconds of 99% of agentic workflows in a system to be processed.

</td></tr><tr><td>

Total agentic workflows executed per hour

</td><td>

Bar chart

</td><td>

Visualization of what time of day agentic workflows have been executed by hour.

</td></tr><tr><td>

Total agentic workflows errors per hour

</td><td>

Bar chart

</td><td>

Visualization of what time of day agentic workflows have been executed and experienced an error by hour.

</td></tr><tr><td>

Agentic workflow latency

</td><td>

Line chart

</td><td>

Agentic workflow latency over time. Uses three different indicators: P90 tracks the fastest 90% of executions, P95 tracks the fastest 95% of executions, and P99 tracks the fastest 99% of executions.

</td></tr><tr><td>

Agentic workflow latency \(weekly average\)

</td><td>

Line chart

</td><td>

Agentic workflow latency over time. Uses three different indicators: P90 tracks the fastest 90% of executions, P95 tracks the fastest 95% of executions, and P99 tracks the fastest 99% of executions.

</td></tr><tr><td>

Agentic workflow latency \(daily average\)

</td><td>

Table

</td><td>

Average agentic workflow latency today. Each row is an agentic workflow and each column is a different latency metric. Uses three different indicators: P90 tracks the fastest 90% of executions, P95 tracks the fastest 95% of executions, and P99 tracks the fastest 99% of executions.

</td></tr><tr><td>

P90 AI agent latency

</td><td>

Score card

</td><td>

Time in seconds of 90% of AI agent executions in a system to be processed.

</td></tr><tr><td>

P95 AI agent latency

</td><td>

Score card

</td><td>

Time in seconds of 95% of AI agent executions in a system to be processed.

</td></tr><tr><td>

P99 AI agent latency

</td><td>

Score card

</td><td>

Time in seconds of 99% of AI agent executions in a system to be processed.

</td></tr><tr><td>

Total AI agents executed per hour

</td><td>

Bar chart

</td><td>

Visualization of what time of day AI agent executions have been executed by hour.

</td></tr><tr><td>

Total AI agent errors per hour

</td><td>

Bar chart

</td><td>

Visualization of what time of day AI agent executions have been executed and experienced an error by hour.

</td></tr><tr><td>

AI agent latency

</td><td>

Line chart

</td><td>

AI agent latency within the time filter. Uses three different indicators: P90 tracks the fastest 90% of executions, P95 tracks the fastest 95% of executions, and P99 tracks the fastest 99% of executions.

</td></tr><tr><td>

AI agent latency \(weekly average\)

</td><td>

Line chart

</td><td>

AI agent latency over time by week. Uses three different indicators: P90 tracks the fastest 90% of executions, P95 tracks the fastest 95% of executions, and P99 tracks the fastest 99% of executions.

</td></tr><tr><td>

AI agent latency \(daily average\)

</td><td>

Table

</td><td>

Average AI agent latency today. Each row is an AI agent and each column is a different latency metric. Uses three different indicators: P90 tracks the fastest 90% of executions, P95 tracks the fastest 95% of executions, and P99 tracks the fastest 99% of executions.

</td></tr><tr><td>

P90 tool latency

</td><td>

Score card

</td><td>

Time in seconds of 90% of tool executions in a system to be processed.

</td></tr><tr><td>

P95 tool latency

</td><td>

Score card

</td><td>

Time in seconds of 95% of tool executions in a system to be processed.

</td></tr><tr><td>

P99 tool latency

</td><td>

Score card

</td><td>

Time in seconds of 99% of tool executions in a system to be processed.

</td></tr><tr><td>

Total tools executed per hour

</td><td>

Bar chart

</td><td>

Visualization of what time of day tool executions have been executed by hour.

</td></tr><tr><td>

Total tool errors per hour

</td><td>

Bar chart

</td><td>

Visualization of what time of day tool executions have been executed and experienced an error by hour.

</td></tr><tr><td>

Tool latency

</td><td>

Line chart

</td><td>

Tool latency within the time filter. Uses three different indicators: P90 tracks the fastest 90% of executions, P95 tracks the fastest 95% of executions, and P99 tracks the fastest 99% of executions.

</td></tr><tr><td>

Tool latency \(weekly average\)

</td><td>

Line chart

</td><td>

Tool latency over time by week. Uses three different indicators: P90 tracks the fastest 90% of executions, P95 tracks the fastest 95% of executions, and P99 tracks the fastest 99% of executions.

</td></tr><tr><td>

Tool latency \(daily average\)

</td><td>

Table

</td><td>

Average tool latency today. Each row is a tool and each column is a different latency metric. Uses three different indicators: P90 tracks the fastest 90% of executions, P95 tracks the fastest 95% of executions, and P99 tracks the fastest 99% of executions.

</td></tr><tr><td>

P90 LLM latency

</td><td>

Score card

</td><td>

Time in seconds of 90% of LLM requests in a system to be processed.

</td></tr><tr><td>

P95 LLM latency

</td><td>

Score card

</td><td>

Time in seconds of 95% of LLM requests in a system to be processed.

</td></tr><tr><td>

P99 LLM latency

</td><td>

Score card

</td><td>

Time in seconds of 99% of LLM requests in a system to be processed.

</td></tr><tr><td>

LLM latency

</td><td>

Line chart

</td><td>

Tool latency within the time filter. Uses three different indicators: P90 tracks the fastest 90% of executions, P95 tracks the fastest 95% of executions, and P99 tracks the fastest 99% of executions.

</td></tr><tr><td>

LLM latency \(weekly average\)

</td><td>

Line chart

</td><td>

Tool latency over time by week. Uses three different indicators: P90 tracks the fastest 90% of executions, P95 tracks the fastest 95% of executions, and P99 tracks the fastest 99% of executions.

</td></tr><tr><td>

LLM calls per hour

</td><td>

Bar chart

</td><td>

Visualization of what time of day LLM calls have been made by hour.

</td></tr><tr><td>

LLM errors per hour

</td><td>

Bar chart

</td><td>

Visualization of what time of day LLM calls have been made and experienced an error by hour.

</td></tr></tbody>
</table><table><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Agentic workflow errors

</td><td>

List

</td><td>

List of agentic workflow errors.

</td></tr><tr><td>

LLM errors

</td><td>

List

</td><td>

List of agentic workflow errors.

</td></tr></tbody>
</table>For more information on security controls for agentic AI, see [Security for AI agents](aia-security-implementation.md).

<table><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Total blocked executions

</td><td>

Score card

</td><td>

Total number of agentic AI executions blocked because of security controls.

</td></tr><tr><td>

Total blocked executions

</td><td>

List

</td><td>

List of executions blocked.

</td></tr><tr><td>

Top agentic workflows with blocked executions

</td><td>

List

</td><td>

List of agentic workflows with the most blocked executions.

</td></tr><tr><td>

Top AI agents with blocked executions

</td><td>

List

</td><td>

List of AI agents with the most blocked executions.

</td></tr><tr><td>

Agentic Workflows w/o ACL defined

</td><td>

Score card

</td><td>

Total number of agentic workflows missing an ACL for user access.

</td></tr><tr><td>

Agentic Workflows ACLs

</td><td>

Pie chart

</td><td>

Pie chart displaying the percentage of agentic workflows with and without ACLs for user access.

</td></tr><tr><td>

Agentic Workflows w/o ACL defined

</td><td>

List

</td><td>

List of agentic workflows missing an ACL for user access.

</td></tr><tr><td>

AI agents with no ACLs defined

</td><td>

Score card

</td><td>

Total number of AI agents missing an ACL for user access.

</td></tr><tr><td>

AI agent ACLs

</td><td>

Pie chart

</td><td>

Pie chart displaying the percentage of AI agents with and without ACLs for user access.

</td></tr><tr><td>

AI agents w/o ACL defined

</td><td>

List

</td><td>

List of AI agents missing an ACL for user access.

</td></tr><tr><td>

Agentic workflows without role masking

</td><td>

Score card

</td><td>

Total number of agentic workflows without roles identified for role masking and data access.

</td></tr><tr><td>

Agentic workflows without role masking

</td><td>

List

</td><td>

List of agentic workflows without roles identified for role masking and data access.

</td></tr><tr><td>

AI agents without role masking

</td><td>

Score card

</td><td>

Total number of AI agents without roles identified for role masking and data access.

</td></tr><tr><td>

AI agents without role masking

</td><td>

List

</td><td>

List of AI agents without roles identified for role masking and data access.

</td></tr><tr><td>

Agentic workflows running as dynamic user

</td><td>

Score card

</td><td>

Total number of agentic workflows running as a dynamic user.

</td></tr><tr><td>

Agentic workflows running as dynamic user

</td><td>

List

</td><td>

List of agentic workflows running as a dynamic user.

</td></tr><tr><td>

AI agents running as dynamic user

</td><td>

Score card

</td><td>

Total number of AI agents running as a dynamic user.

</td></tr><tr><td>

AI agents running as dynamic user

</td><td>

List

</td><td>

List of AI agents running as a dynamic user.

</td></tr><tr><td>

Agentic workflows running as AI user

</td><td>

Score card

</td><td>

Total number of agentic workflows running as an AI user.

</td></tr><tr><td>

Agentic workflows running as AI user

</td><td>

List

</td><td>

List of agentic workflows running as an AI user.

</td></tr><tr><td>

AI agents running as AI user

</td><td>

Score card

</td><td>

Total number of AI agents running as an AI user.

</td></tr><tr><td>

AI agents running as AI user

</td><td>

List

</td><td>

List of AI agents running as an AI user.

</td></tr></tbody>
</table>