---
title: Use entity and risk dependencies using the GRC: Workbench
description: The GRC: Workbench utilizes CMDB information to show the upstream and downstream relationships across all applications. CMDB information is one of the sources. These relationships enable consistent risk mapping and modeling across the enterprise.
locale: en-US
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Risk Management, Governance, Risk, and Compliance]
---

# Use entity and risk dependencies using the GRC: Workbench

The GRC: Workbench utilizes CMDB information to show the upstream and downstream relationships across all applications. CMDB information is one of the sources. These relationships enable consistent risk mapping and modeling across the enterprise.

The GRC Manager \[sn\_grc.manager\] uses the GRC Workbench to:

-   Create entity classes.
-   Define the upstream/downstream relationships between entity classes. These relationships make up the dependency model and ensure that risks are defined and evaluated consistently across the enterprise.
-   Create entity types, create entities, and classify entities

**Note:** The GRC Manager cannot view the GRC: Workbench from **Risk** &gt; **GRC Workbench**. The GRC Manager \[sn\_grc.manager\] enters `/$grc_workbench.do` after their instance name in the url to access the GRC: Workbench.

The Risk Manager \[sn\_risk.manager\] uses the GRC: Workbench to:

-   Perform all the same tasks as the GRC Manager
-   Create risk frameworks, risk statements, and risks
-   Define risk relationships

## Model Setup tab

The Model Setup tab contains links to perform the following tasks.

|Link|Action|
|----|------|
|Dependency Model|Create entity classes and develop the organizational relationship model|
|Entity Types|Create and edit entity types|
|Dependency Map|Create and visualize entity relationships|

## Risk Dependencies tab

The Risk Dependencies tab contains links to perform the following tasks.

|Link|Action|
|----|------|
|Risk Frameworks|Create and edit risk frameworks|
|Risk Statements|Create and edit risk statements|
|Relationships|Create and visualize risk relationships|

-   **[Activate GRC: Workbench](../task/activate-grc-workbench.md)**  
The GRC: Workbench plugin is not activated by default, it is available as a separate subscription within the GRC Suite.
-   **[Create entity class using the GRC: Workbench](../task/create-profile-class-using-grc-workbench.md)**  
GRC managers create entity classes representing the types of things that are part of the dependency model. Reports can be filtered to define relationships between the different enity classes. An entity class defines what a entity actually is.
-   **[Create relationships between entity classes using the GRC: Workbench](../task/create-relationships-between-profile-classes.md)**  
Managers create relationships between entity classes using the GRC: Workbench to build out the dependency map and better understand how entities relate to one another.
-   **[Associate a risk framework or risk statement with an entity type to generate risks](../../grc-risk/task/t_GenerateRiskFromFramework.md)**  
Risks are automatically generated when you make associations between risk frameworks or risk statements and entity types.
-   **[Visualize and edit entity dependencies using the GRC: Workbench](../task/visualize-edit-profile-dependencies.md)**  
The GRC: Workbench gives GRC administrators a graphical interface to create entity dependencies. These relationships enable consistent entity and risk mapping and modeling across the enterprise.
-   **[Delete entity dependencies using the GRC: Workbench](../task/delete-profile-dependencies.md)**  
When deleting entity dependencies, only the relationship between the entities is deleted. The entities themselves remain unmodified.
-   **[Delete an entity class using the GRC: Workbench](../task/delete-profile-class-workbench.md)**  
Deleting an entioty class, deletes all relationships below it.
-   **[Create a risk using the GRC: Workbench](../task/create-risk-using-grc-workbench.md)**  
Risk managers can create risks directly from the GRC: Workbench.
-   **[Visualize and edit risk dependencies using the GRC: Workbench](../task/visualize-edit-risk-dependencies.md)**  
The GRC: Workbench gives GRC administrators a graphical interface to create risk dependencies. These relationships enable consistent entity and risk mapping and modeling across the enterprise.
-   **[Delete risk dependencies using the GRC: Workbench](../task/delete-risk-dependencies.md)**  
When deleting risk dependencies, only the relationship between the risks is deleted. The risks themselves remain unmodified.

**Parent Topic:**[Using Risk Management](../../grc-risk/concept/using-risk-mgmt.md)

