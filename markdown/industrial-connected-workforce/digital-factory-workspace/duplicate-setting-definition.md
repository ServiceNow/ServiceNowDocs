---
title: Duplicate a setting definition
description: Create an independent copy of an existing setting definition to reuse its configuration without re-entering all values.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/industrial-connected-workforce/digital-factory-workspace/duplicate-setting-definition.html
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: task
last_updated: "2026-10-02"
reading_time_minutes: 1
breadcrumb: [Industrial Centerlines, Configure, Digital Factory Workspace, Industrial Connected Workforce]
---

# Duplicate a setting definition

Create an independent copy of an existing setting definition to reuse its configuration without re-entering all values.

## Before you begin

Role required: Industrial Centerlines config \[sn\_icw\_ctl.config\] or Industrial Centerlines admin \[sn\_icw\_ctl.admin\]

## About this task

When you need to create multiple setting definitions with similar configurations, duplicate an existing definition. Duplicating an existing definition takes less time than creating each one individually. After duplicating, update the values in each copy as needed.

## Procedure

1.  Navigate to the equipment record and select the **Settings** tab.

2.  Select the setting definition to duplicate.

    You can select multiple setting definitions to duplicate them at the same time.

3.  Select **Duplicate**.


## Result

A copy of the setting definition is created. The name of the duplicate is prefixed with **Duplicate** to distinguish it from the original.

## What to do next

**Note:**

Duplicating a setting definition creates a new, independent definition. It is not a new version of the original, because the version number resets to 1 and no association with the previous definition is retained. To create a new version, use the versioning workflow instead.

There is no state restriction for duplicating. Setting definitions in any state can be duplicated.

**Parent Topic:**[Configuring Industrial Centerlines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/industrial-connected-workforce/digital-factory-workspace/configuring-industrial-centerlines.md)

