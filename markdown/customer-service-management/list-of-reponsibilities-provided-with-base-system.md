---
title: List of responsibilities provided with the base system
description: List of responsibilities that are provided with the base system.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Create a responsibility definition, Configuring customer access management, User management, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# List of responsibilities provided with the base system

List of responsibilities that are provided with the base system.

<table id="table_pqm_gkg_b2c"><thead><tr><th>

Responsibility

</th><th>

Plugin

</th><th>

Used in Relationship

</th><th>

Role Required

</th><th>

Supported through responsibility access configuration

</th></tr></thead><tbody><tr><td>

Account Manager

</td><td>

Customer Service Base Extension Entities \[com.snc.cs\_base\_extension\]

</td><td>

Account Team Member \[sn\_customerservice\_team\_member\]

</td><td>

-   Relationship Agent \[sn\_customerservice.relationship\_agent\]
-   Relationship Contributor \[sn\_customerservice.relationship\_contributor\]

</td><td>

Yes**Note:**

Responsibility access configurations are currently inactive in Yokohama.

</td></tr><tr><td>

Relationship Manager

</td><td>

Customer Service Base Extension Entities \[com.snc.cs\_base\_extension\]

</td><td>

-   Consumer Team Member \[sn\_customer\_rel\_consumer\_to\_user\]
-   Household Team Member \[sn\_customer\_rel\_household\_to\_user\]

</td><td>

-   Relationship Agent \[sn\_customerservice.relationship\_agent\]
-   Relationship Contributor \[sn\_customerservice.relationship\_contributor\]

</td><td>

No

</td></tr><tr><td rowspan="2">

Authorized Account

</td><td rowspan="2">

Customer Service \[com.sn\_customerservice\]

</td><td>

Sold Product Related Party \[sn\_install\_base\_sold\_product\_related\_party\]

</td><td>

Sold Product Authorized Contact \[sn\_install\_base.sold\_product\_authorized\_contact\]

</td><td rowspan="2">

No

</td></tr><tr><td>

Install Base Related Party \[sn\_install\_base\_related\_party\]

</td><td>

Install Base Authorized Contact \[sn\_install\_base.install\_base\_authorized\_contact\]

</td></tr><tr><td rowspan="5">

Authorized Representative

</td><td rowspan="5">

Customer Service \[com.sn\_customerservice\]

</td><td>

Sold Product Related Party \[sn\_install\_base\_sold\_product\_related\_party\]

</td><td>

-   Sold Product Authorized Contact \[sn\_install\_base.sold\_product\_authorized\_contact\]
-   Sold Product Authorized Consumer \[sn\_install\_base.sold\_product\_authorized\_consumer\]

</td><td rowspan="5">

No

</td></tr><tr><td>

Install Base Related Party \[sn\_install\_base\_related\_party\]

</td><td>

-   Install Base Authorized Contact \[sn\_install\_base.install\_base\_authorized\_contact\]
-   Install Base Authorized Consumer \[sn\_install\_base.install\_base\_authorized\_consumer\]

</td></tr><tr><td>

Related Party \[sn\_customerservice\_related\_party\]

</td><td>

-   Case Authorized Contact \[sn\_customerservice.case\_authorized\_contact\]
-   Case Authorized Consumer \[sn\_customerservice.case\_authorized\_consumer\]
-   Case Authorized Contributor \[sn\_customerservice.case\_authorized\_contributor\]

</td></tr><tr><td>

Consumer to Consumer Relationship \[sn\_customer\_rel\_consumer\_to\_consumer\]

</td><td>

Consumer \[csm\_consumer\]

</td></tr><tr><td>

Household Member Relationship \[sn\_customer\_rel\_household\_member\_relationship\]

</td><td>

Consumer \[csm\_consumer\]

</td></tr><tr><td>

Preferred Technician

</td><td>

Customer Service \[com.sn\_customerservice\]

</td><td>

Account Team Member \[sn\_customerservice\_team\_member\]

</td><td>

N/A

</td><td>

No

</td></tr><tr><td>

Primary Support Agent

</td><td>

Customer Service \[com.sn\_customerservice\]

</td><td>

Account Team Member \[sn\_customerservice\_team\_member\]

</td><td>

N/A

</td><td>

No

</td></tr><tr><td>

Support Manager

</td><td>

Customer Service \[com.sn\_customerservice\]

</td><td>

Account Team Member \[sn\_customerservice\_team\_member\]

</td><td>

N/A

</td><td>

No

</td></tr><tr><td>

Asset Contact

</td><td>

Customer Service \[com.sn\_customerservice\]

</td><td>

Account Team Member \[sn\_customerservice\_team\_member\]

</td><td>

N/A

</td><td>

No

</td></tr><tr><td>

Authorized Service Organization

</td><td>

Customer Service Install Base Management \[com.snc.install\_base\]**Note:** You must install com.snc.service\_organization for activating com.snc.install\_base plugin.

</td><td>

Install Base Related Party \[sn\_install\_base\_related\_party\]

</td><td>

Install Base Authorized Member \[sn\_install\_base.install\_base\_authorized\_member\]

</td><td>

No

</td></tr><tr><td>

Location Relationship Manager

</td><td>

Business Location \[com.snc.business\_location\]

</td><td>

Service Organization Member Responsibility \[sn\_csm\_svc\_org\_member\_responsibility\]

</td><td>

Location Relationship Manager \[sn\_bus\_loc.location\_relationship\_manager\]

</td><td>

No

</td></tr><tr><td>

Location Contributor

</td><td>

Business Location \[com.snc.business\_location\]

</td><td>

Service Organization Member Responsibility \[sn\_csm\_svc\_org\_member\_responsibility\]

</td><td>

Service Organization Contributor \[sn\_customerservice.service\_organization\_contributor\]

</td><td>

No

</td></tr><tr><td>

Location Consumer Agent

</td><td>

Business Location \[com.snc.business\_location\]

</td><td>

Service Organization Member Responsibility \[sn\_csm\_svc\_org\_member\_responsibility\]

</td><td>

Location Consumer Agent \[sn\_customerservice.svc\_location\_consumer\_agent\]

</td><td>

No

</td></tr><tr><td>

Location Agent

</td><td>

Business Location \[com.snc.business\_location\]

</td><td>

Service Organization Member Responsibility \[sn\_csm\_svc\_org\_member\_responsibility\]

</td><td>

Location Agent \[sn\_customerservice.svc\_location\_agent\]

</td><td>

No

</td></tr><tr><td>

Location Manager Fulfiller

</td><td>

Business Location \[com.snc.business\_location\]

</td><td>

Service Organization Member Responsibility \[sn\_csm\_svc\_org\_member\_responsibility\]

</td><td>

Location Manager \[sn\_customerservice.svc\_location\_manager\]

</td><td>

No

</td></tr><tr><td>

Location Manager Contributor

</td><td>

Business Location \[com.snc.business\_location\]

</td><td>

Service Organization Member Responsibility \[sn\_csm\_svc\_org\_member\_responsibility\]

</td><td>

Location Manager Contributor \[sn\_customerservice.svc\_location\_manager\_contributor\]

</td><td>

No

</td></tr><tr><td>

Location Support Agent

</td><td>

Business Location \[com.snc.business\_location\]

</td><td>

Service Organization Member Responsibility \[sn\_csm\_svc\_org\_member\_responsibility\]

</td><td>

Location Support Agent \[sn\_bus\_loc.svc\_location\_support\_agent\]

</td><td>

No

</td></tr></tbody>
</table>