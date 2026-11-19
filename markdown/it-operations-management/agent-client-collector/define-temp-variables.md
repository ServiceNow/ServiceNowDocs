---
title: Define temporary variables for a pattern allowlist
description: Define temporary variables by assigning values such as executable paths, config file paths, and so forth. Defining temporary variables ensures that runtime commands are successful.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-operations-management/agent-client-collector/define-temp-variables.html
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-12-07"
reading_time_minutes: 1
breadcrumb: [Generate a Pattern allowlist, Enabling Agent Client Collector data collection, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Define temporary variables for a pattern allowlist

Define temporary variables by assigning values such as executable paths, config file paths, and so forth. Defining temporary variables ensures that runtime commands are successful.

## About this task

If a Linux command executable relies on an undefined temporary variable, the command fails at runtime.

For example, for the command `$pathToCmd "/log/acc.log"`, if a value is not defined for `$pathToCmd`, the command will fail.

## Before you begin

Role required: agent\_client\_collector\_admin

## Procedure

1.  Navigate to **All** &gt; **Pattern Designer** &gt; **Pattern Allowlist Temporary Variables**.

2.  Select **New** to create a new variable.

3.  Create a record and define the temporary variable.

    For example:

    |Field|Value|
    |-----|-----|
    |Value|bin/sh/testexec|
    |Pattern|.NET Application|
    |Operating system|Linux|
    |Temporary variable|exePath|

4.  Select **Submit**.


**Parent Topic:**[Generate a Pattern allowlist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/agent-client-collector/generate-patterns-allow-list.md)

