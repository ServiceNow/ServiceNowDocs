---
title: Data management for CSM release notes
description: The ServiceNow Data management for Customer Service Management application enables you to organize and manage the data for both your internal users and external customers. Data management for Customer Service Management was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 7
---

# Data management for CSM release notes

The ServiceNow® Data management for Customer Service Management application enables you to organize and manage the data for both your internal users and external customers. Data management for Customer Service Management was enhanced and updated in the Yokohama release.

## Data management highlights for the Yokohama release

-   Track the status and other information that is related to the Customer Life Cycle workflows by using the Sales and Order Management Request Tracker \(sn\_tmt\_core\_inbound\_queue\) table.
-   Track pricing and subscription information for products and services on the CSM Configurable Workspace by using the revenue metrics on the sold product form.
-   Integrate Strategic Portfolio Management \(SPM\) project management with business locations to create and manage projects across your organization.

See [Data management for Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/csm-data-management.md) for more information.

**Important:** Business Location and Install Base Management are available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Naming customer relationship records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/adding-related-party-to-case.md)**

    Use the Type field through related party configurations to name records in the account team member, contact relationship, consumer relationship, and household member relationship tables. With this functionality, you can identify the relationship that is based on the industry use case.

-   **[Ordering customer relationship records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/adding-related-party-to-case.md)**

    Organize records in tables such as account team members, consumer relationships, and more by using the **Order** field. You can set the order manually or auto-populate it based on the selected Type through related party configurations. This way, you can arrange records logically based on your use case.

-   **[Enhancements to the declarative responsibility framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/declarative-resposibility-framework.md)**

    Enhance the declarative responsibility framework to simplify administration and access management by enabling administrators to do the following tasks:

    -   Add new granular roles for accessing customer data that is based on responsibility definitions.
    -   Include additional entities in the framework.
-   **[Subscription metrics for sold products](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/create-sold-item.md)**

    Enable agents to track and analyze the pricing information for products and services by using the pricing and subscription revenue metrics on the sold product form on the CSM Configurable Workspace.

-   **[Project Management for business locations​](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/csm-ppm-integration.md)**

    Integrate SPM project management with business locations to support operations such as opening, closing, or modernizing locations. With the project management integration, your teams can track the timelines, collaborate, and execute the business location-facing tasks more effectively.

-   **[Work orders for business locations​](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/track-work-orders-on-the-blsp.md)**

    Fulfill Field Service Management \(FSM\) work orders at business locations. This way, you can enable location members to view and complete the assigned tasks. By using the existing business location data, you can streamline work order assignments.

-   **[Enhanced data fields for business locations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/data-model-business-location-form.md)**

    Track additional information about business locations by using new fields for opening and closing dates, status, and description.

-   **[Staff movement between internal business locations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/create-internal-business-location.md)**

    Enable managers to transfer the staff between internal business locations. You can streamline updates for organizations that have frequent staff movements.

-   **[Company-owned, third-party operated business locations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/add-user-internal-bus-location.md)**

    Assign external staff to internal business locations to support various operating models, including company-owned, third-party operated locations.

-   **[Customer Life Cycle workflows for Sold Products and Product Inventory records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/customer-life-cycle-management-workflows.md)**

    Use the Customer Life Cycle workflows to do the following tasks:

    -   Create a Modify, Suspend, Resume, and Disconnect order for single or multiple root product inventory records that are associated with a service specification.
    -   Select multiple root product inventories to perform the modify action to create both orders and quotes.
    -   Track the status of the Modify, Suspend, Resume, and Disconnect flows on sold products and product inventory record by using the Sales and Order Management Request Tracker \(sn\_tmt\_core\_inbound\_queue\) table.
-   **[Inbound Request Configuration table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/inbound-request-configuration-table.md)**

    Use the Inbound Request Configuration \[sn\_tmt\_core\_inbound\_queue\_config\] table to enable configurations that determine how a flow is executed, whether synchronous or asynchronous.

    Use the **Trigger Notifications** field on the Inbound Request Configuration \[sn\_tmt\_core\_inbound\_queue\_config\] table to enable configuration of notification types, whether default, custom,or no notifications.

-   **[Activate Customer Life Cycle Management Self-Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/activate-customer-life-cycle-management-self-service.md)**

    Enable customers who are primary contacts associated to a sold product to perform the Modify, Suspend, Resume, and Disconnect actions on the Business portal.

    .

-   **Billing account store application**

    Use the new CSM Billing Account Core store app that provides a foundational data model for managing billing accounts across organizations and users. It enables businesses to define, organize, and maintain billing relationships, supporting accurate billing, payments, and scalable financial operations.


## UI changes

-   **[Specification Class on Product Inventory related list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/product_inventory_configurations.md)**

    The **Specification class** field on the Product Inventory related list provides information on whether the selected product inventory record has a product specification or service specification that is associated with it.


## Changed in this release

-   **[Product Inventories configurations for Customer Life Cycle Management workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/product_inventory_configurations.md)**

    Perform the Modify, Suspend, Resume, and Disconnect operations on product inventory records directly from the Product Inventory related list on the Accounts page.

-   **[Grant write access to account relationships](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/t_CreateAcctRelationshipRecord.md)**

    Enable administrators and customer service managers to update account relationship records.

-   **[Enable write access to contact relationships](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/t_CreateAContactRelationship.md)**

    Enable administrators and customer service managers to update the contact relationship records.

-   **[Populate the Type field in relationship tables using the fix script](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/migration-of-account-manager-responsibility-access.md)**

    Migrate the account manager responsibilities from the account team member relationships to the new responsibility access configurations. The updated framework enables you to manage access settings more efficiently.

-   **[Update roles within relationship agent and relationship contributor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/features-supp-and-unsupp-by-unified-consumer.md)**

    Modify the roles of the relationship agent and relationship contributor to include the new granular roles that can grant access by responsibilities.

-   **[Notification for case tasks at business locations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/manage-business-location-cases.md)**

    View the notifications for the case tasks that are associated with the business locations on the Business Location Service Portal \(BLSP\). This way, your location members can stay informed about their pending tasks.

-   **[Case resolution by location staff at other business locations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/ebl-as-a-fulfiller.md)**

    Enable your location staff, whether at company-owned or third-party-owned organizations \(internal and external business locations\), to handle and resolve issues from other eligible business locations.

-   **[Inbound Request Configuration table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/inbound-request-configuration-table.md)**

    The Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table is renamed to Inbound Request table.

    Use the **Request Configuration** field on the Inbound Request \[sn\_tmt\_core\_inbound\_queue\] table to reference the Inbound Request Configuration \[sn\_tmt\_core\_inbound\_queue\_config\] table while executing synchronous or asynchronous flows.


## Activation information

Customer Service Management is a ServiceNow AI Platform feature that is available with activation of the Customer Service Management plugin \(com.sn\_customerservice\). For details, see [Activate Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/t_ActivateCustomerService.md).

Additional Customer Service Management features are available with the activation of other plugins. For details, see [Additional plugins for Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/r_CustServMgmtAddtlPluginsTable.md).

Sales Customer Relationship Management is a ServiceNow AI Platform feature that is available with the activation of the Lead to Cash Core plugin \(com.snd.l2c.core\). For details, see [Exploring Sales Customer Relationship Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/order-management/som-exploring.md).

Starting from the Yokohama release, the following plugins are available on ServiceNow Store for quicker and better maintenance:

-   Install Base Management \(com.snc.install\_base\)
-   Install base characteristics \(com.snc.install\_base\_characteristics\)
-   Customer Service with Service Portfolio management \(com.snc.csm\_spm\)

For details, see [Configure install base](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/configure-install-base.md).

Starting from the Yokohama release, the Business Location plugin \(com.snc.business\_location\) is available on ServiceNow Store for quicker and better maintenance. For details, see [Activate business locations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/activate-business-location.md).

## Browser requirements

Starting with the Yokohama release, data management for Customer Service Management doesn't support mobile devices and Internet Explorer. For more information, see .

## Related ServiceNow applications and features

-   **[Communities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/servicenow-communities.md)**

    From the Customer Service Portal and Consumer Service Portal, you can enable your customers to connect, engage, and collaborate by using the ServiceNow® Communities application. Customer Service agents can create cases from community discussion threads and resolve cases with the community content.

-   **[Field Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/field-service-management/fsm-application-landing-page.md)**

    Customer Service Management includes an integration with the ServiceNow® Field Service Management application. With this integration, your technicians, agents, consumers, and customers can perform the following tasks:

    -   Field service technicians can view customer account and contact information on work orders and work order tasks in the Field Service Management application.
    -   Customer service agents can create work orders from cases in the Customer Service Management application.
    -   Customers and consumers can view the case-related work orders from the Customer Service Portal and Consumer Service Portal.
-   **[Workforce Optimization for Customer Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/configurable-wfo-cs.md)**

    Manage and maintain the productivity of your workforce from a single application by using ServiceNow® Workforce Optimization for Customer Service. With this application, you can efficiently route work to your team, manage your team's skills and schedules, and monitor their performance.

-   **Workspace**

    ServiceNow® Workspace is a graphical user interface that puts multiple tools on one page, including the tools that agents use to identify, research, and resolve issues. CSM Configurable Workspace and CSM Agent Workspace are customer service implementations that provide tier-1 agents with the tools that they use to respond to customers and to resolve cases.

-   **[Sales Customer Relationship Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/order-management/order-mgt-overview.md)**

    The Sales Customer Relationship Management applications enable you to manage the product sales and order fulfillment life cycles in your organization. It includes pre-sales opportunities, sales quote generation, order capture, order fulfillment, and post-sales engagement.


**Parent Topic:**[Customer Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/customer-service-mgmt-rn-landing.md)

