---
title: Temporary entity model
description: Use temporary ETL entities to avoid repetitive operations in target entities.
locale: en-US
release: xanadu
product: System Import Sets
classification: system-import-sets
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Extract Transform Load \(ETL\) definition overview, Robust Import Set Transformers, Import sets, Imports, Creating integrations with applications]
---

# Temporary entity model

Use temporary ETL entities to avoid repetitive operations in target entities.

In the temporary \(temp\) entity model, temporary entities serve as an intermediate between the input and target entities. Data is mapped from the input entity to the temp entity, then from the temp entity to the target entities. To use the temp entity model:

-   Create a temp entity, with entity fields similar to the ones in the input entity. For example, if the input entity has a field named Type, the temp entity might have a field named Temp Type.
-   Add an RTE entity mapping to map data from the input entity to the temp entity.
-   In the temp entity, add new entity fields and entity operations to support the values required to map the data to the target entities.
-   Add target entities and RTE entity mappings to map data from the temp entity to the target entities.

With this model, there's no need to define operations in the target entity. You create operations only in the temp entity, then map the final values to the target entities. ![An overview of the import process using an ETL definition with a temp entity.](../image/temp-entity-model.png)

## Teams ETL definition

In this example, the Teams ETL definition maps data from the input entity to a temp entity, then from the temp entity to the target entities. The Teams definition has four ETL entities.

-   Group: a target entity
-   Import Set: an input entity
-   Member: a target entity
-   Temp: the temporary, intermediate entity

![The Teams definition has four entities: Group, Import Set, Member, and Temp.](../image/temp-entity-example.png)

The Teams definition also has three RTE entity mappings.

-   Import Set to Temp, which maps data from the input entity to the temp entity.
-   Temp to Member, which maps data from the Temp entity to the Member target entity.
-   Temp to Group, which maps data from the Temp entity to the Group target entity.

![The Teams definition has three entity mappings: Import Set to Temp, Temp to Member, and Temp to Group.](../image/temp-entity-mapping.png)

## Conditional script

In some cases, you might not want to insert or update all the input data to a target table. You can use a conditional script to pick which import set rows to map to a target entity. In the following example, the Temp to Member RTE entity mapping uses a conditional script to specify which rows to map from the Temp entity to the Member entity. Only rows with a type of `member` are mapped to the Member entity. ![Conditional script specifying which rows to map from the Temp entity to the Member entity.](../image/temp-entity-conditional-script.png)

