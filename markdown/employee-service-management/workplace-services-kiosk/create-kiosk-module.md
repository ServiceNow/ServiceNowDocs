---
title: Create a kiosk module
description: Create a kiosk module and module configurations to decide the flow and pages that must be displayed on a kiosk.
locale: en-US
release: zurich
product: Workplace Services Kiosk
classification: workplace-services-kiosk
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Workplace Services Kiosk, Workplace Service Delivery, Employee Service Management]
---

# Create a kiosk module

Create a kiosk module and module configurations to decide the flow and pages that must be displayed on a kiosk.

## Before you begin

**Note:**

-   The kiosk device automatically maintains the session before it times out. The session timeout value can be configured in the **glide.ui.session\_timeout** property.
-   The kiosk header contains the session refresh API; ensure that you do not remove or replace the kiosk theme or the kiosk header.

    For information about customizing the kiosk header, see [Customize the kiosk header](customize-kiosk-header.md).


Role required: sn\_wsd\_kiosk.admin

## Procedure

1.  Navigate to **All** &gt; **Kiosk management** &gt; **Kiosk modules**.

2.  On the Kiosk modules page, select **New**.

3.  On the form, fill in the fields.

<table id="table_gsf_tgf_qbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the kiosk module.

</td></tr><tr><td>

Title

</td><td>

Title of the kiosk module.

</td></tr><tr><td>

Entry point

</td><td>

Page displayed on the home screen of the module.For visitor check in, select **visitor\_check\_in**. For visitor check out, select **visitor\_check\_out**. For kiosk indoor mapping, select **kiosk\_indoor\_map**.

</td></tr></tbody>
</table>4.  Select **Submit**.

5.  On the Kiosk module configuration related list, select **New**.

6.  On the form, enter a **Name** and **Description** for the record, then fill in the fields.

<table id="table_avq_djf_qbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Module

</td><td>

Module that the configuration is linked to.

</td></tr><tr><td>

Configuration table

</td><td>

Table that contains the configuration flow for the kiosk.For example, for visitor check in, select the Kiosk Check-in Flow Configuration \[sn\_wsd\_visitor\_checkin\_flow\_configuration\] table.

For visitor check out, select the Kiosk Check-out Flow Configuration \[sn\_wsd\_visitor\_checkout\_flow\_configuration\] table.

For a kiosk indoor map, select the Kiosk indoor mapping feature configuration \[sn\_wsd\_indoor\_map\_feature\_configuration\] table.

</td></tr><tr><td>

Condition

</td><td>

Condition that selects the configuration flow from the configuration table.The condition must match only one configuration. For example, use the **sys\_id** value to ensure only one record matches the condition.

</td></tr><tr><td>

Requires Camera

</td><td>

Option to use the camera of the kiosk device.If this option is selected, the kiosk operator must provide camera permissions on the kiosk device.

Visitors can use the camera to scan QR codes or to take their picture.

**Note:** If a kiosk flow contains the QR code authentication or requires a visitor picture, this field is automatically enabled when you add the flows to the kiosk.

</td></tr></tbody>
</table>7.  Add Page parameters by entering the name and value of the parameter.

8.  Select **Submit**.


**Parent Topic:**[Configure Workplace Services Kiosk](../concept/configure-workplace-services-kiosk.md)

