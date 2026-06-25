---
title: Custom and Custom with label
description: The custom variable inserts a UI macro into the catalog item. Custom with label variable inserts a UI macro with a label.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-catalog/custom.html
release: australia
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Types of service catalog variables, Service catalog variables, Service Catalog Reference, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Custom and Custom with label

The custom variable inserts a UI macro into the catalog item. Custom with label variable inserts a UI macro with a label.

## Custom

This variable inserts a UI macro into the catalog item.

UI macros in the service catalog do not support the following glide\_list functions: clickthrough, slushbucket editing, and email field.

-   Use [phase one](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/c_ExtensionsToJellySyntax.md) Jelly only for any UI macros added as variables. Phase two Jelly within the macro is not processed and appears on the page as standard content.
-   This variable is not yet supported on Classic Mobile devices.
-   This variable is supported in Service Portal through widgets. Create a widget with the same functionality as that of a macro and link the widget with the variable.

\[Omitted image "Macro.png"\] Alt text: A Custom variable

## Custom with label

This variable inserts a UI macro with a label.

-   This variable is not yet supported on Classic Mobile devices.
-   This variable is supported in Service Portal through widgets. Create a widget with the same functionality as that of a macro with label, and link it with the variable.

\[Omitted image "MacroWithLabel.png"\] Alt text: A Custom with label variable

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

