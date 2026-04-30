---
title: Data sources
description: A data source is a loading mechanism that maps UI elements to specific database fields using element identifiers. Use data sources to retrieve and display data onto input form screens.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure an input form screen, Input form screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Data sources

A data source is a loading mechanism that maps UI elements to specific database fields using element identifiers. Use data sources to retrieve and display data onto input form screens.

## Concept

Data sources enable the mapping of various types of data, such as input values, input actions, and descriptive elements to UI elements on the screen. This mapping is achieved by querying and filtering data from specific tables and fields in the database, and then associating the data with the corresponding UI elements. The mechanism uses an identifier to connect a UI element to a specific data field within a record. This mapping enables the UI element to retrieve and display the specified data.

**Note:** Data sources aren't supported in offline.

## Data source variables

The data source script that maps data into UI elements uses the *DataSourceId* and *ElementIdentifier* variables.

-   **DataSourceId**

    This variable is the unique identifier for the data source that you're working with. You define it to point to the specific data source you're interacting with in your script.

-   **ElementIdentifier**

    This variable is a unique identifier for each UI element. It helps you specify which UI element a particular piece of data should be mapped to.

    **Note:** The *ElementIdentifier* variable is listed as *valuesMapper.addRecordMapping* in the data source script.


## Data source loading mechanism example usage

-   **Descriptive elements**

    These are elements that provide additional information or context, such as pictures or texts that relate to an input or sections. Configuring a data source is required for descriptive elements because it links UI elements to specific fields in a table. This mapping verifies that the data displayed in the UI corresponds to data in the table being iterated by the data source. For more information, see [Configure descriptive elements for input form screens](../task/descriptive-elements-script.md).

-   **Input actions**

    These are actions that are associated with input fields. Input actions include the addition of a comment, attachment, or navigation buttons. For more information, see [Configure input form actions in an input form screen](../task/input-actions-configure.md).

-   **Input form actions and refresh option**

    This action enables you to save current data and concurrently make it available to others. This updated data is available when a user either opens the input form or saves their changes. This displayed data includes input values, comments, and attachments added by other users. For more information, see [Configure input form screen actions](../task/input-form-screen-actions-config.md).


