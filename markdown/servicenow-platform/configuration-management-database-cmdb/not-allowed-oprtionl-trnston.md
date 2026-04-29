---
title: Define a non-allowed operational transition
description: Define a restriction for CI Lifecycle Management in which a specified CI cannot transition from one operational state to another.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CMDB CI Lifecycle Management \(legacy\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Define a non-allowed operational transition

Define a restriction for CI Lifecycle Management in which a specified CI cannot transition from one operational state to another.

## Before you begin

Role required: none

## About this task

By default, CI Lifecycle Management has no restrictions for transitioning CIs from one operational state to another. You can restrict this behavior by defining transitions that are not allowed for a specified CI. For example, you can define a restriction on transitioning a Linux server from non-operational state to repair in progress state.

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CI Lifecycle Management** &gt; **Not Allowed Operational Transitions**.

2.  On the **Not Allowed Operational Transitions** page, click **New** and fill out the form.

    |Field|Description|
    |-----|-----------|
    |CI Type|The CI type for which the restriction applies.|
    |Not Allowed Transition|The CI state into which transitioning is restricted.|
    |Operational State|The operational state that the CI must be in for the restriction to apply.|


## Result

If an API attempts to transition a CI that is in the specified operational state to a state that is not allowed, the operation fails and an error is logged.

**Parent Topic:**[CMDB CI Lifecycle Management \(legacy\)](../concept/cmdb-ci-lifecycle-mgmt.md)

