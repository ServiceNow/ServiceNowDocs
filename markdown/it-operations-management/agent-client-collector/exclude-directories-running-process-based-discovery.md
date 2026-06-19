---
title: Exclude directories from running process-based discovery
description: Exclude specific directories from running process-based discovery so that processes running from those locations aren't recorded or included in File-Based Discovery scans.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/agent-client-collector/exclude-directories-running-process-based-discovery.html
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-06-03"
reading_time_minutes: 1
keywords: [exclude directories, running process-based discovery, file-based discovery, FBD process path exclusions, process scan]
breadcrumb: [Running process-based discovery, Agent Client Collector File-Based Discovery, ACC deployment - endpoints, Agent Client Collector, IT Operations Management]
---

# Exclude directories from running process-based discovery

Exclude specific directories from running process-based discovery so that processes running from those locations aren't recorded or included in File-Based Discovery scans.

## Before you begin

Running process-based discovery must be enabled. For details, see [Enable running process-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/enable-running-process-based-discovery.md).

Role required: disco\_admin

## About this task

Some running processes have no Software Asset Management \(SAM\) value and only add noise to discovery output, such as security tooling or the agent's own processes. Use the FBD Process Path Exclusions \[sn\_acc\_vis\_content\_fbd\_proc\_path\_exclude\] table to prevent those directories from being recorded. A set of common exclusions is included in the base system.

## Procedure

1.  Navigate to the FBD Process Path Exclusions \[sn\_acc\_vis\_content\_fbd\_proc\_path\_exclude\] table.

2.  Select **New**.

3.  Complete the fields for the exclusion record.

    |Field|Description|
    |-----|-----------|
    |**Path**|Absolute directory prefix to exclude. Any process running from this directory or a subdirectory of it is ignored.|
    |**Platform**|Operating system the exclusion applies to: **Windows** or **Unix**. Unix covers Linux and macOS. There is no combined option; specify the platform explicitly.|
    |**Active**|When selected \(the default\), the exclusion is enforced. Clear this check box to disable the exclusion temporarily without deleting the record.|
    |**Description**|Optional notes describing the purpose of the exclusion.|

4.  Select **Submit**.


## Result

The exclusion is pushed to the relevant agents automatically. New collection cycles skip the excluded directories. Any previously collected paths that match the exclusion are removed during the next daily maintenance cycle.

