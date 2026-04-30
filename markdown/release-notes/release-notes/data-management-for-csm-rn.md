---
title: Data management for CSM release notes
description: The ServiceNow Data management for Customer Service Management application enables you to organize and manage the data for both your internal users and external customers. Data management for Customer Service Management was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 5
---

# Data management for CSM release notes

The ServiceNow® Data management for Customer Service Management application enables you to organize and manage the data for both your internal users and external customers. Data management for Customer Service Management was enhanced and updated in the Xanadu release.

## Data management highlights for the Xanadu release

-   Enable your agents to get visibility into the business locations that they support by using the inter-organization support functionality.
-   Enhance the adoption of the service organization data model by unparenting service organizations from the company table.
-   Use the Provider Service Organization information of a sold product to enable agents to create cases.

See [Data management for Customer Service Management](https://www.servicenow.com/docs/access?context=csm-data-management&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US) for more information.

## New in the Xanadu release

-   **[Unified user - employee as a consumer](https://www.servicenow.com/docs/access?context=features-supp-and-unsupp-by-unified-consumer&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    Update the additional features and workflows, such as the case types Order Management, and Field Service Management integration, to support the unified consumer \(sn\_customerservice.unified\_consumer\) role.

-   **[Inter-organization support](https://www.servicenow.com/docs/access?context=setup-bus-loc-serviced-by-bus-loc&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    Enable your agents to get visibility into the business locations that they support so that they can resolve issues efficiently. You can provide the agents that are assigned to the fulfilling service organization with access to the cases, install base items, sold products, and member details of all the requesting service organizations that they’re assisting.

-   **[External business location as a fulfiller](https://www.servicenow.com/docs/access?context=industry-data-model-cases&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    Enable external business locations such as partners, external agencies, and franchises to fulfill customer cases with store-related issues.

-   **[Associating assignment groups with a business location](https://www.servicenow.com/docs/access?context=setting-up-assignment-groups&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    Associate groups with an internal or external business location through a one-to-many \(1:M\) relationship, which means that one or more assignment groups can be associated with a business location.

-   **[Install Base hierarchy visualization](https://www.servicenow.com/docs/access?context=install_base_hierarchy_visualisation&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    View the entire hierarchy of an install base item by using the **Install Base hierarchy** tab on the CSM Configurable Workspace. You can expand the multiple nodes of the hierarchy and create cases for the install base item.


## UI changes

-   **New look and feel for [Outsourced Service Provider dashboard](https://www.servicenow.com/docs/access?context=ocs-dashboard&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US) and [Proactive Customer Service - Advanced dashboard](https://www.servicenow.com/docs/access?context=csm-proactive-monit-dashboard&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US) dashboards**

    Starting from the Xanadu release, the following dashboards have a new, modernized look and feel:

    -   [Outsourced Service Provider dashboard](https://www.servicenow.com/docs/access?context=ocs-dashboard&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)
    -   [Proactive Customer Service - Advanced dashboard](https://www.servicenow.com/docs/access?context=csm-proactive-monit-dashboard&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)
    For more information, see [Next Experience UI](https://www.servicenow.com/docs/access?context=next-experience-landing-page&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).


## Changed in this release

-   **[Unparenting service organizations from a company](https://www.servicenow.com/docs/access?context=associate-company-with-bus-loc&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    Enhanced the adoption of the service organization model to accommodate the various industry verticals, such as Healthcare and Life Sciences Service Management, Public Sector Digital Services, and Financial Services Operations, by unparenting the service organizations from the company table.

-   **[Field Service Management integration with Service Model Foundation](https://www.servicenow.com/docs/access?context=track-work-orders-on-the-blsp&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    Enabled your location staff to track the work orders for their business locations by using the business location service portal \(BLSP\).

-   **[Data model for sold products](https://www.servicenow.com/docs/access?context=create-sold-item&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**
    -   You can now view the Provider Service Organization information that has sold a product or service to the customer on the Sold Product form.
    -   You can now use the **Product Location** and **Product Specification** fields on the Sold Product table \(sn\_install\_base\_sold\_product\) to capture information about the location of the sold product and the sold product that is associated with an offer.
-   **[Product Instance directive for Install Base Management](https://www.servicenow.com/docs/access?context=create-a-sync-between-an-install-base-class-and-asset-class&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    Synchronized the changes between the asset and corresponding install base hierarchy with the extended product instance hierarchy.

-   **[Customer Life Cycle Management Workflows](https://www.servicenow.com/docs/access?context=customer-life-cycle-management-workflows&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    You can now select multiple sold products at the same time to trigger the **Suspend**, **Resume**, and **Disconnect** flows to update the existing root sold products and their services.


-   **[Compose Sales and Order Management workflows](https://www.servicenow.com/docs/access?context=compose_sales_and_order_management_workflows&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    You can now use the sales and order management API to support use cases for order reconfiguration. To learn more about reconfiguration, see [LeadtoCashCore - Scoped](https://www.servicenow.com/docs/access?context=LeadToCashCoreAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).


-   ****
    -   Perform **Modify**, **Suspend**, **Resume**, and **Disconnect** actions on product inventory records from the Product Inventories related list.

        **Note:** The Product Inventories related list is available only from the Yokohama release. If you're using the Washington or Xanadu versions, you can manually add the related list.

        To retain both the Product Inventory and Sold product related lists, filter out the product inventory records from the sold product list. Use the product inventories related list to perform the MACD actions.


-   **Sales and Order Management Request tracker**
    -   Monitor the status of sales and order management workflows and enable agents to track the status of synchronous and asynchronous flows.
    -   Use the enhances inbound Queue to view detailed request information for the sales and order management workflows and improve user experience.

## Activation information

Customer Service Management is a ServiceNow AI Platform feature that is available with activation of the Customer Service Management plugin \(com.sn\_customerservice\). For details, see [Activate Customer Service Management](https://www.servicenow.com/docs/access?context=t_ActivateCustomerService&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US).

Additional Customer Service Management features are available with the activation of other plugins. For details, see [Additional plugins for Customer Service Management](https://www.servicenow.com/docs/access?context=r_CustServMgmtAddtlPluginsTable&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US).

Sales Customer Relationship Management is a ServiceNow AI Platform feature that is available with the activation of the Lead to Cash Core plugin \(com.snd.l2c.core\). For details, see [Exploring Sales Customer Relationship Management](https://www.servicenow.com/docs/access?context=som-exploring&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US).

## Browser requirements

Starting with the Xanadu release, ServiceNow® Data Management doesn't support mobile devices and Internet Explorer. For more information, see [Browser support](https://www.servicenow.com/docs/access?context=browser-support&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Communities](https://www.servicenow.com/docs/access?context=servicenow-communities&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    From the Customer Service Portal and Consumer Service Portal, you can enable your customers to connect, engage, and collaborate using the ServiceNow® Communities application. Customer Service agents can create cases from community discussion threads and resolve cases with community content.

-   **[Field Service Management](https://www.servicenow.com/docs/access?context=fsm-application-landing-page&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US)**

    Customer Service Management includes an integration with the ServiceNow® Field Service Management application. With this integration, your technicians, agents, consumers, and customers can perform the following tasks:

    -   Field service technicians can view customer account and contact information on work orders and work order tasks in the Field Service Management application.
    -   Customer service agents can create work orders from cases in the Customer Service Management application.
    -   Customers and consumers can view case-related work orders from the Customer Service Portal and Consumer Service Portal.
-   **[Workforce Optimization for Customer Service](https://www.servicenow.com/docs/access?context=configurable-wfo-cs&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    Manage and maintain the productivity of your workforce from a single application by using ServiceNow® Workforce Optimization for Customer Service. With this application, you can efficiently route work to your team, manage your team's skills and schedules, and monitor their performance.

-   **[Workspace](https://www.servicenow.com/docs/access?context=workspace-landing-page&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

    ServiceNow® Workspace is a graphical user interface that puts multiple tools on one page, including the tools agents use to identify, research, and resolve issues. CSM Configurable Workspace and CSM Agent Workspace are customer service implementations that provide tier-1 agents with the tools that they must respond to customers and to resolve cases.

-   **[Sales Customer Relationship Management](https://www.servicenow.com/docs/access?context=order-mgt-overview&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

    The Sales Customer Relationship Management applications enable you to manage the product sales and order fulfillment life cycles in your organization. It includes pre-sales opportunities, sales quote generation, order capture, order fulfillment, and post-sales engagement.


**Parent Topic:**[Customer Service Management release notes](customer-service-mgmt-rn-landing.md)

