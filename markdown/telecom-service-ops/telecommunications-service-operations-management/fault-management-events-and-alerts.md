---
title: Fault Management: Events and alerts
description: Fault Management supports the monitoring, detection, and resolution of configuration and performance issues across SD-WAN-managed network devices. It integrates with Event Management to generate alerts and track events automatically.
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Telecom Assurance, Explore, Telecommunications Service Operations Management]
---

# Fault Management: Events and alerts

Fault Management supports the monitoring, detection, and resolution of configuration and performance issues across SD-WAN-managed network devices. It integrates with Event Management to generate alerts and track events automatically.

Fault Management helps you monitor network devices by collecting alerts related to configuration and performance issues. Key features include alerting, customizable event rules, webhook-based notifications, and integration through the Integrations Launchpad.

Alerts are central to detecting and responding to configuration issues. Each alert is generated based on three core attributes:

-   Device name: The affected device \(for example, IP router, IP switch, access point\)
-   Alert type: The category of the event
-   Alert level: The severity level \(informational, warning, critical\)

When a monitored event occurs, you can create an alert with these attributes and begin tracking it. You can configure event rules to control what happens next: grouping related alerts, escalating critical ones, or suppressing noise so your team only sees issues that require action. The Integrations Launchpad provides a central place to manage integrations with external systems.

## Managing alerts with event rules

Event rules and alert suppression give you control over how alerts are generated and managed. Configure the following options to control alert generation:

-   Event rules: Set criteria such as the device name, alert type, severity, and frequency to determine the events and create the appropriate alert.
-   Alert suppression: Consolidate multiple alerts from the same device into a single record.
-   Alert grouping: Combine related events into a single alert for easier management.
-   Correlation IDs: Link related events and alerts with unique identifiers, improving traceability across the event life cycle. These IDs create connections between relevant objects and alerts, enabling you to navigate directly between them.

For instructions on how to configure Event Management solutions, see the following documentation:

-   [Configure a webhook](../task/configure-fault-management.md)
-   [Configure an event pull connector](../task/configure-an-event-pull-connector.md)
-   [Cisco Meraki installed integrations](meraki-installed-integrations.md)
-   [Fortinet installed integrations](fortinet-installed-integrations.md)

