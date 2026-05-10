---
title: Custom and Custom with label
description: The custom variable inserts a UI macro into the catalog item. Custom with label variable inserts a UI macro with a label.
locale: en-US
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

![A Custom variable](../image/Macro.png "Example: Custom variable")

## Custom with label

This variable inserts a UI macro with a label.

-   This variable is not yet supported on Classic Mobile devices.
-   This variable is supported in Service Portal through widgets. Create a widget with the same functionality as that of a macro with label, and link it with the variable.

![A Custom with label variable](../image/MacroWithLabel.png "Example: Custom with label variable")

**Parent Topic:**[Types of service catalog variables](r_VariableTypes.md)

**Related topics**  


[Attachment](attachment.md)

[Break](break.md)

[Check box](check-box.md)

[Container start, container split, and container end](contain-start-split-end.md)

[Date, Date and time, and Duration](date.md)

[Email](email.md)

[HTML](html.md)

[IP Address](ip-address.md)

[Label](label.md)

[List collector](list-collector.md)

[Lookup multiple choice](lookup-multiple-choice.md)

[Lookup select box](lookup-select-box.md)

[Masked](masked.md)

[Multi-line text](multi-line.md)

[Multiple choice](multiple-choice.md)

[Numeric scale](numeric-scale.md)

[Reference](reference.md)

[Requested for](requested-for.md)

[Rich Text Label](rich-text-label.md)

[Select box](select-box.md)

[Single-line text](single-line-text.md)

[UI page](ui-page.md)

[URL](url.md)

[Wide single-line text](wide-single-line-text.md)

[Yes/No](yes-no.md)

[Variable support in various channels](variables-availability.md)

