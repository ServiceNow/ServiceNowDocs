---
title: Granular roles and entities for responsibility framework
description: Starting with the Yokohama release, module-level granular roles simplify defining and configuring the responsibility framework. The base system uses these roles in its table-level access control lists \(ACLs\) for the supported entities, so you can avoid creating custom table-level ACLs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/granular-roles-and-supported-entities-CAM.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Configure responsibility access, Configuring customer access management, User management, Set up your environment, Configure, Customer Service Management]
---

# Granular roles and entities for responsibility framework

Starting with the Yokohama release, module-level granular roles simplify defining and configuring the responsibility framework. The base system uses these roles in its table-level access control lists \(ACLs\) for the supported entities, so you can avoid creating custom table-level ACLs.

## Granular roles for access through entities

The granular roles provide Create, Read, and Update \(CRU\) access across entities, based on the access permissions defined for each responsibility within the declarative responsibility framework.

**Note:** You don't assign granular roles to users directly. Instead, you assign a functional role that's enabled for the responsibility framework, and that role contains the granular roles, so users inherit them through role containment. On its own, a granular role has no effect.

|Granular roles|Description|
|--------------|-----------|
|sn\_customerservice.cust\_data\_resp\_granular|Provides granular access to customer-related foundational entities \(including accounts, contacts, consumers, and households\) through the responsibility framework.|
|sn\_billing\_account.resp\_granular|Provides granular access to billing accounts and related entities through the responsibility framework.|
|sn\_customerservice.case\_mgmt\_resp\_granular|Provides granular access to case and related entities through the responsibility framework.|
|sn\_install\_base.resp\_granular|Provides granular access to installed base items, sold products, and related entities through the responsibility framework.|
|sn\_customerservice.contract\_entitlement\_resp\_granular|Provides granular access to contracts, entitlements, and related entities through the responsibility framework.|

## Granular roles and supported entities

Granular roles are designed based on feature sets and can be used to provide access to supported tables or entities though the responsibility framework.

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
-   Account Relationship \[account\_relationship\] 
-   Contact Relationship \[sn\_customerservice\_contact\_relationship\]
-   Contact \[customer\_contact\]
-   Consumer \[csm\_consumer\]
-   Consumer Profile Location \[sn\_csm\_consumer\_profile\_location\]
-   Escalation \[sn\_customerservice\_escalation\]
-   Location \[cmn\_location\]
-   Asset Contact \[sn\_customerservice\_m2m\_asset\_contact\]

</td></tr><tr><td>

Billing Account

</td><td>

sn\_billing\_account.resp\_granular

</td><td>

-   Location \[cmn\_location\]
-   Schedule \[cmn\_schedule\]
-   Schedule Entry \[cmn\_schedule\_span\]
-   Billing Account \[sn\_billing\_account\_billing\_account\]
-   Billing Account Address \[sn\_billing\_account\_address\]
-   Billing Account Payment Profile \[sn\_billing\_account\_payment\_profile\]
-   Billing Account Related Party \[sn\_billing\_account\_related\_party\]

</td></tr><tr><td>

Case Management

</td><td>

sn\_customerservice.case\_mgmt\_resp\_granular

</td><td>

-   Case \[sn\_customerservice\_case\]
-   Task \[sn\_customerservice\_task \]
-   Task service-level agreement \(SLA\) \[task\_sla \]
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
</table>**Note:** The granular roles include table-level ACLs in the base system. They don't include field-level ACLs. To provide access to specific fields, create field-level ACLs separately on the required roles.

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
</table>## How granular roles, functional roles, and query rules interact

In the responsibility framework, functional roles, granular roles, and query rules each control access in a different way:

-   **Functional role**

    The role assigned to the user. The responsibility framework uses it as the role condition on responsibility access configurations and on query rules. For example, `sn_customerservice.relationship_agent`.

-   **Granular role**

    The role inherited through the functional role that contains it. The base system uses it as the role condition on the table-level ACLs for a supported entity, such as `sn_customerservice.case_mgmt_resp_granular`. On its own, a granular role has no effect.

-   **Query rule**

    A performance mechanism that a functional role activates. A query rule narrows the set of records the platform evaluates ACLs against, so the platform doesn't evaluate ACLs against every record in a large table. For more information on query rules, see [CSM Query Rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/csm-query-rules.md).


The ACLs make the access decision. Table-level ACLs use the granular role as the role condition. Record-level ACLs also use the granular role and call the responsibility framework to check whether the user's relationship and responsibility grant access to a specific record.

For a user to see relationship-based records in a list or in the CSM workspace, all of the following must be in place:

-   A responsibility access configuration and a responsibility definition.
-   An account team member record that links the user to the account.
-   The functional role that activates the query rule, such as `sn_customerservice.relationship_agent`, or a custom query rule scoped to the user's functional role.

**Note:** If the user doesn't hold the functional role that activates the query rule, the platform may skip the query rule and the list returns no records. To give a custom role visibility to a relationship-based list, create a query rule scoped to that role.

