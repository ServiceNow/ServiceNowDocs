---
title: Add a CI relationship to CMDB Group CI Relations
description: Add a CMDB group CI relationship for a CI class to enable accurate alert group generation.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [CMDB based alert grouping, Alert grouping types, Alert grouping, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Add a CI relationship to CMDB Group CI Relations

Add a CMDB group CI relationship for a CI class to enable accurate alert group generation.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

Configure the **sa\_analytics.agg.query\_cmdb\_suggested\_relationship\_enabled** property to further enhance alert grouping by using suggested relationships. For more information on properties, see [CMDB alert grouping — properties and functionality](../reference/cmdb-alert-group-properties.md).

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Administration** &gt; **CMDB Group CI Relations**.

    1.  Click **New**.

        ![Form to create a new CMDB Group CI Relation.](../image/em-cmdb-ci-relationship.png)

    2.  Complete the form.

        |Field|Description|
        |-----|-----------|
        |Base class|The base class in the relationship serves as either the parent or the child, depending on the type of relationship established.|
        |Relationship|The type of relationship that defines how two or more entities are connected.|
        |Dependent class|The class that relies on another class in the relationship, serving as either the parent or the child depending on the relationship type.|

2.  Click **Submit**.


## CMDB Group CI relation

|Base Class|Relationship|Dependent/Target Class|
|----------|------------|----------------------|
|Oracle|Is Hosted On|Linux Server|
|Oracle|Is Hosted On|Solaris Server|

**Note:** The same parent class and relationship can appear more than once.

