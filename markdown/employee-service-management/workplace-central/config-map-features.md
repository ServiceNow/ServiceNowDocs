---
title: Configure map features for kiosk
description: Configure map features such as actions and data visualization for the kiosk.
locale: en-US
release: australia
product: Workplace Central
classification: workplace-central
topic_type: task
last_updated: "2026-03-25"
reading_time_minutes: 2
breadcrumb: [Working with Kiosk Indoor Mapping, Use, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# Configure map features for kiosk

Configure map features such as actions and data visualization for the kiosk.

## Before you begin

Role required: sn\_wsd\_indoor\_map.admin and sn\_wsd\_central.workspace\_user

## Procedure

1.  Navigate to **All** &gt; **Workplace Central**.

    You can also open Workplace Central from the Employee Center by navigating to **Workspaces** &gt; **Workplace Central**.

2.  Select the Kiosk Indoor Mapping icon \(![Kiosk Indoor Mapping icon.](../images/kiosk-indoor-mapping-icon.png)\).

3.  On the Map Feature Configurations list, select **New**.

4.  On the form, fill in the fields.

<table id="table_y25_phq_rdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the feature configuration record.

</td></tr><tr><td>

Order

</td><td>

Order of the feature configuration on the kiosk.

</td></tr><tr><td>

Reservable Module

</td><td>

Browse and select the Kiosk Reservable module. For more information, see [Configure Reservable Module for kiosk reservation](../../workplace-services-kiosk/task/config-rsv-module-kiosk.md).

</td></tr><tr><td>

Space Reservation

</td><td>

Select the check box option to allow employees and guests to select a space on the map and make a reservation on the Kiosk Map. If this option is not selected, the option to select a **Reservable Module** for Kiosk is not displayed.After selecting the Reservable Module for a kiosk and enabling Space Reservation option, kiosk operators can bind a physical device to a kiosk. This allows visitors or guests to make a reservation on the Kiosk Map. For more information, see [Select a kiosk for a device](../../workplace-services-kiosk/concept/setting-up-kiosk-device.md#).

After a kiosk is assigned to a physical device, employees and guests can make reservations on a selected kiosk device. For more information, [Make workplace reservations on the kiosk](../../workplace-services-kiosk/task/rsv-space-kiosk-map.md).

</td></tr><tr><td>

Allowed actions

</td><td>

Actions that the user can perform on the kiosk. You can select multiple actions from the list.The **Raise a case** action is available if you have installed [Workplace Case Management](../../workplace-case-mgmt/concept/workplace-case-mgmt-feat.md).

</td></tr><tr><td>

Data visualization

</td><td>

Data visualization elements, such as neighborhoods and space filters, for the kiosk user. You can select multiple visualization options from the list.The available elements depend on the applications that you have installed in your instance. For example, **Occupancy data** is available only if you have installed [Workplace Connectors](../../workplace-connectors/concept/workplace-connectors-landing-page.md).

</td></tr></tbody>
</table>5.  Save the record.


## Result

The map configuration is saved as a record in the Indoor map kiosk module.

**Parent Topic:**[Working with Kiosk Indoor Mapping](../concept/working-kiosk-ind-map.md)

**Previous topic:**[Working with Kiosk Indoor Mapping](../concept/working-kiosk-ind-map.md)

**Next topic:**[Configure the kiosk position and map settings](config-kiosk-map.md)

