---
title: Create a check type
description: Create a check type to execute the osquery command on the Agent.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Collect data from your system devices, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Create a check type

Create a check type to execute the `osquery` command on the Agent.

## Before you begin

Role required: agent\_client\_collector\_integration or agent\_client\_collector\_admin

## Procedure

1.  In an Event Management instance, enter `sn_agent_check_type.list` into the navigation bar.

    The **Check Types** page appears.

2.  Click **New**.

    The `Check Type - New Record` page appears.

3.  In the **Name** field, enter `osquery`.

4.  In the **Instance Script** field, enter the following script:

    ```
    for (var index = 0; index < checkResults.length; index++) { 
    var check = checkResults[index].check; 
    gs.info('result ' +  
    index + ': requestId: ' +  
    check.requestId + ' agent_name: ' +  
    checkResults[index].agent_id +  
    ' ci_id: ' + check.ci_id +  
    ' status: ' + check.status +  
    ' output: ' + check.output); 
    
    } 
    ```

    You can modify this script, as needed, but this initial script helps you to verify that your setup was successful.

5.  Click **Submit**.


