---
title: Configure a module for kiosk indoor mapping
description: Create a module for the kiosk to decide the flow for the kiosk.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/workplace-central/config-kiosk-ind-map-module.html
release: zurich
product: Workplace Central
classification: workplace-central
topic_type: task
last_updated: "2026-03-25"
reading_time_minutes: 1
breadcrumb: [Working with Kiosk Indoor Mapping, Use, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# Configure a module for kiosk indoor mapping

Create a module for the kiosk to decide the flow for the kiosk.

## Before you begin

Role required: sn\_wsd\_kiosk.admin and sn\_wsd\_central.workspace\_user

## Procedure

1.  Navigate to **All** &gt; **Workplace Central**.

2.  Select the Kiosk Indoor Mapping icon \(\[Omitted image "kiosk-indoor-mapping-icon.png"\] Alt text: Kiosk Indoor Mapping icon.\).

3.  On the Kiosk Map Configurations list, select the record that you want to configure.

    For more information about creating a kiosk configuration, see [Create a kiosk configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-services-kiosk/create-kiosk-device-config.md).

    The **Map configuration** tab is open by default.

4.  Select the **Module configuration** tab.

5.  On the Kiosk modules list, select **New**.

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

Configuration record for the kiosk module.For more information about creating a module, see [Create a kiosk module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-services-kiosk/create-kiosk-module.md).

For more information about creating a map configuration, see [Configure map features for kiosk](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-central/config-map-features.md).

</td></tr><tr><td>

Active

</td><td>

Status of the kiosk module configuration.

</td></tr><tr><td>

Type

</td><td>

Type of color scheme you want to set for the kiosk module configuration.The type can be set to primary or secondary.

\[Omitted image "wsd-kiosk-page-type.png"\] Alt text: Homepage of a kiosk showing the primary and secondary module type.

</td></tr><tr><td>

Order

</td><td>

Order of preference of the kiosk module.

</td></tr></tbody>
</table>    **Note:**

    -   The kiosk device automatically maintains the session before it times out. The session timeout value can be configured in the **glide.ui.session\_timeout** property.
    -   The kiosk header contains the session refresh API; ensure that you do not remove or replace the kiosk theme or the kiosk header.

        For information about customizing the kiosk header, see [Customize the kiosk header](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-services-kiosk/customize-kiosk-header.md).

7.  Save the record.

    The Kiosk module is created and linked to the configuration.


**Parent Topic:**[Working with Kiosk Indoor Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-central/working-kiosk-ind-map.md)

**Previous topic:**[Configure the kiosk position and map settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-central/config-kiosk-map.md)

**Next topic:**[Manage Workplace Central](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-central/manage-workplace-central.md)

