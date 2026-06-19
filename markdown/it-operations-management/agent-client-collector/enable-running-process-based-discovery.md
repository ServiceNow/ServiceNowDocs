---
title: Enable running process-based discovery
description: Enable running process-based discovery so that the Agent Client Collector for Visibility - Content agent detects software running from directories outside your configured File-Based Discovery scan paths.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/agent-client-collector/enable-running-process-based-discovery.html
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-06-03"
reading_time_minutes: 1
keywords: [enable running process-based discovery, file-based discovery, FBD, process scan, system property]
breadcrumb: [Running process-based discovery, Agent Client Collector File-Based Discovery, ACC deployment - endpoints, Agent Client Collector, IT Operations Management]
---

# Enable running process-based discovery

Enable running process-based discovery so that the Agent Client Collector for Visibility - Content agent detects software running from directories outside your configured File-Based Discovery scan paths.

## Before you begin

File-Based Discovery must be active on the configuration console.

The Agent Client Collector for Visibility - Content Windows agent must be deployed on the endpoints.

Role required: disco\_admin

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  Search for the **sn\_acc\_vis\_content.file\_discovery.fbd\_process\_scan\_enabled** property.

3.  Set the **Value** field to `true`.

    The default value is `false`. Setting this property to `true` activates the agent policy that collects process directories.

4.  Save the record.


## Result

The associated agent policy activates during the next agent synchronization. From that point, the host runs the FBD SAM Process Scan Policy and begins collecting process directories every five minutes. The next daily FBD scan includes the process-discovered directories in its SAM output.

**Note:** A directory is removed from discovery when its software is no longer present on disk. If the software runs again, it is rediscovered within 24 hours.

## What to do next

For Linux and macOS hosts, complete the privilege configuration to obtain full coverage across all users. For details, see [Platform coverage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/running-process-based-discovery-platform-coverage-properties.md).

To exclude specific directories from running process-based discovery, see [Exclude directories from running process-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/exclude-directories-running-process-based-discovery.md).

