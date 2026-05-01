---
title: Granular roles and supported entities for responsibility framework
description: Starting with the Yokohama release, multiple module-level granular roles are introduced to simplify defining and configuring the responsibility framework. These new granular roles simplify tasks by removing the need to create custom access control lists \(ACLs\) on the target table when a responsibility ACL is already in place. This change promotes a more straightforward and declarative migration process.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-05-01"
reading_time_minutes: 1
breadcrumb: [Configure responsibility access, Configuring customer access management, User management, Set up your environment, Configure, Customer Service Management]
---

# Granular roles and supported entities for responsibility framework

Starting with the Yokohama release, multiple module-level granular roles are introduced to simplify defining and configuring the responsibility framework. These new granular roles simplify tasks by removing the need to create custom access control lists \(ACLs\) on the target table when a responsibility ACL is already in place. This change promotes a more straightforward and declarative migration process.

|Granular roles|Description|
|--------------|-----------|
|sn\_customerservice.cust\_data\_resp\_granular|Provides granular access to customer-related foundational entities \(including accounts, contacts, consumers, and households\) through the responsibility framework.|
|sn\_customerservice.case\_mgmt\_resp\_granular|Provides granular access to case and related entities through the responsibility framework.|
|sn\_install\_base.resp\_granular|Provides granular access to installed base items, sold products, and related entities through the responsibility framework.|
|sn\_customerservice.contract\_entitlement\_resp\_granular|Provides granular access to contracts, entitlements, and related entities through the responsibility framework.|

<table id="table_mc1_d4v_c2c"><thead><tr><th>

Feature Set

</th><th>

Granular Role

</th><th>

Supported Tables/Entities

</th></tr></thead><tbody><tr><td>

Customer Data

</td><td>

sn\_customerservice.cust\_data\_resp\_granular

</td><td>

-   Account \[customer\_account\]
-   Account Team Member \[sn\_customerservice\_team\_member\] 
-   Account Address \[account\_address\_relationship\]
-   Account Access \[sn\_csm\_account\_access\] 
-   Account Relationship \[account\_relationship\] 
-   Contact Relationship \[sn\_customerservice\_contact\_relationship\]
-   Contact \[customer\_contact\]
-   Consumer \[csm\_consumer\]
-   Account Consumer \[sn\_acct\_consumer\_account\_consumer\]
-   Consumer Profile Location \[sn\_csm\_consumer\_profile\_location\]
-   Escalation \[sn\_customerservice\_escalation\]
-   Location \[cmn\_location\]

</td></tr><tr><td>

Case Management

</td><td>

sn\_customerservice.case\_mgmt\_resp\_granular

</td><td>

-   Case \[sn\_customerservice\_case\]
-   Task \[sn\_customerservice\_task \]
-   Task SLA \[task\_sla \]
-   Escalation \[sn\_customerservice\_escalation\]
-   Work Order \[wm\_order\]

</td></tr><tr><td>

Install Base Management

</td><td>

sn\_install\_base.resp\_granular

</td><td>

-   Installed Product \[sn\_install\_base\_m2m\_installed\_product\]
-   Affected Install Base \[sn\_install\_base\_m2m\_affected\_install\_base\]
-   Install Base Item \[sn\_install\_base\_item\]
-   Sold Product Covered \[sn\_install\_base\_m2m\_contract\_sold\_product\]
-   Sold Product \[sn\_install\_base\_sold\_product\]
-   Install Base Related Party \[sn\_install\_base\_related\_party\]
-   Sold Product Related Party \[sn\_install\_base\_sold\_product\_related\_party\]
-   Asset Contact \[sn\_customerservice\_m2m\_asset\_contact\]
-   Asset \[alm\_asset\]

</td></tr><tr><td>

Contracts and Entitlements

</td><td>

sn\_customerservice.contract\_entitlement\_resp\_granular

</td><td>

-   Contract \[ast\_contract\]
-   Entitlement \[service\_entitlement\]

</td></tr></tbody>
</table>## System roles containing responsibility granular roles

<table id="table_pgp_kqv_c2c"><thead><tr><th>

System Roles

</th><th>

Granular Roles

</th></tr></thead><tbody><tr><td>

sn\_customerservice.relationship\_contributor

</td><td>

-   sn\_customerservice.cust\_data\_resp\_granular
-   sn\_install\_base.resp\_granular
-   sn\_customerservice.case\_mgmt\_resp\_granular

</td></tr><tr><td>

sn\_customerservice.relationship\_agent

</td><td>

-   sn\_customerservice.cust\_data\_resp\_granular
-   sn\_install\_base.resp\_granular
-   sn\_customerservice.case\_mgmt\_resp\_granular
-   sn\_customerservice.contract\_entitlement\_resp\_granular

</td></tr></tbody>
</table>