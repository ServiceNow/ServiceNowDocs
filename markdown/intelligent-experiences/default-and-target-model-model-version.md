---
title: Default and target model version
description: Model version is the large language model version a skill uses to route requests to process users' queries. Default model version is where all the requests route to by default. This is pre-set by ServiceNow. A target model version is chosen to route your requests to a different version at run-time, rather than using the default version.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-01-28"
reading_time_minutes: 1
breadcrumb: [Now Assist reference, Now Assist, Enable AI experiences]
---

# Default and target model version

Model version is the large language model version a skill uses to route requests to process users' queries. Default model version is where all the requests route to by default. This is pre-set by ServiceNow®. A target model version is chosen to route your requests to a different version at run-time, rather than using the default version.

## Updating the target model version at the instance level

**Note:** A model version will not be available for selection as target model version, if it is in deprecated, retired, in review or rejected state.

A default mapping of default and target model version is pre-configured. If you update the target model version for a selected default model version, all the associated skills with this version mapping at the current instance level, get impacted.

![Updating target model version at the instance level](../image/version-management-instance-ref.png)

## Updating the target model version at the skill level

If you update the target model version for a selected default model version at the skill level, the mapping is updated for that skill only. Customizing the model version for skills overrides the instance-level model version currently assigned to each provider. This action is typically reserved for specific situations.

**Parent Topic:**[Now Assist reference](now-assist-reference-landing.md)

