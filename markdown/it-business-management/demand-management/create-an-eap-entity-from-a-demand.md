---
title: Create an Enterprise Agile Planning \(EAP\) entity from a demand
description: Create an Enterprise Agile Planning \(EAP\) entity, such as an epic, feature, or capability, from a demand so that you can start to work on these entities in Enterprise Agile Planning.
locale: en-US
release: zurich
product: Demand Management
classification: demand-management
topic_type: task
last_updated: "2025-11-13"
reading_time_minutes: 2
breadcrumb: [Create an artifact from a demand, Create a demand, Use, Demand Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Create an Enterprise Agile Planning \(EAP\) entity from a demand

Create an Enterprise Agile Planning \(EAP\) entity, such as an epic, feature, or capability, from a demand so that you can start to work on these entities in Enterprise Agile Planning.

## Before you begin

The [Strategic Planning](../../alignment-planner-workspace/concept/alignment-planner-workspace-landing-page.md) application must be installed.

Role required: sn\_apw\_advanced.eap\_user

**Note:** A demand manager requires the sn\_apw\_advanced.eap\_user role to convert a demand to an EAP entity.

## Procedure

1.  Navigate to **All** &gt; **Demand** &gt; **Demands** &gt; **All**.

2.  Open the demand that you want to convert into an artifact.

3.  Set the demand category and type for EAP entities.

    1.  From the Category list, select **Strategic**.

    2.  From the Type list, select **EAP Epic**, **EAP Feature**, or **EAP Capability**.

4.  In the EAP Details section, select the team that you want the EAP entity to be assigned to in the **Team** field.

    This field becomes read-only once the entity is created.

5.  Save the demand by selecting **Save**.

6.  Create an entity that will be associated with this demand by selecting the appropriate related link.

    **Note:** The related links aren’t available once the demand is converted to the selected entity.

    The available related links are:

    -   Create EAP Epic
    -   Create EAP Feature
    -   Create EAP Capability

## Result

The EAP entity is created successfully and the demand is moved to the Completed state. A message with a link to the created entity in Strategic Planning Workspace that enables you to immediately view or work on the entity is displayed.

For information about the data migrated from the demand to the EAP entity, see [Data migrated from demands to Enterprise Agile Planning \(EAP\) entities](../reference/data-copied-from-demands-to-eap-entities.md).

## What to do next

View and work on the new entity in Strategic Planning Workspace right away by selecting the link to the entity in the message that is displayed when the entity creation is successful.

**Note:** To access the entity at a later time, in the demand form, select the entity name in the **Converted to** field in the EAP Details section.

For more information, see [Strategic Planning](../../alignment-planner-workspace/concept/alignment-planner-workspace-landing-page.md) and [Enterprise Agile Planning in Strategic Planning](../../spw-eap/concept/eap-landing.md).

**Parent Topic:**[Create an artifact from a demand](t_CrtArtftDmdMnu.md)

