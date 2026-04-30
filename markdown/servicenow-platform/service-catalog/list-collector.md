---
title: List collector
description: The list collector variable creates an interface that lets you select and add multiple records from a table.
locale: en-US
release: yokohama
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Types of service catalog variables, Service catalog variables, Service Catalog Reference, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# List collector

The list collector variable creates an interface that lets you select and add multiple records from a table.

For attributes supported by this variable, see [variable attributes](variable-attributes.md).

![A list collector variable](../image/VariableListCollectorG.png "Example: list collector variable")

**Note:**

-   The Reference Qualifier and glide\_list attribute applies to releases from Helsinki onward only. The attribute does not apply to Geneva.
-   You can set a value for this variable using the g\_form.setValue\(\) function in a catalog client script.
-   When the glide\_list attribute is not true, you can only set the value that is visible in the **Available** list using the g\_form.setValue\(\) function. This functionality is not applicable when the setValue\(\) function is called onLoad.
-   Table with large data causes performance issues when loading the page. Use reference qualifiers to reduce data or use the glide\_list attribute.
-   The values in the referenced table do not appear if the user is not logged in.
-   The list collector displays a maximum of 100 items in a list. After moving items to the **Selected** list, you can click **Run Filter** to refresh the **Available** list. This action will add more available items to the list, to a maximum of 100 items.

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

[Lookup multiple choice](lookup-multiple-choice.md)

[Lookup select box](lookup-select-box.md)

[Custom and Custom with label](custom.md)

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

