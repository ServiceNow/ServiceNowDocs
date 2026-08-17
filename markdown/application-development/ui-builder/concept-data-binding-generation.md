---
title: Data binding generation
description: ServiceNow Otto generates data bindings for component properties using natural language instructions, reducing the need to manually navigate data trees or construct formulas.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/concept-data-binding-generation.html
release: australia
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2026-08-17"
reading_time_minutes: 2
breadcrumb: [Explore, UI generation, UI Builder, Builder library, Developing your application, Building applications]
---

# Data binding generation

ServiceNow Otto generates data bindings for component properties using natural language instructions, reducing the need to manually navigate data trees or construct formulas.

When you configure a component property in UI Builder, the **Bind data** dialog includes a **Generate data binding with ServiceNow Otto** option. You describe the binding you want in plain language, and ServiceNow Otto produces the corresponding formula or data reference, which you can review before applying it.

## How data binding generation works

When you submit a natural language instruction, ServiceNow Otto interprets your intent and maps it to the available data sources for the component. The generator has access to the following data source categories shown in the **Data types** panel:

-   **Page properties**

    The properties defined at the experience or page level.

-   **Data resource**

    The data resources added to the page, such as a list of records returned from a table.

-   **Client states**

    The client-side state parameters defined for the experience.

-   **Event payload**

    The data carried by a component event, available when configuring an event handler.


The **Pill view** and **JSON** tabs let you inspect the data structure of each source before or after generating a binding. The **Formulas** tab shows available formula functions, such as `CONCAT` and `WHERE_GT`, that ServiceNow Otto may use to satisfy your instruction.

## Types of generated bindings

Depending on the component property and your instruction, ServiceNow Otto generates one of the following binding types:

-   **Concatenation formula**

    Combines static text with a data pill. For example, the instruction `Show "Choose your ride" and the user's full name` produces a `CONCAT` formula that joins a string literal with the session user name pill.

-   **Filter formula**

    Applies a condition to a data resource. For example, the instruction `Return from fleet whose year of manufacture is greater than 2020` produces a `WHERE_GT` formula on the fleet data resource, filtering the result set to records whose `year` field exceeds 2020.

-   **Direct data pill reference**

    References a single field from a data source without transformation. For example, the instruction `Use the pillId from event payload` resolves to the `pillId` pill from the event payload data source.


## Suggested prompts

The **Generate data binding** panel displays suggested prompts based on the component's context and the data sources available on the page. You can select a suggestion to populate the instruction field, then submit it as-is or modify it before generating. The panel also includes a **Show more** option to display additional suggestions.

## Reviewing generated bindings

After ServiceNow Otto generates a binding, a preview appears in the component's property panel before the binding is applied. You can inspect the formula or data pill reference and close the dialog without applying it if the result doesn't match your intent. You can also stop an in-progress generation by selecting **Stop generating**.

**Parent Topic:**[Exploring UI generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/exploring-ui-generation.md)

**Related topics**  


[Generate a data binding and formula](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/generate-data-bindings-and-formulas.md)

[Use case: Generate a data binding and formula](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/use-case-data-binding-generation.md)

