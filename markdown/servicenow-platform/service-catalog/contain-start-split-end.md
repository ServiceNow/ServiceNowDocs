---
title: Container start, container split, and container end
description: The container start, container split, and container end variables define a layout for a container that can hold more variables.
locale: en-US
release: zurich
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Types of service catalog variables, Service catalog variables, Service Catalog Reference, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Container start, container split, and container end

The container start, container split, and container end variables define a layout for a container that can hold more variables.

Use the container start and container end variables to define the start and end points of a container layout. The container end must be used along with the container start to close a container.

A container layout can be split into two or three columns using the container split variable. By default, the split is calculated at the 50% mark.

A container is similar to a [variable set](../concept/c_ServiceCatalogVariableSets.md). Unlike a variable set, containers can be used anywhere, including inside a variable set. Containers can also be nested inside each other.

For more help with selecting the appropriate container type, see the [Determining if you are using the correct container variable \[KB0539982\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0539982) article in the HI Knowledge Base.

**Note:**

-   The container variables are not yet supported on mobile devices.
-   Container start, container split, and container end variables are supported in Service Portal. However, if the settings are done on the top-level container, a maximum of two-column layouts can be achieved.
-   Variable sets are also considered as containers. So, a container start variable with a two-column layout under a variable set is not supported in Service Portal.

To reproduce the container shown in the following figure, enter the following settings when creating a container start variable:

-   Select a **Layout** with 2 Columns Wide, alternating sides.
-   Select the **Display title** check box to use a collapsible title bar.

![A variable container](../image/VariableContainerG.png "Example: container variable")

**Parent Topic:**[Types of service catalog variables](r_VariableTypes.md)

**Related topics**  


[Attachment](attachment.md)

[Break](break.md)

[Check box](check-box.md)

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

