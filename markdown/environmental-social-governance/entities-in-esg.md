---
title: Manage entities in Operational Sustainability Management \(formerly ESG Management\)
description: You can learn about how Operational Sustainability Management is used by the investors and reporting agencies to evaluate different entities that they want to invest in, such as different business units in an organization.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Manage entities in Operational Sustainability Management \(formerly ESG Management\)

You can learn about how Operational Sustainability Management is used by the investors and reporting agencies to evaluate different entities that they want to invest in, such as different business units in an organization.

Entities can be people, processes, departments, or applications. For example, if your goal is to reduce the carbon emission from the datacenters, then you can consider datacenters as entities.

As another example, assume you’re a company that has subsidiary companies. Your goal is to measure greenhouse gas emissions \(GHG\) in your subsidiary companies. Both your company and your subsidiary companies are your entities. Your company is the parent entity, while the subsidiary companies are the child entities. Typically, the parent entity handles reporting and measuring the GHG of the child entities.

As part of your ESG Management strategy, you have to provide disclosures to your stakeholders. ESG Management disclosures refer to the disclosure of data that relate to an organization's Operational Sustainability Management performance. These disclosures concern the goals, targets, and metrics that are associated with your entities. By using these disclosures and other metrics, the investors assess and rate the performance of entities based on the operational sustainability parameters.

A parent entity that has the child entities is said to have downstream entities. Any child entity that has the parent entities is said to have upstream entities.

After creating the entities, you can tag similar entities by individually defining an entity class for them or by linking them to an existing entity class.

## Entity classes

Entity classes are used to tag an entity or to add the conceptual information about an entity. For example, consider a company that has office branches in three cities. The office space is considered as an entity, while the entity class for these entities is the location of the offices.

## Entity types

An entity type is a grouping of entities that is based on filtering attributes. An entity type defines a set of the entities that have the same attributes. An entity type is used to describe and identify an entity that is based on a set of filter conditions.

Consider the following two entity types: Employee and Product. Each entity type has its own attributes.

For Employee, its attributes are employee number, name, department, and designation. In the Employee table of the company database, the sample attributes of an employee are displayed in row E1 as 1001 \(employee number\), Paul \(name\), Marketing \(department\), and PM \(designation\).

For Product, its attributes are product ID, name, cost, and currency. In the Product table in the company database, the sample attributes of an energy-efficient product are displayed in row P1 as 800 \(product ID\), Solar Panel \(name\), 200 \(cost\), and USD \(currency\).

Entities and entity types can have a one-to-many relationship. For example, an entity called Hope can have an entity type called Person and an entity type called Organization.

-   **[Create an entity](../task/create-entity.md)**  
Create an entity and measure its performance against the goals. Defining an entity ensures that the entity owners are also identified. After an entity is defined, ESG Management goals are applied to the entity.
-   **[Update an entity](../task/update-an-entity.md)**  
Update the details of an existing entity.
-   **[Create an entity type](../task/create-entity-type.md)**  
Create an entity type for the entities in your system. Entity types enable you to find and create entities that have the same attributes and that match a set of filter conditions.
-   **[Update an entity type](../task/update-entity-type.md)**  
Update an existing entity type to add entity filters, policies, and control objectives.
-   **[Create an entity class](../task/create-entity-class.md)**  
Create an entity class that is to be associated with an entity. Define the parent class, root entity, and tier for an entity class.
-   **[Update an entity class](../task/update-entity-class.md)**  
Update an existing entity class that is associated with an entity. Entity classes are used to add the conceptual information about an entity or tag the entity.

**Parent Topic:**[Configure Operational Sustainability Management \(formerly ESG Management\)](configuring-esg.md)

**Related topics**  


[Create an entity](../task/create-entity.md)

