---
title: Lookup select box
description: The lookup select box variable creates a choice list using data queried from a table or from a choice list. Its functionality is similar to the lookup multiple choice variable, which creates radio buttons from the same sources.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-catalog/lookup-select-box.html
release: brazil
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Types of service catalog variables, Service catalog variables, Service Catalog Reference, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Lookup select box

The lookup select box variable creates a choice list using data queried from a table or from a choice list. Its functionality is similar to the lookup multiple choice variable, which creates radio buttons from the same sources.

You can also configure this variable, and the lookup multiple choice variable, to source its values from a choice list instead of a table. This is useful when the values you want to offer are already maintained as choices on a field on another table, rather than as records in a table.

By default, choices are ordered by their label. You can control the order in which values appear by using the ref\_ac\_order\_by variable attribute to sort by a specific column first.

For attributes supported by this variable, see [variable attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-catalog/variable-attributes.md).

To create the lookup select box, enter the following values when creating the variable:

-   **Lookup from table**: `Incident [incident]`
-   **Lookup value field**: `Sys ID`
-   **Lookup label field**: `number, category, priority`
-   **Reference qual**: `caller_id=javascript:gs.getUserID()^active=true`

## Use choice list values as the lookup source

Instead of sourcing values from a table, you can configure the lookup select box or lookup multiple choice variable to source its values from a choice list. Complete the following fields to source values from a choice list:

-   In the **Lookup source** field, select `Choices`. The default value is `Table`.
-   Optionally, in the **Choices depend on** field, select another question on the same catalog item. The choice list then filters to the choices that are valid for the current value of that question.

**Note:**

-   This option is available for the lookup select box and lookup multiple choice variable types. It is supported in the Service Portal, mobile, and Virtual Agent channels.
-   Table with large data causes performance issues when loading the page. Use reference qualifiers to reduce data or use the reference type variable.
-   You can't add more than 10,000 choices.

## Question \[item\_option\_new\] fields

|Field|Description|Type|
|-----|-----------|----|
|Lookup source \(lookup\_source\)|Determines where the variable's choice values come from. Set to Table to query a table, or Choices to source values from the sys\_choice table. Only shown for the lookup select box and lookup multiple choice variable types.|Choice \(default: Table\)|
|Choices depend on \(lookup\_dependent\_question\)|Optional. References another question on the same catalog item. When set, the choice list filters to the choices that are valid for the current value of that question. Only shown when Lookup source is set to Choices.|Reference \(to Question \[item\_option\_new\]\)|

**Parent Topic:**[Types of service catalog variables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-catalog/r_VariableTypes.md)

**Related topics**  


[Attachment]()

[Break]()

[Check box]()

[Container start, container split, and container end]()

[Date, Date and time, and Duration]()

[Email](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-catalog/email.md)

[HTML]()

[IP Address]()

[Label]()

[List collector]()

[Lookup multiple choice]()

[Custom and Custom with label]()

[Masked]()

[Multi-line text]()

[Multiple choice]()

[Numeric scale]()

[Reference]()

[Requested for]()

[Rich Text Label]()

[Select box]()

[Single-line text]()

[UI page]()

[URL]()

[Wide single-line text]()

[Yes/No]()

[Variable support in various channels]()

