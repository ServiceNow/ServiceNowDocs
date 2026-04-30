---
title: Create a check definition
description: Create a check definition to execute the osquery command on the Agent.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Working with checks and policies, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Create a check definition

Create a check definition to execute the `osquery` command on the Agent.

## Before you begin

Role required: agent\_client\_collector\_integration or agent\_client\_collector\_admin

## Procedure

1.  In an Event Management instance, navigate to **Agent Client Collector** &gt; **Check Definitions**.

2.  Click **New**.

3.  In the **Name** field, enter `util.osquery`.

4.  In the **Check type** field, enter `osquery`.

5.  In the **Command** field, enter the following script:

    ```
    osqueryi  --logger_min_status 1 --json "{{.labels.params_query}} "
    ```

6.  In the **Plugins** field, enter the `osquery` plugin.

7.  In the **Parameters** section, enter the following values for a check parameter definition.

    |Column|Value|
    |------|-----|
    |**Name**|query|
    |**Default value**|select \* from logged\_in\_users|
    |**Mandatory**|true|

8.  Click **Test check** and select one of the available agents.

    The test result appears, indicating its success or failure.


**Parent Topic:**[Working with checks and policies](../concept/checks-policies-working-with.md)

