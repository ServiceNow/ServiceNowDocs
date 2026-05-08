---
title: Reference
description: A reference variable references a record in another table. For example, a variable named point\_of\_contact references the User \[sys\_user\] table.
locale: en-US
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

For attributes supported by this variable, see [variable attributes](variable-attributes.md).

Keep the following information in mind when you create a reference variable:

-   Reference variables use the auto-complete feature . To ensure that users have enough information to make the selection, configure the reference lookup list .
-   Reference variables store the sys\_id of the selected record \(like reference fields\). To use the display value in a script, use the same methods as for a reference field.

```
current.variables.<variable name>.getDisplayValue()
```

![A reference variable](../image/VariableReferenceG.png "Example: reference variable")

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

[Custom and Custom with label](custom.md)

[Masked](masked.md)

[Multi-line text](multi-line.md)

[Multiple choice](multiple-choice.md)

[Numeric scale](numeric-scale.md)

[Requested for](requested-for.md)

[Rich Text Label](rich-text-label.md)

[Select box](select-box.md)

[Single-line text](single-line-text.md)

[UI page](ui-page.md)

[URL](url.md)

[Wide single-line text](wide-single-line-text.md)

[Yes/No](yes-no.md)

[Variable support in various channels](variables-availability.md)

