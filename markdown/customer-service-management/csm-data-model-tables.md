---
title: Service Model Foundation tables
description: Tables that are included with or modified by the plugins that enable the Service Model Foundation feature.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Service Model Foundation overview, Configure Service Model Foundation, Data models, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Service Model Foundation tables

Tables that are included with or modified by the plugins that enable the Service Model Foundation feature.

The Service Model Foundation feature adds new tables or modifies existing tables when you activate the following plugins:

-   Business Location \(com.snc.business\_location\)
-   Customer Service Household \(com.snc.household\)
-   Service Organization \(com.snc.service\_organization\)
-   Customer Service Base Extension Entities \(com.snc.cs\_base\_extension\)
-   Customer Service Install Base Management \(com.snc.install\_base\)

## Business Location plugin

The Business Location plugin adds the following tables.

<table id="table_u4f_d5c_2mb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Business Location\[sn\_csm\_business\_location\]

</td><td>

Extends the Service Organization \[sn\_customer\_service\_organization\] table.

 A business location is one type of service organization. This table stores business location records.

</td></tr><tr><td>

Internal Business Location\[sn\_csm\_business\_location\_internal\]

</td><td>

Extends the Business Location \[sn\_csm\_business\_location\] table.

 This table stores internal business location records.

**Note:** An internal business location is a business location with the **Internal** field set to **true**.

</td></tr><tr><td>

External Business Location\[sn\_csm\_business\_location\_external\]

</td><td>

Extends the Business Location \[sn\_csm\_business\_location\] table.

 This table stores external business location records.

**Note:** An external business location is a business location with the **Internal** field set to **false**.

</td></tr></tbody>
</table>## Customer Service Household plugin

The Customer Service Household plugin adds or modifies the following tables.

<table id="table_c21_rkd_llb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Household\[csm\_household\]

</td><td>

Stores consumer household records.

 For the Service Model Foundation feature, this table is updated to support the head of household.

</td></tr><tr><td>

Household Member\[csm\_household\_member\]

</td><td>

Stores records of the consumers who have been added to households.

</td></tr><tr><td>

Household Team Member\[sn\_customer\_rel\_household\_to\_user\]

</td><td>

Stores records for each of the household team member relationships that have been created between an internal user and a household.

</td></tr><tr><td>

Household Member Relationship\[sn\_customer\_rel\_household\_member\_relationship\]

</td><td>

Extends the Consumer to Consumer Relationship \[sn\_customer\_rel\_consumer\_to\_consumer\] table.

 This table stores records for each of the relationships that have been created between two consumers who belong to the same household.

</td></tr></tbody>
</table>## Service Organization plugin

The Service Organization plugin adds the following tables.

<table id="table_rp1_zrc_2mb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service Organization\[sn\_customer\_service\_organization\]

</td><td>

A unidirectional relationship between a company and a service organization, with a reference to the company record added from the service organization.

 Stores records for service organizations, including business locations and internal business locations.

 **Note:** The following new columns are replicated from the company \[core\_company\] table to the service organization \[sn\_customer\_service\_organization\] table:

-   Active: Track the operational status of the service organization.
-   Domain: Enable domain separation.
-   Company: Reference to the core\_company table.

</td></tr><tr><td>

Service Organization Member\[sn\_csm\_service\_organization\_member\]

</td><td>

Stores records for the users who belong to internal service organizations.

</td></tr><tr><td>

Service Organization External Staff\[sn\_csm\_service\_organization\_external\_staff\]

</td><td>

Extends the User \[sys\_user\] table.

 Stores records for the users who belong to external service organizations.

 **Note:** If the **Company** field is populated, the **Service Organization** field displays only those service organizations that are associated with the company record. Similarly, if the **Service Organization** field is populated, the **Company** field displays only those companies that are associated with the service organization.

</td></tr><tr><td>

Service Organization Member Responsibility\[sn\_csm\_svc\_org\_member\_responsibility\]

</td><td>

Configure the responsibilities of the staff working at service organizations or its extended entities.

</td></tr></tbody>
</table>## Customer Service Base Extension Entities plugin

The Customer Service Base Extension Entities plugin adds the following tables.

<table id="table_ylm_vld_llb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Consumer to Consumer Relationship\[sn\_customer\_rel\_consumer\_to\_consumer\]

</td><td>

Stores records for each of the relationships that have been created between two consumers, regardless of household.

</td></tr><tr><td>

Consumer Team Member\[sn\_customer\_rel\_consumer\_to\_user\]

</td><td>

Stores records for each of the consumer team member relationships that have been created between an internal user and a consumer.

</td></tr></tbody>
</table>## Customer Service Install Base Management plugin

The Customer Service Install Base Management plugin adds the Consumer Sold Product \[sn\_install\_base\_m2m\_consumer\_sold\_product\] table. This table stores records for each sold product \(products and components\) that have been sold to a consumer.

## Tables used by Service Model Foundation

Tables from existing plugins that are used by the Service Model Foundation feature to support customers.

<table id="table_rh2_cjw_gmb"><thead><tr><th>

Plugin

</th><th>

Table

</th><th>

New columns

</th></tr></thead><tbody><tr><td rowspan="4">

Customer Service \(com.sn\_customerservice\)

</td><td>

Responsibility Definition\[sn\_customerservice\_responsibility\]​

</td><td>

 

</td></tr><tr><td>

Account Team Member\[sn\_customerservice\_team\_member\]​

</td><td>

 

</td></tr><tr><td>

Related Party Configuration\[sn\_customerservice\_related\_party\_configuration\]

</td><td>

 

</td></tr><tr><td>

Case\[sn\_customersrevice\_case\]

</td><td>

​Household

 Service Organization​

 Consumer Profile

</td></tr><tr><td rowspan="2">

Customer Service Install Base Management \(com.snc.install\_base\)

</td><td>

Sold Product\[sn\_install\_base\_sold\_product​\]

</td><td>

Household

 Consumer Profile

</td></tr><tr><td>

Install Base Item\[sn\_install\_base\_item\]

</td><td>

Consumer Profile

</td></tr><tr><td>

Customer Service Management for Orders \(com.snc.csm.order\)

</td><td>

Order\[csm\_order\]​

</td><td>

Household​

 Service Organization​

</td></tr></tbody>
</table>