---
title: Agent Client Collector plugins
description: An Agent Client Collector plugin is a script or group of scripts which provides additional agent capabilities. For example, collecting more metrics, performing more checks, or generating events when an application queue size is 60% or 80% full.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Exploring Agent Client Collector Framework, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector plugins

An Agent Client Collector plugin is a script or group of scripts which provides additional agent capabilities. For example, collecting more metrics, performing more checks, or generating events when an application queue size is 60% or 80% full.

You associate a check with a plugin by creating a dependency between the check and the plugin. A plugin can have a dependency with several checks at a time; similarly, checks can depend on several plugins at a time. Plugins run on the same agent as the check.

For details on the plugins installed with Agent Client Collector Framework, see [Plugins or applications installed with ITOM Health](../../it-operations-management/reference/plugin-app-itom-health.md).

You can create Agent Client Collector plugins, as needed. Plugins are formatted as tar.gz files and run together with their associated check.

