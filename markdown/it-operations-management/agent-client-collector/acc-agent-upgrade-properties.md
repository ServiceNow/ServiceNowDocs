---
title: Agent Client Collector upgrade properties
description: System properties that control Agent Client Collector upgrade behavior, including the target version, rate limits, retry logic, and timeouts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/agent-client-collector/acc-agent-upgrade-properties.html
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2026-05-28"
reading_time_minutes: 1
keywords: [ACC upgrade properties, sn\_agent auto\_upgrade, upgrade configuration]
breadcrumb: [Agent Client Collector Framework reference, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector upgrade properties

System properties that control Agent Client Collector upgrade behavior, including the target version, rate limits, retry logic, and timeouts.

## Selective upgrade properties

Set these properties before running any selective upgrade. Navigate to **All** &gt; **System Properties** &gt; **All Properties** and search for each property name.

|Property|Value|Description|
|--------|-----|-----------|
|**sn\_agent.auto\_upgrade.enabled**|`true`|Enables the upgrade feature. Set to **true** before running any upgrade, manual or scheduled.|
|**sn\_agent.agent\_upgrade\_version**|Target version, for example `5.0.1`|The version agents upgrade to. If empty, the system uses the current Agent Client Collector Framework application version. Must be a valid version number.|

## Optional properties

These properties have default values suitable for most environments. Adjust them only when your environment requires different rate limits or timeout thresholds.

|Property|Default|Description|
|--------|-------|-----------|
|**sn\_agent.auto\_upgrade.max\_upgrades\_per\_hour**|1000|Maximum agents upgraded per job run across all MID Servers. Lower this value for a more gradual rollout pace.|
|**sn\_agent.auto\_upgrade.max\_upgrades\_per\_handler\_per\_hour**|50|Maximum agents upgraded through a single MID Server per job run. Prevents overloading individual MID Servers.|
|**sn\_agent.auto\_upgrade.retry\_limit**|3|Number of times the system retries a failed upgrade before permanently skipping the agent. After an agent reaches this limit, reset the `failed_upgrade_attempts` field on the Agent Extended Info record to allow retries.|
|**sn\_agent.agent\_upgrade\_wait\_time**|30|Minutes the system waits for an agent to complete its upgrade before marking it as failed and transitioning the agent to **Warning** status.|
|**sn\_agent.upgrade.timeout\_minutes**|10|Minutes allowed for the initial upgrade validation check on the agent \(AgentVerification stage\).|
|**sn\_agent.min\_upgrade\_history\_per\_agent**|2|Number of upgrade history records retained per agent. Older records are automatically removed.|

## Property usage note

The **sn\_agent.agent\_upgrade\_version** property is specifically for overriding the upgrade target version. The **sn\_agent.agent\_version** property controls package download URLs, version display, and other system behaviors. Use **sn\_agent.agent\_upgrade\_version** when you want to target a specific version for upgrades without affecting other system behavior.

**Parent Topic:**[Agent Client Collector Framework reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/agent-client-collector-reference.md)

