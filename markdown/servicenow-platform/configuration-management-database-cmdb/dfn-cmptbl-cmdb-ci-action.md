---
title: Define compatible CI actions
description: Allow a CMDB CI Lifecycle Management operation in which two specified CI actions can be applied simultaneously to a CI.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CMDB CI Lifecycle Management \(legacy\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Define compatible CI actions

Allow a CMDB CI Lifecycle Management operation in which two specified CI actions can be applied simultaneously to a CI.

## Before you begin

Role required: none

## About this task

By default, it is not allowed to apply more than a single action to a CI. You can change that behavior by defining pairs of CI actions as compatible and therefore these actions can be applied simultaneously to a CI. For example you can specify that Provisioning and Patching are compatible CI actions, which lets you apply both to a CI at the same time.

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **Compatible CI Actions**.

2.  On the **Compatible CI Actions** page click **New** and fill out the form.

    |Field|Description|
    |-----|-----------|
    |Action|First action in the compatibility actions pair.|
    |Compatible Action|Second action in the compatibility actions pair.|


## Result

An API can successfully apply the two specified actions simultaneously to a CI.

**Parent Topic:**[CMDB CI Lifecycle Management \(legacy\)](../concept/cmdb-ci-lifecycle-mgmt.md)

