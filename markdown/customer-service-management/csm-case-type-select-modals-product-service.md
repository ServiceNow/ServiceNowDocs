---
title: Product Service select version of the case type selector
description: With the Product Service select version of the case type selector, agents can create cases of the correct type based on the selected product or service.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Case type selector, Customer service case types, Case management, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Product Service select version of the case type selector

With the Product Service select version of the case type selector, agents can create cases of the correct type based on the selected product or service.

The Product Service select version of the case type selector supports services as well as case types. This version of the case type selector makes it easier for agents to find the available services for a product. This version of the case type selector enables the agent to do the following:

-   Select a product from a list of products owned by the account or consumer and see the available services for that product. This list includes sold products and install base items.
-   Select a category of services and see the available services within that category.
-   Search for a service by entering keywords in the search box.
-   Browse the available services using scroll bars and pagination.
-   Select a service and create a case based on the service or case type.

![Product Service select version of the case type selector with fields for selecting a product, service category, and service](../image/product-service-select-modal.png "Case type selector (Product Service select version)")

## Creating cases using the Product Service select version

The system displays the case type selector when an agent creates a case from a list or a record. The fields that are available in the Product Service select version of the case type selector are context-driven based on how an agent creates a case.

<table id="table_ulq_m3j_yxb"><thead><tr><th>

Agent action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Select **New**

</td><td>

Select this action from case lists and case type lists such as My Cases or My Complaint Cases.

</td></tr><tr><td>

Select **Create Case**

</td><td>

Select this action from the following records:-   Interaction
-   Account
-   Contact
-   Consumer
-   Sold Product
-   Install Base Item
-   Case
-   Child Case

</td></tr></tbody>
</table>## Creating cases from a record

When creating a case from a record, the Product Service select version of the case type selector includes the following sections and fields:

<table id="table_px4_nkf_svb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Product filter

</td><td>

Use the fields in this section to select a product

</td></tr><tr><td>

Only show services related to owned products

</td><td>

This check box controls the display of the **Owned product** field and determines the services included in the Services section.-   If checked, the system lists the services categorized as post-sales that are relevant to the product selected in the **Owned product** field.
-   If cleared, the system lists the services categorized as pre-sales and general.

</td></tr><tr><td>

Owned product

</td><td>

Use the **Owned product** field to select a product.

 This field uses typeahead search. Place the cursor in the field and start typing to display a list of products. Selecting a product filters the available services in the Services section.

 For sold products and install base items, the first line of an entry in the **Product** drop-down list displays the name of the product from the Product Model record. The second line displays the name of the sold product or install base item associated with the product model.

</td></tr><tr><td>

Service category

</td><td>

Select a category to see the available services within that category or select **All categories** to see all available services.

</td></tr><tr><td>

Services

</td><td>

Select a service in the Services section.-   Services are displayed in a card format that show the service name, description, and image or icon.
-   Use a keyword search to narrow the list of available services.
-   Use the scroll bars and pagination to view the available services.

</td></tr></tbody>
</table>Agents can select **Create Case** from the following records, which provide context about their owned products and services.

|Record|Description|
|------|-----------|
|Interaction|Applicable services are based on products owned by the contact or consumer.|
|Account|Applicable services are based on products owned by the account.|
|Contact|Applicable services are based on products owned by the contact and products that the contact has access to based on related party access.|
|Consumer|Applicable services are based on products owned by the consumer.|
|Sold Product|The **Owned product** field is auto-filled with the product model from the Sold Product record.|
|Install Base Item|The **Owned product** field is auto-filled with the product model if the install base item is mapped to the product model. If there's no product model associated with the install base item, the **Owed product** field lists the products for the account and contact.|
|Case| |
|Child Case| |

## Creating cases from a list

Agents can select **New** from a case list or case type. Because there's no customer context, the services listed include all available services \(pre-sale, post-sale, and general\).

## Service categories

The administrator can group services into categories so that it's easier for agents to find the services the need. Categories are displayed in the Service categories section. Agents can select a specific category to see the available services within that group or **All categories** to see all available services.

## Service cards

The Product Service select version of the case type selector displays the available services in a card view. Each card can include the following information for a service, depending on the configuration:

-   Name
-   Description
-   Image

When an administrator creates a service definition, they can provide a name for the service. They can also provide a description of the service and add an image to represent the service. For more information, see [Create a service definition](../task/create-csm-service-definition.md).

## Browsing services in the case type selector

Agents can browse the available services for a selected category or for all categories. These services are displayed in a card view.

The Product Service select version of the case type selector can display multiple pages of services. It can display 24 services at a time and a total of 200 services.

The agent can perform the following actions:

-   Use the scroll bars to view all the displayed services.
-   Select **Show more** to see the next set of services \(up to a maximum of 200\) if more than 24 services are available.
-   Filter the displayed services by selecting a category.
-   View a count of the available services after applying a filter.

**Note:** The system displays the services that the logged-in agent has access to.

When the agent reaches the limit of 200 services, the system directs the agent to refine the results.

## Searching for a service

Agents can search for a service by entering keywords in the search box.

-   A list of recent searches appears below the search box
-   Search results include the services with names or descriptions that contain the keywords.
-   Results are displayed in a card view.

## Creating a case for a service

Agents can create cases from lists and from records.

Agents can create cases by selecting a service from the Product Service select version of the case type selector and then selecting **Create Case**.

Agents see the Product Service select version with the Product filter when they create a case from the following records.

-   Interaction
-   Account
-   Contact
-   Consumer
-   Sold Product
-   Install Base
-   Case
-   Child Case

The **Only show services related to owned products** check box is selected by default.

-   When selected, the agent can see Post-sales services.
-   When cleared, the agent can see Pre-sales, Post-sales, and General services.

If the agent is on a Sold Product or Install Base record, the **Owned product** field is auto-populated.

If a customer hasn't activated the install base:

-   The Product Service Select version displays the **Service** and **Case type** fields.
-   The **Service** field lists all services, including pre-sales and post-sales.
-   Agents can select **Create Case** from an interaction, account, contact, or consumer record and select a case type in the **Case type** field.

## Case type selector configuration

The Product Service select version of the case type selector includes a product filter. If you have the administrator role, you can configure the case type selector to hide this filter.

By default, this configuration setting is false. The case type selector displays the product filter, the **Only show services related to owned products** check box is empty, and the case type selector shows all available service definitions.

To hide the filter:

1.  In the application navigator, **sys\_declarative\_action\_payload\_definition.list** and press **Enter**.
2.  In the Key column, select **CREATE\_CASE\_TYPE**.
3.  In the **Payload** field, locate the **hideProductFilter** setting.
4.  Change the value of the setting from false to true and select **Update**.

When this configuration setting is true, the case type selector doesn't display the product filter. The case type selector shows all available service definitions.

