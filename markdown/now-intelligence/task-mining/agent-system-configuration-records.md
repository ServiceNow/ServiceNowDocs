---
title: Agent configuration records in Task Mining
description: Agent configuration records manage the behavior of the workstation agent.
locale: en-US
release: yokohama
product: Task Mining
classification: task-mining
topic_type: reference
last_updated: "2025-04-22"
reading_time_minutes: 1
breadcrumb: [Reference, Task Mining, Platform Analytics]
---

# Agent configuration records in Task Mining

Agent configuration records manage the behavior of the workstation agent.

For information about agent configuration, see [Adjust Task Mining agent parameters](../task/set-system-parameters.md).

|Record|Description|Default value|
|------|-----------|-------------|
|Agent config update frequency|Determines how often a workstation agent checks for configuration updates.|30|
|Agent default status|Determines the default agent status after the user signs in to their workstation.|standard|
|Agent event properties timeout|Determines the timeout for GUI object properties search in milliseconds.|none|
|Agent restart check frequency|Determines how often a workstation agent checks for restart in seconds.|30|
|Disabled collectors|Determines if any collectors are not enabled on the Windows agent, using a comma-separated list. Options include SAP, Java, and Excel.|none|
|Maximum value length|Determines the maximum length of the string that the system accepts while processing raw data.|1024|
|Private mode allowed|Determines whether the agent can be switched to the private mode.|true|
|Show systray icon|Determines whether the menu bar icon is shown.|true|

|Record|Description|Default value|
|------|-----------|-------------|
|Aggregation date range interval|Determines the length of the date range interval for user data aggregation. Value in days. If you're having trouble loading your categorization data, try lowering the value.|7|
|Categories excluded from dashboard|Determines the application categories that are not displayed in analyses.|Off, Break|
|Length of license period|Length of license period is used for reporting purposes on the number of active users.|180|
|License period start date|Date from which the number of active users is counted. The date affects the reporting of the number of licenses.|none|

**Parent Topic:**[Task Mining Reference](../concept/reference-task-mining.md)

