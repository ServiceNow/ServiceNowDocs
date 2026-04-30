---
title: Lookup select box
description: The lookup select box variable creates a choice list using data queried from a table. Its functionality is similar to the lookup multiple choice variable, which creates radio buttons from queried data.
locale: en-US
release: xanadu
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2025-01-20"
reading_time_minutes: 3
breadcrumb: [Types of service catalog variables, Service catalog variables, Service Catalog Reference, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Lookup select box

The lookup select box variable creates a choice list using data queried from a table. Its functionality is similar to the lookup multiple choice variable, which creates radio buttons from queried data.

For attributes supported by this variable, see [variable attributes](variable-attributes.md).

To create the lookup select box, enter the following values when creating the variable:

-   **Lookup from table**: `Incident [incident]`
-   **Lookup value field**: `Sys ID`
-   **Lookup label field**: `number, category, priority`
-   **Reference qual**: `caller_id=javascript:gs.getUserID()^active=true`

**Note:**

-   Table with large data causes performance issues when loading the page. Use reference qualifiers to reduce data or use the reference type variable.
-   You cannot add more than 10,000 choices.

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

