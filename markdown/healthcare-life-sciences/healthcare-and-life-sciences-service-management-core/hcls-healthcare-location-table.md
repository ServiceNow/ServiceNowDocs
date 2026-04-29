---
title: Healthcare location table
description: The Healthcare Location \[sn\_hcls\_location\] table provides the ability to map common locations to Healthcare Organizations.
locale: en-US
release: australia
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data model tables, Reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Healthcare location table

The Healthcare Location \[sn\_hcls\_location\] table provides the ability to map common locations to Healthcare Organizations.

## Key features

-   Models locations of different physical types including a site, a hospital building, a research lab, a parking lot, or a patient’s home.
-   Enables a location to include multiple locations.
-   Related lists for procedures, care specialities, and conditions are shown for records created via the Codeset location \[sn\_hcls\_codeset\_location\] table.
-   Maps with devices via the Medical device install base item \[sn\_hcls\_medical\_device\_install\_base\_item\] table.
-   Maps with practitioners via the Practitioner location \[sn\_hcls\_practitioner\_facility\] table.
-   Contains the Location field, which references the common location \[cmn\_location\] table.
-   To associate healthcare locations with healthcare organizations, see [Associate healthcare locations with a healthcare organizations](../task/hcls-sm-associate-healthcare-locations-organization.md).

For more information on how healthcare locations and healthcare organizations function, see [Setting up healthcare locations and healthcare organizations](../concept/understanding-healthcare-locations-and-healthcare-organizations.md).

Role required to configure the table: sn\_hcls.admin.

For more information, see [Healthcare and Life Sciences data model](../concept/hcls-serv-mgmt-core-1.md).

<table id="table_ync_1ts_mpb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Altitude

</td><td>

Floating Point Number

</td><td>

Altitude of the absolute geographic location.

</td></tr><tr><td>

Description

</td><td>

String

</td><td>

More details about the location that could be displayed as further information to identify the location beyond its name.

</td></tr><tr><td>

Identifier

</td><td>

String

</td><td>

The unique identifier of the healthcare location.

</td></tr><tr><td>

Location

</td><td>

Reference

</td><td>

Physical location of this healthcare location.

 Entry selected here populates address fields.

 References the Common location \[cmn\_location\] table.

</td></tr><tr><td>

Name

</td><td>

String

</td><td>

Name to identify the healthcare location.

</td></tr><tr><td>

Number

</td><td>

String

</td><td>

ID number associated with the healthcare location record.

 This field is read-only.

</td></tr><tr><td>

Parent location

</td><td>

Reference

</td><td>

Sys\_id of the parent healthcare location associated with this healthcare location.

</td></tr><tr><td>

Physical type

</td><td>

Choice list

</td><td>

Physical form of the location.

</td></tr><tr><td>

Status

</td><td>

Choice list

</td><td>

Option to indicate whether the healthcare location is in use.

 The following statuses are available by default:

-   Active
-   Inactive
-   Suspended

</td></tr></tbody>
</table>**Parent Topic:**[Healthcare and Life Sciences data model tables](hcls-healthcare-data-tables.md)

