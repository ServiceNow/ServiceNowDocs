---
title: Create a setting specification
description: Create a setting specification to define the target values and limits for a setting definition within a setting plan.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/industrial-connected-workforce/digital-factory-workspace/create-setting-specification.html
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: task
last_updated: "2026-10-02"
reading_time_minutes: 1
breadcrumb: [Industrial Centerlines, Configure, Digital Factory Workspace, Industrial Connected Workforce]
---

# Create a setting specification

Create a setting specification to define the target values and limits for a setting definition within a setting plan.

## Before you begin

Role required: Industrial Centerlines config \[sn\_icw\_ctl.config\] or Industrial Centerlines admin \[sn\_icw\_ctl.admin\]

A setting definition must exist for the equipment before you can create a setting specification.

## About this task

Setting specifications define the actual standard values for a setting definition within a setting plan. The fields available on the form depend on the type of the associated setting definition. **Numeric range** shows limit fields and **Choice** shows a choice target field.

## Procedure

1.  Navigate to the setting plan record.

2.  Select the **Settings Specifications** related list.

3.  Select **New**.

4.  In the **Setting definition** field, select the setting definition for this specification.

    After you select a setting definition, the form updates to show the fields relevant to the type of the definition. If the definition type is **Choice**, a **Choice target** field appears. If the type is **Numeric range**, the limit level fields appear.

5.  Complete the value fields for the selected setting type.

    **Note:**

    For **Numeric range** specifications, at least one of **Upper specification** or **Lower specification** must be provided. **Upper warning**, **Lower warning**, and **Target** are optional.

6.  Select **Save**.


## Result

The setting specification is created and associated with the selected setting definition. It appears in the setting specifications list.

**Parent Topic:**[Configuring Industrial Centerlines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/industrial-connected-workforce/digital-factory-workspace/configuring-industrial-centerlines.md)

