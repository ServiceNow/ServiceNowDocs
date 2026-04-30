---
title: Creating many-to-many task relations
description: By default, tasks can be related to each other using a parent/child relationship, such as a Problem with a group of child Incidents or a Catalog Request with a group of child Catalog Tasks.
locale: en-US
release: zurich
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Working with Task table, Table admin, Tables and data, Configure core features, Administer]
---

# Creating many-to-many task relations

By default, tasks can be related to each other using a parent/child relationship, such as a Problem with a group of child Incidents or a Catalog Request with a group of child Catalog Tasks.

However, it may prove useful to record exactly the nature of the relationship between the task records. When activated, the Many-to-Many Task Relations plugin allows administrators to define relationships between different tasks.

-   **[Request many to many task relations](../task/t_RequestManyToManyTaskRelations.md)**  
The Many to Many Task Relations plugin \(com.snc.task\_relations\) is included with several plugins. You can request activation of the plugin by itself.
-   **[Plugin manifest](../reference/r_PluginManifest.md)**  
When the plugin is activated, the Task Relationships application is available with certain modules.
-   **[Define a relationship type](../task/t_DefineARelationshipType.md)**  
Create type codes that define the relationship between parent and child tasks.
-   **[Define a task relationship allowed from the task relationship type record](../task/t_DefineATaskRelationshipAllowed.md)**  
Define the Task Relationships Allowed from the Task Relationship Type record.
-   **[Modify the displayed field](../task/t_ModifyTheDisplayedField.md)**  
The list view of the Reference Lookup defines the fields displayed in the Task Relations field and editing interface.
-   **[Mark as Solution button](c_MarkAsSolutionButton.md)**  
The **Mark as Solution** button is added to the KB popup view and displayed when you search the knowledge base from a task record.
-   **[Task relationships with UI actions](../reference/r_UIActions.md)**  
After defining task relationships, you can use UI Actions to define the task relationship when a new task is being created from an old task.

**Parent Topic:**[Working with the Task table](c_TaskTable.md)

