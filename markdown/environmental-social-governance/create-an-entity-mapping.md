---
title: Create a record identifier in an entity
description: Create record identifiers with text for correctly mapping the entities. This activity saves time for the ESG program managers by not having to create new entities.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integrating Operational Sustainability Management \(formerly ESG\) with Watershed, Integrating Operational Sustainability Management \(formerly ESG\) with other applications, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Create a record identifier in an entity

Create record identifiers with text for correctly mapping the entities. This activity saves time for the ESG program managers by not having to create new entities.

## Before you begin

Role required: sn\_esg.program\_manager

## About this task

You can map the existing data in your system, such as an entity, an entity type, and the metric definition, with the data from the Watershed spreadsheets. If the format of the data is different in the spreadsheets, you can create mapping record identifiers. This procedure uses an entity with the entity class as Location as an example. For example, assume that you already have an entity titled Akaska, Japan in your system and the spreadsheet contains the entity name as Akaska, Minato, JP. In this case, you must enable the system to map Akaska, Minato, JP with Akaska, Japan. To do this task, you must create a record identifier to identify the entity in your system.

## Procedure

1.  Navigate to **All** &gt; **Operational Sustainability Management** &gt; **Scoping** &gt; **All Entities**.

2.  Search for and open the entity for which you want to add a record identifier.

3.  Select the Mapping related list.

4.  Select **New**.

5.  Copy the text that you want to map to the entity from the spreadsheet.

6.  In the **Record identifier** field, paste the text that you copied in the previous step.

7.  Select **Submit**.


## Result

The identifier is added to the entity. When the system detects the record identifier text during the importing of data, the record will be mapped to the correct entity.

**Parent Topic:**[Integrating Operational Sustainability Management \(formerly ESG\) with Watershed](../concept/integrate-esg-with-watershed.md)

