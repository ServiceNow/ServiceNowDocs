---
title: Create a healthcare location in Healthcare Operations Core
description: Create healthcare locations to designate the locations in which your care teams operate.
locale: en-US
release: yokohama
product: Care Team Operations
classification: care-team-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Healthcare Operations Core, Healthcare Operations Core, Healthcare Operations, Healthcare and Life Sciences]
---

# Create a healthcare location in Healthcare Operations Core

Create healthcare locations to designate the locations in which your care teams operate.

## About this task

A healthcare location represents a physical location that a healthcare organization has responsibility for and aligns with a common location.

A single healthcare location can also be associated to multiple healthcare organization when they have a shared responsibility.

The Healthcare Location \[sn\_hcls\_location\] table stores details of the location associated with your healthcare organization.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Healthcare Operations** &gt; **Healthcare locations** &gt; **All**.

2.  Select **New**.

3.  Fill in the following fields.

<table id="table_isz_btj_vcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Location

</td><td>

Physical location of this healthcare location.

This value must already exist to be selected.

 Entry selected here populates address fields.

</td></tr><tr><td>

Name

</td><td>

Name to identify the healthcare location.

</td></tr><tr><td>

Physical type

</td><td>

The type of location being created - for example, a building, ward, or bed.

 For more information about the available physical types, see [location types](http://hl7.org/fhir/STU3/valueset-location-physical-type.html) defined in the FHIR specifications.

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

</td></tr></tbody>
</table>4.  Select **Submit**.


