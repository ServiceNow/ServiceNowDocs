---
title: Multi-table data configuration
description: Present data from multiple tables using components and control the layout and styling.
locale: en-US
release: zurich
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Dynamically expose data in UI Builder pages \(advanced feature\), Advanced UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Multi-table data configuration

Present data from multiple tables using components and control the layout and styling.

A data resource fetches the data that UI Builder uses to display information in a [component](ui-builder-glossary.md#). Most often, a component is mapped to data contained in one table. However, there are numerous use cases where there’s a need to map a single component to information in multiple tables, for example:

-   Place the card component in a repeater and use multi-table data configuration to pull data from different sources to display on the cards.
-   Create a portal page that displays a list of tasks pulled from different locations.

![Multi-table data resource displayed with incident and problem tables used as data sources.](../image/multi-table-data-source23.png)

**Note:** You can configure more than one multi-table data resource on a single page to display different sets of data.

## Multi-table data configuration and Entity View Action Mapper

The Entity View Action Mapper \(EVAM\) can also be used to configure cards and lists using different data sources. The EVAM is an option for users who understand and are comfortable working with JSON. The multi-table data configuration option gives you greater control over the presentation of data, makes it easier to configure the data, and enables you to remain in UI Builder. Use the option that you prefer. For more information about EVAM, see [Work with the Entity View Action Mapper for UI Builder](evam-ui-builder.md).

-   **[Fetch data from multiple sources](../task/fetch-data-from-multiple-sources.md)**  
Learn how to obtain data from different sources to use in a single component.

**Parent Topic:**[Dynamically expose data in UI Builder pages \(advanced feature\)](data-resources.md)

