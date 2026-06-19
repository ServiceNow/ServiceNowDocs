---
title: Define temporary variables for a pattern allowlist
description: Define temporary variables by assigning values such as executable paths, config file paths, and so forth. If a Linux command contains a string that isn’t defined, the command fails when run.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/agent-client-collector/define-temp-variables.html
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-12-07"
reading_time_minutes: 1
breadcrumb: [Generate a Pattern allowlist, ACC deployment - endpoints, Agent Client Collector, IT Operations Management]
---

# Define temporary variables for a pattern allowlist

Define temporary variables by assigning values such as executable paths, config file paths, and so forth. If a Linux command contains a string that isn’t defined, the command fails when run.

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


