---
title: Components installed with Opportunity Management
description: Several types of components are installed with activation of the Opportunity Management plugin, including user roles and tables.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Opportunity Management reference, Lead and opportunity management, Reference, Sales and Order Management]
---

# Components installed with Opportunity Management

Several types of components are installed with activation of the Opportunity Management plugin, including user roles and tables.

## Roles installed

<table id="table_nkn_5py_3hc"><thead><tr><th>

Role name

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

sn\_opty\_mgmt\_core.opportunity\_viewer

</td><td>

A granular role created to give read access to Opportunity and Opportunity Line Item.

</td><td>

-   sn\_csm\_pricing.pricelist\_viewer
-   sn\_prd\_pm.product\_catalog\_viewer
-   sn\_customerservice.customer\_data\_viewer
-   sn\_opty\_mgmt\_core.opportunity\_setup\_viewer

</td></tr><tr><td>

sn\_opty\_mgmt\_core.opportunity\_responsibility\_read\_granular

</td><td>

Provides granular read access to opportunity and its related entities through the responsibility framework.

</td><td>

None

</td></tr><tr><td>

sn\_opty\_mgmt\_core.opportunity\_admin

</td><td>

A granular role created to give CRUD access to Opportunity tables.

</td><td>

-   sn\_opty\_mgmt\_core.opportunity\_setup\_writer
-   sn\_opty\_mgmt\_core.opportunity\_writer
-   sn\_opty\_mgmt\_core.opportunity\_allocation\_writer

</td></tr><tr><td>

sn\_opty\_mgmt\_core.opportunity\_responsibility\_write\_granular

</td><td>

Provides granular access to opportunity and related entities through the responsibility framework.

</td><td>

sn\_opty\_mgmt\_core.opportunity\_responsibility\_read\_granular

</td></tr><tr><td>

sn\_opty\_mgmt\_core.opportunity\_setup\_viewer

</td><td>

Provides read-only access to the Sales cycle and Opportunity stage tables.

</td><td>

None

</td></tr><tr><td>

sn\_opty\_mgmt\_core.opportunity\_writer

</td><td>

A granular role created to give write access to Opportunity and Opportunity Line Item.

</td><td>

-   sn\_opty\_mgmt\_core.opportunity\_viewer
-   sn\_quote\_mgmt\_core.quote\_writer

</td></tr><tr><td>

sn\_opty\_mgmt\_core.opportunity\_contributor

</td><td>

Provides limited permissions to FSM/CSM agents to generate opportunities and view their progress across the sales life cycle.

</td><td>

-   sn\_prd\_pm.product\_catalog\_viewer
-   sn\_opty\_mgmt\_core.opportunity\_setup\_viewer
-   sn\_csm\_pricing.pricelist\_viewer
-   sn\_customerservice.customer\_data\_viewer

</td></tr><tr><td>

sn\_opty\_mgmt\_core.opportunity\_setup\_writer

</td><td>

Provides access to read, create, and write the Sales cycle and Opportunity stage tables.

</td><td>

sn\_opty\_mgmt\_core.opportunity\_setup\_viewer

</td></tr><tr><td>

sn\_opty\_mgmt\_core.opportunity\_allocation\_viewer

</td><td>

Provides granular access to view opportunity allocations.

</td><td>

None

</td></tr><tr><td>

sn\_opty\_mgmt\_core.opportunity\_allocation\_writer

</td><td>

Provides granular access to manage opportunity allocations.

</td><td>

sn\_opty\_mgmt\_core.opportunity\_allocation\_viewer

</td></tr><tr><td>

sn\_opty\_mgmt\_core.opportunity\_allocation\_responsibility\_read\_granular

</td><td>

Provides granular read access to opportunity allocations through the responsibility framework.

</td><td>

None

</td></tr><tr><td>

sn\_opty\_mgmt\_core.opportunity\_allocation\_responsibility\_write\_granular

</td><td>

Provides granular write access to opportunity allocations through the responsibility framework.

</td><td>

sn\_opty\_mgmt\_core.opportunity\_allocation\_responsibility\_read\_granular

</td></tr></tbody>
</table>## Tables installed

<table id="table_pf3_1kw_v3c"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Opportunitysn\_opty\_mgmt\_core\_opportunity

</td><td>

Potential sales deal with a customer account.

</td></tr><tr><td>

Opportunity Tasksn\_opty\_mgmt\_core\_opportunity\_task

</td><td>

Tasks associated with an opportunity, such as follow‑ups, reviews, or sales actions required to progress the opportunity through its stages.

</td></tr><tr><td>

Opportunity Line Itemsn\_opty\_mgmt\_core\_opportunity\_line\_item

</td><td>

Individual products or services included in an opportunity.

</td></tr><tr><td>

Opportunity Line Characteristicsn\_opty\_mgmt\_core\_opportunity\_line\_characteristic

</td><td>

Additional attributes or characteristics associated with an opportunity line item, such as product‑specific options, classifications, or dimensions required for pricing, reporting, or allocation logic.

</td></tr><tr><td>

Opportunity Needssn\_opty\_mgmt\_opportunity\_needs

</td><td>

Customer‑expressed business needs or requirements linked to an opportunity.

</td></tr><tr><td>

Opportunity Competitorsn\_opty\_mgmt\_core\_opportunity\_competitor

</td><td>

Competitors associated with an opportunity, enabling sales teams to record competitive presence, assess deal risk, and analyze win/loss patterns across opportunities.

</td></tr><tr><td>

Opportunity Team Membersn\_opty\_mgmt\_core\_opportunity\_team\_member

</td><td>

Users involved in working on an opportunity, along with their roles and responsibilities.

</td></tr><tr><td>

Opportunity Associated Contactsn\_opty\_mgmt\_core\_opportunity\_associated\_contact

</td><td>

Contacts related to an opportunity, such as decision‑makers, influencers, or stakeholders at the customer account.

</td></tr><tr><td>

Opportunity Stagesn\_opty\_mgmt\_core\_opportunity\_stage

</td><td>

The current phase of an opportunity within a sales cycle, such as Qualify, Develop, Propose, or Close.

</td></tr><tr><td>

Sales Cycle Typesn\_opty\_mgmt\_core\_sales\_cycle\_type

</td><td>

A category of sales motion for opportunities, such as New Customer, Renewal, or Upsell.

</td></tr><tr><td>

Sales Cycle Stagesn\_opty\_mgmt\_core\_sales\_cycle\_stage

</td><td>

A stage configuration within a specific sales cycle type.

</td></tr><tr><td>

Opportunity Related Partysn\_opty\_mgmt\_core\_opportunity\_related\_party

</td><td>

Non‑user entities related to an opportunity, such as partners, resellers, or external organizations.

</td></tr><tr><td>

Opportunity Related Channel Partnersn\_bus\_org\_opptym\_related\_business\_organization

</td><td>

Channel partners associated with an opportunity, such as distributors or resellers.

</td></tr><tr><td>

Opportunity Allocationsn\_opty\_mgmt\_core\_opportunity\_allocation

</td><td>

Transactional allocation records that represent how opportunity value is distributed across participants, such as team members, territories, or product groupings.

</td></tr><tr><td>

Opportunity Allocation Typesn\_opty\_mgmt\_core\_opportunity\_allocation\_type

</td><td>

Allocation configuration metadata, such as what entity is allocated \(opportunity or line item\), which numeric field is used, and whether allocations must total 100%.

</td></tr><tr><td>

Opportunity Allocation Dimensionsn\_opty\_mgmt\_core\_opportunity\_allocation\_dimension

</td><td>

Allocation values that are grouped or categorized, such as by territory or product family.

</td></tr></tbody>
</table>**Parent Topic:**[Opportunity Management reference](../concept/opportunity-management-reference.md)

