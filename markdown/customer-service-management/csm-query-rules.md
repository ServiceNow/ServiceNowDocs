---
title: CSM Query Rules
description: Query rules are used to filter the records in CSM-related tables that are accessible by users with CSM roles. These filters, which are applied in query business rules and READ ACLs on CSM-related tables, are stored in a metadata table.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Customer Service Management reference, Customer Service Management]
---

# CSM Query Rules

Query rules are used to filter the records in CSM-related tables that are accessible by users with CSM roles. These filters, which are applied in query business rules and READ ACLs on CSM-related tables, are stored in a metadata table.

Starting with the London release, query rules and filters were defined in the CSQueryBRUtilOOBConstants script include. In the Quebec release, these filters have been moved to the Query Rule \(sn\_query\_rule\) table.

This change applies to Query business rules \(QBRs\) and read ACLs on CSM-related tables. Each data table that used QBRs prior to Quebec now has a new QBR that uses the new logic. Tables with read ACLs that used filters from the CSQueryBRUtilOOBConstants script include now have one more read ACL that uses the filters from the Query Rule table.

## Availability

The CSM query filters feature is active on zBoot instances. Existing customers must contact ServiceNow Customer Support to enable this feature.

## Query rules property

The **sn\_cs\_queryrules.use\_query\_rules** property determines whether to use the Query Rule table or the CSQueryBRUtilOOBConstants script include. This property is set to true for zBoot instances and false for upgraded instances.

-   If true, the instance uses rules and filters from the Query Rule table to determine read access to the CSM tables for the logged-in user.
-   If false, the instance uses rules and filters from the CSQueryBRUtilOOBConstants and its extensions to determine read access to the CSM tables for the logged-in user.

## Query Rule table

The Query Rule \(sn\_query\_rule\) table extends the sys\_metadata table and stores filters for the following tables:

-   Case \(sn\_customerservice\_case\)
-   Affected Install Bases \(sn\_install\_base\_m2m\_affected\_install\_base\)
-   Install Base Items \(sn\_install\_base\_item\)
-   Installed Products \(sn\_install\_base\_m2m\_installed\_product\)
-   Sold Products \(sn\_install\_base\_sold\_product\)
-   Order Case \(csm\_order\_case\)
-   Sold Product Covered \(sn\_install\_base\_m2m\_contract\_sold\_product\)
-   Orders \(csm\_order\)
-   Asset \(alm\_asset\)
-   Entitlement \(service\_entitlement\)
-   Account \(customer\_account\)
-   Work Order \(wm\_order\)
-   Contact \(customer\_contact\)
-   Contract \(ast\_contract\)

