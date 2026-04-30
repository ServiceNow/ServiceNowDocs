---
title: Components installed with Workplace Services Kiosk
description: Several types of components are installed with activation of the Workplace Services Kiosk plugin, including tables, user roles, and business rules.
locale: en-US
release: yokohama
product: Workplace Services Kiosk
classification: workplace-services-kiosk
topic_type: reference
last_updated: "2025-12-09"
reading_time_minutes: 1
breadcrumb: [Reference, Workplace Services Kiosk, Workplace Service Delivery, Employee Service Management]
---

# Components installed with Workplace Services Kiosk

Several types of components are installed with activation of the Workplace Services Kiosk plugin, including tables, user roles, and business rules.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

## Roles

|Role|Description|Contains roles|
|----|-----------|--------------|
|sn\_wsd\_kiosk.admin|Has access to configure the kiosk features and experience.|None|
|sn\_wsd\_kiosk.operator|Has access to bind a kiosk configuration to a physical kiosk device.|None|
|sn\_wsd\_kiosk.viewer|Has access to view and use the kiosk experience.|sn\_wsd.core\_workplace\_user. Workplace users can make reservations using the kiosk map. For more information, see [Make workplace reservations on the kiosk](../task/rsv-space-kiosk-map.md)|

## Tables

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Kiosk configuration\[sn\_wsd\_kiosk\_configuration\]

</td><td>

Stores information about the kiosk configurations created in the application.

</td></tr><tr><td>

Kiosk module configurations\[sn\_wsd\_kiosk\_device\_m2m\_module\_configuration\]

</td><td>

Stores information about the modules created for a kiosk configuration.

</td></tr><tr><td>

Kiosk homepage\[sn\_wsd\_kiosk\_home\_page\]

</td><td>

Stores information about the homepages that are created for kiosks.

</td></tr><tr><td>

Kiosk module\[sn\_wsd\_kiosk\_module\]

</td><td>

Stores information about the modules that are displayed on kiosk devices.

</td></tr><tr><td>

Kiosk module configuration\[sn\_wsd\_kiosk\_module\_configuration\]

</td><td>

Stores information about the configurations created for a kiosk module.

</td></tr><tr><td>

Kiosk Status\[sn\_wsd\_kiosk\_last\_alive\]

</td><td>

Stores information about the status of kiosk devices such as the date and time of the last activity on the kioskand the status of the camera permission.

</td></tr></tbody>
</table>## Properties

|Property|Description|
|--------|-----------|
|sn\_wsd\_kiosk.kiosk\_reset\_delay|Specifies the duration of inactivity before the kiosk resets to the home page.|
|sn\_wsd\_kiosk.kiosk\_heartbeat\_delay|Specifies the duration after which the kiosk pings the instance to update the **Kiosk Status** table.|

**Parent Topic:**[Workplace Services Kiosk reference](workplace-services-kiosk-reference.md)

