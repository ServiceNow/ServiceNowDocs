---
title: Order guides
description: Order guide submits a single service catalog request that generates several items.
locale: en-US
release: yokohama
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Types of catalog items, Exploring Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Order guides

Order guide submits a single service catalog request that generates several items.

For example, a New Employee Hire order guide can contain several items that new employees commonly need, such as business cards, computer, and cell phone. After selecting this order guide, the customer can then provide information about the new employee, including location and job title. The order guide then submits an order for catalog items like business cards, based on the details provided.

Order guides determine which catalog items to order by evaluating order guide rule conditions. Information the customer enters within the order guide can be passed as cascading variables to the ordered items, allowing common information to be reused across multiple items.

Administrators and catalog administrators can create order guides for the service catalog.

Order guides can be run automatically, generating a set of ordered items without needing to manually submit a service catalog request. For example, an onboarding workflow for a new employee can automatically run an order guide to order items for that employee. Order guides can also be configured to order the items of an order guide in a logical sequence. For example, you can configure your order guide to run the request for a new laptop before running the request for a new email.

Use the **Script** field in an order guide to add or remove catalog items to or from the order guide. Add catalog items to the order guide form by configuring the form layout.

-   To add a catalog item that is not added to the order guide via a rule base, write the following code in the script field:

    ```
    guide.add(“<sys_id_of_cat_item>")
    ```

-   To remove a catalog item that is added to the order guide via a rule base, write the following code in the script field:

    ```
    guide.remove(“<sys_id_of_cat_item>")
    ```


-   **[Create an order guide](../task/t_CreateAnOrderGuide.md)**  
You can create an order guide with a two-step or three-step ordering process.
-   **[Request an order guide](../task/t_OrderProcess.md#)**  
Once created, order guides present the customer with a three-step ordering process by default.
-   **[Create an order guide rule to add a catalog item](../task/t_CreateARule.md)**  
You can add a catalog item to an order guide using specific rules.
-   **[Create an order guide variable](c_CreateVariables.md)**  
You can create variables within an order guide.
-   **[Avoid enforcement of a mandatory field](../task/t_AvoidEnforceOfMandFieldWinTab.md)**  
You can avoid enforcing a mandatory field within tabs.
-   **[Run order guides automatically](c_RunOrderGuidesAutomatically.md)**  
You can run an order guide automatically from within a workflow or a server script, passing parameters to that order guide to define variable values.

**Parent Topic:**[Types of catalog items](../reference/r_ExtendedCatalogItemFunctions.md)

