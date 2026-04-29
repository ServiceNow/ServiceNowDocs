---
title: Restore save as you go functionality
description: Restore save as you go functionality that was disabled in the Washington DC release.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Save as you go flows, Build flows, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Restore save as you go functionality

Restore save as you go functionality that was disabled in the Washington DC release.

## Before you begin

Role required: admin

## About this task

An earlier version of the save as you go feature was released and withdrawn from the Washington DC release. If you're upgrading from the Washington DC release, you might have manually turned off the save as you go features by setting a system property. The upgrade process can't automatically change this system property setting because it's current value is considered customer data.

## Procedure

1.  In the navigation filter, enter `sys_properties.list`.

    The entire list of properties in the System Properties \[sys\_properties\] table appears.

2.  Search for the property named `sn_flow_designer.save_as_you_go_enabled`.

3.  Change the **Value** from `false` to `true`.

4.  Select **Save**.

5.  Log out and log back into the instance.


## What to do next

Open Workflow Studio and verify that save as you go is working as expected.

**Parent Topic:**[Save as you go flows](../concept/save-as-you-go-flows.md)

