---
title: Event field mapping configuration
description: Use Event field mappings rules to map values from specific fields to values in other fields.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Processing Events, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Event field mapping configuration

Use Event field mappings rules to map values from specific fields to values in other fields.

Event Management stores event field mappings in the Event Field Mapping \[em\_mapping\_rule\] table. The mappings apply after event rule processing and prior to alert generation. The mapping values from the Event Mapping Pair \[em\_mapping\_pair\] table apply to the alert. The original event severity remains unchanged.

For example, if events come with the field "**org\_severity**" with the values "**Low**, **Medium**, **High**" and you want the alert **Severity** to hold this value, create an event field mapping rule that maps the field **org\_severity** to **Severity**, with these values:

|Original org\_severity value|Map to alert Severity value|
|----------------------------|---------------------------|
|Low|Warning|
|Medium|Major|
|High|Critical|

## Default event field mappings

Event Management provides default event field mappings for commonly used system monitoring tools. The Transform Value Pairs from event field mappings format the incoming event data for Event Management.

You can view the default event field mappings and mapping pairs by navigating to **Event Management** &gt; **Rules** &gt; **Event Field Mappings** and double-clicking **Name**.

-   **[Create event field mappings](../task/t_EMCreateEventFieldMapping2.md)**  
Use event field mappings to map values from specific event fields to values in other fields to provide more comprehensive information in an alert. Use team-based integrations in event rules to make sure that connector ownership and execution of rules give precedence to global rules. Teams can maintain consistency and hierarchy while offering flexibility and customization options.

**Parent Topic:**[Processing Events](processing-events.md)

