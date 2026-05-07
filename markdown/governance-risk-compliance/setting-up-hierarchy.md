---
title: Setting up pillars, entity types, entity filters, and entities
description: This section helps you configure the Operational Resilience application to organize and track your organization's operational data through a structured hierarchy of pillars, entity types, and entities.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Configure, Operational Resilience, Governance, Risk, and Compliance]
---

# Setting up pillars, entity types, entity filters, and entities

This section helps you configure the Operational Resilience application to organize and track your organization's operational data through a structured hierarchy of pillars, entity types, and entities.

## Key concepts and definitions in Operational Resilience

It is essential to understand the core terminology and how different components relate to each other. This section defines the key concepts that form the foundation of the application's data structure. Knowledge of these terms enables informed decision-making during setup and confirms that the system is configured correctly for your organization's needs. The table provides definitions and practical examples for each concept.

|Term|Definition|Example|
|----|----------|-------|
|Pillar|Top-level organizational category that groups the related entity types|Technology, Services, People, Facilities|
|Entity type|A classification within a Pillar that defines what kind of data to track|Within Technology pillar: Servers,Applications, Databases|
|Entity Filter|Criteria that automatically select records from ServiceNow tables|Filter: "Operational Status = Active AND Location = US"|
|Entity|An individual record that meets the Entity filter criteria|A specific server: "PROD-WEB-01"|
|CSDM|Common Service Data Model - Company standard for organizing IT data|Confirms consistency across ServiceNow applications|
|CMDB|Configuration Management Database \(CMDB\) - Stores IT infrastructure data|Source of servers, applications, and relationships|

Consider the example of organizing a filing cabinet where pillars are drawers, entity types are folders within each drawer, entity filters are the labels that determine what goes in each folder, and entities are the actual documents.

## Understanding the data hierarchy

The Operational Resilience application organizes data in a multi-level hierarchy as shown in the example.

![Data in a 4-level hierarchy.](../image/hierarchy-flow.png)

## Key relationships between pillars, entity types, and entity filters

Understanding how different levels of the data hierarchy interact with each other is crucial for effective configuration and maintenance of the Operational Resilience application.

|Relationship|Example|
|------------|-------|
|One pillar and many entity types|The "Technology" pillar can contain many entity types such as Servers, Applications, Network Devices.|
|One entity type and many entity filters|The "Servers" entity type can have many entity filters such as ones for "Production Servers","Test Servers".|
|One entity filter and many entities|An entity filter for "Active Production Servers in US" generates many individual server entities.|
|Entities and CMDB relationships|When CMDB relationships change, entity relationships update automatically.|

**Note:** The CMDB relationships flow into Operational Resilience in one direction only. Changes to Operational Resilience entities do not update the CMDB relationships automatically. If relationships change in the CMDB, new entity relationships are created, but old relationships aren’t automatically deleted—you may need to delete them manually.

## Required roles, their capabilities, and checklist

Before beginning the setup process, verify that you have the required roles to perform the setup.

-   **Required roles for the setup**

    sn\_oper\_res.admin, sn\_oper\_res.manager

-   **Role capabilities**

    |Role|Can activate pillars|Can create Entity types|Can delete Entity types|Can generate entities|
    |----|--------------------|-----------------------|-----------------------|---------------------|
    |sn\_oper\_res.admin|Yes|Yes|Yes|Yes|
    |sn\_oper\_res.manager|Yes|Yes|No|Yes|

-   **Checklist**

    Complete the checklist before you begin the setup:

    1.  Confirm that you have the required roles to perform the setup.
    2.  Review the list of default pillars. The default pillars are: Services, Business Services, Business Processes, Technology, Facilities, People, Suppliers, Data, Application Services, and Service Offerings.
    3.  Identify the pillars and entity types that you would need for your organization.
    4.  Determine if you need custom entity types in addition to the default entity types.
    5.  Understand your CMDB structure and relationships.
    6.  Allocate sufficient time for the initial setup.

**Note:** Beginning with Operational Resilience, Release 21.x.x, all pillars are shipped in an "Inactive" state. You must activate the pillars before activating the entity types, as the entity types depend on the pillars. Entity types can be activated only after their parent pillars are active.

## Using the Workspace UI or Admin setup

This section provides a high-level overview of the Workspace UI or the Admin setup from Core UI in the Operational Resilience.

|Feature|Workspace UI interface \(Suggested method\)|Core UI \(UI16\) interface|
|-------|-------------------------------------------|--------------------------|
|Visual design|Modern and streamlined|Classic interface|
|Learning curve|Easier for new users|Familiar to experienced admins|
|Navigation|Operational Resilience Workspace &gt; Entity types \| Pillars|All &gt; Operational Resilience &gt; Admin &gt; Entity types &gt; Pillars|
|Functionality|Complete setup capability|Complete setup capability|
|When to use|General setup tasks|Preference for classic UI|

**Note:** Use the Workspace UI to use latest features and enhancements. The Core UI is part of the classic interface. You can switch between them at any time.

## Step-by-step overview

Setting up Operational Resilience follows a logical progression from foundational components to data generation. This overview helps you understand what each step accomplishes and why the sequence matters. Detailed procedures with screenshots and examples are available in the subsequent sections.

<table id="table_aqy_dvc_23c"><thead><tr><th>

Step number

</th><th>

Action

</th><th>

Reference

</th></tr></thead><tbody><tr><td>

Step 1

</td><td>

Activate Pillars -   Navigate to the Pillars module.
-   Review default pillars available with the application.
-   Activate pillars that are needed for your organization
-   Confirm that you follow the sequence \(order\) and activate pillars before entity types.

</td><td>

[Set up pillars and entity types from Workspace UI](../task/set-up-from-ws.md)

</td></tr><tr><td>

Step 2

</td><td>

Activate entity types -   Navigate to the Entity types module.
-   Review the default entity types within each pillar.
-   Activate the entity types that you need.
-   Create custom entity types if needed.

</td><td>

[Set up pillars and entity types from Workspace UI](../task/set-up-from-ws.md)

</td></tr><tr><td>

Step 3

</td><td>

Configure entity filters -   Within each entity type, configure filters.
-   Choose "Build custom conditions" or "Select predefined queries."
-   Define a criteria to select records from CMDB tables.
-   Activate entity filters.

</td><td>

[Configure the entity filters](../task/conf-ent-filter.md), [Activate the entity filters](../task/activate-ent-fil-directly.md), and [Verify the configuration of entity filters](../task/verify-ent-fil.md)

</td></tr><tr><td>

Step 4

</td><td>

Generate entities -   Run entity generation process. Entities are created automatically based on filters.
-   Option: Manually add entities if needed.
-   Verify that entities appear in the Entity Types record.

</td><td>

[Generate entities automatically using a scheduled job](../task/gen-ent-auto.md)

</td></tr><tr><td>

Step 5

</td><td>

Configure Main node \(Post-setup\) -   Set up CMDB integration.
-   Configure relationship mapping.

</td><td>

[Configure the Main node configurations](../task/set-up-main-node.md)

</td></tr></tbody>
</table>