---
title: Lookup select box
description: The lookup select box variable creates a choice list using data queried from a table. Its functionality is similar to the lookup multiple choice variable, which creates radio buttons from queried data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-catalog/lookup-select-box.html
release: australia
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Types of service catalog variables, Service catalog variables, Service Catalog Reference, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Lookup select box

The lookup select box variable creates a choice list using data queried from a table. Its functionality is similar to the lookup multiple choice variable, which creates radio buttons from queried data.

For attributes supported by this variable, see [variable attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/variable-attributes.md).

To create the lookup select box, enter the following values when creating the variable:

-   **Lookup from table**: `Incident [incident]`
-   **Lookup value field**: `Sys ID`
-   **Lookup label field**: `number, category, priority`
-   **Reference qual**: `caller_id=javascript:gs.getUserID()^active=true`

**Note:**

-   Table with large data causes performance issues when loading the page. Use reference qualifiers to reduce data or use the reference type variable.
-   You cannot add more than 10,000 choices.

**Parent Topic:**[Types of service catalog variables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/r_VariableTypes.md)

**Related topics**  


[Attachment]()

[Break]()

[Check box]()

[Container start, container split, and container end]()

[Date, Date and time, and Duration]()

[Email](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/email.md)

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

