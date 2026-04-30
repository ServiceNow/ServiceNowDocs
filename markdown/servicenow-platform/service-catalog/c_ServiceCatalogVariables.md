---
title: Service catalog variables
description: Service catalog variables capture and pass on information about choices a customer makes when ordering a catalog item. Variables help define the structure of a catalog item form that is displayed to the customer.
locale: en-US
release: zurich
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Service Catalog Reference, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Service catalog variables

Service catalog variables capture and pass on information about choices a customer makes when ordering a catalog item. Variables help define the structure of a catalog item form that is displayed to the customer.

For example, you can define a variable called **Memory** to provide users with memory options at an extra cost for a PC catalog item. An Apple iPhone catalog item can use a variable called **Color** that allows customers to select the color when they order the phone from the catalog. You can define some variables to affect an item price, depending on the choices made.

Service Catalog provides several types of variables, which are also referred to as questions. Variables can be stored, accessed from multiple places, and passed between tasks in a process when fulfilling a request. They can be displayed on the Requested Item and Catalog Task forms after an item has been ordered.

You can define service catalog variables with the catalog\_admin role.

-   **[Types of service catalog variables](../reference/r_VariableTypes.md)**  
Variables allow you to specify questions for a catalog item. Several types of service catalog variables are provided. Some variable types accept variable attributes.
-   **[Create a service catalog variable](../task/t_CreateAVariableForACatalogItem.md)**  
Create service catalogs variables to gather information from users ordering a catalog item, for example, to ask users which options they want for the item.
-   **[Service catalog data lookup](c_ServiceCatalogDataLookup.md)**  
The Data Lookup and Record Matching Support for Service Catalog plugin offers similar features to the general Data Lookup and Record Matching Support plugin.
-   **[Audit service catalog variables](../task/t_AuditableServiceCatalogVariables.md)**  
Audit the variables so that the audit history records all changes to the named variables.
-   **[Service Catalog variable editors](service-catalog-variable-editor.md)**  
Variable editor displays variable values in fulfiller forms. A requester, while requesting the item, specifies these variable values in the catalog item questions.
-   **[Prefilling variable values on the catalog item form in the portal and Next Experience UIs](prefill-variable-values-catalog-item-form.md)**  
When catalog item requesters want to order items on portals or Next Experience UI, you can set the catalog items to use the key-value pairs, which prefill the variable values. The requesters can finish forms faster.

**Parent Topic:**[Service Catalog Reference](service-catalog-reference.md)

**Related topics**  


[Scriptable service catalog variables](https://www.servicenow.com/docs/access?context=c_ScriptableServiceCatalogVariables&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

[Use service catalog variables in a report – Report Designer](https://www.servicenow.com/docs/access?context=use-service-catalog-variables-in-report&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)

