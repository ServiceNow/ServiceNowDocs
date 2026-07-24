---
title: List collector
description: The list collector variable creates an interface that lets you select and add multiple records from a table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-catalog/list-collector.html
release: australia
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Types of service catalog variables, Service catalog variables, Service Catalog Reference, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# List collector

The list collector variable creates an interface that lets you select and add multiple records from a table.

For attributes supported by this variable, see [variable attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/variable-attributes.md).

\[Omitted image "VariableListCollectorG.png"\] Alt text: A list collector variable

**Note:**

-   The Reference Qualifier and glide\_list attribute applies to releases from Helsinki onward only. The attribute does not apply to Geneva.
-   You can set a value for this variable using the g\_form.setValue\(\) function in a catalog client script.
-   When the glide\_list attribute is not true, you can only set the value that is visible in the **Available** list using the g\_form.setValue\(\) function. This functionality is not applicable when the setValue\(\) function is called onLoad.
-   Table with large data causes performance issues when loading the page. Use reference qualifiers to reduce data or use the glide\_list attribute.
-   The values in the referenced table do not appear if the user is not logged in.
-   The list collector displays a maximum of 100 items in a list. After moving items to the **Selected** list, you can click **Run Filter** to refresh the **Available** list. This action will add more available items to the list, to a maximum of 100 items.

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

[Lookup multiple choice]()

[Lookup select box]()

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

