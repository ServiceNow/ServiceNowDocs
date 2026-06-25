---
title: Requested for
description: Before submitting a catalog item request, this variable helps you specify who this request can be submitted for.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-catalog/requested-for.html
release: australia
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Types of service catalog variables, Service catalog variables, Service Catalog Reference, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Requested for

Before submitting a catalog item request, this variable helps you specify who this request can be submitted for.

## Requested For

You should specify this information while answering catalog item questions.

**Important:**

-   You can only specify users from the User \[sys\_user\] table.
-   If you don’t specify the default value for this variable, the current logged-in user requesting the item is considered as the default Requested For variable value.
-   You can submit the request for a user based on access to a catalog item. The **Access Type** field of the catalog item can be used to specify if a request can be submitted for a user who does not have access to the catalog item.
-   For this variable, item variable assignment is not supported in the rule base of an order guide. If the order guide contains the Requested For variable, the value would be cascaded to the equivalent variable of items in the rule base as read-only.

Using the **Enable also request for** field of the Requested For variable, you can request a catalog item for different users under one request.

For information about delegated request experience, see [Delegated request experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/delegated-request-exp.md).

**Important:**

-   You can add this variable to a catalog item or variable set. However, when submitting the request, a catalog item can have only one Requested For variable.
-   You can add only one Requested For variable for a variable set.
-   This variable is not supported in a multi-row variable set.
-   After the request is submitted, this variable value is visible in the variable editor and variable summarizer.

\[Omitted image "ReqForVariable.png"\] Alt text: Screenshot for the Requested For variable

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

[Reference]()

[Rich Text Label]()

[Select box]()

[Single-line text]()

[UI page]()

[URL]()

[Wide single-line text]()

[Yes/No]()

[Variable support in various channels]()

