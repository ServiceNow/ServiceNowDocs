---
title: Order management
description: The Order Management application streamlines the order life cycle from capture to fulfillment. It automates decomposition, enrichment, and orchestration workflows, empowering users to accelerate delivery, reduce fallouts, and manage complex orders efficiently through a unified workspace and customer portal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/explore-order-management.html
release: australia
topic_type: concept
last_updated: "2025-12-04"
reading_time_minutes: 8
keywords: [explore]
breadcrumb: [Explore, Sales Customer Relationship Management]
---

# Order management

The Order Management application streamlines the order life cycle from capture to fulfillment. It automates decomposition, enrichment, and orchestration workflows, empowering users to accelerate delivery, reduce fallouts, and manage complex orders efficiently through a unified workspace and customer portal.

## Order Management overview

Automate and streamline the complex process of capturing and fulfilling customer orders with Order Management, a central hub that connects sales, operations, and technical teams.

-   Order decomposition: Automatically break down a single, complex customer order into smaller, manageable tasks using predefine product catalogs and decomposition rules.
-   Pricing capabilities: Ensure accurate billing with dynamic price lists, pricing matrices, and adjustment features.
-   Order enrichment: Add necessary data to orders post-capture before they're decomposed.
-   Single source of truth: Establish a unified source for all order data, eliminating silos and ensuring real-time consistency for all stakeholders.
-   Jeopardy and fallout management: Proactively flag at risk orders and automate the handling of fulfillment errors to manage issues effectively.

With Telecommunications Service Management \(TSM\) or Technology Provider Service Management \(TPSM\) subscriptions, you can use workflows that help you manage your industry-specific products and services.

## Order Management users

|User|Description|
|----|-----------|
|Customer|Accesses the Business Portal to browse catalogs, place and track orders, raise issues or request changes to orders, or work offline with agents to place orders or request services.|
|Order agent|Engages with customers and helps them place orders.|
|Order fulfillment agent|Monitors the fulfillment process and updates fulfillment tasks such as receiving, reviewing, and processing orders.|
|Order manager|Manages customer and service orders.|
|Order approver|Approves customer orders and ensures order accuracy.|
|Order fulfillment manager|Manages order fulfillment tasks, reviews and approves orders.|
|Order fallout agent|Investigates and diagnoses order fallout issues, eliminates order processing errors, and unblocks blocked orders.|
|Order fallout manager|Oversees order fallout agent and monitors fallout tasks to ensure that order fallouts are being addressed.|
|Process admin|Manages automated Order Management workflows such as order enrichment, order decomposition, jeopardy management, and so on.|

## Order Management workflow

The following illustration describes the tasks involved in configuring and using Order Management to manage the end-to-end order life cycle.

\[Omitted image "order-management-workflow-landing.svg"\] Alt text: Infographic showing how process admins configure flows and orchestration logic for sales agents and managers who then capture and fulfill orders. For details, refer to the following description.

1.  Process admins create order enrichment flows, decomposition rules, order orchestration plans, and order fallout logic using Workflow Studio and decision tables. Optionally, they also install and configure Jeopardy Management.
2.  Order agent initiates the order life cycle by capturing an order in Order Management.
3.  The fulfillment agent captures additional technical information essential to fulfillment.
4.  The fulfillment manager reviews the order for accuracy and approves the order.
5.  The system creates domain orders \(product, service, and resource orders\) based on the specification relationships set in the product catalog and decomposition rules. If some of the information isn’t available when order decomposition starts, Order Management can stagger the decomposition to create certain orders using the information available at the time. Order tasks and work orders are created and assigned to the fulfillment based on the orchestration logic.
6.  Using the order timeline view and orchestration UI, the fulfillment manager monitors the order status, fallouts, and jeopardy scenarios.
7.  The fulfillment agents fulfill the order. This could involving installing products at customer sites or provisioning services.
8.  After all order tasks are complete and order is closed, the product inventory records are created, which can be used to cater to future customer requests like disconnecting, suspending, or resuming products or services. The system also creates contracts and entitlements against the sold products and services respectively.

## Order Management benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Create and implement enrichment flows that the system applies during order orchestration.|[Configure order enrichment flows using Decision Tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configure-order-enrichment.md)|Process admin|
|Configure jeopardy management rules to monitor fulfillment tasks ans alert managers when tasks are at risk.|[Configuring Jeopardy Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configuring-jeopardy-management.md)|Fulfillment managers|
|Detect errors or exceptions during order processing and take corrective actions to improve SLA compliance and expedite order processing.|[Managing order fallout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/fallout-management-overview.md)|Fallout agent|
|Create and track orders via the workspace, or import orders from third-party systems.|[Methods of creating orders in Sales Customer Relationship Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/order-capture-methods-som.md)|Order agents|
|Speed up fulfillment with orchestration workflows driven by an advanced product catalog using the order orchestration UI.|[Using the order orchestration UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/orchestration-plans-for-order-fulfillment.md)|Fulfillment agents, fulfillment managers|
|Track orders, prioritize tasks, and allocate resources using Gantt charts to see order status and risks.|[View an order timeline](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/view-order-timelines.md)|Fulfillment agents, fulfillment managers|
|Drive flexibility and efficiency of complex order orchestration by processing domain orders when the required information becomes available.|[Staggered decomposition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/staggered-decomposition.md)|Fulfillment agents|
|Enable post-sale support and drive customer satisfaction by effectively managing customers requests for disconnecting, suspending, or resuming products or services.|[Managing post-fulfillment order changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/managing-orders.md)|Order agents|

## Order Management variants

The industry-agnostic Order Management \(sn\_ind\_tmt\_orm\) application supports a wide range of order processes for retail, e-commerce, and standard business operations. It focuses on product catalog management, order capture, and fulfillment, and is suitable for businesses with straightforward order processes. Key features include the ability to:

-   Define products, underlying services, and the relationships between them.
-   Create offerings for these products and services and market them to customers.
-   Capture and enrich new orders received through channels which include the Product Order and Service Order Open API.
-   Decompose orders into the appropriate product, service, and resource orders, and order tasks required to fulfill those orders.
-   Define catalog rules that dictate how order characteristics are propagated and transformed during order fulfillment.
-   Manage and orchestrate product, service, and resource orders to the external fulfillment and billing systems.
-   Identify order fallout and automatically route fallout tasks to the appropriate team to investigate and diagnose.

The demo data available with Order Management demonstrates order intake and fulfillment for enterprise mobility products.

The Order Management for Telecommunications, Media, and Technology application \(sn\_om\_tmt\) is a tailored version of the industry-agnostic Order Management \(sn\_ind\_tmt\_orm\) application, suitable for telecommunications and technology service providers. It contains reusable demo data related to telecom-specific offerings, specifications, decision tables, flows, ordering, and inventory. It provides TM Forum-compliant APIs for order capture and fulfillment. It enables you to handle complex service orders including:

-   Single-domain service orders
-   Multi-domain service orders
-   All ordering scenarios including number portability
-   Integration with network inventory, resource provisioning, service activation, field service, billing, ERP, assurance, and partner provisioning.

The following are some key differentiators for Order Management for Telecommunications, Media, and Technology:

-   **Complex product bundles**

    Handles highly intricate product and service bundles common in telecom \(for example, voice, data, TV packages\) and technology \(XaaS, cloud services\).

-   **Subscription and usage-based billing**

    Native support for the complex life cycle of recurring, subscription, and consumption-based services.

-   **Service provisioning and activation**

    Specialized workflows and integrations for activating network services, provisioning cloud resources, or deploying software licenses.

-   **Network-as-a-Service \(NaaS\)**

    Support for following the NaaS architecture pattern with dual-layered decomposition and orchestration using the CFSS \(Customer-facing Service Specification\) abstraction.

-   **Network inventory integration**

    Integrates deeply with network inventory to manage the technical aspects of service fulfillment.

-   **High-volume MACD**

    Optimized for frequent commercial changes \(Modify, Add, Change, Disconnect\), common in subscription-based services.

-   **TM Forum \(TMF\) Open API alignment**

    Aligns with industry standards like TM Forum Open APIs for easier integration in complex telecom ecosystems. For more information, see [TMF APIs for TMT](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/tmt-api-reference.md).

-   **Specific orchestration models**

    Includes concepts like staggered decomposition and horizontal relationships unique to these industries.


Order Management for Telecommunications, Media, and Technology is part of the Sales CRM for Telecommunications. For more information, see [Exploring Sales CRM for Telecommunications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/sales-order-management-telecommunications.md).

## What to explore next

To learn more about configuring and using Order Management, see:

-   [Configuring Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/order-mgt-configuring.md)
-   [Using Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/using-order-management.md)
-   [Extending Order Management with ServiceNow applications and integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/order-mgt-integrating.md)
-   [Order Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/order-mgt-reference.md)

