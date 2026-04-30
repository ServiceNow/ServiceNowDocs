---
title: Agent Client Collector plugins
description: An Agent Client Collector plugin is a script or group of scripts that extend the Agent Client Collector's capabilities. Plugins enhance monitoring by collecting metrics, performing specialized checks, and triggering events based on conditions, like monitoring an application's queue size when it reaches 60% or 80%. Plugins ensure scalable, customizable monitoring to adapt to evolving infrastructure or application needs.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Exploring Agent Client Collector Framework, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector plugins

An Agent Client Collector plugin is a script or group of scripts that extend the Agent Client Collector's capabilities. Plugins enhance monitoring by collecting metrics, performing specialized checks, and triggering events based on conditions, like monitoring an application's queue size when it reaches 60% or 80%. Plugins ensure scalable, customizable monitoring to adapt to evolving infrastructure or application needs.

## Plugin-check dependency

Plugins are tightly integrated with checks in the Agent Client Collector Framework. A dependency is created between the plugin and the check to ensure that the plugin is executed alongside the associated check.

-   Plugin Dependency: A plugin can be associated with one or more checks, and vice versa, where checks can depend on multiple plugins.
-   Execution: Plugins and checks run on the same agent, working in unison to gather data, perform specialized tasks, or trigger necessary events

## Creating and managing plugins

You can create Agent Client Collector plugins as needed to customize the monitoring to your specific environment. These plugins are typically formatted as tar.gz files, which contain the scripts that define the plugin's functionality.

-   Plugin creation: Custom plugins are developed and packaged into tar.gz files.
-   Integration with checks: Once created, the plugin is integrated with checks by establishing the appropriate dependencies, ensuring that the plugin and check run together.
-   Customization: Plugins can be customized to meet the specific requirements of your monitoring needs, whether it's adding more detailed metrics, checking system thresholds, or generating custom events.

## Pre-installed plugins

Agent Client Collector Framework includes a set of pre-installed plugins that provide basic functionalities for common monitoring tasks, such as gathering standard metrics or monitoring key system parameters. For more detailed information on the plugins that come with the Agent Client Collector as part of ITOM AIOps, see [Plugins or applications installed with ITOM AIOps](../../it-operations-management/reference/plugin-app-itom-health.md).

**Parent Topic:**[Exploring Agent Client Collector Framework](exploring-agent-client-collector-framework.md)

