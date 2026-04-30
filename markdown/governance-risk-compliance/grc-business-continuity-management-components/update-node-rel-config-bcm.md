---
title: Update the node relationship configuration
description: Update the node relationship configuration for each main node configuration. You can select the sequence of the node configuration in the Node relationship configurations related list and update the source table, relationships such as relationship registry, relationship table, target table, target conditions, and so on.
locale: en-US
release: yokohama
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-04-12"
reading_time_minutes: 1
breadcrumb: [Data Relationships Framework, Reference, Business Continuity Management, Governance, Risk, and Compliance]
---

# Update the node relationship configuration

Update the node relationship configuration for each main node configuration. You can select the sequence of the node configuration in the Node relationship configurations related list and update the source table, relationships such as relationship registry, relationship table, target table, target conditions, and so on.

## Before you begin

Role required: sn\_bcm.admin

## Procedure

1.  Navigate to **All** &gt; **Data Relationships Framework** &gt; **Main node configurations**.

    The main node configurations are displayed.

2.  Choose the main node configuration for which you want to update the node relationship settings.

3.  Select the sequence number in the **Sequence** field.

    The Node relationship configuration displays the **Source**, **Relationship**, and **Target** tabs for the selected main node as shown in the example.

    The **Source** tab shows the source table, which is the input for the configuration.

    The **Relationship** tab displays the relationship table where the relationship is defined, and you can update the relationship registry here. It shows the relationship registry, the name of the registry, the relationship type \(such as one-to-one or scripted\), the relationship table \(like Location \[cmn\_location\]\), and the relationship conditions. The relationship conditions are pre-processing, meaning they are added to the query whenever the system runs it.

    The **Target** tab displays the target table you want to configure. It includes the target table, the target conditions you want to filter out, and the target reference field, which indicates where this reference is located. The target conditions are applied post-processing, meaning that any conditions you add to the target filters the results after the query is executed.

4.  Select **Update**.

    The node relationship configuration for the selected main node configuration is updated.


**Parent Topic:**[Data Relationships Framework](../../grc-common/concept/data-relationship-framework.md)

