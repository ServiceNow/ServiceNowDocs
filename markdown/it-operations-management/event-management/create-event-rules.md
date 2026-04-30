---
title: Event rules
description: Use event rules to generate alerts for tracking and remediation. Event rules are stored in the Event Rule \[em\_match\_rule\] table. Configure and customize event rules to manage events and alert generation.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Processing Events, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Event rules

Use event rules to generate alerts for tracking and remediation. Event rules are stored in the Event Rule \[em\_match\_rule\] table. Configure and customize event rules to manage events and alert generation.

Event rules do not change the event records in the Event table. Changes to event data are stored in the ServiceNow instance memory.

![Event Management rule](../image/event-rule-designer.png)

Use the Event rule designer to create and configure event rules. You can use the default event rules or event rules that you have created to:

-   Apply an event rule filter to determine whether the rule applies to an event.
-   Apply a transform with **Event Match Fields** and optional **Event Compose Fields** to format the alert text.
-   Apply a threshold to create custom alerts for rapidly recurring events.
-   Automatically create or close alerts.
-   Bind alerts to CI information from the CMDB.
-   Run multiple sequential rules defined for the same event by selecting the **Apply additional matching rules** check box. The event rules run in ascending order as defined in the **Order** field. Event rules applied to assignment groups only run after the global rules have run.


-   **[Create or edit an event rule](../task/create-or-edit-event-rule.md)**  
You can create event rules to generate alerts for tracking and remediation. Use team-based integrations in event rules to make sure that connector ownership and execution of rules give precedence to general rules. Teams can maintain consistency and hierarchy while offering flexibility and customization options.
-   **[Use event input information](event-input-information.md)**  
The **Event Input** pane that is included in the steps to create an event rule provides a reference to the information that you can use when configuring an event rule.
-   **[Filter the events that an event rule applies to](../task/t_EMCreateFilter.md)**  
Define a filter to restrict to which events the event rule must apply. Configure the filter by providing a set of conditions that each event must match to be either excluded or included from applying to the event rule.
-   **[Find events that are not matched to rules](../task/t_EMFindEventNoRule.md)**  
Find events that are not matched to any rules, and determine if it is necessary to create event rules to manage them.
-   **[View event rules](../task/t_EMViewEventRule.md)**  
You can view all event rules on the Event Rules list.
-   **[Configure an event rule to customize alert content](../task/t_EMComposeOuput.md)**  
You can configure an event rule to customize alert content. You can customize the order of the fields and select which fields display. The fields in the left-hand work area of the **Transform and Compose Alert Output** section of an event rule are the fields that appear in the generated alert.
-   **[Set a threshold to suppress alert generation](../task/t_EMISetThresholdEvent.md)**  
The event threshold is the rate upon which Event Management generates an alert. Receiving multiple events for a device over a short interval may warrant creating an alert, as the condition may be serious. However, receiving events over a longer interval may indicate a less serious situation which would not warrant creating an alert.
-   **[View patterns for event group creation](../task/t_EMViewEventGroup.md)**  
Event groups are sets of events that do not have a matching event rule. You can view the patterns in a group of events to learn the impact of creating a rule based on the event source and description patterns.
-   **[Refresh event rules](../task/refresh-event-rule.md)**  
Manually update event rules to reflect current event information because once an event rule is created, the **Event Additional info** and **Event Raw info** fields are not automatically updated.
-   **[Find rules that will be applied to an event](../task/t_EMViewRuleApply.md)**  
View the rules that will be applied on an event to determine how this event will be processed.
-   **[Simulate event processing](../task/simulate-event-processing.md)**  
You can simulate event processing logic on events and display the resulting alert to better understand which rules are executed on a given event and how the event fields change after the rule is executed.

**Parent Topic:**[Processing Events](processing-events.md)

