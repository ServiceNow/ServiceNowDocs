---
title: Define a not-allowed CI action
description: Define a restriction for CI Lifecycle Management in which a specified action is not allowed for a CI that is in a specified operational state.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CMDB CI Lifecycle Management \(legacy\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Define a not-allowed CI action

Define a restriction for CI Lifecycle Management in which a specified action is not allowed for a CI that is in a specified operational state.

## Before you begin

Role required: none

## About this task

By default, there are no restrictions in the CMDB CI Lifecycle Management on applying CI actions. You can restrict this behavior by not allowing a specified action to be applied to a CI when it is in a specified operational state. For example, you can define a restriction in which the provisioning action cannot be applied to a Linux Server that is in a non-operational state.

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CI Lifecycle Management** &gt; **Not Allowed CI Actions**.

2.  Click **New** on the **Not Allowed CI Actions** page, and fill out the form.

    |Field|Description|
    |-----|-----------|
    |Not Allowed Action|The action that is being restricted.|
    |CI Type|The CI type for which the restriction applies to. To apply a rule to all CIs, select Configuration Item.|
    |Operational State|The operational state that the CI must be at in order to apply the restriction.|

3.  Click **Submit**.


## Result

If an API attempts to apply the specified action to the specified CIs, while it is in the specified operational state, the operation fails and an error is logged.

**Parent Topic:**[CMDB CI Lifecycle Management \(legacy\)](../concept/cmdb-ci-lifecycle-mgmt.md)

