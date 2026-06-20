---
title: Event Management setup
description: After activating Event Management, set it up to receive and process events, and generate and analyze alerts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-operations-management/event-management/c\_EMConfiguration.html
release: yokohama
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Event Management setup

After activating Event Management, set it up to receive and process events, and generate and analyze alerts.

## Event Management setup without using guided setup

Set up Event Management by completing these tasks in the following order:

1.  Configure a MID Server to receive and process events via the MID Server.
2.  [Configure the MID Web Server extension](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/event-management/configure-mid-web-server-extension.md).
3.  Configure [Configure Event Management connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/event-management/connectors-and-listeners.md).
4.  Configure [event field mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/event-management/c_EMEventFieldMapping.md) and [Binding alerts to CIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/event-management/ci-binding-alert.md) to manage alert generation.
5.  [Alert management rules for resolving alerts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/event-management/alert-management-rule.md), perform, and [CI remediation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/event-management/t_SACreateCIRemediation.md) for alert management.
6.  [Request Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/service-mapping/t_ActivateServiceMappingPlugin.md) and get a top-down [discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/event-management/t_EMGetBaselineServiceMapping.md) to receive CI relationships for software and hardware.
7.  Configure [impact calculation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/event-management/c_EMImpactCalculation.md) for services, to establish priority for alert resolution.
8.  Configure [alert groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/event-management/t_EMCreateAlertGroup.md) to consolidate related alerts.
9.  Configure the Predictive Intelligence plugin \(com.glide.platform\_ml\) to enable machine learning and finding similar alerts.
10. Configure any other general tasks that appear in this section as appropriate.

**Note:** Event Management does not support creating incidents on remote instances.

## Event Management setup using guided setup

Event Management guided setup provides a sequence of tasks that help you configure Event Management on your ServiceNow instance. To open Event Management guided setup, navigate to **Guided Setup** &gt; **ITOM Guided Setup**. For more information about using the guided setup interface, see Using guided setup.

-   **[Event Management during a platform upgrade](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/event-management/platform-upgrade-and-event-management.md)**  
During a platform upgrade Event Management jobs whose **Upgrade safe** flag is marked as `true` remain running.
-   **[MID Web Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/event-management/mid-web-server.md)**  
The MID Web Server is part of the common infrastructure of the MID Server.
-   **[Event Management configuration preferences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/event-management/r_EMBestPractice.md)**  
Preferred settings of properties and general configuration.

**Parent Topic:**[Configuring Event Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/event-management/using-event-management.md)

