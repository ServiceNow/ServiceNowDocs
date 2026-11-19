---
title: Create a setting definition
description: Define configurable parameters on operational equipment, including type, value format, and classification properties, to support centerline task configuration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/industrial-connected-workforce/digital-factory-workspace/create-setting-definition.html
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: task
last_updated: "2026-10-02"
reading_time_minutes: 1
breadcrumb: [Industrial Centerlines, Configure, Digital Factory Workspace, Industrial Connected Workforce]
---

# Create a setting definition

Define configurable parameters on operational equipment, including type, value format, and classification properties, to support centerline task configuration.

## Before you begin

You must select an equipment record before creating a setting definition. Setting definitions are created directly on equipment items.

Role required: Industrial Centerlines config \[sn\_icw\_ctl.config\] or Industrial Centerlines admin \[sn\_icw\_ctl.admin\]

## Procedure

1.  Navigate to the equipment record and select the **Settings** tab.

2.  Select **New**.

3.  In the **Setting type** field, select the type for this definition.

    The form displays different fields depending on the type you select. For **Choice**, a related list appears where you can define the available choices. For **Numeric range**, fields for the limit levels appear.

4.  Complete the remaining fields on the form.

    **Note:**

    The **Effective start** and **Effective end** fields define when the setting definition is valid. A warning appears if no effective date range is specified.

5.  Select **Save**.


## Result

The setting definition is created in **Draft** state and appears in the **Settings** tab of the equipment record.

## What to do next

A setting definition in **Draft** state requires approval before use in a centerline task. Select **Request approval** to submit it for review.

**Parent Topic:**[Configuring Industrial Centerlines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/industrial-connected-workforce/digital-factory-workspace/configuring-industrial-centerlines.md)

