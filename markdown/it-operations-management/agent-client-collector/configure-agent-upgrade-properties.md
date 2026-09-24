---
title: Configure Agent Client Collector upgrade properties
description: Set the system properties that control Agent Client Collector upgrade behavior, including the target version and rate limits for mass upgrades.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/agent-client-collector/configure-agent-upgrade-properties.html
release: brazil
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [ACC upgrade properties, auto-upgrade configuration, sn\_agent.auto\_upgrade.enabled]
breadcrumb: [Agent Client Collector upgrade overview, ACC deployment - servers, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Configure Agent Client Collector upgrade properties

Set the system properties that control Agent Client Collector upgrade behavior, including the target version and rate limits for mass upgrades.

## Before you begin

Role required: agent\_client\_collector\_admin

## About this task

Two properties are required before any upgrade can run. Additional optional properties let you control rate limits, retry behavior, and timeout thresholds.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  Set the required upgrade properties.

    |Property|Value|Description|
    |--------|-----|-----------|
    |**sn\_agent.auto\_upgrade.enabled**|`true`|Enables the upgrade feature. Set to **true** before running any upgrade, manual or scheduled.|
    |**sn\_agent.agent\_upgrade\_version**|Target version number, for example `5.0.1`|The version agents upgrade to. If left empty, the system uses the current Agent Client Collector Framework application version.|

3.  Set optional properties to adjust rate limits and timeout behavior.

    |Property|Default|Description|
    |--------|-------|-----------|
    |**sn\_agent.auto\_upgrade.max\_upgrades\_per\_hour**|1000|Maximum agents upgraded per job run. Lower this value for a more gradual rollout.|
    |**sn\_agent.auto\_upgrade.max\_upgrades\_per\_handler\_per\_hour**|50|Maximum agents upgraded through a single MID Server per job run. Prevents overloading individual MID Servers.|
    |**sn\_agent.auto\_upgrade.retry\_limit**|3|Number of times the system retries a failed upgrade before permanently skipping the agent.|
    |**sn\_agent.agent\_upgrade\_wait\_time**|30|Minutes the system waits for an agent to complete its upgrade before marking it as failed.|
    |**sn\_agent.upgrade.timeout\_minutes**|10|Minutes allowed for the initial upgrade validation check on the agent.|
    |**sn\_agent.min\_upgrade\_history\_per\_agent**|2|Number of upgrade history records kept per agent. Older records are automatically removed.|


**Parent Topic:**[Agent Client Collector upgrade overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/agent-client-collector/acc-agent-upgrade-overview.md)

