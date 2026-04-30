---
title: Specify data for your application
description: In its most basic form, building applications on the ServiceNow AI Platform means you're storing and using data in some way. Defining your application's data model is up to you and is based on the type of application you want to build.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Planning your application, Building applications]
---

# Specify data for your application

In its most basic form, building applications on the ServiceNow AI Platform means you're storing and using data in some way. Defining your application's data model is up to you and is based on the type of application you want to build.

You can use any combination of the following three methods to define your application's data model.

-   **Reuse existing tables and fields to store record data.** For example, use the existing Task table to work on existing record types such as incidents and problems. Typically, this option is only available for tables in the global scope or tables that make their data available to all application scopes.
-   **Extend existing tables to store record data.** For example, extend the Task table to create VIP incidents. The extended table inherits the fields from the parent table, but you can add new fields as needed.
-   **Create new tables and fields to store record data.** You can use a variety of available tools to create new tables. If you have access to App Engine Studio, use Table Builder to create new tables and fields as you build applications. Alternatively, you can create tables and fields separately from application development using basic Table administration in the ServiceNow AI Platform.

## More resources

These concepts are explained in further detail in the App Engine Studio, Table Builder, and Table administration documentation.

-   **[Create a data model for your application](../../app-engine-studio/concept/add-data.md)**

    Add data to apps that you build in App Engine Studio.

-   **[Table administration](https://www.servicenow.com/docs/access?context=c_TableAdministration&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Table administration currently contains more comprehensive functionality and options for managing tables.

-   **[Table Builder](../../../administer/form-builder/concept/tb-landing-page.md)**

    Table Builder offers an intuitive way to visually build tables and forms in the ServiceNow AI Platform.


