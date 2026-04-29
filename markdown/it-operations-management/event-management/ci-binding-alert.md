---
title: Binding alerts to CIs
description: CI binding or linking is the process of finding and connecting a Configuration Item \(CI\) from the Configuration Management Database \(CMDB\) to an alert, using the logic defined in event rules. This helps ensure alerts are tied to the right IT components for better visibility and faster issue resolution.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Event rules, Processing Events, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Binding alerts to CIs

CI binding or linking is the process of finding and connecting a Configuration Item \(CI\) from the Configuration Management Database \(CMDB\) to an alert, using the logic defined in event rules. This helps ensure alerts are tied to the right IT components for better visibility and faster issue resolution.

## Understanding CI binding

Binding alerts to CIs links incoming alerts to the correct Configuration Item \(CI\) representing a specific host, such as a computer, server, router, or virtual machine in your IT infrastructure. This ensures accurate alert tracking, simplifies troubleshooting by identifying the source of issues, and maintains a historical record of alerts tied to specific systems.

In IT Operations Management, the relationship between alerts and CIs plays a critical role in effectively managing services and infrastructure. A CI represents a component within your IT environment, such as a server, application, or database. Linking alerts to CIs ensures that alerts and incidents are directly associated with the affected component, enabling accurate impact analysis and faster resolution.

In dynamic and large-scale environments, it’s often challenging to pinpoint which CI is responsible for triggering an alert. Alerts are generated from raw event data captured across multiple sources, but this data may not explicitly reference a CI. Without a reliable method to bind alerts to CIs, IT teams face the risk of:

-   Poor visibility into service impact.
-   Longer mean time to resolution \(MTTR\).
-   Inefficient alert management processes.

Event rules provide a structured way to analyze incoming event data, enrich it with additional context, and map it to the correct CI. These rules act as a bridge, transforming raw event data into actionable alerts linked to CIs. For example, event rules can:

-   Parse incoming event data: The process involves breaking down raw event data to extract important details, such as hostnames, IP addresses, or service tags. These details are then used to analyze the event—identifying its source, type, and impact—and to enrich the alert by adding relevant context, like affected services, priorities, or resolution steps, ensuring it’s actionable for IT teams.
-   Match patterns: Here, the extracted event details—such as hostnames, IP addresses, or service tags—are compared against entries in the CMDB to identify the corresponding Configuration Item \(CI\) based on predefined rules or logic. Once matched, the alert is linked to the CI, providing context about the affected IT component for better visibility and faster resolution.
-   Bind the CI to the alert: At this point, the alert is automatically associated with the identified CI. It ensures that the alert is connected to the right IT component in the system, making it easier to track and manage, and helping teams quickly address the issue.

## Types of CI binding

|Binding type|Description|
|------------|-----------|
|Implicit Node binding \(Default binding\)|Binds alerts to host CIs by matching the **Node** field in the event with attributes like Name, FQDN, IP, or MAC address.|
|CI field matching binding|Binds alerts using the **CI Identifier** field, a JSON structure containing column names and values \(e.g., Name, FQDN, IP, or MAC Address\).|
|CI identification binding|Binds alerts to specific applications on hosts using event rules.|
|Process-level binding|Binds alerts to application CIs by matching process-related attributes.|
|Device-level binding|Binds alerts to device CIs by matching event data with attributes like hostname, IP address, or MAC address.|

## Key benefits

-   Improved service visibility: Alerts linked to CIs provide a clear picture of which IT components are affected.
-   Enhanced automation: Automated CI binding reduces manual effort, ensuring consistency.
-   Faster resolution: Teams can quickly diagnose and resolve issues by focusing on the impacted CI.

## Example use case

Scenario: A company’s email server named MailServer-01 goes down.

Process:

1.  Alert generation: An alert is triggered when MailServer-01 becomes unresponsive.
2.  CI binding: Event Management automatically looks for MailServer-01 in the CMDB \(Configuration Management Database\).
    -   If found, the alert is linked to this specific server \(CI\).
    -   If not found, the alert remains unlinked until more information is provided.

Result: The alert now shows that MailServer-01 is the affected system.

-   Impact: IT teams immediately know which server to investigate.
-   Efficiency: They don't need to check other infrastructure components or systems, saving time and effort.

This direct link helps streamline troubleshooting by pointing to the exact problem source.

**Related topics**  


[Simulate event processing](../task/simulate-event-processing.md)

