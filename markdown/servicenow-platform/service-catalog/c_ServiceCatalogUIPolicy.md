---
title: Service catalog UI policy
description: UI policies can be used to define custom process flows for tasks.
locale: en-US
release: zurich
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Debugging Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Service catalog UI policy

UI policies can be used to define custom process flows for tasks.

Catalog UI policies control the behavior of catalog item forms when presented to your users. Catalog UI policies can be applied to a catalog item or a variable set.

[UI policies](https://www.servicenow.com/docs/access?context=t_CreateAUIPolicy&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) are useful when applied to service catalog items. Keep the following points in mind when creating service catalog UI policies:

-   A catalog UI policy applies to either a specific catalog item or any item that uses a specific variable set.
-   A catalog UI policy can only contain and reference variables that are defined for the catalog item or variable set.
-   Like UI policy conditions, the variables in a service catalog UI policy condition must be visible \(even if hidden by UI policy or read-only\) on the form for the condition to be tested. Also, ensure that the variables have names. For more information, see [Create a catalog client script](https://www.servicenow.com/docs/access?context=c_CatalogClientScriptCreation&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).
-   Limited UI policy functionality applies to following variables:
    -   The Mandatory and Read Only policy do not apply to the following variable types: Break, Container Split, Container End, UI Macro, UI Macro with Label, Label, UI Page.
    -   The Set visible policy does not apply to the following variable types: Break, Container Split, Container End.
-   Service catalog UI policies are applied to variables and variable sets of catalog items ordered in the service catalog. Policies can also be applied when the variables are present in a Requested Item or Catalog Task form.

    **Note:** The **Clear the variable value** UI policy action is not applicable on variable sets and containers.

-   Catalog UI policy actions can be applied on a variable set. The actions on a variable set are applied on all variables within the variable set. If different catalog UI policy actions are applied on a variable or a variable set, the action with the lowest order is considered.
-   The priority order for UI actions types is:

    1.  Mandatory \(highest\)
    2.  ReadOnly/Display
    If a variable is set to mandatory and does not have value, readonly or hide do not work on that variable. If a variable is hidden or readonly, and then set to mandatory, the variable field becomes visible or editable.

    This priority order is also applicable for variable sets and containers. If a variable set or container has a mandatory variable without any value, then the container or variable set cannot be hidden.

-   Catalog UI policies are supported for catalog items viewed in a service catalog wizard.

    **Note:** The UI policy for catalog items always takes precedence over UI policy for variable sets. You can change this behavior by editing the **glide.sc.ui\_policy.variable\_set\_run\_first** property.


-   **[Create a UI policy for catalog items](../task/t_CreatUIPolicyForSvcCalgIt.md#)**  
You can apply UI policies for catalog items ordered in the service catalog.

**Parent Topic:**[Debugging Service Catalog](debugging-service-catalog.md)

