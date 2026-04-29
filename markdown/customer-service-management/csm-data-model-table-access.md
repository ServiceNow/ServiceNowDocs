---
title: Service Model Foundation table access by role
description: The user roles that can access the Service Model Foundation tables.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Overview, Configure Service Model Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# Service Model Foundation table access by role

The user roles that can access the Service Model Foundation tables.

<table id="table_zj3_gj2_2mb"><thead><tr><th>

Table

</th><th>

Create

</th><th>

Read

</th><th>

Update

</th><th>

Delete

</th></tr></thead><tbody><tr><td>

Organization Core

 \[sn\_customer\_service\_organization\]

</td><td>

 

</td><td>

-   CSM manager
-   Customer agent
-   Consumer agent

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Business Organization

 \[sn\_csm\_business\_location\]

</td><td>

 

</td><td>

-   CSM manager
-   Customer agent
-   Consumer agent
-   Location manager
-   Location agent
-   Location consumer agent

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Internal Organization

 \[sn\_csm\_business\_location\_internal\]

</td><td>

 

</td><td>

-   CSM manager
-   Customer agent
-   Consumer agent
-   Location manager
-   Location agent
-   Location consumer agent
-   Location manager contributor
-   Service organization contributor

</td><td>

 

</td><td>

 

</td></tr><tr><td>

External Organization

 \[sn\_csm\_business\_location\_external\]

</td><td>

 

</td><td>

-   CSM manager
-   Customer agent
-   Consumer agent
-   Location manager contributor
-   Location relationship manager
-   Service organization contributor

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Service Organization Member\[sn\_csm\_service\_organization\_member\]

</td><td>

-   CSM manager
-   location managers \(for their hierarchy only\)

</td><td>

-   CSM manager
-   Customer agent
-   Consumer agent
-   Location managers \(for their hierarchy only\)
-   Location agents \(for their locations only\)
-   Location consumer agents \(their locations only\)

</td><td>

-   CSM manager
-   Location managers \(for their hierarchy only\)

</td><td>

-   CSM manager
-   Location managers \(for their hierarchy only\)

</td></tr><tr><td>

Household\[csm\_household\]

</td><td>

 

</td><td>

-   CSM manager
-   Consumer agent
-   Location manager
-   Location consumer agent
-   Relationship agents \(for households they have relationships with\)
-   Consumers \(for their households\)

</td><td>

CSM manager

</td><td>

 

</td></tr><tr><td>

Household Member\[csm\_household\_member\]

</td><td>

CSM manager

</td><td>

-   CSM manager
-   Consumer agent
-   Location manager
-   Location consumer agent
-   Relationship agents \(for households they have relationships with\)
-   Consumers \(for households where they’re head of household or for consumers that they represent\)

</td><td>

-   CSM manager
-   Relationship agents \(for households they have relationships with\)

</td><td>

 

</td></tr><tr><td>

Consumer to Consumer Relationship\[sn\_customer\_rel\_consumer\_to\_consumer\]

</td><td>

CSM manager

</td><td>

-   CSM manager
-   Consumer agent
-   Location manager
-   Location consumer agent

</td><td>

CSM manager

</td><td>

 

</td></tr><tr><td>

Household Member Relationship\[sn\_customer\_rel\_household\_member\_relationship\]

</td><td>

CSM manager

</td><td>

-   CSM manager
-   Consumer agent
-   Location manager
-   Location consumer agent

</td><td>

CSM manager

</td><td>

 

</td></tr><tr><td>

Account Team Member\[sn\_customerservice\_team\_member\]

</td><td>

-   CSM manager
-   Location manager

</td><td>

-   CSM manager
-   customer agent
-   Location manager
-   Location agents \(for their locations\)
-   Relationship agents \(for accounts that they have relationships with\)

</td><td>

-   CSM manager
-   Location manager

</td><td>

-   CSM manager
-   Location manager

</td></tr><tr><td>

Consumer Team Member\[sn\_customer\_rel\_consumer\_to\_user\]

</td><td>

-   CSM manager
-   Location manager

</td><td>

-   CSM manager
-   Consumer agent
-   Location manager
-   Location consumer agents \(for their locations\)
-   Relationship agents \(for consumers that they have relationships with\)

</td><td>

-   CSM manager
-   Location manager

</td><td>

-   CSM manager
-   Location manager

</td></tr><tr><td>

Household Team Member\[sn\_customer\_rel\_household\_to\_user\]

</td><td>

-   CSM manager
-   Location manager

</td><td>

-   CSM managers
-   Consumer agents
-   Location manager
-   Location consumer agents \(for their locations\)
-   Relationship agents \(for households that they have relationships with\)

</td><td>

-   CSM manager
-   Location manager

</td><td>

-   CSM manager
-   Location manager

</td></tr></tbody>
</table>