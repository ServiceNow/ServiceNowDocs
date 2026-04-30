---
title: Integrate Sumo Logic events
description: Use the Sumo Logic push connector to integrate Sumo Logic with Event Management by adding a standard webhook in the Sumo Logic platform.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Integrate with push connectors, Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Integrate Sumo Logic events

Use the Sumo Logic push connector to integrate Sumo Logic with Event Management by adding a standard webhook in the Sumo Logic platform.

## Before you begin

Ensure that the Event Management connector's plugin is installed on the ServiceNow AI Platform instance.

Role required: evt\_mgmt\_integration

## About this task

Configure the Event Management environment for the collection of events from Sumo Logic by authenticating Sumo Logic as a data source. In the Sumo logic site, set your ServiceNow AI Platform instance as the rest endpoint using a webhook.

## Procedure

1.  In the Sumo Logic site, create a notification destination.

2.  Go to Monitoring and select **Custom Webhook**.

3.  Fill in the form with the Name, Description, and the URL.

    Use this URL format to push events from Sumo logic to the ServiceNow Instance .`https://<username>:<password>@<instance-name>.service-now.com/api/sn_em_connector/em/inbound_event?source=sumologic`

    **Note:** Use a credential having the evt\_mgmt\_integration role as the username and password.

    In the Payload section, use the following template:

    ```
    {
        "type": "{{MonitorType}}",
        "node": "{{ResultsJSON._sourceHost}}",
        "metric_name": "{{Name}}",
        "description": "monitor Query: {{Query}}\n Trigger Condition:{{TriggerCondition}}\n Trigger Value:{{TriggerValue}}\n Trigger Time Range:{{TriggerTimeRange}}\n View Trigger Query:{{TriggerQueryURL}}\n View Monitor:{{QueryURL}} \n Results:{{ResultsJSON}}",
        "name": "{{Name}}",
        "short_description": "{{Description}}",
        "MonitorType": "{{MonitorType}}",
        "Query": "{{Query}}",
        "QueryURL": "{{QueryURL}}",
        "ResultsJson": "{{ResultsJson}}",
        "NumQueryResults": "{{NumQueryResults}}",
        "Id": "{{Id}}",
        "DetectionMethod": "{{DetectionMethod}}",
        "TriggerType": "{{TriggerType}}",
        "TriggerTimeRange": "{{TriggerTimeRange}}",
        "time_of_event": "{{TriggerTime}}",
        "TriggerCondition": "{{TriggerCondition}}",
        "TriggerValue": "{{TriggerValue}}",
        "TriggerTimeStart": "{{TriggerTimeStart}}",
        "TriggerTimeEnd": "{{TriggerTimeEnd}}",
        "SourceURL": "{{SourceURL}}",
        "alertResponseUrl": "{{alertResponseUrl}}"
      }
    
    ```

    Log Monitors Type events can be created without CI binding since you’re receiving the node value as "node": "\{\{ResultsJSON.\_sourceHost\}\}" in the event payload from Sumo Logic. You can create events but you can’t bind them since you don’t get them as host names for the log monitor type. A push connector parameter was created - “create\_log\_monitorType\_events” with a value of False. If the param value is False, the payload is ignored, and “log” events aren’t created. If you change the param to True, events are created, and then you must define event rules for CI binding.

    Refer to the following ServiceNow Severity Mapping with Sumo logic TriggerType table:

    |**Sumo Logic Trigger Type**|**Severity**|
    |---------------------------|------------|
    |Critical|Critical|
    |Warning|Minor|
    |MissingData|Warning|
    |ResolvedCritical/ResolvedWarning/ResolvedMissingData|Clear|


-   **[Integrate Sumo Logic with REST API key token](integrate-sumologic-api-key.md)**  
Integrate using an API key to establish secure communication and automate data exchange via REST API. This simplifies integration, enabling seamless access to services and enhancing operational efficiency.

**Parent Topic:**[Integrate with push connectors](configure-listener-transform-script.md)

