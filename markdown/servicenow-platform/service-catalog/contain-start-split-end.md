---
title: Container start, container split, and container end
description: The container start, container split, and container end variables define a layout for a container that can hold more variables.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-catalog/contain-start-split-end.html
release: australia
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Types of service catalog variables, Service catalog variables, Service Catalog Reference, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Container start, container split, and container end

The container start, container split, and container end variables define a layout for a container that can hold more variables.

Use the container start and container end variables to define the start and end points of a container layout. The container end must be used along with the container start to close a container.

A container layout can be split into two or three columns using the container split variable. By default, the split is calculated at the 50% mark.

A container is similar to a [variable set](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/c_ServiceCatalogVariableSets.md). Unlike a variable set, containers can be used anywhere, including inside a variable set. Containers can also be nested inside each other.

For more help with selecting the appropriate container type, see the [Determining if you are using the correct container variable \[KB0539982\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0539982) article in the HI Knowledge Base.

**Note:**

-   The container variables are not yet supported on mobile devices.
-   Container start, container split, and container end variables are supported in Service Portal. However, if the settings are done on the top-level container, a maximum of two-column layouts can be achieved.
-   Variable sets are also considered as containers. So, a container start variable with a two-column layout under a variable set is not supported in Service Portal.

To reproduce the container shown in the following figure, enter the following settings when creating a container start variable:

-   Select a **Layout** with 2 Columns Wide, alternating sides.
-   Select the **Display title** check box to use a collapsible title bar.

\[Omitted image "VariableContainerG.png"\] Alt text: A variable container

**Parent Topic:**[Types of service catalog variables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/r_VariableTypes.md)

**Related topics**  


[Attachment]()

[Break]()

[Check box]()

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

