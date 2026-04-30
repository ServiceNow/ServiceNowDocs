---
title: Agent Client Collector Security Incident Response capabilities
description: Agent Client Collector Security Incident Response capabilities that come with the base system are listed on the ACC Capabilities page \( Agent Client Collector SIR Integration ACC Integration Capabilities \). These capabilities run on security incidents to gather information about the incident.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Security Incident Response, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector Security Incident Response capabilities

Agent Client Collector Security Incident Response capabilities that come with the base system are listed on the ACC Capabilities page \(**Agent Client Collector SIR Integration** &gt; **ACC Integration Capabilities**\). These capabilities run on security incidents to gather information about the incident.

You select a capability from the **Agent Client Collector Capabilities** option in the Related Links section of the security incident. Capabilities are part of existing system flows, which are referenced on the ACC Capabilities page.

|Capability Name|Description|Flow|
|---------------|-----------|----|
|Get Logged on Users|Gathers data of logged on users and relates it to the security incident.|ACC SIR - Get Logged on Users|
|Get Network Statistics|Gathers network statistics for the CI associated with the security incident.|ACC SIR - Get Network Statistics|
|Get Processes|Gathers process data and relates it to the security incident.|ACC SIR - Get Processes|
|Get Services|Gathers service data and relates it to the security incident.|ACC SIR - Get Services|
|Get System Details|Gathers system details for the CI associated with the security incident.|ACC SIR - System Details|
|Run Command on Agent|Runs a custom command on the Agent Client Collector and sends results to the security incident.|ACC SIR - Run Command from Security Incident|
|Run OSQuery on Agent|Runs a custom OSQuery on the Agent Client Collector and sends results to the security incident.|ACC SIR - Run OSQuery from Security Incident|

**Parent Topic:**[Agent Client Collector Security Incident Response](../concept/acc-security-incident-response.md)

