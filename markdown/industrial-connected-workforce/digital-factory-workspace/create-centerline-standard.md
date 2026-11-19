---
title: Create a centerline standard
description: Create a centerline standard to define which equipment settings operators confirm, and for which equipment and materials.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/industrial-connected-workforce/digital-factory-workspace/create-centerline-standard.html
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: task
last_updated: "2026-10-02"
reading_time_minutes: 1
breadcrumb: [Centerline standards, Industrial Centerlines, Use, Digital Factory Workspace, Industrial Connected Workforce]
---

# Create a centerline standard

Create a centerline standard to define which equipment settings operators confirm, and for which equipment and materials.

## Before you begin

Setting definitions must be created before you create the standard. For more information, see [Create a setting definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/industrial-connected-workforce/digital-factory-workspace/create-setting-definition.md).

Role required: sn\_icw\_cl.standard\_author

## Procedure

1.  Navigate to the Standards Hub in the Digital Factory Workspace.

2.  Select **New standard**.

3.  In the Create a new standard dialog, select **Centerlining**.

4.  Complete the general information fields for the standard.

5.  In the **Where** section, select the functional locations, equipment models, or equipment that the standard applies to.

6.  In the **Where** section, select the material classifications or material models that the standard covers.

    The materials that you select determine which materials operators can choose when they execute the task on mobile, and which setting specifications apply.

7.  In the **Centerline configuration** section, add conditions in the **Query** field to filter the setting definitions available for the standard.

    All conditions must be met for a setting definition to be available.

8.  In the **Setting definition** field, select the setting definitions that operators confirm.

    Only setting definitions that match the query are available to select.

9.  Select **Save**.


## Result

The centerline standard is saved in the Draft state and appears as a card in the Standards hub, where you can select **Edit** to update it.

## What to do next

Publish the standard so that centerline tasks can be generated from it. For more information about publishing and scheduling standards, see [Exploring Industrial Standards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/industrial-connected-workforce/digital-factory-workspace/industrial-standards-landing-page.md).

**Parent Topic:**[Centerline standards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/industrial-connected-workforce/digital-factory-workspace/icw-centerline-standards.md)

