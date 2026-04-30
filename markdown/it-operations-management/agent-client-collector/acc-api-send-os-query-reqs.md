---
title: Create a call API to send an osquery request
description: Create a background script to send an osquery request. The osquery request enables data collection from your host's operating system.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Enabling ACC data collection, ACC deployment - shared between servers and endpoints, Agent Client Collector, IT Operations Management]
---

# Create a call API to send an osquery request

Create a background script to send an `osquery` request. The `osquery` request enables data collection from your host's operating system.

## Before you begin

Role required: administrator

## Procedure

1.  Create the following background script:

    -   `"MTLV9DE22016"` is the name of the server running an agent
    -   `"c8bf9072539333003e76ddeeff7b12c5"` is the sys\_id of the previously created check definition
    ```
    
    cis = new GlideRecord("cmdb_ci_server"); 
        cis.addQuery("name", "MTLV9DE22016"); 
        cis.query(); 
        check = { 
            "checkDefId": "c8bf9072539333003e76ddeeff7b12c5",
            "params": { 
                "query": "select pid,cmdLine from processes limit 4" 
            } 
        }; 
        var agentNow = new sn_agent.AgentNowHandler(); 
        gs.info('request_id: ' + agentNow.runCheckForCis(cis,check,'1',60000));
    ```

2.  Run the script to print the request ID:

    request\_id: `eefbff7ab75733003e766068de11a981`

3.  Check the system logs for messages coming from the instance script.

    ```
    result 0 requestId: 06c6c887b79733003e766068de11a912 agent_name: MTLV9DE22016 ci_id:
    00726c36539333003e76ddeeff7b12db status: 0 output: [ 
    {"cmdline":"","pid":"0"}, 
    {"cmdline":"","pid":"1"}, 
    {"cmdline":"","pid":"45"}, 
    {"cmdline":"","pid":"46"} 
    ] 
    ```


**Parent Topic:**[Enabling Agent Client Collector data collection](../concept/data-collection-enabling.md)

