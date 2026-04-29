---
title: ITSM Virtual Agent chat analytics
description: Track all closed chats, ITSM Virtual Agent chat resolutions, and the chat resolution rate to measure overall demand and ITSM Virtual Agent effectiveness.
locale: en-US
release: australia
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [Now Assist, Agentic AI, generative AI, Gen AI]
breadcrumb: [Use ITSM Virtual Agent analytics dashboard, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# ITSM Virtual Agent chat analytics

Track all closed chats, ITSM Virtual Agent chat resolutions, and the chat resolution rate to measure overall demand and ITSM Virtual Agent effectiveness.

Using the Chat analytics tab you can monitor the ITSM Virtual Agent chat metrics. It provides comprehensive metrics on chat volume, resolution effectiveness, escalation patterns, user engagement, and channel distribution. These insights help evaluate automation success and identify opportunities to improve Virtual Agent capabilities.

## Track metrics for the Chat analytics - Overview

Analyze chat metrics when you use ITSM Virtual Agent or a live agent to chat with users.

|Example of chat metrics|Description|
|-----------------------|-----------|
|Monitor the Virtual Agent chat resolution rate|Track automation effectiveness and identify improvement opportunities. This metric is measured as a percentage of chats closed by ITSM Virtual Agents.|
|Segment performance analysis on different dimensions|Analyze data for the desired date range based on the caller company, user's department, user's location, whether it was handled by a live or virtual agent, and the type of communication channels.|
|Analyze engagement patterns in time-series charts|Identify peak usage periods and plan staffing or infrastructure capacity accordingly.|
|Compare daily chat volume to unique user counts|Understand if high volumes represent many users with issues or repeated interactions from fewer users.|
|Review the chats by state distribution|Assess conversation chat completion quality based on the state of the chat such as Closed Complete and identify potential user experience issues such a users abandoning a chat.|
|View departmental and geographical distribution|Ensure that the ITSM Virtual Agent capabilities align with actual demand patterns across your organization.|
|Track trends over time|Measure the impact of Virtual Agent enhancements, topic additions, or process improvements over a given time period.|
|Select specific data points in the visualizations|Drill down to underlying conversation details for deeper analysis.|

## Conditional filters to view the Chat analytics

**Note:**

-   To analyze for a given date range, in the Date dropdown, select the start and end date for which you'd like to analyze the chat data and select **Apply**.
-   To filter using the other options, double-click one or more desired items in a given category to move it from the Available list to the Applied list and select **Apply**.

    You can analyze based on Caller company, User's department, User's location, Handled by, and Channels filter options. A user's location could be a business address or a personal address based on the implementation. When the location is a user's personal address, then the analysis based on location may not provide valuable insights as compared to using the user's business address as the location.


## Chat analytics—Usage and success metrics

![Chat analytics—Usage and success metrics](../image/now-assist-itsm-va-analytics-chatanalytics.png)

|Indicators|Descriptions|
|----------|------------|
|All chats closed|The total number of customer chats that were closed within the selected date range. This metric represents overall demand for support across all channels such as Teams or Web chats and agent types. The trend line helps identify patterns in support volume, such as seasonal variations or the impact of product releases. Use this data to understand total workload and plan resource allocation.|
|All chats closed by the ITSM Virtual Agent|The total number of customer chats that were successfully resolved by the ITSM Virtual Agent. These are conversations that reached completion without requiring escalation to a live agent. This metric is crucial for measuring automation success and the business value delivered by ITSM Virtual Agent. Higher numbers indicate effective self-service capabilities that reduce live agent workload.|
|Percent of chats closed by ITSM Virtual Agent|The percentage of all closed chats that were resolved by the ITSM Virtual Agent, indicating its efficacy. This is the resolution rate—a key performance indicator for automation success. A higher percentage indicates that the ITSM Virtual Agent is handling more queries independently, reducing the burden on live agents.|

## Chat analytics—Transfer to live agent

![Chat analytics—Transfer to live agent](../image/now-assist-itsm-va-analytics-liveagent.png)

<table id="table_s4b_xvz_23c"><thead><tr><th>

Indicators

</th><th>

Descriptions

</th></tr></thead><tbody><tr><td>

All chats closed by a live agent

</td><td>

The total number of customer chats that were escalated to a live agent, helping identify gaps in automation. These represent cases where ITSM Virtual Agent could not resolve the issue independently. For example, analyzing these escalations could helps identify:

-   Topics requiring additional automation
-   Complex scenarios needing better handling logic
-   Appropriate escalation patterns for sensitive issues

</td></tr><tr><td>

Percent of chats closed by a live agent

</td><td>

The percentage of all closed chats that were escalated to a live agent. This is the inverse of the ITSM Virtual Agent resolution rate and indicates the proportion of cases requiring human intervention. Monitor this metric to understand escalation patterns and identify opportunities to expand ITSM Virtual Agent capabilities.

</td></tr></tbody>
</table>## Chat analytics—Engagement over time

![Chat analytics—Engagement over time](../image/now-assist-itsm-va-analytics-engage-time.png)

<table id="table_qf3_jzg_f3c"><thead><tr><th>

Indicators

</th><th>

Descriptions

</th></tr></thead><tbody><tr><td>

Number of chats over time - Daily count

</td><td>

The number of users engaged in chat interactions per day over time. This time-series visualization shows daily chat volume patterns, helping identify peak usage times, day-of-week trends, seasonal variations, and the impact of external events. As an example, you can use this to plan staffing levels and understand when users most need support.

</td></tr><tr><td>

Number of unique users over time - Daily count

</td><td>

The number of unique users engaged in chat interactions per day. This metric differs from total chat count by showing distinct users rather than total conversations. Comparing unique users to total chats reveals whether issues are affecting many users as shown by the high unique count metric or if some users are having repeated interactions as shown by the high chat-to-user ratio metric.

</td></tr></tbody>
</table>## Chat analytics—Chat distribution

![Chat analytics—Chat distribution](../image/now-assist-itsm-va-analytics-chatdistro.png)

<table id="table_isj_bb1_f3c"><thead><tr><th>

Indicators

</th><th>

Descriptions

</th></tr></thead><tbody><tr><td>

Chats by state

</td><td>

The distribution of closed chat interactions based on the final status of the interactions. For example, Closed Complete indicates that it was successfully resolved and Closed Abandoned indicates that the user left before resolution. This breakdown helps assess conversation completion quality. For example, a high Closed Complete percentage could indicate that ITSM Virtual Agent is highly effective, while high Closed Abandoned rates may suggest issues with conversation length, complexity, or user experience.

</td></tr><tr><td>

Chats by department

</td><td>

The distribution of chat interactions categorized by the department that interacted with the user. This horizontal bar chart shows which departments are handling the most support conversations. For example, you can use this to:

-   Understand departmental support loads.
-   Identify departments that could benefit from enhanced ITSM Virtual Agent capabilities.
-   Ensure that the resources are aligned with actual demand patterns.

</td></tr><tr><td>

Chats by user's location

</td><td>

The distribution of chat interactions based on the geographical location of the users initiating them. This visualization shows support demand by location, which could be valuable for understanding global support patterns, planning regional coverage and language support, identifying location-specific issues, and ensuring that the ITSM Virtual Agent content addresses regional needs.

</td></tr></tbody>
</table>**Parent Topic:**[Use ITSM Virtual Agent Analytics dashboard](using-itsm-conversational-analytics-dashboard.md)

