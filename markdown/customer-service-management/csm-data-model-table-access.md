---
title: Service Model Foundation table access by role
description: The user roles that can access the Service Model Foundation tables.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Service Model Foundation overview, Configure Service Model Foundation, Data models, Set up your environment, Configuring Customer Service Management, Customer Service Management]
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

Service Organization\[sn\_customer\_service\_organization\]

</td><td>

 

</td><td>

-   CSM manager
-   Customer agent
-   Consumer agent

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Business Location\[sn\_csm\_business\_location\]

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

Internal Business Location\[sn\_csm\_business\_location\_internal\]

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

External Business Location\[sn\_csm\_business\_location\_external\]

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
-   location manager \(for their hierarchy only\)

</td><td>

-   CSM manager
-   Customer agent
-   Consumer agent
-   Location manager \(for their hierarchy only\)
-   Location agent \(for their locations only\)
-   Location consumer agent \(their locations only\)

</td><td>

-   CSM manager
-   Location manager \(for their hierarchy only\)

</td><td>

-   CSM manager
-   Location manager \(for their hierarchy only\)

</td></tr><tr><td>

Household\[csm\_household\]

</td><td>

 

</td><td>

-   CSM manager
-   Consumer agent
-   Location manager
-   Location consumer agent
-   Relationship agent \(for households they have relationships with\)
-   Consumer \(for their households\)

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
-   Relationship agent \(for households they have relationships with\)
-   Consumer \(for households where they are head of household or for consumers that they represent\)

</td><td>

-   CSM manager
-   Relationship agent \(for households they have relationships with\)

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
-   Location manager \(for their hierarchy\)

</td><td>

-   CSM manager
-   customer agent
-   Location manager \(for their hierarchy\)
-   Location agent \(for their locations\)
-   Relationship agent \(for accounts that they have relationships with\)

</td><td>

-   CSM manager
-   Location manager \(for their hierarchy\)

</td><td>

-   CSM manager
-   Location manager \(for their hierarchy\)

</td></tr><tr><td>

Consumer Team Member\[sn\_customer\_rel\_consumer\_to\_user\]

</td><td>

-   CSM manager
-   Location manager \(for their hierarchy\)

</td><td>

-   CSM manager
-   Consumer agent
-   Location manager \(for their hierarchy\)
-   Location consumer agent \(for their locations\)
-   Relationship agent \(for consumers that they have relationships with\)

</td><td>

-   CSM manager
-   Location manager \(for their hierarchy\)

</td><td>

-   CSM manager
-   Location manager \(for their hierarchy\)

</td></tr><tr><td>

Household Team Member\[sn\_customer\_rel\_household\_to\_user\]

</td><td>

-   CSM manager
-   Location manager \(for their hierarchy\)

</td><td>

-   CSM manager
-   Consumer agent
-   Location manager \(for their hierarchy\)
-   Location consumer agent \(for their locations\)
-   Relationship agent \(for households that they have relationships with\)

</td><td>

-   CSM manager
-   Location manager \(for their hierarchy\)

</td><td>

-   CSM manager
-   Location manager \(for their hierarchy\)

</td></tr></tbody>
</table>