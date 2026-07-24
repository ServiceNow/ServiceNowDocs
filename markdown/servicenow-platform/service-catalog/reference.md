---
title: Reference
description: A reference variable references a record in another table. For example, a variable named point\_of\_contact references the User \[sys\_user\] table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-catalog/reference.html
release: australia
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Types of service catalog variables, Service catalog variables, Service Catalog Reference, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Reference

A reference variable references a record in another table. For example, a variable named point\_of\_contact references the User \[sys\_user\] table.

For attributes supported by this variable, see [variable attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/variable-attributes.md).

Keep the following information in mind when you create a reference variable:

-   Reference variables use the [auto-complete feature](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_AutoCompleteForReferenceFields.md) . To ensure that users have enough information to make the selection, configure the [reference lookup list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_ReferenceLookup.md) .
-   Reference variables store the sys\_id of the selected record \(like reference fields\). To use the display value in a script, use the same methods as for a reference field.

```
current.variables.<variable name>.getDisplayValue()
```

\[Omitted image "VariableReferenceG.png"\] Alt text: A reference variable

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

[Lookup select box]()

[Custom and Custom with label]()

[Masked]()

[Multi-line text]()

[Multiple choice]()

[Numeric scale]()

[Requested for]()

[Rich Text Label]()

[Select box]()

[Single-line text]()

[UI page]()

[URL]()

[Wide single-line text]()

[Yes/No]()

[Variable support in various channels]()

