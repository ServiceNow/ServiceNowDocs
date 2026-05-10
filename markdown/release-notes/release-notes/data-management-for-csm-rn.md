---
title: Data Management for CSM release notes
description: The ServiceNow Data Management for Customer Service Management \(CSM\) application enables you to organize and manage the data for both your internal users and external customers. Data Management for CSM was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 8
---

# Data Management for CSM release notes

The ServiceNow® Data Management for Customer Service Management \(CSM\) application enables you to organize and manage the data for both your internal users and external customers. Data Management for CSM was enhanced and updated in the Australia release.

## Data Management highlights for the Australia release

-   Implement granular administrative roles across the Customer Data Foundation \(CDF\) for better access control over user permissions and data.
-   Support unified user modeling with Contact as Consumer functionality, enabling the user to function as both a business-to-business \(B2B\) and a business-to-consumer \(B2C\).
-   Migrate the Household \(com.snc.household\) plugin to ServiceNow Store for improved packaging and deployment flexibility.
-   Renamed Service Model Foundation entities for clarity and consistency. Update any configurations, scripts, or integrations that reference these entities.
-   Enable billing account support on Sold Products to give agents instant financial context, accelerate billing case resolution, and improve billing accuracy and transparency.

See [Data management for Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-data-management.md) feature for more information.

**Important:** Business Location and Install Base Management are available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **[Configuring a contact as a consumer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/configuring-a-contact-as-a-unified-consumer.md)**

    Model a single user who functions as both a contact and a consumer within your customer data structure. This capability improves administrative efficiency by reducing the overhead of creating and maintaining multiple user records for the same individual. It also provides a unified experience, eliminating the need to switch logins across different personas.

-   **[Granular administrative roles for Customer Data Foundation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customer-data.md)**

    Implemented administrative roles that provide fine-grained access control across CDF. These roles can be assigned to administrators and other personas based on job functions and security requirements. It includes the following capabilities:

    -   Added 25 admin roles with specific read, write, create, and delete permissions.
    -   Updated Before you begin sections across all Customer Data Foundation configuration topics with role prerequisites.
    -   Improved security compliance through role-based access segregation.
-   **[New fields in the Customer Account table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customer-data.md)**

    Added the following fields to the Customer Account \(customer\_account\) table to improve business identification and record management:

    -   DUNS Number: Store the Data Universal Numbering System \(DUNS\) identifier for business accounts to support data enrichment and third-party integrations.
    -   Active: Indicates whether an account record is active for filtering and workflow purposes.
-   **[Description field added Customer Data Foundation configuration tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-cust-access-mgmt-tables.md)**

    Added a Description field to the following Customer Data Foundation \(CDF\) configuration tables to capture additional details about each record:

    -   Related Party Configuration \[sn\_customerservice\_related\_party\_configuration\] table
    -   Responsibility Definition \[sn\_customerservice\_responsibility\_def\] table
    -   Responsibility Access Configuration \[sn\_customerservice\_responsibility\_access\_config\] table
-   **[Billing accounts data model enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/add-related-parties-to-a-billing-account.md)**

    Grant contacts and consumers access to billing accounts through the related parties data model, using out of base system responsibilities and roles.

-   **[Service Model Foundation Granular admin roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/granular-admin-roles.md)**

    Added new granular admin roles to enable targeted permission assignments based on functional responsibilities, replacing broad admin access.

-   **[Add related parties to an install base item](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/add-related-party-install-base.md)**

    The Sold product is enhanced to support Related pricing.

-   **[Adding related parties to a sold product](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/add-related-parties-to-sp.md)**

    Use flexible price and quantity ramps that adapt over a product’s lifecycle, enabling time-based pricing, segment modifications during post-sale workflows, and accurate calculations across multi-year contracts.

-   **[Sold product form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/sold-product-form.md)**

    Use scheduled jobs to update the state of the Sold product based on start and end dates. Ensure that sold products follow clear start and end dates with automatic state updates, giving customers fair access, predictable billing, and reducing errors through accurate lifecycle management and delta pricing.

-   **[Sold product form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/sold-product-form.md)**

    Billing Account support on Sold Products to give agents immediate financial context, streamline billing‑related case resolution, and improve billing accuracy and transparency for customers and enterprises.


## Changed in this release

-   **[Enhanced Customer Data Viewer role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/business-stakeholder-for-csm.md)**

    The Customer Data Viewer \(sn\_customerservice.customer\_data\_viewer\) role includes expanded access to additional data tables and menu items. These enhancements enable users to view a broader range of customer data while maintaining read-only access restrictions. With this enhancement, you can:

    -   Extend access to additional tables for the customer data viewer role
        -   Inherit household role in customer data viewer role
    -   Explore additional menu items now accessible to the customer data viewer role.

-   **[Household plugin migration to ServiceNow Store](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/activate-customer-service-household.md)**

    Starting with the Australia release, the Household family plugin \(com.snc.household\) has been migrated to the ServiceNow Store as a standalone application. Any new enhancements to this application are delivered through the Household store app. This change provides improved packaging, versioning, and deployment flexibility for B2C implementations that require household relationship management.


-   **[Guided setup access for granular admin roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/import-csm-accounts.md)**

    Access to foundation data steps in guided setup now aligns with CDF admin roles. This access change enables administrators to delegate specific configuration tasks to users based on their assigned roles, providing greater flexibility in managing setup responsibilities.

-   **[Extensible account code support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-account-code-account-path.md)**

    Updated the account code generation logic to support dynamic length scalability. Account codes now automatically expand from 4 digits to 5 or more as needed, ensuring unlimited account growth without manual intervention. Administrators can resolve invalid insert errors by clearing the system property to regenerate codes based on the maximum existing code.

-   **[Declarative Responsibility Framework enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/declarative-resposibility-framework.md)**

    Introduced usability and functional enhancements to the Customer Access Management \(CAM\) Declarative Responsibility Framework. These updates streamline access configuration management and improve flexibility for responsibility definitions. With this enhancement, you can now:

    -   Import or copy access configurations from one responsibility definition to another.
    -   Manage CAM-related assets through improved cleanup capabilities.
    -   Reference any field name in the Responsibility Definition field configuration.
-   **[Unified User configuration enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/configuring-unified-user.md)**

    Added a system property \(sn\_customerservice.consumer.allowed\_user\_types\) to enhance unified user management. This property specifies which user types \(classes\) can be associated with consumers.

-   **[Customer Life Cycle Management Workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customer-life-cycle-management-workflows.md)**

    Added core primitives to support price and quantity ramps, enabling flexible, time‑based changes across the sold product lifecycle. The feature delivers scalable pricing aligned with usage, simplifies post-sale workflows, and improves revenue forecasting without custom scripts.

-   **[Install base data model enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/create-install-base-item.md)**

    Improve traceability and product life cycle management with the **Install Base Identifier** field on the install base form. Base install base items are mapped directly to model categories to support industry-specific product configurations.

    Added **Provider Service Org** field on the install base form to support tracking, recall workflows, and post-sale engagement with dealers and partners.

-   **[Sold product form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/sold-product-form.md)**

    Create future‑dated subscription products in a **Pending Activation** state to improve the Add‑Order‑to‑Sold‑Product process. It also ensures lifecycle accuracy, predictable billing, and fair access for customers while improving revenue recognition for businesses.


-   **[Service Model Foundation renamed Entities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/renamed-entities.md)**

    Renamed Service Model Foundation entities to improve clarity and maintain consistency across the platform. Review your existing configurations, scripts, or integrations that reference these entities and update them accordingly.

    **Note:** The entity name changes are available in the Business Location 5.2.0 store app.


## Deprecated features

-   As part of the CAM Declarative Responsibility Framework enhancements, the following legacy fields have been marked deprecated:
    -   **Restrict access to** field from the Responsibility Access Configuration \[sn\_customerservice\_responsibility\_access\_config\] table
    -   **Applicable to** field from the Responsibility Definition \[sn\_customerservice\_responsibility\_def\] table
-   Starting with the Australia release, the Household plugin \(com.snc.household\) is available as a store plugin and, as such, the family version of the plugin is being prepared for future deprecation. Upon upgrading, customers will automatically move to the store version of the plugin. It will be hidden from the family plugins and no longer installed on new instances but will continue to be supported as a store plugin. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## Activation information

CSM is a ServiceNow AI Platform application that is available with activation of the Customer Service Management \(CSM\) plugin \(com.sn\_customerservice\). For details, see [Activate Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/t_ActivateCustomerService.md).

Additional CSM features are available with the activation of other plugins. For details, see [Additional plugins for Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/r_CustServMgmtAddtlPluginsTable.md).

Sales Customer Relationship Management is a ServiceNow AI Platform feature that is available with the activation of the Lead to Cash Core plugin \(com.snd.l2c.core\). For details, see [Exploring Sales Customer Relationship Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/som-exploring.md).

## Plugin information

-   **Changed plugins**

    The following plugins are moved to store:

    -   CSM Contributor User \(com.snc.csm\_contributor\_user\)
    -   Outsourced Customer Service \(com.snc.csm\_ocs\)
    -   Service Organization \(com.snc.service\_organization\)
    -   Outsourced Service Provider \(com.snc.outsourced\_service\_provider\)
-   **Plugins planned for deprecation**

    The following plugins are planned for deprecation in a future release:

    These plugins are planned for deprecation in the C release. Beginning with the Australia release these plugins will be migrated to a store application. Upgrade your instance to Australia or later release versions and the store applications will be automatically installed.

    -   CSM Contributor User \(com.snc.csm\_contributor\_user\)
    -   Service Organization \(com.snc.service\_organization\)
-   **Renamed plugins**

    The Customer Service Household \(com.snc.household\) plugin has been renamed to Customer Household Data Model \(com.snc.household\) in the Australia release.


## Browser requirements

Starting with the Australia release, data management for Customer Service Management doesn't support mobile devices and Internet Explorer. For more information, see [Browser support](../../administer/navigation-and-ui/reference/browser-support.md).

## Related ServiceNow applications and features

-   **[Communities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/communities/servicenow-communities.md)**

    From the Customer Service Portal and Consumer Service Portal, you can enable your customers to connect, engage, and collaborate by using the ServiceNow® Communities application. Customer Service agents can create cases from community discussion threads and resolve cases with the community content.

-   **[Field Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/fsm-application-landing-page.md)**

    Customer Service Management includes an integration with the ServiceNow® Field Service Management application. With this integration, your technicians, agents, consumers, and customers can perform the following tasks:

    -   Field service technicians can view customer account and contact information on work orders and work order tasks in the Field Service Management application.
    -   Customer service agents can create work orders from cases in the Customer Service Management application.
    -   Customers and consumers can view the case-related work orders from the Customer Service Portal and Consumer Service Portal.
-   **[Workforce Optimization for Customer Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/configurable-wfo-cs.md)**

    Manage and maintain the productivity of your workforce from a single application by using ServiceNow® Workforce Optimization for Customer Service. With this application, you can efficiently route work to your team, manage your team's skills and schedules, and monitor their performance.

-   **[Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/workspace-landing-page.md)**

    ServiceNow® Workspace is a graphical user interface that puts multiple tools on one page, including the tools that agents use to identify, research, and resolve issues. CSM Configurable Workspace and CSM Agent Workspace are customer service implementations that provide tier-1 agents with the tools that they use to respond to customers and to resolve cases.

-   **[Sales Customer Relationship Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/order-mgt-overview.md)**

    The Sales Customer Relationship Management applications enable you to manage the product sales and order fulfillment life cycles in your organization. It includes pre-sales opportunities, sales quote generation, order capture, order fulfillment, and post-sales engagement.


**Parent Topic:**[Customer Service Management release notes](customer-service-mgmt-rn-landing.md)

