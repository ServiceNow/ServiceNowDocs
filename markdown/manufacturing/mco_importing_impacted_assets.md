---
title: Importing impacted assets
description: Recall campaign management enables you to import the impacted assets.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-10-08"
reading_time_minutes: 1
breadcrumb: [Create a campaign, Recall management, Agent management, Use, Manufacturing Commercial Operations]
---

# Importing impacted assets

Recall campaign management enables you to import the impacted assets.

## Before you begin

Role required: sn\_rcl\_claim\_mgmt.recall\_manager

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace** &gt; **Lists** &gt; **Recall Management** &gt; **My Campaigns**.

2.  Choose the recall campaign record where you want to import the affected asset.

3.  Select **Import Impacted Assets**.

4.  On the form, fill in the fields.

<table id="table_ick_kgj_wfc"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Import set table

</td><td>

Select Existing table. Choose sn\_rcl\_claim\_mgmt\_impacted\_asset\_import table from the option.

</td></tr><tr><td>

Source of the import

</td><td>

Select the source of import from the option:-   File
-   Data source


</td></tr></tbody>
</table>5.  Select **File**.

6.  Select **Choose file**.

7.  Choose Import Impacted Assets Template.

    The template consists of Serial number and Recall campaign number.

    Serial numbers help manufacturers and dealers identify products, track assets, handle claims, and manage recalls or promotions throughout a product's life-cycle. For a vehicle, VIN \(Vehicle Identification number\) will be its serial number.

    If the install base item or the asset record is missing, the import process throws an error for that serial number.

8.  Select **Open**.

9.  Select **Submit**.

    The impacted assets data is uploaded.

10. Select **Run Transform**.

    **Note:** Transform job should be run. If it isn’t set to run automatically, perform manually.

11. Select **Transform**.

12. Select **Transform History**, to view logs.


