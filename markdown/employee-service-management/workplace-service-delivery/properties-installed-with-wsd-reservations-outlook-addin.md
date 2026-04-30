---
title: Properties installed with Workplace Reservations for Microsoft Outlook Add-in
description: Customize the properties available with Workplace Reservations for Microsoft Outlook Add-in.
locale: en-US
release: zurich
product: Workplace Service Delivery
classification: workplace-service-delivery
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Workplace Reservations for Microsoft Outlook Add-in, Workplace Service Delivery, Employee Service Management]
---

# Properties installed with Workplace Reservations for Microsoft Outlook Add-in

Customize the properties available with Workplace Reservations for Microsoft Outlook Add-in.

These properties are available for Workplace Space Management.

**Note:** All of these properties are located in the System Properties \[sys\_properties\] table. To access the table, enter `sys_properties.list` in the navigation filter.

<table id="table_sv1_vzh_rpb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_wsd\_msaddin.default\_reservable\_module

</td><td>

This property enables you to specify the default reservable module make a reservation. The workplace items of the reservable module are displayed to make a reservation. Specify the sys\_id of the reservable module.-   Type: String
-   Default value: **c31241cedb7650106c731dcd13961917**

</td></tr><tr><td>

sn\_wsd\_msaddin.oauth.debug

</td><td>

This property enables logging of the debug information when using the Microsoft Outlook Add-in page.-   Type: String
-   Default value: **false**

</td></tr><tr><td>

sn\_wsd\_msaddin.resource\_exclude\_list

</td><td>

This property enables you to exclude a room if you do not want it to appear in the Microsoft Outlook Add-in page. Specify either the room name or the email id of the room. If you are specifying the room name, ensure that the name is same as configured in the Workplace Reservation Management application.-   Type: String
-   Default value: &lt;empty&gt;

</td></tr></tbody>
</table>**Parent Topic:**[Workplace Reservations for Microsoft Outlook Add-in references](../concept/workplace-rsv-for-outlook-addin-reference.md)

**Related topics**  


[Components installed with Workplace Reservations for Microsoft Outlook Add-in](components-installed-with-wsd-reservations-outlookaddin.md)

