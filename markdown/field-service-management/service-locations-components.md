---
title: Field Service with Service Locations Support components
description: Components installed with activation of the Field Service with Service Locations Support \(com.snc.fsm\_service\_locations\) plugin.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Components installed with additional plugins, Reference, Field Service Management]
---

# Field Service with Service Locations Support components

Components installed with activation of the Field Service with Service Locations Support \(com.snc.fsm\_service\_locations\) plugin.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md).

Demo data is available for this feature.

## Roles installed

Field Service with Service Locations Support installs the role mentioned in the following table.

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Service Locations Write\[wm\_service\_location\_write\]

</td><td>

Provides access for creating a new service location address.

</td><td>

None

</td></tr></tbody>
</table>## UX Client Script Includes

Field Service with Service Locations Support installs the UX Client Script Includes mentioned in the following table.

|UX Client Script Include|Description|
|------------------------|-----------|
|ResponseHandlerServiceLocationSNC|Contains read-only script to set location for a work order from map interface.|
|ResponseHandlerServiceLocation|Contains script to set location for a work order from map interface. You can modify the script to customize the fields of location to suit the business preference and set the location more accurately. For more information, see [Customize fields for mapping location](../task/customize-fields-for-mapping-location.md).|

**Parent Topic:**[Components installed with additional plugins for Field Service Management](../reference/components-inst-additional-plugin.md)

