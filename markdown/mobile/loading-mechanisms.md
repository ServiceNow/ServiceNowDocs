---
title: Loading mechanisms for input form screens
description: The input form screen contains various UI elements, such as inputs, input actions, and descriptive elements. These elements can be populated either manually by the user or automatically using data sources and autofill variables.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure an input form screen, Input form screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Loading mechanisms for input form screens

The input form screen contains various UI elements, such as inputs, input actions, and descriptive elements. These elements can be populated either manually by the user or automatically using data sources and autofill variables.

The two mechanisms for loading data from the database into an input form are:

-   **Variables**: Variables can be used to set default values when the input form is first opened, verifying that users begin with prefilled information. Additionally, they can retrieve the most up-to-date values from the database when the form is refreshed or reopened, keeping inputs synchronized with the latest data. Variables can also be used for providing data for write-back actions when submitting or saving progress.
-   **Data sources**: Like variables, data sources can be used to load default values when the form is first opened. Additionally, data sources retrieve the most recent data from the database whenever the form is accessed or refreshed.

    To map descriptive elements, such as images, rich text, and plain text to an input form, you must configure the data source loading mechanism.


**Note:** A variable can be assigned to a single UI element, whereas data sources can be mapped to multiple elements.

The following scenarios are supported by at least one of the loading mechanisms:

-   Setting default values for input fields and input actions, such as comments and attachments.
-   Populating the form with the most current data from the database when triggering an input form action, such as saving progress.
-   Providing data for write-back actions when submitting or saving progress. \(Variables only\)

For a table listing which loading mechanisms support various input form UI elements, see [Loading mechanisms for input form UI elements](../reference/loading-mechanisms-table.md)

## Examples for autofill variables and data sources

-   **Default values**: When a Field Service Management agent opens a Work Order Task form, a variable or a data source can automatically set the default task category to ‘Inspection’. This configuration minimizes manual selection while enabling users to modify the category, if needed.
-   **Most up-to-date data**: When a supervisor updates a Work Order Task priority from Medium to High, a variable or data source can be configured to fetch and display this updated priority the next time an agent opens the form.

For more information, refer to the following topics:

-   [Data sources](data-sources.md)
-   [Configure attributes for input form screen variables](../task/param-screen-config-variables.md)
-   [Configure auto-fill inputs on input form screens](../task/config-autofil-inputs-nptfrmscrn.md)

