---
title: Event Management process flow
description: Event Management collects, analyzes, and converts events into alerts, enabling efficient tracking and remediation.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Exploring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Event Management process flow

Event Management collects, analyzes, and converts events into alerts, enabling efficient tracking and remediation.

Event Management receives external events and generates alerts based on event and alert management rules. Events are sent directly to your instance via email server, script, SNMP trap, or web service API. The corresponding alerts appear on dashboards for tracking and remediation purposes.

As the computer, software, or service generates events, the MID Server polls the external event tracking tool. The MID Server, maintaining a connection to Event Management, sends the information to your instance for storage, processing, and remediation.

The instance stores events in the Event \[em\_event\] table and attempts to generate alerts based on predefined rules and event mappings. Regardless of whether an alert is generated, the original event is available for review and remediation. Alerts are generated according to the following process flow.

1.  Match Event Rule: Find the best matching event rule for an event.

    A rule is matched if the source of the event matches the source specified in an existing rule. Additionally, a rule is matched if the event matches the optional rule filter and the event additional\_info value matches the rule Additional Information filter. A rule without any filter is ignored, such as when the source filter or Additional Information filter is missing. If multiple rules are defined for the same type of event, use the rule order to determine the sequence of rule application.

2.  Ignore Rule: If the rule **Ignore** check box is selected, no alert is generated. However, the event is still available for review and remediation.
3.  Apply Transforms:
    -   If transforms have been defined, apply them.
    -   If compose parameters are set, apply the additional content to display to the user in the alert.
4.  Threshold Accumulation: If Active in the threshold section is selected, accumulate all events until the threshold is met, then generate a single alert for the events.
5.  Event Field Mapping
    -   Search for an event field mapping even if there was no event rule.
    -   If an event field mapping is found, apply the mapping information.
    -   If the event has no severity after the event transformations, retain the event for reference purposes and do not generate an alert.
6.  Alert Generation
    -   Search the Alert \[em\_alert\] table for a matching message key.
    -   If a matching message key exists, update the alert according to the event information.
    -   If a matching message key does not exist, create an alert.
    -   If another event has the same matching key, associate the events under a single alert.
    -   For root cause analysis purposes, bind the alert to a specific Configuration Item \(CI\).

![Event workflow](../image/EMEventFlow.png "Event workflow")

