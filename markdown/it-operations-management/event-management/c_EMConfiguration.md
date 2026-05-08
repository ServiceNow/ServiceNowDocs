---
title: Event Management setup
description: After activating Event Management, set it up to receive and process events, and generate and analyze alerts.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Event Management setup

After activating Event Management, set it up to receive and process events, and generate and analyze alerts.

## Event Management setup without using guided setup

Set up Event Management by completing these tasks in the following order:

1.  Configure a MID Server to receive and process events via the MID Server.
2.  [Configure the MID Web Server extension](../task/configure-mid-web-server-extension.md).
3.  Configure [Configure Event Management connectors](../reference/connectors-and-listeners.md).
4.  Configure [event field mappings](c_EMEventFieldMapping.md) and [Binding alerts to CIs](ci-binding-alert.md) to manage alert generation.
5.  [Alert management rules for resolving alerts](alert-management-rule.md), perform, and [CI remediation](../task/t_SACreateCIRemediation.md) for alert management.
6.  [Request Service Mapping](../../service-mapping/task/t_ActivateServiceMappingPlugin.md) and get a top-down [discovery](../task/t_EMGetBaselineServiceMapping.md) to receive CI relationships for software and hardware.
7.  Configure [impact calculation](c_EMImpactCalculation.md) for services, to establish priority for alert resolution.
8.  Configure [alert groups](../task/t_EMCreateAlertGroup.md) to consolidate related alerts.
9.  Configure the Predictive Intelligence plugin \(com.glide.platform\_ml\) to enable machine learning and finding similar alerts.
10. Configure any other general tasks that appear in this section as appropriate.

**Note:** Event Management does not support creating incidents on remote instances.

## Event Management setup using guided setup

Event Management guided setup provides a sequence of tasks that help you configure Event Management on your ServiceNow instance. To open Event Management guided setup, navigate to **Guided Setup** &gt; **ITOM Guided Setup**. For more information about using the guided setup interface, see Using guided setup.

