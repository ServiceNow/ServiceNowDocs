---
title: Entity scoping in GRC
description: Entity scoping is permitted in each of the core GRC applications. Scoping provides a way to allocate risks and controls at different levels. Dependencies are created using the dependency map in the GRC Workbench.
locale: en-US
release: yokohama
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Explore entities, Common GRC features, Governance, Risk, and Compliance]
---

# Entity scoping in GRC

Entity scoping is permitted in each of the core GRC applications. Scoping provides a way to allocate risks and controls at different levels. Dependencies are created using the dependency map in the GRC Workbench.

## Entity scoping overview

**Note:** Starting with the New York release, the term profile was replaced with the term entity. See [Governance, Risk, and Compliance application nomenclature updates and industry terminology](../reference/grc-terms.md) for more information about all updated GRC application terms.

Organizations have various control owners maintaining individual files and spreadsheets for tracking the compliance of different systems, projects, organizations, etc. In this environment, risk managers cannot prevent or even be aware of the duplicate risks and controls created on shared entities. The entire purpose of entity scoping is to provide a top-down approach for maintaining your risk universe, which is the hierarchical library of both risks and controls. Mature organizations with a healthy risk posture find that most risks are standard and recurring. Entity scoping helps you catalog and visualize upstream and downstream risks and controls based on the roll up of the related entities.

![Legacy bottom-up approach to improved top-down system](../../grc-risk/image/entity-approach.png "From an organic approach to a structured system")

1.  Create or edit **Entity Types** and map them using the **Entity Filter** to existing ServiceNow® tables.
2.  Map these entity types to external regulations and internal policies using control objectives and risk statements.
3.  Generate risk and control instances on related entities.
4.  Maintain your risk appetite and scoring results by the aggregated calculation for entities; all combos for risk scores on risk roll up.

![image shows scoping process with old and new terms](../../grc-risk/image/scoping-process.png "Scoping process")

-   **[Generate risks and controls from entity types](../task/t_CreateProfileTypes.md)**  
Create and edit entity types and map them to existing ServiceNow® tables for which you must track compliance \(applications, departments, regions, processes, systems, etc.\). Entities are assigned to control objectives and risk statements, which generate controls and risks for every entity type.
-   **[Create independent entities](../task/create-a-profile.md)**  
Entities can be created manually, rather than generating them from the entity types. Entities can also be created without needing to refer to an existing ServiceNow® table, like assets, applications, business services, or processes.
-   **[Relate entities to each other](../task/relate-profiles-to-each-other.md)**  
Create relationships between entities to understand how controls and risks affect each other and how they affect the enterprise.

**Parent Topic:**[Exploring the entities](exploring-the-entities.md)

