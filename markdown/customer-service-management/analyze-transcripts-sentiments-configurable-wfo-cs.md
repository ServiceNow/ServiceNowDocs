---
title: Analyze transcripts and sentiments for the Amazon Connect phone channel
description: Analyze your agent's call recordings, transcripts, and sentiment reports. With this information, you can assess the call quality and train your agents to handle calls better in the future.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/analyze-transcripts-sentiments-configurable-wfo-cs.html
release: australia
product: Customer Service Management
classification: customer-service-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Voice, Using Channel Management, Channel Management, Workforce Optimization for Customer Service, Agent management, Use, Customer Service Management]
---

# Analyze transcripts and sentiments for the Amazon Connect phone channel

Analyze your agent's call recordings, transcripts, and sentiment reports. With this information, you can assess the call quality and train your agents to handle calls better in the future.

## Before you begin

Role required: sn\_cti\_core.user\_manager

## About this task

When an agent interacts with an external caller, the call gets recorded and transcribed. The application tags every statement within a transcript with a sentiment score. After a call has been completed, a sentiment report is automatically generated.

**Note:** The manager must have an active session with Amazon Connect to view the transcripts and sentiments. The transcripts and sentiments are generated in the Amazon Connect application. They are then displayed in the Channels application in Workforce Optimization for Customer Service.

## Procedure

1.  Navigate to **Workspaces** &gt; **Manager Workspace**.

2.  Select an interaction record to analyze transcripts and sentiments.

<table id="choicetable_icf_qv5_1nb"><thead><tr><th align="left" id="d34941e88">

To analyze call transcripts and sentiments

</th><th align="left" id="d34941e91">

Do this

</th></tr></thead><tbody><tr><td id="d34941e97">

**From Channels**

</td><td>

**Note:** You can view call transcripts and sentiments for all interactions that were closed today.

 1.  Click the Channels \(\[Omitted image "channels-new.png"\] Alt text: Channels icon.\) icon.
2.  Click **Amazon Connect \(Phone\)**.
3.  Select an interaction record.


</td></tr><tr><td id="d34941e130">

**From Teams**

</td><td>

1.  Click the Teams icon \(\[Omitted image "teams-new.png"\] Alt text: Teams icon.\).
2.  Select a team.
3.  Select a user.
4.  Select a KPI.
5.  Select an interaction record.


</td></tr><tr><td id="d34941e163">

**From Coaching**

</td><td>

**Note:** When you have assessments triggered from calls, you can view call transcripts and sentiments for those interactions.

 1.  Click the Coaching \(\[Omitted image "coaching-new.png"\] Alt text: Coaching icon.\) icon.
2.  Click the **Active Assessments** tab.
3.  Select an assessment.


</td></tr><tr><td id="d34941e196">

**From Lists**

</td><td>

1.  Click the Lists \(\[Omitted image "list-new.png"\] Alt text: Lists icon.\)icon.
2.  Select an interaction record.


</td></tr></tbody>
</table>3.  Click **Call Analysis**.

    The Amazon Connect application generates the interactions and sentiment analysis of those interactions and displays them as a report in Workforce Optimization for Customer Service.

    In the CSM Configurable Workspace, agents use the **Call Analysis** tab to review calls, transcripts, and sentiment analysis. The recording playback widget is available if the agent's Amazon Connect security profile is configured to enable access to call recordings.

4.  [Analyze transcripts and sentiments for the Amazon Connect phone channel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/analyze-transcripts-sentiments-configurable-wfo-cs.md) and assign training to coach the agents.


**Parent Topic:**[Using Voice with Workforce Optimization for Customer Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/configurable-servicenow-voice-cs.md)

