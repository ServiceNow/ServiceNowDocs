---
title: Enable custom item types in Strategic Planning
description: Enable the usage of a custom planning item type in Strategic Planning so that your planning managers can start adding them to their free-form roadmaps or portfolio plans.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/scenario-planning-in-spw/enable-custom-item-types-strategic-planning-workspace.html
release: australia
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Planning item configuration for lenses and portfolio plans, Configure, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Enable custom item types in Strategic Planning

Enable the usage of a custom planning item type in Strategic Planning so that your planning managers can start adding them to their free-form roadmaps or portfolio plans.

## Before you begin

Role required: sn\_align\_core.apw\_admin

## About this task

Add the table that you want to allow for planning in Portfolio plans and free-form roadmaps to a system property.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  Open one of the following system properties.

    -   For portfolio plans: **sn\_align\_core.planning\_item\_types\_allow\_list**
    -   For free-form roadmaps: **sn\_align\_ws.freeform\_planning\_items\_creation\_list**
3.  In the **Value** field, add your custom table.

    For example, add **sn\_align\_core\_custom\_planning\_item\_1**.

    \[Omitted image "allow\_list.png"\] Alt text: Enable custom item types in Strategic Planning.

4.  Select **Update**.


## What to do next

-   For portfolio plans: Add your custom planning item type to the lens that your planning managers want to use. See [Lens form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scenario-planning-in-spw/lens-form-alignment-planner-workspace.md).
-   For free-form roadmaps: [Create planning items from the roadmap view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scenario-planning-in-spw/create-new-items-from-a-roadmap.md).

