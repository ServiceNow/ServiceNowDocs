---
title: Running process-based discovery platform coverage and properties
description: Platform coverage identifies which operating systems are supported and what privileges the agent needs for full coverage. The system property controls whether the feature is enabled or disabled.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/agent-client-collector/running-process-based-discovery-platform-coverage-properties.html
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2026-06-05"
reading_time_minutes: 1
keywords: [running process-based discovery, platform coverage, system property, file-based discovery, FBD, agent client collector]
breadcrumb: [Agent Client Collector for Visibility - Content reference, Agent Client Collector, IT Operations Management]
---

# Running process-based discovery platform coverage and properties

Platform coverage identifies which operating systems are supported and what privileges the agent needs for full coverage. The system property controls whether the feature is enabled or disabled.

## Platform coverage

Coverage depends on the privileges available to the agent on each operating system.

|Platform|Default coverage|Requirement for full coverage|
|--------|----------------|-----------------------------|
|Windows|Full coverage of all running processes.|The ACC service must run as the Local System account. Set the ACC service's **Log On As** to **Local System**.|
|Linux|Limited to processes owned by the agent service account.|The agent service account must have permission to query process information for processes owned by other users. The `servicenow` user must be able to run `osqueryi` without a password. For more information about `servicenow` user permissions for `osqueryi`, see [Configure ServiceNow sudoers file](https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-dex/config-sudoers-file.html).|
|macOS|Limited to processes owned by the agent service account.|The agent service account must have permission to query process information for processes owned by other users. The `_servicenow` user must be able to run `osqueryi` without a password. For more information about `_servicenow` user permissions for `osqueryi`, see [Configure ServiceNow sudoers file](https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-dex/config-sudoers-file.html).|

**Note:** On Linux and macOS, if the additional privilege is not granted, the feature still runs but discovers directories only for processes owned by the agent service account. The daily scan continues normally on your configured directories. No errors are raised.

## System property

The following property controls whether running process-based discovery is active. You can configure it from the System Properties page \(**All** &gt; **System Properties** &gt; **All Properties**\).

|Property|Default|Description|
|--------|-------|-----------|
|**sn\_acc\_vis\_content.file\_discovery.fbd\_process\_scan\_enabled**|`false`|Primary on/off control for running process-based discovery. When set to `true`, the agent policy that collects process directories is activated and the daily FBD scan includes process-discovered directories. When set to `false`, collection stops and the daily scan uses only your configured scan directories.|

