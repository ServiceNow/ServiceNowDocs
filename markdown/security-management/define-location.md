---
title: Define Location
description: Define a geographic location to provide more context to other SDOs.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Locations, IoC Repository, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Define Location

Define a geographic location to provide more context to other SDOs.

## Before you begin

Role required: sn\_ti.admin

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence** &gt; **IoC Repository** &gt; **Locations**.

2.  Click **New**.

3.  Complete the fields in the form as appropriate.

<table id="choicetable_sq4_yvf_wmb"><thead><tr><th align="left" id="d208301e84">

Field

</th><th align="left" id="d208301e87">

Description

</th></tr></thead><tbody><tr><td id="d208301e93">

**Name**

</td><td>

Enter a descriptive name to identify the location.

</td></tr><tr><td id="d208301e102">

**Street Address**

</td><td>

The street address that this location describes. This property includes all aspects or parts of the street address.

</td></tr><tr><td id="d208301e111">

**City**

</td><td>

The city that this location is in.

</td></tr><tr><td id="d208301e120">

**Postal Code**

</td><td>

The postal code that this location is in.

</td></tr><tr><td id="d208301e130">

**Region**

</td><td>

The region that this location is in.

</td></tr><tr><td id="d208301e139">

**Country**

</td><td>

The country that this location is in.

</td></tr><tr><td id="d208301e148">

**Latitude**

</td><td>

The latitude of the Location in decimal degrees. Positive numbers describe latitudes north of the equator, and negative numbers describe latitudes south of the equator. The value of this property must be from -90.0 through 90.0 respectively.

</td></tr><tr><td id="d208301e160">

**Longitude**

</td><td>

The longitude of the location in decimal degrees. Positive numbers describe longitudes east of the prime meridian and negative numbers describe longitudes west of the prime meridian. The value of this property must be from -180.0 through 180.0, inclusive.

</td></tr><tr><td id="d208301e172">

**Source**

</td><td>

Specifies the threat source from which this record is created.

</td></tr><tr><td id="d208301e181">

**Description**

</td><td>

A description that provides more details and context about the intrusion set, potentially including its purpose and its key characteristics.

</td></tr><tr><td id="d208301e191">

**Source ID**

</td><td>

Unique identifier for this object in the threat source.

</td></tr><tr><td id="d208301e200">

**Created Time in Source**

</td><td>

Specifies the time the object is created in the source.

</td></tr><tr><td id="d208301e209">

**Modified Time in Source**

</td><td>

Specifies the time the object is modified in the source.

</td></tr></tbody>
</table>4.  Click **Submit**.


## What to do next

Click any of the following related lists to view additional information about objects associated with the location.

<table id="table_xsp_trv_wmb"><thead><tr><th>

Related Links and Related Lists

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Show Relationships

</td><td>

Opens the STIX Visualizer where you can view the relationship of the STIX object.Show Relationships appears only when the object has an associated object.

</td></tr><tr><td>

External References

</td><td>

Lists external references which refer to non-STIX information. This property is used to provide one or more external object identifiers.

</td></tr><tr><td>

Attack Patterns

</td><td>

Lists the attack patterns that help categorize attacks that are associated with this object.

</td></tr><tr><td>

Campaigns

</td><td>

Lists campaigns associated with this object.

</td></tr><tr><td>

Identities

</td><td>

List of identities associated with this object.

</td></tr><tr><td>

Infrastructure

</td><td>

Lists systems, software services, and any associated physical or virtual resources that are associated with this object.

</td></tr><tr><td>

Intrusion Set

</td><td>

Lists a set of adversarial behaviors and resources with common properties associated with this object.

</td></tr><tr><td>

Malware

</td><td>

Lists malicious code associated with this object.

</td></tr><tr><td>

Threat Actors

</td><td>

Lists individuals, groups, or organizations who act with malicious intent associated with this object.

</td></tr><tr><td>

Tools

</td><td>

Lists legitimate software that is used by threat actors to perform attacks associated with this object.

</td></tr></tbody>
</table>**Parent Topic:**[Locations](../concept/threat-intelligence-locations.md)

