---
title: Map Kafka message payload attributes to alert fields
description: Map Kafka message attributes to alert fields to make alerts based on the messages more meaningful. Use event field mapping to map Kafka severity values to appropriate ServiceNow values.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Apache Kafka Consumer Connector, Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Map Kafka message payload attributes to alert fields

Map Kafka message attributes to alert fields to make alerts based on the messages more meaningful. Use event field mapping to map Kafka severity values to appropriate ServiceNow values.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

Depending on your payload, Use event field mappings to provide more comprehensive information in an event alert by substituting values from the event field mapping rule into the event. Depending on your payload, transform information in events to populate specified alert field values and compose alert fields from various values to generate alerts for tracking and remediation. If needed, use both event field mappings and alert rules.

The following table compares a message received from a topic and a flattened payload in the event **Additional info** field. The message received from a topic is flattened as a single field and appears in the event **Additional info** field. Use these flattened messages to create event rules and mappings.

<table id="table_v4p_xtx_svb"><thead><tr><th>

Actual Payload inserted into a topic

</th><th>

Flattened payload in the Additional Info field

</th></tr></thead><tbody><tr><td>

```
{ 

  "version": "v0.1.0", 

  "name": "fibsrc", 

  "id": "mnop6789", 

  "trigger_description": "Triggers on duration_ms goes above 5K", 

  "status": "TRIGGERED", 

  "alert_type": "on_true", 

  "summary": "Triggered: fibsrc", 

  "description": "Current value (12.296815 k) greater than threshold value (5 k)", 

  "operator": "greater than", 

  "threshold": 5000, 

  "groups": [ 

    { 

      "Group": "GroupA", 

      "Result": 12296.815478000368 

    } 

  ], 

  "trigger": { 

    "Result": 12296.815478000368 

  } 

} 
```

</td><td>

```
{ 

  "flattened.alert_type": "on_true", 

  "flattened.description": "Current value (12.296815 k) greater than threshold value (5 k)", 

  "flattened.id": " mnop6789", 

  "flattened.kafkaKey": "null", 

  "flattened.kafkaOffset": "28", 

  "flattened.kafkaPartition": "0", 

  "flattened.kafkaTopicName": "topic123", 

  "flattened.name": "fibsrc", 

  "flattened.operator": "greater than", 

  "flattened.status": "TRIGGERED", 

  "flattened.summary": "Triggered: fibsrc", 

  "flattened.trigger_description": "Triggers on duration_ms goesa above 5K", 

  "flattened.version": "v0.1.0", 

  "flattened.version": 5000, 

  "flattened.groups.0.Group": "GroupA", 

  "flattened.groups.0.Result": 12296.815478000368, 

  "flattened.trigger.Result": 12296.815478000368 

} 




```

</td></tr></tbody>
</table>## Procedure

1.  To map the Kafka message attributes to the predefined alert fields to generate alerts by creating event field mappings.

    1.  Navigate to **All** &gt; **Event Management** &gt; **Rules** &gt; **Event Field Mapping**.

    2.  In the Event Field Mapping window, select **New**.

    3.  In the Name field, enter a name for the field mapping.

    4.  In the Source field, enter **Kafka Consumer**.

    5.  In the Mapping type field, select the appropriate mapping type

    6.  For a list of the available mapping types, see [Event Field Mappings](t_EMCreateEventFieldMapping2.md).

2.  To map the Kafka message attributes to the predefined alert fields to generate alerts by creating event rules.

    1.  Navigate to **All** &gt; **Event Management** &gt; **Rules** &gt; **Event Rules**.

    2.  Select **New** .

    3.  In the Name field, enter a name for the event rule.

    4.  In the Source field, enter **Kafka Consumer**.

    5.  Select **Event Filter**.

    6.  Enter the appropriate filter according to your requirement.

    7.  Select **Transform and compose alert output**.

        When creating event rules, the event fields are displayed in the Event Rules Transform and Compose Alert Output tab. Because the Kafka message varies from user to user, you must transform the event fields to the alert fields to see the details in the alert.

        **Note:** Because the severity value is required to create an alert, you must map the **Severity** field using event rules or event field mappings. If the Severity field is empty, the event isn’t processed and enters into an error state.

    8.  Map the fields of the event and **Additional Info** field to the fields of the alert.

    9.  Select **Binding**.

    10. Enter the appropriate binding according to your requirement.

    11. Select **Submit**.

        For more information, see [Create or edit an event rule](create-or-edit-event-rule.md).

3.  In the All Events screen, check whether any of the events from Kafka are in an error state due to a missing event rule and provide missing rules.

    1.  Navigate to **All** &gt; **Event Management** &gt; **All Events**.

    2.  In the All Events table, open any Kafka consumer event that shows Error as the state in the **Severity** column.

        The message received from the Kafka consumer can vary. Because the connector cannot know the attributes that will be received, you must map the **Severity** field or other event fields to the fields in the message to ensure that alert fields are correctly populated.

    3.  On the All Events screen, create a new event rule by selecting **Create Event Rule**.

        For more information on creating event rules, see [Event Rules.](create-or-edit-event-rule.md)

        If no event field mappings exist to handle the new type of event, create event field mappings. For more information, see [Create event field mappings](t_EMCreateEventFieldMapping2.md).


## Result

Your Apache Kafka consumer connector is configured. When new messages arrive into the Kafka topic, they are received into the ServiceNow instance as events, and alerts are then created from those events.

**Parent Topic:**[Apache Kafka Consumer Connector](../concept/apache-kafka-consumer-connector.md)

