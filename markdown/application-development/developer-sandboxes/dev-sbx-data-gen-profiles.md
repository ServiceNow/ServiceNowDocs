---
title: Data Generation Profiles in Developer Sandboxes
description: Because Developer Sandboxes copy metadata, not record data, from the base instance, you might need to generate specific data using a Data Generation Profile.
locale: en-US
release: zurich
product: Developer Sandboxes
classification: developer-sandboxes
topic_type: concept
last_updated: "2025-08-11"
reading_time_minutes: 2
breadcrumb: [Administer data, Developer Sandboxes, Developing your application, Building applications]
---

# Data Generation Profiles in Developer Sandboxes

Because Developer Sandboxes copy metadata, not record data, from the base instance, you might need to generate specific data using a Data Generation Profile.

## Data Generation Profile overview

Data Generation Profiles help you create test data for sandboxes. They work by:

-   Selecting specific tables to sample data from
-   Creating mappings to populate your sandbox with the necessary data
-   Providing the data needed to build and test your application

Data Generation Profiles generate realistic test data for your development environment, making it easier to build and test your application without using real data.

When generating data, Developer Sandboxes doesn't copy all the instance data. Data Generation Profiles enable a statistical sampling of data from selected tables with curated mappings to populate the sandbox with the data needed for building an application. Data Generation Profiles can also call definitions that run Business Rules to automatically create additional data when a record is generated.

Data Generation Profiles define the tables and fields that you want data populated in for development purposes. For example, the \[sys\_user\] table might need ten Service Desk users added to it for development and testing.

A Developer Sandboxes Data Generation Profile uses the definition of a data model, which you must also create. A Data Generation Definition is a JSON file that's stored as an attachment. The data model collects the defined details from the existing table to generate data and populates it with specified data based on the number of records in the Data Generation Profile.

## Data Generation Profile and tables

Data Generation Definitions are the tables that you want data to be configured in. You can do the following:

-   Provide a name for the Data Generation Profile definition
-   Select the table to generate data in
-   Change the number of records to display
-   Specify that the definition runs business rules
-   Choose the date and time for the records

You can create a Data Generation Profile that can target multiple tables. Each table definition can map fields to either generated, template, or literal values, and the remaining categorical values will be populated from a statistical table model built using the last 1000 records created in that table.

## Data Generation Profile field mappings

Data Generation Profile field mappings enable you to specify the relationships between the different definitions. This semi-curated approach of data generation field mappings creates some control over the details of generated data while still automating the bulk of the process.

## Data Generation Profile actions

Data Generation Profile actions enable you to generate fake or random data that fits your criteria. There are several actions that can generate fake usernames, IDs, emails, and phone numbers.

Additionally, new actions can be defined via a scripted API to provide customer-specific methods of data generation. New actions can help populate fields where the statistical model is not quite adequate, or where Personally Identifiable Information \(PII\) needs to be protected.

