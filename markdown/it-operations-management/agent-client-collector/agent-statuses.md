---
title: Agent Client Collector statuses
description: The following table lists and describes the Agent Client Collector statuses.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/agent-client-collector/agent-statuses.html
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Framework reference, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector statuses

The following table lists and describes the Agent Client Collector statuses.

|Status|Description|
|------|-----------|
|Up|Agent is connected and working properly.|
|Warning|Agent has not been refreshed in over 2 minutes \(based on the value of the sn\_agent.keep\_alive.alive\_duration property\).|
|Down|Agent is shut down.|
|Restarting|Agent restart is in progress.|
|Upgrading|Agent upgrade is in progress.|
|Disconnected|Agent's MID Server is down.|
|Unknown|Agent’s MID Server has not sent a keepalive communication for over 10 minutes \(based on the value of the sn\_agent.keep\_alive.disconnected\_duration system property\).|

**Parent Topic:**[Agent Client Collector Framework reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/agent-client-collector-reference.md)

