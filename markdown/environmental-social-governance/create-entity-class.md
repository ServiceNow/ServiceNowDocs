---
title: Create an entity class
description: Create an entity class that is to be associated with an entity. Define the parent class, root entity, and tier for an entity class.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage entities in Operational Sustainability Management \(formerly ESG Management\), Configure, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Create an entity class

Create an entity class that is to be associated with an entity. Define the parent class, root entity, and tier for an entity class.

## Before you begin

Role required: \(per product\)

-   In Operational Sustainability Management: sn\_esg.program\_manager
-   In GRC: Metrics: sn\_grc\_metric.manager
-   In Risk Management: sn\_risk\_workspace.IT\_risk\_manager and sn\_risk\_workspace.operational\_risk\_manager

## About this task

Entity classes are used to add conceptual information about an entity. Entity classes represent a collection of entities that have the same attributes such as Department, Business Unit, or Business Service. You can gather data about an entity based on its entity class.

## Procedure

1.  Navigate to **All** &gt; **Operational Sustainability Management** &gt; **Operational Sustainability Workspace** &gt; **Scoping** &gt; **Entity classes**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the entity class.|
    |Parent class|Parent class that is associated with the entity class, such as Company or Department.|
    |Is root|Condition to check if the new entity class has a root entity. Options are **True** or **False**.|
    |Tier|Tier for the new entity class, such as Application or Business.|

4.  To save the entity class, click **Save**.

    **Note:** In the New entity class form, only the **Details** tab is displayed. Only after an entity class is created, the **Details** tab, **Entities** related list, and **Child classes** related list are displayed in the entity class form.


## What to do next

[Update an entity class](update-entity-class.md)

**Parent Topic:**[Manage entities in Operational Sustainability Management \(formerly ESG Management\)](../concept/entities-in-esg.md)

