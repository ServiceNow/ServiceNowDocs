---
title: Service catalog variable sets
description: Administrators and catalog administrators often define multiple catalog items that use the same group of service catalog variables. Catalog managers and catalog editors can attach a variable set for items to which they are assigned. However, catalog managers and catalog editors cannot create a variable set.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Service Catalog Reference, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Service catalog variable sets

Administrators and catalog administrators often define multiple catalog items that use the same group of service catalog variables. Catalog managers and catalog editors can attach a variable set for items to which they are assigned. However, catalog managers and catalog editors cannot create a variable set.

For example, a catalog administrator defines 10 catalog items for types of servers. The request process for all these items asks the same five questions, using the same variables.

Associating these variables individually per catalog item is repetitive, time-consuming, and error-prone. Also, to make a single change to multiple catalog items involves manually changing each item. For example, to add a variable to 10 catalog items, you would need to manually associate the variable with each item.

Variable sets allow you to create a collection of variables that can be reused across multiple catalog items and order guides. Using variable sets saves time because you do not have to create the same variables individually for many catalog items. Also, when variables should be modified, you can modify the variable set and the changes are reflected across all the catalog items that are associated with the variable set.

Variable sets also allow you to define catalog client scripts and UI policies that are applicable to the variables in the set.

**Note:** Variables in a set use the same rules as other variables to determine when the variables in a set appear on a task. For example, variables must either be global or be attached directly to an item.

A catalog administrator can provide read, write, and update roles to access a variable set. When you access variables of a variable set, a validation is first done at the variable set level, and then at the variable level. If the access is blocked at the variable set level, then the access settings on the variable are over-ridden. If the access is allowed at the variable set level, then access at the variable level is verified.

**Note:** Both single-row and multi-row variable sets are supported in ServiceNow AI Platform, Service Portal, Now Mobile, and in the Variable editor in Agent Workspace.

## Single-row variable set

Use a single-row variable set to capture data from variables that are grouped together, while submitting a catalog item request for a single entity.

## Multi-row variable set

Use a multi-row variable set \(MRVS\) to capture variable data in a grid layout while submitting a catalog item request for a group of entities. For example, for HR during the reorganization of employees, a single record producer should be able to capture the relevant information such as the department and manager for a group of employees. Also, when you request a catalog item to order virtual machines and servers, configuration options should be captured as a single request. In this case, a requester can define multiple hardware units as rows and their configuration options as columns of an MRVS.

You cannot include the following variable types in an MRVS:

-   Attachment
-   Break
-   Container End
-   Container Start
-   Container Split
-   HTML
-   Label
-   Macro
-   Macro with label
-   Rich Text Label
-   UI Page

**Note:**

-   You can configure an MRVS variable to disallow duplicate values. For information about the **Unique** field, see [Create a service catalog variable](../task/t_CreateAVariableForACatalogItem.md).
-   You can hide a variable in the MRVS so that it does not appear when the dialog box is open.
-   The **Map to field** functionality is not supported for variables used in an MRVS.
-   Only the glide list interface is supported for the List Collector variable.
-   Cascading functionality for variables in an order guide is not supported in an MRVS.
-   An MRVS is not displayed when added within a container.
-   You cannot add variables with read roles in an MRVS.
-   When you clone a request that contains an MRVS, the information that is specified in the MRVS is available in all cloned requests. All UI policies and client scripts on the MRVS are also cloned.
-   Set a limit to the number of rows that you can add to an MRVS by using the **max\_rows** attribute in the **Variable Set attributes** field.
-   In the RITM and request view in Now Mobile, an MRVS is not supported. A message is displayed in this view that this variable set is not viewable.
-   An MRVS is supported in the variable summarizer only in Service Portal.
-   You can include an MRVS in the GetCatalogVariables and CreateCatalogTask actions using Workflow Studio.
-   You can iterate through individual rows and access variables using the For Each flow logic.
-   You can include MRVS while creating a catalog task using a workflow.

An MRVS form changes dynamically based on the data in the catalog item form that includes the following:

-   Other rows of that MRVS
-   Other variables outside of that MRVS on the catalog item form.

For information about accessing data in a multi-row variable set \(MRVS\) when a dialog box is open, see g\_service\_catalog - Client.

You can define catalog client scripts, catalog UI policies, and catalog data lookups for an MRVS. Visibility is honored just on the MRVS form and not in the list.

**Note:**

-   onSubmit catalog client scripts are not supported for an MRVS.
-   Catalog UI policies and catalog client scripts defined at the item level are not applicable for variables in an MRVS. Only those catalog UI policies and catalog client scripts defined within the MRVS are applicable for variables in the MRVS.
-   Scripts that are not included in an MRVS cannot affect variables inside the MRVS. Similarly, the scripts included in the MRVS cannot affect the variables that are not included in the MRVS.
-   Variables that are not included in an MRVS cannot be used in dependent reference qualifiers for variables in the MRVS. Similarly, the variables included in the MRVS cannot be used in dependent reference qualifiers for variables that are not in the MRVS. For a reference qualifier, the current row is the one that is being edited.

You cannot set **Global** as `True` for any variable that belongs to an MRVS. So, an MRVS is not available in catalog tasks.

If the variables included in the MRVS have price implications for a catalog item, the price of the catalog item reflects the corresponding changes when a row is added, edited, or removed from this variable set.

**Note:** When you disable the **glide.sc.use\_cart\_layouts** property, the Order Item Widget does not reflect the price changes of the item from the MRVS. However, when you add this item to the cart, these price changes are reflected.

You cannot select variables of an MRVS when defining the following for a catalog item:

-   UI policy conditions
-   Unsupported ATF step configurations. You can only validate if an MRVS is visible, mandatory, or read only.
-   Reporting

-   **[Create a variable set and add it to an item](../task/t_CreateAVariableSet.md#)**  
Create a set of variables and add them to multiple catalog items and order guides for reuse.
-   **[Variable set layout](c_DefineVariableSetLayout.md#)**  
Variable sets can have one of many layouts. You can define the order of the variables for each item.

**Parent Topic:**[Service Catalog Reference](service-catalog-reference.md)

