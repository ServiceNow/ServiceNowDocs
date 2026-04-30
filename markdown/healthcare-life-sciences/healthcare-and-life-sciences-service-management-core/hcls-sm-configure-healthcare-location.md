---
title: Create a healthcare location in Healthcare and Life Sciences Service Management Core
description: Create healthcare locations to designate the locations in which your care teams operate.
locale: en-US
release: yokohama
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Create a healthcare location in Healthcare and Life Sciences Service Management Core

Create healthcare locations to designate the locations in which your care teams operate.

## Before you begin

Role required: admin

## About this task

Healthcare locations are physical entities in which care operations take place.

The Healthcare Location \[sn\_hcls\_location\] table stores details of the location associated with your healthcare organization.

## Procedure

1.  Navigate to **All** &gt; **HCLS Service Management** &gt; **Organization data** &gt; **Healthcare location**.

2.  Select **New**.

3.  Fill in the following fields.

<table id="table_isz_btj_vcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to identify the healthcare location.

</td></tr><tr><td>

Physical type

</td><td>

Physical form of the location.

 The following types are available by default:

 -   Area

-   Bed

-   Building

-   Cabinet

-   Corridor

-   Jurisdiction

-   Level

-   Room

-   Road

-   Site

-   Vehicle

-   Wing

-   Ward

 For more information about the available physical types, see [location types](http://hl7.org/fhir/STU3/valueset-location-physical-type.html) defined in the FHIR specifications.

</td></tr><tr><td>

Parent location

</td><td>

The parent location of this healthcare location.

 Set your parent location to create a hierarchy of locations in which the current healthcare location is nested under that parent location.

 For more information, see Example - Organizing your healthcare locations.

</td></tr><tr><td>

Location

</td><td>

Physical location of this healthcare location.

 Entry selected here populates address fields.

 Value here references the Common Location \[cmn\_location\] table.

</td></tr><tr><td>

Latitude

</td><td>

Latitude of the absolute geographic location.

</td></tr><tr><td>

Longitude

</td><td>

Longitude of the absolute geographic location.

</td></tr><tr><td>

Altitude

</td><td>

Altitude of the absolute geographic location.

</td></tr><tr><td>

Status

</td><td>

Option to indicate whether the healthcare location is in use.

 The following statuses are available by default:

 -   Active

-   Inactive

-   Suspended

 For more information about the available statuses, see [location statuses](https://www.hl7.org/fhir/http:/hl7.org/fhir/STU3/valueset-location-status.html) defined in the FHIR specifications.

</td></tr><tr><td>

Street

</td><td>

Mailing street address of the physical location.

</td></tr><tr><td>

City

</td><td>

City in which the physical location is located.

</td></tr><tr><td>

State/Province

</td><td>

State or province in which the physical location is located.

</td></tr><tr><td>

Zip / Postal Code

</td><td>

ZIP or postal code for the physical location.

</td></tr><tr><td>

Phone

</td><td>

Phone number of the physical location.

</td></tr><tr><td>

Identifier

</td><td>

Unique identifier associated with this location.

</td></tr><tr><td>

Description

</td><td>

A description of this healthcare location.

</td></tr></tbody>
</table>4.  Select **Submit**.


