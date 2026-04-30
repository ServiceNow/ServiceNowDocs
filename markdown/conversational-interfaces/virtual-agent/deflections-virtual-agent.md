---
title: Using the deflection topic block to track deflections in Virtual Agent
description: Use the pre-built deflection topic block in ServiceNow Virtual Agent to track the issues that Virtual Agent helped to resolve or actually resolved for a user. Incident deflection patterns and metrics can help you optimize and analyze the effectiveness of Virtual Agent.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Case and incident deflection, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Using the deflection topic block to track deflections in Virtual Agent

Use the pre-built deflection topic block in ServiceNow® Virtual Agent to track the issues that Virtual Agent helped to resolve or actually resolved for a user. Incident deflection patterns and metrics can help you optimize and analyze the effectiveness of Virtual Agent.

A deflection occurs when Virtual Agent automatically redirect users to self-service options or knowledge base articles that can help them solve their problems without requiring the assistance of a live agent. As a result, the user might not need to create an incident. If necessary, however, Virtual Agent can ask relevant questions and then create an incident in the correct assignment group. This workflow becomes more efficient because no live agent has to get involved.

The Virtual Agent deflection tracking is enabled by default, but you must set up the deflection configuration and deflection patterns to capture certain deflection metrics. For more information, see [Create deflection configurations and patterns](../task/set-up-deflection-settings-va.md).

You use deflection configurations to group deflection patterns. A deflection configuration can consist of one or more deflection patterns. Deflection patterns categorize Virtual Agent activities in conversations for tracking deflection metrics. For example, let's say that Virtual Agent adds a user to an email list without creating a task in the Task table to complete the workflow. You can categorize this activity as a self-resolving deflection pattern.

You can view the deflection metrics for each deflection pattern. A deflection pattern can lead to these deflection outcomes in a conversation:

-   Confirmed deflection: Virtual Agent provided a resolution to the user, which prevented the user from creating an incident or transferring to a live agent.
-   Potential deflection: It is unclear whether Virtual Agent provided a resolution to the user. An example is when search results are displayed to a user in a conversation.
-   No deflection: Virtual Agent did not provide a resolution, and the user created an incident or transferred to a live agent.

You can either create new deflection patterns, or use these pre-built deflection patterns in the **VA Default** deflection configuration:

|Deflection pattern|Activity|Outcome|
|------------------|--------|-------|
|VA-Search-served|Virtual Agent showed search results to the user.|Potential deflection|
|VA-Triage &amp; Created|Virtual Agent creates an incident in the correct assignment group. This action improves the assignment accuracy. For example, Virtual Agent identifies a reimbursement-related intent in a user conversation and creates a reimbursement incident instead of a general incident.|Confirmed deflection|
|VA-Self-Resolving|Virtual Agent completes the workflow on its own without creating an incident. For example, Virtual Agent adds a user to a distribution list.|Confirmed deflection|
|VA-Intercept &amp; Resolved|Virtual Agent intercepts an incident that was created by a user and provides a resolution to close the incident. An example is when Incident Auto Resolution resolves an incident.|Confirmed deflection|

The deflection configuration and deflection pattern that you create in the deflection settings are mapped to the deflection topic block. For example, the pre-built Issue Auto Resolution topic uses a deflection topic block to track deflections. For more information, see [Maximizing code reuse with topic blocks](topic-blocks-overview.md) and [Virtual Agent pre-built topic blocks for NLU](../reference/va-platform-topicblocks.md).

The deflection metrics are generated and stored in the Deflection Metric \[ssa\_deflection\_metric\] table. To view the deflection metrics, navigate to the Deflection Metrics module in the Self-Service Analytics framework.

**Note:** The Self-Service Analytics framework requires the Self-Service Analytics Core plugin \(com.snc.self\_service\_analytics\_core\). For more information, see [Activate Self-Service Analytics](https://www.servicenow.com/docs/access?context=activate-ssa-cs&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

![Deflection metrics for Virtual Agent deflections.](../images/def-metrics.png "Deflection metrics")

You can also view the visualization for deflection metrics in the **Overview** tab of the Conversational Analytics Dashboard. For more information, see .

-   **[Create deflection configurations and patterns](../task/set-up-deflection-settings-va.md)**  
Set up deflection settings to create deflection configurations and deflection patterns that you can map to deflection topic blocks in Virtual Agent conversation topics. These deflections help you to track the issues that Virtual Agent helped to resolve or actually resolved for a user.

**Parent Topic:**[Case and incident deflection in Virtual Agent](case-incident-deflection-virtual-agent.md)

