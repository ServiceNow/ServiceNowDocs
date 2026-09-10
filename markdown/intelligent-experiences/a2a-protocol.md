---
title: Agent2Agent Protocol
description: Agent2Agent \(A2A\) is an open standard that enables cross-platform AI agent communication by associating each agent with an Agent Card containing provider information.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/a2a-protocol.html
release: australia
topic_type: concept
last_updated: "2026-08-28"
reading_time_minutes: 1
breadcrumb: [Integrate external AI agents, AI Agent Studio, Enable AI experiences]
---

# Agent2Agent Protocol

Agent2Agent \(A2A\) is an open standard that enables cross-platform AI agent communication by associating each agent with an Agent Card containing provider information.

## Agent2Agent Protocol overview

The standard relies on every AI agent having an Agent Card associated with it. The Agent Card provides basic information for providers like the ServiceNow AI Platform, Azure, and Google to use them. The supported A2A version is 0.3.

An AI agent's Agent Card uses standardized JSON to help different providers understand its capabilities. The Agent Card is accessed by a specific type of endpoint from a provider's server. Execution plans are communicated through an execution endpoint so that both the provider's server and the ServiceNow AI Platform can track what the external AI agent is doing.

See [Create an external AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-a2a-agent-new.md) for instructions for using this protocol to create an AI agent.

## Configuring A2A authentication

A2A connections require authorization from the source platform to execute on the ServiceNow AI Platform. Authentication is established by creating two Connection &amp; Credential Alias and Connection records, one with an Agent Card endpoint and another with an execution endpoint.

## Custom Headers for External Agent Configuration

When configuring external agents, you can pass custom HTTP headers to be included in the API calls to external endpoints. In the External Agent Configuration \[sn\_aia\_external\_agent\_configuration\] table, use the custom headers column to specify headers in JSON format. These headers are applied to all HTTP requests made by that agent during offline execution, regardless of the connection type \(OAuth, API Key, or other\). The configured headers are sent alongside the agent's authentication credentials and are useful for passing additional metadata or requirements that your external API expects.

**Note:** Custom headers apply only to the Premium Chat experience.

## Configuration Properties

The following properties configure different aspects of how your agents can interact with the ServiceNow AI Platform.

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_aia.external\_agents.enabled

</td><td>

Set to `true` to enable external agent features

</td></tr><tr><td>

sn\_aia.external\_agents.parallel\_conversations.enabled

</td><td>

Enables or disables multiple simultaneous conversations per user

</td></tr></tbody>
</table>