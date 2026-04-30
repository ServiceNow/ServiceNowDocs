---
title: Configuring the Business Portal
description: As an admin, you can configure the Business Portal \(sn\_b2b\_portal\) so your customers can browse products and create orders in Sales Customer Relationship Management.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-11-14"
reading_time_minutes: 3
breadcrumb: [Configure, Sales Customer Relationship Management]
---

# Configuring the Business Portal

As an admin, you can configure the Business Portal \(sn\_b2b\_portal\) so your customers can browse products and create orders in Sales Customer Relationship Management.

## Configuration overview

1.  Install the following applications and features in the specified order using the Application Manager to set up the Business Portal:

    1.  Order Management Portal: sn\_ord\_mgmt\_portal
    2.  Product Catalog Management Portal: sn\_prd\_pm\_portal
    3.  Customer Service Portal: sn\_csm\_portal

        **Note:** The Business Portal application \(sn\_b2b\_portal\) is automatically installed when you install the Customer Service Portal.

    4.  UI Components for Customer Portals: sn\_ciwf\_ui\_cmpnt
    5.  Sales Cart plugin: sn\_sales\_cart
    6.  Customer Request for Quote plugin: sn\_cust\_rfq
2.  [Enable the Business Portal](../task/order-management-enable-business-portal.md)

    Enable the Business Portal \(sn\_b2b\_portal\) so customers can browse products and create orders.

3.  [Install Sales Cart](../task/install-sales-cart-plugin.md)

    Provide easy order creation and checkout processes to your customers through the Sales Cart application.

4.  \(Optional\) [Install Customer Request for Quote](../task/install-rfq-plugin.md)

    Enable B2B customers to request for quotes \(RFQ\) from the Business Portal. Installing this application also installs the Request for Quote module in the CSM Configurable Workspace, which enables sales agents to generate quotes from the RFQs.

5.  \(Optional\) [Install apps for self-service order case management](activating-self-service-order-case-management-business-portal.md)

    Install the applications or features that provide the self-service options that you want to offer customers for managing order cases on the Business Portal.


## Additional configurations and customizations

The following tasks help you further customize and configure the Business Portal to support self-service Sales Customer Relationship Management workflows for B2B customers:

-   [Add a logo to the sales cart PDF](../task/add-logo-sales-cart-pdf.md)

    Customize and embed your company logo in sales cart summary PDFs to ensure consistent branding and alignment with corporate identity standards.

-   [Modifying the data retention and table cleanup policy for the Sales Cart application](modify-data-retention-table-cleanup-sales-cart.md)

    A default data retention and table cleanup policy automatically deletes records from the Sales Cart application based on predefined conditions that match your organization's policies.

-   [Modify terms and conditions for the sales cart](../task/modify-terms-conditions-sales-cart.md)

    Add order checkout terms and conditions in the CartTermsAndCo document template block for your Business Portal.


**Related topics**  


[Customer self-service using the Business Portal](order-mgt-business-portal.md)

[Business Portal reference for Sales Customer Relationship Management](../reference/som-business-portal-reference.md)

[Enable the manage order operations agent on the Business Portal](../../now-assist-order-mgmt/task/enable-manage-order-operations-ai-agent.md)

[now-assist-om-ai-agents]

