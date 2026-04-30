---
title: Set up pillars, entity types, and generate entities
description: Create entity types and pillars from the Operational Resilience Workspace and generate the entities based on the setup in the Operational Resilience application.
locale: en-US
release: xanadu
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure, Operational Resilience, Governance, Risk, and Compliance]
---

# Set up pillars, entity types, and generate entities

Create entity types and pillars from the Operational Resilience Workspace and generate the entities based on the setup in the Operational Resilience application.

## Before you begin

Role required: sn\_oper\_res.manager

## About this task

**Note:** As an Operational Resilience administrator, you must perform the following tasks:

1.  Activate the necessary entity types.
2.  Activate the necessary entity filters.
3.  Create new or update the existing pillars and entity types.
4.  Generate entities based on the setup.

Operational Resilience managers can create or update the entity types, but they cannot delete the entity types. The entities can be manually added to the entity types or Operational Resilience managers can use the entity filters to create entities automatically. The entities are required for the relationships to be created when running the scheduled job.

If the  CMDB relationship changes, and there are entities on both sides of the CMDB relationship, the entity relationship is created on the  Operational Resilience side. However, if an entity relationship is created or deleted, these changes are not reflected in the  CMDB.

![Deletion of entities.](../image/deletion-of-ent-from-opres-cmdb.png)

**Note:** If the relationship changes in the CMDB, it creates the relationship into an entity hierarchy, but it does delete the old relationship in the entity hierarchy. You may have to delete the old relationship manually in the entity hierarchy.

## Procedure

1.  Navigate to **Operational Resilience Workspace** &gt; **Entity types \| Pillars** module.

    The entity types are displayed in the list view.

    ![Entity types.](../image/entity-types-module-in-ws.png)

    For services, use the Services \(OR\) entity type. For business services, use the Business Services entity type.

    **Note:**

    The Services \(OR\), Business Services, and Business Processes entity types are associated with the main CSDM pillars, which are used by the Opres with the CSDM header configuration. Therefore, you must not change the Services \(OR\), Business Services, and Business Processes entity types. You can only add, update, or delete the following entity types.

    1.  Application services
    2.  Data
    3.  Facilities
    4.  People
    5.  Suppliers
    6.  Technology
    ![Entity type false.](../image/ent-type-false.png)

2.  To create an entity type, select **New** in the Entity types view.

3.  To create an entity type, return to the Entity Types screen, and select **New**.

    ![New entity type.](../image/create-a-new-entity-type.png "New entity type")

    For information on the fields, see [Entity Type New record form](../reference/entity-type-reference.md).

4.  To create a pillar from the Operational Resilience application, select **New** in the Pillars view.

    **Note:** The main CSDM pillars \(used by Opres with the CSDM header in the Main node configuration\) and the supplementary pillars are shown in the following example. The main CSDM pillars are Services, Business Services, Service Offering, and Process. The supporting pillars are Application Service, People, Data, Suppliers, Technology, and Facilities.

    ![Pillars.](../image/pillars-main-suppl.png)

    If you delete an existing pillar and add a pillar, you must update the pillars property manually in the **Value** field.

    ![Pillars.](../image/dep-pillars-change-value.png)

5.  To create a pillar, select **New**.

    The GRC Choice record is shown in the example.

    For information on the fields, see [GRC Choices form](../reference/pillars-reference.md).

    ![Sample configuration form for creating a new pillar.](../image/new-pillar.png "GRC Choice record for creating a pillar")

    **Note:** You can create entity types and pillars, then generate entities from either the Workspace view or the Core UI \(UI16\) view. Once the entity types, pillars, and entities are set up, complete the remaining required administrative tasks as outlined in [Completing general administrative tasks](../concept/admin-module-tasks.md), and then proceed to set up the Main node configurations.


## What to do next

To complete the remaining required administrative tasks, refer to the other sections in [Completing general administrative tasks](../concept/admin-module-tasks.md).

For information on setting up the Main node configurations, see [Main node configurations: A component of the Data Relationships Framework](../concept/main-node-relationship-fw.md).

