---
title: Create a kiosk configuration
description: Create a kiosk configuration, assign a homepage, and link a kiosk device module.
locale: en-US
release: yokohama
product: Workplace Services Kiosk
classification: workplace-services-kiosk
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure, Workplace Services Kiosk, Workplace Service Delivery, Employee Service Management]
---

# Create a kiosk configuration

Create a kiosk configuration, assign a homepage, and link a kiosk device module.

## Before you begin

**Note:**

-   The kiosk device automatically maintains the session before it times out. The session timeout value can be configured in the **glide.ui.session\_timeout** property.
-   The kiosk header contains the session refresh API; ensure that you do not remove or replace the kiosk theme or the kiosk header.

    For information about customizing the kiosk header, see [Customize the kiosk header](customize-kiosk-header.md).


Role required: sn\_wsd\_kiosk.admin

## Procedure

1.  Navigate to **All** &gt; **Kiosk management** &gt; **All Kiosks**.

    For Workplace Services Kiosk version 1.1.0 or earlier, navigate to **All** &gt; **Kiosk management** &gt; **Kiosk configurations**.

2.  On the Kiosk configurations list, select **New**.

3.  On the Kiosk configuration form, fill in the fields.

    For a description of the field values, see [Kiosk configuration form](../reference/kiosk-configuration-form.md).

4.  Select **Submit**.

5.  On the Kiosk module configurations related list, select **New**.

6.  On the form, fill in the fields.

<table id="kiosk-config-modules-form"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Kiosk configuration

</td><td>

Kiosk configuration that the module is linked to.

</td></tr><tr><td>

Module configuration

</td><td>

Configuration record for the kiosk module.For more information about creating a module, see [Create a kiosk module](create-kiosk-module.md).

For more information about creating a map configuration, see [Configure map features for kiosk](../../workplace-central/task/config-map-features.md).

</td></tr><tr><td>

Active

</td><td>

Status of the kiosk module configuration.

</td></tr><tr><td>

Type

</td><td>

Type of color scheme you want to set for the kiosk module configuration.The type can be set to primary or secondary.

![Homepage of a kiosk showing the primary and secondary module type.](../images/wsd-kiosk-page-type.png)

</td></tr><tr><td>

Order

</td><td>

Order of preference of the kiosk module.

</td></tr></tbody>
</table>    **Note:**

    -   The kiosk device automatically maintains the session before it times out. The session timeout value can be configured in the **glide.ui.session\_timeout** property.
    -   The kiosk header contains the session refresh API; ensure that you do not remove or replace the kiosk theme or the kiosk header.

        For information about customizing the kiosk header, see [Customize the kiosk header](customize-kiosk-header.md).

7.  Select **Submit**.


## Result

You have configured a kiosk configuration and linked it to a kiosk module.

**Parent Topic:**[Configure Workplace Services Kiosk](../concept/configure-workplace-services-kiosk.md)

