---
title: Components installed with Scaled Change
description: Several components are installed with the Major Change \(com.sn\_major\_change\) plugin. These include system properties and a data retention rule for Child changes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/change-management/installed-with-scaled-change.html
release: brazil
product: Change Management
classification: change-management
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Scaled change, Configure, Change Management, IT Service Management]
---

# Components installed with Scaled Change

Several components are installed with the Major Change \(**com.sn\_major\_change**\) plugin. These include system properties and a data retention rule for Child changes.

## Scaled change properties

To view or edit them, enter `sys_properties.list` in the navigator text box and filter for **sn\_major\_change**.

**Note:** Activate the Major Change \(**com.sn\_major\_change**\) plugin to get these components. For more information, see [Activate a plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/t_ActivateAPlugin.md).

|Property|Description|Default value|
|--------|-----------|-------------|
|`sn_major_change.affected_ci_threshold`|Sets the maximum number of affected configuration items allowed on a Primary change before the threshold enforcement mode takes effect.|`2000`|
|`sn_major_change.threshold_enforcement_mode`|Determines the behavior when the affected configuration item count on a Primary change exceeds the value in `sn_major_change.affected_ci_threshold`. Set to `warning` to log the condition and still allow Child change generation, or `blocking` to log the condition and stop Child change generation.|`warning`|
|`sn_major_change.child_change_generation_batch_size`|Sets the maximum number of configuration items processed together in a single Child change generation batch.|`500`|

**Note:** If `sn_major_change.threshold_enforcement_mode` is missing or set to a value other than `warning` or `blocking`, the system falls back to `warning` mode.

The system logs the condition, whether the mode is `warning` or `blocking`.

## Data retention

The Major Change plugin installs the following data archive rule. For general information about data archiving, see [Activate Change Management - Data Archiving](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/activate-data-retention-archive-rule.md).

|Rule|Description|
|----|-----------|
|Archive Child Changes|Archives a Child change \(a Change Request \[**change\_request**\] record with the Primary change request field set\) six months after its Primary change's **Active** field is set to false.|

**Parent Topic:**[Scaled change](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/scaled-change-overview.md)

