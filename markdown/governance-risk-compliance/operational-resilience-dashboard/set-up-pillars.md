---
title: Configure the pillars
description: Configure the pillar using the Core UI \(UI16\) view in the Operational Resilience application. You can then define the core areas relevant to your business entity.
locale: en-US
release: yokohama
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Set up pillars, entity types, and generate entities, Configure, Operational Resilience, Governance, Risk, and Compliance]
---

# Configure the pillars

Configure the pillar using the Core UI \(UI16\) view in the Operational Resilience application. You can then define the core areas relevant to your business entity.

## Before you begin

Role required: sn\_oper\_res.admin

## About this task

**Note:** If you have set up the entity types and pillars from the Workspace view in the earlier step \([Set up pillars, entity types, and generate entities](manage-entity-types-pillars-from-ws.md)\), you can ignore this step and proceed to [Main node configurations: A component of the Data Relationships Framework](../concept/main-node-relationship-fw.md).

The Operational Resilience base system includes the pre-defined pillars such as Technology, Facilities, People, Services, Processes, and Suppliers. You can create a pillar or use the pre-defined pillar for your business requirement.

The following pillars are now added in the tables: Application Service, Service Offering, Business Services, and Data.

For the pillars to function, entity types are used to create the necessary entities.

## Procedure

1.  Navigate to **All** &gt; **Operational Resilience** &gt; **Admin** &gt; **Pillars**.

    The following example shows the pillars in the base system. For each of the pillars, a default entity type is included in the base system. For example, the Technology pillar has the Technology entity type pre-selected.

    ![Pillars in the base system.](../image/pillars.png "Pillars in the base system")

    Beginning with Release 20.0.x, the following entity types have been added in the tables:

    -   Application Service
    -   Service Offering
    -   Business Services
    -   Data
2.  To create a pillar, select **New**.

    ![Sample configuration form for creating a new pillar.](../image/new-pillar.png "GRC Choice record for creating a pillar")

    Beginning with Release 21.x.x, the \[sn\_grc\_choice\] table includes an **Active** field. The pillars are shipped in an inactive state by default. You must activate the pillars from the list view before activating the entity types, as the entity types depend on the pillars. Activation of entity types can only occur after pillar activation.

3.  On the form, fill in the fields.

    For a description of the field values, see [GRC Choices form](../reference/pillars-reference.md).

4.  Select **Submit**.


