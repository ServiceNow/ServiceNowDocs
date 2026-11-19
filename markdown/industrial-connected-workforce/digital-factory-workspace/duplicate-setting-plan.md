---
title: Duplicate a setting plan
description: Duplicate a setting plan to create a copy with all field values carried over, so you can reuse its configuration without re-entering all values.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/industrial-connected-workforce/digital-factory-workspace/duplicate-setting-plan.html
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: task
last_updated: "2026-10-02"
reading_time_minutes: 1
breadcrumb: [Industrial Centerlines, Configure, Digital Factory Workspace, Industrial Connected Workforce]
---

# Duplicate a setting plan

Duplicate a setting plan to create a copy with all field values carried over, so you can reuse its configuration without re-entering all values.

## Before you begin

Role required: Industrial Centerlines config \[sn\_icw\_ctl.config\] or Industrial Centerlines admin \[sn\_icw\_ctl.admin\]

## About this task

Duplicate a setting plan when you need to create one based on an existing plan. Duplicating a plan copies all visible field values, so you can update only the fields that differ without re-entering all values.

## Procedure

1.  Navigate to the setting plan that you want to duplicate.

    You can duplicate a setting plan from the **Settings Plans** tab on the equipment record, or from within the setting plan form.

2.  Select **Duplicate**.


## Result

A copy of the setting plan is created and opens immediately. All visible field values are copied from the original, except for the approval, version, and state fields. The duplicate is created in the **Draft** state.

## What to do next

**Note:**

The duplicate must go through the approval workflow before it can be used in a centerline task.

Update the fields in the duplicate as needed, then submit it for approval.

**Parent Topic:**[Configuring Industrial Centerlines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/industrial-connected-workforce/digital-factory-workspace/configuring-industrial-centerlines.md)

