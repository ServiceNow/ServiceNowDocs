---
title: Create a facility model
description: Create a facility model in the Telecommunications Network Inventory application to define the physical characteristics data of the facility record according to the product manufacturer's recommendations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/create-facility-model.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create inventory models, Use, Telecommunications Network Inventory]
---

# Create a facility model

Create a facility model in the Telecommunications Network Inventory application to define the physical characteristics data of the facility record according to the product manufacturer's recommendations.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.telco\_inventory\_catalog\_manager

## About this task

When you create a facility model, it creates the model record in the facility model \[sn\_ent\_facility\_model\] table.

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(\[Omitted image "ni-workspace-list-icon.png"\] Alt text: List icon.\), and then go to **Inventory Models** &gt; **Facility Models**.

3.  Select **New**.

4.  On the **Details** tab, fill in the fields.

<table id="table_htp_wkd_wrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Name that appears for the facility model. The **glide.cmdb\_model.display\_name.shorten** system property controls how display names are generated for the equipment holder model.

</td></tr><tr><td>

Manufacturer

</td><td>

Name of the network asset's manufacturer. Select the search icon \(\[Omitted image "search.png"\] Alt text: Search icon.\) and select a manufacturer code. To learn more, see [Create manufacturer and vendor codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/add-company-designate-manufacturer-tni.md).

</td></tr><tr><td>

Name

</td><td>

Name of the facility model. The ServiceNow AI Platform uses this name to identify it in your network inventory.

</td></tr></tbody>
</table>5.  On the **Details** tab, fill in the General section.

    **Note:** To learn more about the fields, see [Inventory Model form - General](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/tni-model-form-general.md).

6.  On the **Details** tab, fill in the Information section.

    **Note:** To learn more about the fields, see [Inventory Model form - Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/tni-model-form-information.md).

7.  Select **Save**.


## Result

The related tabs appear on the form. You can view or modify the tabs information. To learn more about the related tabs, see [Inventory models additional tabs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/additional-tabs-of-inventory-models.md).

**Parent Topic:**[Create inventory models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/creating-your-inventory-models.md)

**Related topics**  


[Network inventory models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/using-inventory-models-tni.md)

