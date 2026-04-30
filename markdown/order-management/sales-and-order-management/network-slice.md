---
title: Orders for 5G sliced networks
description: A communication service provider \(CSP\) can define 5G services in the technical catalog and manage the creation and fulfillment of these orders for a sliced network.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Managing service orders, Order Management, Use, Sales Customer Relationship Management]
---

# Orders for 5G sliced networks

A communication service provider \(CSP\) can define 5G services in the technical catalog and manage the creation and fulfillment of these orders for a sliced network.

## Network slicing

Network slicing refers to a method of partitioning a physical network into multiple, separate networks. These separate networks are called slices.

By slicing a 5G network, a CSP can do the following tasks:

-   Create and manage the slice templates with the required slice attributes in their product catalog.
-   Support slice specifications by using the slice templates to define the slice services.
-   Support the ingestion of slice orders from external systems through the existing product order API.
-   Decompose the slice orders and trigger the fulfillment workflows for the decomposed orders.
-   Trigger the southbound slice orders with southbound attributes toward southbound systems, such as Network Slice Management Function \(NSMF\), by using the service order open API.

## How a slicing order is managed

A product catalog administrator creates templates in the product catalog by defining the template characteristics and template characteristic options. When the product catalog administrator is finished creating the templates, they publish it to the product catalog. With this process, the product catalog administrator can create templates for the various types of slices with the slice attributes and attribute values for the 5G network services.

Next, the product catalog administrator maps the slice templates with the various specification categories. The product catalog administrator does the mapping by using the Template Selection Policy decision table in the Decision Builder. The mapped templates are automatically filled in the service specification form when a user selects a specification category. For a description of the Service specifications form fields, see .

**Note:**

-   If a specification category is mapped with multiple templates, the latest published template is considered to be in the service specification.
-   If a specification category is not mapped with any templates, the default category-template mapping is considered to be in the service specification.

The product catalog manager then uses the templates to define the new specifications for the 5G services.

After the 5G service specifications are created, they can be used in the slice order creation and fulfillment process. The 5G slice ordering process follows the existing order approval, decomposition, and fulfillment process in the Order Management application.

**Parent Topic:**[Managing service orders](managing-service-orders.md)

