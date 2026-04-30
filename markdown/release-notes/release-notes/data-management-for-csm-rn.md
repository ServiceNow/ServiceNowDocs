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

See [Data management for Customer Service Management](https://www.servicenow.com/docs/access?context=csm-data-management&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US) for more information.

**Important:** Business Location and Install Base Management are available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Naming customer relationship records](https://www.servicenow.com/docs/access?context=adding-related-party-to-case&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Use the Type field through related party configurations to name records in the account team member, contact relationship, consumer relationship, and household member relationship tables. With this functionality, you can identify the relationship that is based on the industry use case.

-   **[Ordering customer relationship records](https://www.servicenow.com/docs/access?context=adding-related-party-to-case&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Organize records in tables such as account team members, consumer relationships, and more by using the **Order** field. You can set the order manually or auto-populate it based on the selected Type through related party configurations. This way, you can arrange records logically based on your use case.

-   **[Enhancements to the declarative responsibility framework](https://www.servicenow.com/docs/access?context=declarative-resposibility-framework&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Enhance the declarative responsibility framework to simplify administration and access management by enabling administrators to do the following tasks:

    -   Add new granular roles for accessing customer data that is based on responsibility definitions.
    -   Include additional entities in the framework.
-   **[Subscription metrics for sold products](https://www.servicenow.com/docs/access?context=create-sold-item&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Enable agents to track and analyze the pricing information for products and services by using the pricing and subscription revenue metrics on the sold product form on the CSM Configurable Workspace.

-   **[Project Management for business locations​](https://www.servicenow.com/docs/access?context=csm-ppm-integration&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Integrate SPM project management with business locations to support operations such as opening, closing, or modernizing locations. With the project management integration, your teams can track the timelines, collaborate, and execute the business location-facing tasks more effectively.

-   **[Work orders for business locations​](https://www.servicenow.com/docs/access?context=track-work-orders-on-the-blsp&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Fulfill Field Service Management \(FSM\) work orders at business locations. This way, you can enable location members to view and complete the assigned tasks. By using the existing business location data, you can streamline work order assignments.

-   **[Enhanced data fields for business locations](https://www.servicenow.com/docs/access?context=data-model-business-location-form&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Track additional information about business locations by using new fields for opening and closing dates, status, and description.

-   **[Staff movement between internal business locations](https://www.servicenow.com/docs/access?context=create-internal-business-location&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Enable managers to transfer the staff between internal business locations. You can streamline updates for organizations that have frequent staff movements.

-   **[Company-owned, third-party operated business locations](https://www.servicenow.com/docs/access?context=add-user-internal-bus-location&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Assign external staff to internal business locations to support various operating models, including company-owned, third-party operated locations.

-   **[Customer Life Cycle workflows for Sold Products and Product Inventory records](https://www.servicenow.com/docs/access?context=customer-life-cycle-management-workflows&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Use the Customer Life Cycle workflows to do the following tasks:

    -   Create a Modify, Suspend, Resume, and Disconnect order for single or multiple root product inventory records that are associated with a service specification.
    -   Select multiple root product inventories to perform the modify action to create both orders and quotes.
    -   Track the status of the Modify, Suspend, Resume, and Disconnect flows on sold products and product inventory record by using the Sales and Order Management Request Tracker \(sn\_tmt\_core\_inbound\_queue\) table.
-   **[Inbound Request Configuration table](https://www.servicenow.com/docs/access?context=inbound-request-configuration-table&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Use the Inbound Request Configuration \[sn\_tmt\_core\_inbound\_queue\_config\] table to enable configurations that determine how a flow is executed, whether synchronous or asynchronous.

    Use the **Trigger Notifications** field on the Inbound Request Configuration \[sn\_tmt\_core\_inbound\_queue\_config\] table to enable configuration of notification types, whether default, custom,or no notifications.

-   **[Activate Customer Life Cycle Management Self-Service](https://www.servicenow.com/docs/access?context=activate-customer-life-cycle-management-self-service&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Enable customers who are primary contacts associated to a sold product to perform the Modify, Suspend, Resume, and Disconnect actions on the Business portal.

    .

-   **Billing account store application**

    Use the new CSM Billing Account Core store app that provides a foundational data model for managing billing accounts across organizations and users. It enables businesses to define, organize, and maintain billing relationships, supporting accurate billing, payments, and scalable financial operations.


## UI changes

-   **[Specification Class on Product Inventory related list](https://www.servicenow.com/docs/access?context=product_inventory_configurations&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    The **Specification class** field on the Product Inventory related list provides information on whether the selected product inventory record has a product specification or service specification that is associated with it.


## Changed in this release

-   **[Product Inventories configurations for Customer Life Cycle Management workflows](https://www.servicenow.com/docs/access?context=product_inventory_configurations&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Perform the Modify, Suspend, Resume, and Disconnect operations on product inventory records directly from the Product Inventory related list on the Accounts page.

-   **[Grant write access to account relationships](https://www.servicenow.com/docs/access?context=t_CreateAcctRelationshipRecord&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Enable administrators and customer service managers to update account relationship records.

-   **[Enable write access to contact relationships](https://www.servicenow.com/docs/access?context=t_CreateAContactRelationship&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Enable administrators and customer service managers to update the contact relationship records.

-   **[Populate the Type field in relationship tables using the fix script](https://www.servicenow.com/docs/access?context=migration-of-account-manager-responsibility-access&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Migrate the account manager responsibilities from the account team member relationships to the new responsibility access configurations. The updated framework enables you to manage access settings more efficiently.

-   **[Update roles within relationship agent and relationship contributor](https://www.servicenow.com/docs/access?context=features-supp-and-unsupp-by-unified-consumer&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Modify the roles of the relationship agent and relationship contributor to include the new granular roles that can grant access by responsibilities.

-   **[Notification for case tasks at business locations](https://www.servicenow.com/docs/access?context=manage-business-location-cases&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    View the notifications for the case tasks that are associated with the business locations on the Business Location Service Portal \(BLSP\). This way, your location members can stay informed about their pending tasks.

-   **[Case resolution by location staff at other business locations](https://www.servicenow.com/docs/access?context=ebl-as-a-fulfiller&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Enable your location staff, whether at company-owned or third-party-owned organizations \(internal and external business locations\), to handle and resolve issues from other eligible business locations.

-   **[Inbound Request Configuration table](https://www.servicenow.com/docs/access?context=inbound-request-configuration-table&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    The Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table is renamed to Inbound Request table.

    Use the **Request Configuration** field on the Inbound Request \[sn\_tmt\_core\_inbound\_queue\] table to reference the Inbound Request Configuration \[sn\_tmt\_core\_inbound\_queue\_config\] table while executing synchronous or asynchronous flows.


## Activation information

Customer Service Management is a ServiceNow AI Platform feature that is available with activation of the Customer Service Management plugin \(com.sn\_customerservice\). For details, see [Activate Customer Service Management](https://www.servicenow.com/docs/access?context=t_ActivateCustomerService&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US).

Additional Customer Service Management features are available with the activation of other plugins. For details, see [Additional plugins for Customer Service Management](https://www.servicenow.com/docs/access?context=r_CustServMgmtAddtlPluginsTable&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US).

Sales Customer Relationship Management is a ServiceNow AI Platform feature that is available with the activation of the Lead to Cash Core plugin \(com.snd.l2c.core\). For details, see [Exploring Sales Customer Relationship Management](https://www.servicenow.com/docs/access?context=som-exploring&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US).

Starting from the Yokohama release, the following plugins are available on ServiceNow Store for quicker and better maintenance:

-   Install Base Management \(com.snc.install\_base\)
-   Install base characteristics \(com.snc.install\_base\_characteristics\)
-   Customer Service with Service Portfolio management \(com.snc.csm\_spm\)

For details, see [Configure install base](https://www.servicenow.com/docs/access?context=configure-install-base&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US).

Starting from the Yokohama release, the Business Location plugin \(com.snc.business\_location\) is available on ServiceNow Store for quicker and better maintenance. For details, see [Activate business locations](https://www.servicenow.com/docs/access?context=activate-business-location&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US).

## Browser requirements

Starting with the Yokohama release, data management for Customer Service Management doesn't support mobile devices and Internet Explorer. For more information, see [Browser support](https://www.servicenow.com/docs/access?context=browser-support&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Communities](https://www.servicenow.com/docs/access?context=servicenow-communities&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    From the Customer Service Portal and Consumer Service Portal, you can enable your customers to connect, engage, and collaborate by using the ServiceNow® Communities application. Customer Service agents can create cases from community discussion threads and resolve cases with the community content.

-   **[Field Service Management](https://www.servicenow.com/docs/access?context=fsm-application-landing-page&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US)**

    Customer Service Management includes an integration with the ServiceNow® Field Service Management application. With this integration, your technicians, agents, consumers, and customers can perform the following tasks:

    -   Field service technicians can view customer account and contact information on work orders and work order tasks in the Field Service Management application.
    -   Customer service agents can create work orders from cases in the Customer Service Management application.
    -   Customers and consumers can view the case-related work orders from the Customer Service Portal and Consumer Service Portal.
-   **[Workforce Optimization for Customer Service](https://www.servicenow.com/docs/access?context=configurable-wfo-cs&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Manage and maintain the productivity of your workforce from a single application by using ServiceNow® Workforce Optimization for Customer Service. With this application, you can efficiently route work to your team, manage your team's skills and schedules, and monitor their performance.

-   **[Workspace](https://www.servicenow.com/docs/access?context=workspace-landing-page&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)**

    ServiceNow® Workspace is a graphical user interface that puts multiple tools on one page, including the tools that agents use to identify, research, and resolve issues. CSM Configurable Workspace and CSM Agent Workspace are customer service implementations that provide tier-1 agents with the tools that they use to respond to customers and to resolve cases.

-   **[Sales Customer Relationship Management](https://www.servicenow.com/docs/access?context=order-mgt-overview&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

    The Sales Customer Relationship Management applications enable you to manage the product sales and order fulfillment life cycles in your organization. It includes pre-sales opportunities, sales quote generation, order capture, order fulfillment, and post-sales engagement.


**Parent Topic:**[Customer Service Management release notes](customer-service-mgmt-rn-landing.md)

