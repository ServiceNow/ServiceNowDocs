---
title: Event forwarding properties
description: Several system properties enable you to customize an event forwarding job.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Event Management reference, Event Management, ITOM AIOps, IT Operations Management]
---

# Event forwarding properties

Several system properties enable you to customize an event forwarding job.

**Note:** To access the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_gw2_vg1_fwb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

evt\_mgmt.event\_forwarding.sources\_to\_exclude

</td><td>

List of event sources from which events should not be forwarded. By default, all events are forwarded. Separate multiple sources by commas.-   **Type**: string
-   **Default value**: Empty

</td></tr><tr><td>

evt\_mgmt.event\_forwarding.event\_fields\_to\_include

</td><td>

List of event fields to include when sending events to the target instance besides the required default fields: resolution\_state, event\_class, additional\_info, node, resource, cmdb\_ci,severity, time\_of\_event, message\_key, sys\_domain, metric\_name, ci\_type, ci\_identifier, type, source, description, and sys\_domain\_path.Separate multiple fields by commas.

-   **Type**: string
-   **Default value**: Empty

</td></tr><tr><td>

evt\_mgmt.event\_forwarding.event\_batch\_size

</td><td>

Maximum number of events to batch while sending to the target instance.-   **Type**: integer
-   **Default value**: 500

</td></tr><tr><td>

evt\_mgmt.event\_forwarding.max\_payload\_size\_in\_mb

</td><td>

Maximum size of the event payload, in MB, sent to the target instance at a single time.-   **Type**: integer
-   **Default value**: 5

</td></tr><tr><td>

evt\_mgmt.event\_forwarding.max\_events\_to\_forward\_per\_day

</td><td>

Maximum number of events that can be forwarded from the instance per day to minimize the performance impact on the source instance. -   **Type**: integer
-   **Default value**: 100000

</td></tr><tr><td>

evt\_mgmt.event\_forwarding.log\_debug

</td><td>

Enables or disables debug logging for event forwarding. Set this property to true to log debugging information.-   **Type**: Boolean
-   **Default value**: False

</td></tr></tbody>
</table>**Parent Topic:**[Event Management reference](event-management-reference.md)

