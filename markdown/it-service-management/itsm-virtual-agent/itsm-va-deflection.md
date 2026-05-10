---
title: Tracking deflections in ITSM Virtual Agent
description: You can use the pre-built deflection topics and topic blocks in Virtual Agent conversations to track the incidents that ITSM Virtual Agent helped to resolve.
locale: en-US
release: australia
product: ITSM Virtual Agent
classification: itsm-virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [ITSM Virtual Agent pre-built actionable notifications, ITSM Virtual Agent, IT Service Management]
---

# Tracking deflections in ITSM Virtual Agent

You can use the pre-built deflection topics and topic blocks in Virtual Agent conversations to track the incidents that ITSM Virtual Agent helped to resolve.

A deflection happens when ITSM Virtual Agent resolves an issue for you. By asking you relevant questions, ITSM Virtual Agent can create an incident in the correct assignment group. As a result, you might not need to create an incident, or need the assistance of a live agent.

Deflection tracking uses the topics and topic blocks created in Virtual Agent Designer and is enabled by default. For more information, see [Tracking deflections using deflection topic blocks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/deflections-virtual-agent.md).

By default, ITSM Virtual Agent includes pre-built deflection configurations in the base system. You can use the deflection configurations in the base system or customize them, as needed. For more information, see [Create deflection configurations and patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/set-up-deflection-settings-va.md).

![Base system deflection configuration and patterns.](../image/itsm-deflection-tracking-default-configurations.png)

The pre-built deflection patterns in the base system are described in the following table.

|Deflection pattern name|Description|Outcome|
|-----------------------|-----------|-------|
|ITSM VA-Self-Resolving|Virtual Agent completes a task with or without filing a task record for ITSM. For example, Virtual Agent adds a user to a distribution list.|Confirmed deflection|
|ITSM VA-Triage &amp; Created|Virtual Agent filed and created a task record based on end-user input. Creating this task record shortens the time to resolution.|Confirmed deflection|
|ITSM VA-KB-Resolve|User resolved the issue by using the Knowledge Base \(KB\) articles displayed.|Confirmed deflection|
|ITSM VA-Intercept &amp; Resolved|Virtual Agent intercepted an end user-created incident, and helped to resolve and close it. For example, Virtual Agent resolves and closes the incident with Issue Auto-Resolution \(IAR\).|Confirmed deflection|
|ITSM VA-Search-served|Virtual Agent shows the search results based on the user's IT service needs.|Potential deflection|
|ITSM VA-AI-Search|Virtual Agent uses the AI Search results to provide support.|Confirmed deflection|
|ITSM VA-Query-response|Virtual Agent responds to a customer query. It's unclear whether the response was helpful.|Potential deflection|
|ITSM VA-No-deflection|Virtual Agent is unable to assist the user.|No deflection|
|ITSM VA-User Productivity-Complete|User completes a task using Virtual Agent. This pattern tracks those completed tasks that saved time and improved productivity.|No deflection|
|ITSM VA-User Productivity-Info Provided|User was provided information that might be helpful to them.|No deflection|
|ITSM VA-User Productivity-Incomplete|User wasn't able to complete a task using Virtual Agent.|No deflection|
|ITSM VA-Agent Productivity-Complete|Agent \(fulfiller\) was able to complete a task using Virtual Agent as a service channel. This pattern tracks those completed tasks that saved time and improved productivity.|No deflection|
|ITSM VA-Agent Productivity-Info Provided|Agent \(fulfiller\) was provided information that might be helpful to them.|No deflection|
|ITSM VA-Agent Productivity-Incomplete|Agent \(fulfiller\) wasn't able to complete a task using Virtual Agent as a service channel.|No deflection|

The deflection metrics are generated and stored in the Deflection Metric \[ssa\_deflection\_metric\] table. To view the deflection metrics for each deflection pattern, you can choose one of the following methods:

-   Navigate to the Deflection Metrics module in the Self-Service Analytics framework.

    **Note:** The Self-Service Analytics framework requires the Self-Service Analytics Core plugin \(com.snc.self\_service\_analytics\_core\).

    For more information, see [Activate Self-Service Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/activate-ssa-cs.md).

-   Use the **Overview** tab of the Conversational Analytics Dashboard.

    For more information about this dashboard, see Conversational Analytics Dashboard.


**Parent Topic:**[ITSM Virtual Agent pre-built actionable notifications](itsm-actionable-notifications.md)

