---
title: Configuring order fulfillment
description: Order fulfillment is the process for fulfilling customer orders by using Workflow Studio.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Order management, Configure, Sales Customer Relationship Management]
---

# Configuring order fulfillment

Order fulfillment is the process for fulfilling customer orders by using Workflow Studio.

Order fulfillment, also referred to as order orchestration, defines how to coordinate the fulfillment of orders. You can define the order fulfillment processes that you require and then configure them by performing the tasks in the following table.

|Task|Description|
|----|-----------|
|Configure subflows for order fulfillment|Subflows define the task flow for fulfillment agents to fulfill customer orders. You can copy a subflow from the base system and make changes for your business needs. For more information on configuring subflows, see [Building Subflows](https://www.servicenow.com/docs/access?context=subflows&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).|
|Configure decision tables for order fulfillment|Decision tables define the conditions for triggering the order fulfillment subflow. The Order Management for Telecommunications, Media, and Technology application uses the Order fulfillment Policy decision table. For more information on configuring decision tables, see [Decision tables](https://www.servicenow.com/docs/access?context=decision-table&version=zurich&pubname=zurich-application-development&ft:locale=en-US).|
|Configure order assignment rules to route tasks to agents, based on their skill sets|For more information on assignment rules, see [Create an assignment rule](https://www.servicenow.com/docs/access?context=t_AssignmentModuleRule&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).|

-   **[Flow actions for fulfillment subflow definition](../reference/order-mgt-flow-actions-fulfillment-subflows.md)**  
If you define your own fulfillment subflows in Workflow Studio, you can use the standard flow actions that are available in the ServiceNow AI Platform. Each action deals with different aspects of the fulfillment or inventory maintenance that provides some consistency in retrieving and updating data.
-   **[Integrate with Field Service Management](../../customer-service-management/task/activate-fsm-csm-integration.md)**  
Customer Service Management provides an integration with the Field Service Management application. This integration enables you to view work order and work order task information from a case.
-   **[Configure customer product data management](../../customer-service-management/task/configure-customer-product-data-management.md)**  
Learn how to use the sn\_ind\_tmt\_orm.enable\_prod\_invt\_for\_order\_management system property to either create sold products or product inventory records after an order is completed and fulfilled.

**Parent Topic:**[Configuring Order Management](order-mgt-configuring.md)

