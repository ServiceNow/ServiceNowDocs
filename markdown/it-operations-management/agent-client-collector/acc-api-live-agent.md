---
title: Verify API is associated with a live agent
description: Call the AgentNowHandler.hasAgent API to determine if the CI is associated with a live agent. The API gets a sys\_id of the CI and returns a true/false result.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Framework reference, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Verify API is associated with a live agent

Call the AgentNowHandler.hasAgent API to determine if the CI is associated with a live agent. The API gets a sys\_id of the CI and returns a true/false result.

The hasAgent\(\) method takes a sys\_id of the CI as a string parameter and returns **true** when the CI fulfills one of the following conditions:

-   The CI is `sn_agent_cmdb_ci_agent` and this agent is alive.
-   The CI is a host \(extends `cmdb_ci_hardware`\) and is associated with a live agent.
-   The CI is an application \(extends `cmdb_ci_appl`\) and has a runs-on relation to a host associated with a live agent.

For example:

```
var agentNow = new sn_agent.AgentNowHandler(); 
gs.info(‘Agent assocation with CI? ‘ + 
agentNow.hasAgent(‘158279505372b30034b8ddeeff7b1270’); // sys_id of agent 

```

**Parent Topic:**[Agent Client Collector Framework reference](../reference/agent-client-collector-reference.md)

