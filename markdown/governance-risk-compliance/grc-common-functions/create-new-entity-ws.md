---
title: Create an entity
description: Create an entity for your enterprise. In Governance, Risk, and Compliance, entities can be people, processes, departments, applications, or objects. These entities have controls that are defined to mitigate their exposure, and their audits must be completed.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Entities in workspace view, Explore entities, Common GRC features, Governance, Risk, and Compliance]
---

# Create an entity

Create an entity for your enterprise. In Governance, Risk, and Compliance, entities can be people, processes, departments, applications, or objects. These entities have controls that are defined to mitigate their exposure, and their audits must be completed.

## Before you begin

Roles required: sn\_grc.manager, sn\_risk\_workspace.IT\_risk\_manager, and sn\_risk\_workspace.operational\_risk\_manager

## About this task

An entity is an object for an action. The entities have controls to mitigate their risk exposure. Follow this procedure to create new entities for your organization and view the downstream hierarchy, entity types, policies, and so on, related to the entity.

## Procedure

1.  Navigate to the desired workspace, go to the List view, and click **Entities**.

2.  To create a new entity, click **New**.

3.  Navigate to the **Details** tab and fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Refers to existing record|Option that refers the new entity to an existing record.|
    |Name|Name of the entity.|
    |Active|Option that indicates whether the entity is active.|
    |Owned by|Details of the owner of the entity such as System administrator.|
    |Class|Name of the class associated with the entity such as Application or Business Entity.|
    |Location|Location record of the entity with details such as address, city, state, and country.|
    |Description|Description of the entity.|
    |Compliance|
    |Attestation frequency|Option for attestation frequency such as daily or weekly.|

4.  Under the Compliance section, add the attestation frequency such as **Weekly** or **Annually**.

5.  View attachments for the entity in the side panel.

6.  To save the entity, click **Save**.

    **Note:** When you create a new entity, only the **Details** tab is displayed. After the new entity is created, the **Overview** tab, **Details** tab, and other related lists are displayed.

    After saving the entity, a new entity form is displayed with the Details tab, Hierarchy tab, and the following related lists:

    -   Entity types
    -   Downstream risks
    -   Downstream controls
    -   Downstream engagements
    -   Downstream issues
    -   Downstream tasks
    -   Policy exceptions
    -   Privacy assessments
    -   CRI Tiering assessments
    -   CRI assessments
    For information on the fields in these related lists, see [An entity in the workspace view](../concept/entities-in-risk-ws.md).

7.  View the highlighted details side-panel for information such as the downstream hierarchy, entity types, and policies related to the entity.

8.  To save the updates to the entity, click **Save**.


**Parent Topic:**[An entity in the workspace view](../concept/entities-in-risk-ws.md)

