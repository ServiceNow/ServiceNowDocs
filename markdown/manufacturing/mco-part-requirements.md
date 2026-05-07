---
title: Generate a part requirement
description: Capture all the part requirements at the campaign level.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Corrective actions, Related lists for my campaigns, Create a campaign, Recall management, Agent management, Use, Manufacturing Commercial Operations]
---

# Generate a part requirement

Capture all the part requirements at the campaign level.

## Before you begin

Role required: sn\_rcl\_claim\_mgmt.recall\_manager

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace** &gt; **Lists** &gt; **Recall Management** &gt; **My Campaigns** &gt; **Corrective Action**.

2.  Select the corresponding campaign record in which you want to generate the part requirements.

3.  Move the corrective action to **Ready for use**.

4.  Select the corrective action record to generate part requirements.

    If the Corrective action charges with **Type** is set to **Part** and the **Status** is set to **In Use**, then the following fields are automatically populated.

<table id="table_c4z_wrv_n3c"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Parts requirement number that is automatically generated. The number starts with RCPPR.

</td></tr><tr><td>

Part

</td><td>

Part name to be replaced.

</td></tr><tr><td>

Quantity required

</td><td>

Quantity of the item required. It is based on the number of assets, impacted asset on which the corrective action charges are applicable.

</td></tr><tr><td>

Unit of measure

</td><td>

Unit of measure. Available options are:-   Box
-   Bundle
-   Carton
-   Case
-   Days
-   Each
-   Kit
-   Month
-   Pack
-   Year


</td></tr></tbody>
</table>    **Note:** When corrective action status changes to Draft, part details in part requirements are reset to 0.


-   **[Create a part availability](mco-part-availability.md)**  
Track current part availability and expected availability dates for required parts.

**Parent Topic:**[Corrective actions](mco-corrective-actions.md)

