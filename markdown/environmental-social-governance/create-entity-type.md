---
title: Create an entity type
description: Create an entity type for the entities in your system. Entity types enable you to find and create entities that have the same attributes and that match a set of filter conditions.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Manage entities in ESG Management, Configuring ESG Management, Environmental, Social, and Governance Management]
---

# Create an entity type

Create an entity type for the entities in your system. Entity types enable you to find and create entities that have the same attributes and that match a set of filter conditions.

## Before you begin

Role required: \(per product\)

-   In Environmental, Social, and Governance Management: sn\_esg.program\_manager
-   In GRC: Metrics: sn\_grc\_metric.manager
-   In Risk Management: sn\_risk\_workspace.IT\_risk\_manager and sn\_risk\_workspace.operational\_risk\_manager

## Procedure

1.  Navigate to **All** &gt; **Environmental, Social, and Governance** &gt; **ESG Workspace**.

2.  Under **Scoping**, select **Entity types** and click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the entity type.|
    |Active|Option to set the entity type as active.|
    |Compliance score \(%\)|Compliance score of the entity type. The value is a percentage. This field is automatically set.|
    |Description|Description of the entity type.|

4.  To save the entity type, click **Save**.

    **Note:** In the new entity type form, only the **Details** tab is displayed. After a new entity type is created, the **Details** tab and other related lists are displayed in the entity type form.

5.  To activate the entity type, do the following:

    1.  Click **Activate**.

        The following message displays: `Are you sure you want to activate this entity type?`

    2.  To activate the entity type, click **OK**.

6.  To delete the entity type, click **Delete**.


## Result

The entity type is created. The new entity type form is displayed with the **Details** tab and the related lists:

-   Entities
-   Risk Frameworks
-   Risk Statements
-   Policies
-   Control Objectives
-   Entity Filters
-   Policy exceptions
-   Content References

**Note:** Some related lists appear in the entity type form only when certain applications are installed. For example, the Risk Frameworks and Risk Statements related lists appear only when the Risk Management application is installed. The Policies, Control Objectives, and Policy exceptions related lists appear only when the Policy and Compliance Management application is installed.

## What to do next

You can also [update an entity type](update-entity-type.md).

**Parent Topic:**[Manage entities in ESG Management](../concept/entities-in-esg.md)

