---
title: Create an internal lifecycle in the Hardware Asset Workspace
description: Create a custom \(internal\) lifecycle to explicitly specify lifecycle dates for a selected hardware or consumable model in the Hardware Asset Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/hardware-asset-management/create-internal-lifecycle-hardware-models.html
release: brazil
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [custom hardware lifecycle, custom consumable lifecycle, internal hardware lifecycle, internal consumable lifecycle]
breadcrumb: [Calculated lifecycle templates, Repair and maintenance, Use, Hardware Asset Management, IT Asset Management, Asset Management]
---

# Create an internal lifecycle in the Hardware Asset Workspace

Create a custom \(internal\) lifecycle to explicitly specify lifecycle dates for a selected hardware or consumable model in the Hardware Asset Workspace.

## Before you begin

Role required: asset

## About this task

Beyond approximated and calculated lifecycles, Hardware Asset Management supports custom \(internal\) lifecycle records. You can define a custom lifecycle phase for a hardware or consumable model. A custom \(internal\) lifecycle enables you to specify lifecycle dates that are specific to your organization or override existing Content Library data, to improve lifecycle coverage and accuracy. Each custom lifecycle record represents a single lifecycle phase and includes a manually defined phase start date.

## Procedure

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace** &gt; **Model management**.

2.  Open the create lifecycle form for the hardware model or consumable model record.

<table id="choicetable_z1b_lpx_jjc"><thead><tr><th align="left" id="d171310e95">

Option

</th><th align="left" id="d171310e98">

Description

</th></tr></thead><tbody><tr><td id="d171310e104">

**Open the __Hardware Model Lifecycles__ tab**

</td><td>

1.  Select the **Hardware models** tab in the Model management page.
2.  Select a hardware model record.
3.  Select the **Hardware Model Lifecycles** tab.
4.  Select **New**.

The Create New Hardware Model Lifecycle form is displayed.

</td></tr><tr><td id="d171310e142">

**Open the __Consumable Lifecycles__ tab**

</td><td>

1.  Select the **Consumable models** tab in the Model management page.
2.  Select a consumable model record.
3.  Select the **Consumable Model Lifecycles** tab.
4.  Select **New**.

The Create New Consumable Model Lifecycle form is displayed.

</td></tr></tbody>
</table>3.  On the form, fill in the fields.

    For field descriptions, see [Model lifecycle form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/model-lifecycle-fields.md).

4.  Select **Save**.


## Result

The custom lifecycle record is created and listed in the Hardware Model Lifecycle or Consumable Model Lifecycle related list. The **Source** field is automatically set to **Internal**.

**Parent Topic:**[Manage the lifecycle of hardware models with calculated lifecycle templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/manage-ham-lifecycle-temp.md)

**Related topics**  


[Model lifecycle form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/model-lifecycle-fields.md)

[Hardware model details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/hardware-model-fields.md)

[Consumable model fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/consumable-model-fields.md)

