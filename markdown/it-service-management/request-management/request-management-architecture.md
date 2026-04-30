---
title: Request Management architecture
description: Request Management allows catalog items to be requested and fulfilled based on defined flows.
locale: en-US
release: yokohama
product: Request Management
classification: request-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Explore, Request Management, IT Service Management]
---

# Request Management architecture

Request Management allows catalog items to be requested and fulfilled based on defined flows.

## Request Management hierarchy

Service Catalog is the starting point of the request management process. The request management process is triggered only when a catalog item from the Catalog Item \[sc\_cat\_item\] table is requested.

When a user submits a request for a catalog item, records are generated in the following hierarchy.

**Note:** Variables are associated only with the Requested Item \[sc\_req\_item\] table. Variables are not supported for extended tables.

![Screenshot for the Request Management hierarchy](../image/requestManagement.png "Request Management hierarchy")

**Note:** When you configure Request Management:

-   The data model does not support a record producer generating request management objects such as request, request item, and catalog task. Hence, do not use a record producer to insert records in the following request management tables or their extensions:
    -   Request \[sc\_request\]
    -   Request Item \[sc\_req\_item\]
    -   Catalog Task \[sc\_task\]
-   Do not write business rules with the `before` trigger for the following tables:
    -   Request \[sc\_request\]
    -   Request Item \[sc\_req\_item\]
    -   Cart \[sc\_cart\]
    -   Cart Item \[sc\_cart\_item\]

## Request management process

-   **Catalog item is ordered directly without adding it to the cart**

    When a catalog item is ordered or requested directly without adding it to the cart, the following steps are performed:

    1.  A temporary cart, sc\_cart, is created.
    2.  The catalog item along with the variables \(values entered by the user\) is added to the temporary cart as a record in the Cart Item \[sc\_cart\_item\] table.
    3.  The variables are saved in the Options \[sc\_item\_option\] and Variable Ownership \[sc\_item\_option\_mtom\] tables.
    4.  The temporary cart is checked out by performing these steps.
        1.  A record in the Request \[sc\_request\] table is initialized but not committed in the database.
        2.  A record in Request Item \[sc\_req\_item\] table is initialized but not committed in the database.
        3.  The request reference for the Request Item \[sc\_req\_item\] table record is updated with the Request \[sc\_request\] table record.
        4.  The variables record in the Options \[sc\_item\_option\] and Variable Ownership \[sc\_item\_option\_mtom\] tables are updated based on the Request Item \[sc\_req\_item\] table record.
        5.  The Request Item \[sc\_req\_item\] table record is committed in the database.
        6.  The Request \[sc\_request\] table record is committed in the database.
-   **Request is submitted after adding the item to the cart**

    If a catalog item is added to the cart and the request is submitted using the checkout process, the default cart is checked out.

    All steps mentioned in the preceding scenario, Catalog item is ordered directly without adding it to the cart, are applicable. However, if multiple catalog items are added to the cart, step b to step e are repeated for each item.

-   **Request is submitted using an order guide**

    For a two-step order guide checkout, the temporary cart is used for all items. For a three-step order guide checkout, the default cart is used for the items.

    All steps mentioned in the preceding scenario, Catalog item is ordered directly without adding it to the cart, are applicable.


**Note:** The base system workflow attached to the request is demo data.

**Parent Topic:**[Exploring Request Management](../../request-management/concept/exploring-request-management.md)

**Related topics**  


[Create a catalog request in Agent Workspace](../../service-catalog-management/task/create-request-workspace.md)

[Create a request from Universal Request](../../request-management/task/create-request-from-ur.md)

