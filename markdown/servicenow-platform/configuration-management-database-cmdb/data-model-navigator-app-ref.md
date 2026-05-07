---
title: Data Model Navigator app features
description: The Data Model Navigator app provides comprehensive information about CMDB tables, attributes, and relationships with context-aware guidance for specific use cases. While users can view the data, the primary purpose is to generate up-to-date indexed data for use by Now Assist agents and skills.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2026-04-29"
reading_time_minutes: 1
keywords: [Data Model Navigator, CMDB data model, tables, attributes, relationships, IP address management, cloud]
breadcrumb: [Explore, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Data Model Navigator app features

The Data Model Navigator app provides comprehensive information about CMDB tables, attributes, and relationships with context-aware guidance for specific use cases. While users can view the data, the primary purpose is to generate up-to-date indexed data for use by Now Assist agents and skills.

## App overview

The Data Model Navigator app gathers comprehensive information about the base-system CMDB data model, starting with the CMDB structure \(Configuration Item \[cmdb\_ci\] table\). The app provides use-case and context-driven guidance to help you identify which tables capture specific types of information, identify key attributes and how they differ from similar attributes, and learn how to model relationships between classes.

## Prerequisites

The Data Model Navigator store app must be installed. It is installed automatically when you install the Service Graph Workspace - Content store app.

Role required: sn\_data\_model\_nav.data\_model\_navigator\_write or sn\_data\_model\_nav.data\_model\_navigator\_read

## Navigation path

Navigate to **All** &gt; **Data Model Navigator**.

## App features

|Feature|Description|
|-------|-----------|
|Contexts|Browse the data model organized by use-case contexts, such as IP address management or cloud resources. Contexts map to CI classes and help you identify the parts of the data model that support specific uses and outcomes.|
|Tables|Review the types of information captured in each table, how that information varies by context, and data samples that clarify the table's purpose.|
|Fields|Identify and review key attributes for a class. The app differentiates key attributes from similar ones in the same table and highlights attributes that are important in specific use cases.|
|Relationships|Review guidance on how and why to model relationships between specific classes.|

## Use cases

The app provides context-driven guidance for specific scenarios:

-   Identify tables and attributes that strengthen solutions for IP address management
-   Learn the differences between data modeling in cloud and non-cloud environments
-   Make informed decisions about how to structure and populate your CMDB data
-   Determine which tables and attributes to prioritize for your use case

## Integration with Now Assist

Users benefit from the information that the app generates when asking questions in the Now Assist panel. Example questions include:

-   `What is the purpose of the "subcategory" field on a CI?`
-   `Which table is used for storing flexible key-value pairs for CIs, often from cloud sources, within the CMDB?`
-   `What is the relationship between a hardware CI and a network adapter?`

