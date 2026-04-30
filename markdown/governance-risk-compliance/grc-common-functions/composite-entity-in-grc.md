---
title: Composite entity in Governance, Risk, and Compliance
description: Composite entity in Governance, Risk, and Compliance is a combination of two or more entities created from different entity classes. The Composite Entity Management application enables you to create multidimensional entities and manage them in a more granular level.
locale: en-US
release: xanadu
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Explore entities, Common GRC features, Governance, Risk, and Compliance]
---

# Composite entity in Governance, Risk, and Compliance

Composite entity in Governance, Risk, and Compliance is a combination of two or more entities created from different entity classes. The Composite Entity Management application enables you to create multidimensional entities and manage them in a more granular level.

## Overview of a composite entity

A composite entity is a multidimensional entity that consists of entities from different entity classes. In a single entity structure, you can only manage risk and compliance on individual entities, which limits visibility and control for complex organizations with multifaceted structures. Using the composite entity structure, you can define valid combinations by setting up relevant entity classes and then creating the composite entities. Composite entities integrate into existing workflows, enabling risk and compliance management with the same depth and flexibility as standalone entities. Composite entity enables you to assess and manage risks and compliance across a combination of multiple entities from different entity classes.

For example, consider an organization's Retail Banking division wants to evaluate its KYC \(Know Your Customer\) process within its UK operations. Creating a composite entity, “Retail Banking \| KYC \| UK,” enables stakeholders from KYC, the Retail Banking division, and the UK location to assess and monitor risks, compliance, and controls impacting each area. This approach enables for more granular and interconnected risk management, which is important for large organizations with multiple business lines and locations.

**Note:** Activate the `sn_grc_comp_ent` plugin to use the composite entity functionality.

## Benefits of composite entity

The following are the key benefits of a composite entity:

-   Manage risk and compliance workflows at multiple levels, combining different entity dimensions, such as Company \| Department \| Business Process for a clearer and more detailed assessment context.
-   Aggregate risk and compliance posture automatically across impacted entity hierarchies, and confirming accurate risk score roll-ups.
-   Add stakeholders with customizable roles relevant to composite entities, enabling effective team involvement in assessment projects.
-   Map relevant risks and controls to composite entities that can be used for the risk assessment project.

-   **[Create a composite entity](../task/create-composite-entity-ws.md)**  
Create multidimensional entities by combining two or more entities from different entity classes using the Composite Entity Management application. In Governance, Risk, and Compliance, entities can be people, processes, departments, applications, or objects.

**Parent Topic:**[Exploring the entities](../../grc-common/concept/exploring-the-entities.md)

**Related topics**  


[Create an entity class](../task/create-new-entity-class-ws.md)

[Create a composite entity](../task/create-composite-entity-ws.md)

