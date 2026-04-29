---
title: Using Investigative Case Management Entity Management
description: Investigators can use the Investigative Case Management Entity Management feature to manage all entities \(persons, locations, vehicles, property, firearms, organizations\) related to a case.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Using Investigative Case Management, Solutions, Use, Public Sector Digital Services \(PSDS\)]
---

# Using Investigative Case Management Entity Management

Investigators can use the Investigative Case Management Entity Management feature to manage all entities \(persons, locations, vehicles, property, firearms, organizations\) related to a case.

Use a centralized Investigative Entity Management system with m@ster indexes for to reduce duplication and improve cross-case visibility. It enables creation and management of incident and investigation event timelines, role assignments, and entity linking within case workspaces. Key features include dedicated management tabs, data models for entities and relationships, audit tracking, and retention policies. This enhances investigative insights, data integrity, and collaboration while supporting Now Assist AI efforts for smart import and case creation.

Investigators can view all individuals, entities, and locations connected to a case or recurring across cases. This improves investigative insights, reduces data entry duplication, and ensures that critical connections—like repeat offenders or high-risk addresses—are not missed. Analysts and supervisors benefit from improved data integrity, faster case development, and more informed decision-making.

With the Entity Management feature, investigators can:

-   Create and view common master indices for Persons, Locations, Organizations, Vehicles, Property associated with the case through dedicated entity tabs. This can help reduce duplicates for all entities \(“John Smith” and “Johnny Smith” might be the same person\).
-   Associate multiple entities to each other and to the case
-   Create and manage a centralized Firearms master index to unify firearm records across investigations, storing critical identifiers, traits, and historical data in a dedicated Firearms tab and allowing firearms to be linked to related entities \(persons, events, cases, evidence, organizations, locations, property\) within the case
-   Create incident and investigation event records to help capture the timeline for important events that happen during the investigation, and the timeline of the investigation itself
-   View audit logs for all firearm record changes and relationship updates
-   Associate multiple entities to each other and to the case, as well as manage all entities and their relationships to the case

## Entities in Investigative Case Management

Investigators can access Entity Management directly from the Investigative Case Management workspace through any of the seven dedicated Entity tabs.

The following entity types are included with Investigative Case Management by default, and investigators can add as many as necessary to the case through the ICM workspace.

-   Persons
-   Locations
-   Events
-   Vehicles
-   Property
-   Organization
-   Firearm

ICM supports management of persons, property, vehicles, organizations, locations, and events, as well as specialized entity types like firearms with detailed identification, specifications, origin, and ballistic information, all linkable to cases and to each other.

## Entity Tabs

Investigators and supervisors will mainly interact with case entities through the dedicated entity tabs in the workspace. Each tab allows the user to create as many records as needed, as well as add related cases and associate other entities.

![Entity tabs in Entity Management](../image/psds-icm-entities-tabs-highlight.png)

-   **Persons**

    The Person tab allows users to create and manage person records. Users are able to add new Persons, view existing ones in a related tab or list, and edit records. Users can add different person types to a case using the categories provided. Users are also able to link/delete other associated entities to a person, and view associated entities.

    ![entity persons view](../image/psds-icm-persons-tab-entity.png)

-   **Vehicles**

    The Vehicles tab allows users to create and manage vehicle records. Users are able to add new vehicles, view existing ones in a related tab or list, and edit them. It also supports linking to other entities for context and traceability. The vehicle index and firearm index tables are an extension of the property index table.

-   **Locations**

    The Locations tab allows users to store critical information about case locations and their relationship to the case.

-   **Events**

    The Events tab allows users to create incident and investigation event records to help capture the timeline for important events that happen during the investigation, and the timeline of the investigation itself.

-   **Property**

    The Property tab allows users to create and manage property records. Users are able to add new properties, view existing ones in a related tab or list, and edit them. It also supports linking to other entities for context and traceability.

-   **Organizations**

    The Organization tab allows users to create and manage records of organizations that are related to the case. Users are able to add new organizations, view existing ones in a related tab or list, and edit details as they become available. It also supports linking to other entities for context and traceability.

-   **Firearm**

    The Firearm tab allows users to create and manage firearm records. Users can create and manage firearms and manually related entities. Each firearm profile stores critical identifiers, traits, and historical data. Users are able to add new firearms, view existing ones in a related tab or list, and edit them. The vehicle index and firearm index tables are an extension of the property index table.

    ![entity firearms view](../image/psds-icm-firearms-tab-entity.png)


## Entity Completeness

In the Entity Management form, not every field is mandatory, and is designed to capture as much information as possible, without imposing strict restrictions on the information that can be added. However, each entity record contains a completeness field that tracks whether the record has sufficient data to be searchable within ICM.

An entity is only returned in search results when its completeness field is set to true. Completeness is recalculated automatically whenever relevant fields are updated, ensuring search visibility reflects the current state of the record. To see completeness rules for each entity type, see [Completeness Rules by Entity Type](../reference/psds-icm-ref-entity-man-completeness-rules.md).

