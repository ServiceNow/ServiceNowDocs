---
title: Combined Data Management for CSM release notes for upgrades from Yokohama to Australia
description: Consolidated page of all release notes for Data Management for CSM from Yokohama to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-australia/australia-yokohama-datamanagementforcsm-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 16
breadcrumb: [Products combined by family]
---

# Combined Data Management for CSM release notes for upgrades from Yokohama to Australia

Consolidated page of all release notes for Data Management for CSM from Yokohama to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Data Management for CSM release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Data Management for CSM to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Data Management for CSM.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **Naming customer relationship records for [Consumer team member relationship tables](https://www.servicenow.com/docs/access?context=assign-team-member-to-consumer&family=zurich&ft:locale=en-US) and [Household team member relationship tables](https://www.servicenow.com/docs/access?context=assign-team-member-to-household&family=zurich&ft:locale=en-US)**

Use the **Type** field through related party configurations to name records in the consumer team member and household team member relationship tables. This functionality enables you to label relationships based on the purpose of the association and relevant industry use cases.

-   **[Migrating legacy workflow to low code](https://www.servicenow.com/docs/access?context=create-escalation-template&family=zurich&ft:locale=en-US)**

Added an **Escalation Approval Flow** field to the Escalation Template \[sn\_customerservice\_escalation\_template\] table where existing customers can continue using their current escalation workflows or migrate to the new flows, depending on their customizations.

As part of this update:

    -   The legacy Escalation-Approval workflow has been migrated to the low-code flow designer.
    -   The Escalation Master–Approval workflow has been converted into a business rule.
-   **[Account address enhancements](https://www.servicenow.com/docs/access?context=account-address-access-for-contacts&family=zurich&ft:locale=en-US)**

Enable contacts to access the account addresses that permit contacts to view both account-address records and the associated location information for accounts they’re authorized to access.

-   **Using [CSM Data Classification application](https://www.servicenow.com/docs/access?context=using-csm-data-classification&family=zurich&ft:locale=en-US)**

Use the new CSM Data Classification \(com.snc.csm\_data\_privacy\) Store app that delivers base system classifications for CRM data, categorizing it as internal, personally identifiable information \(PII\), confidential, and more. The solution uses the ServiceNow AI Platform data privacy capabilities, such as data classification, to apply protection measures and enhance data security.

-   **Support indirect sales through Business Locations with [Order Management for business location](https://www.servicenow.com/docs/access?context=order-managment-for-business-location&family=zurich&ft:locale=en-US), [Quote Management for business location](https://www.servicenow.com/docs/access?context=quote-management-for-business-location&family=zurich&ft:locale=en-US).**

Use the Sales Customer Relationship Management capabilities for both internal and external business organizations to enable Order Management, and Quote Management systems for business locations. Support channel sales and indirect sales by enabling business location staff to collaborate with an enterprise in managing customer orders, quotes, and performing the following actions:

    -   Permit enterprise sales agents to associate business locations as channel partners to create and fulfill customer orders and quotes.
    -   Enable self-service order tracking for internal and external business location staff through the Business Location Service Portal to track and manage customer orders.
    -   Support the tracking of multiple business locations for a single order or quote, either at the order line item level, order related party, quote line item level, or the quote related party.
    -   Improve the indirect sales cycle efficiency by converting approved channel quotes into customer orders.
-   **Support indirect sales through Business Locations with [Opportunity Management for business location](https://www.servicenow.com/docs/access?context=opportunity-management-for-business-location&family=zurich&ft:locale=en-US).**

Use the Sales Customer Relationship Management capabilities with both internal and external business organizations using Opportunity Management for business locations. Support channel sales by enabling business location staff to create and modify business opportunities and to track end-to-end life cycle of opportunities.

-   **CPQ integration with MACD workflows**

Introduced new data model changes to enable CPQ configurator usage for MACD workflows.

-   **[Sales and Service API Core](https://www.servicenow.com/docs/access?context=sales-and-services-api-core&family=zurich&ft:locale=en-US) and [Lead to Cash Core](https://www.servicenow.com/docs/access?context=entity-configuration-and-mapping&family=zurich&ft:locale=en-US)**

Granular admin roles introduced in Lead to Cash Core and Sales and Service API core.

-   **[Explore partial sync](https://www.servicenow.com/docs/access?context=about-partial-sync&family=zurich&ft:locale=en-US)**

Synchronize only specific sections of your data structure using the new partial sync capability in the create instance flow. This enhancement introduces the `allowedContextTypes` parameter, which enables you to specify exactly which types should be processed during synchronization operations. This leads to the following benefits:

    -   Improved performance: Reduction in processing time for targeted updates.
    -   Reduced resource consumption: Lower database queries, memory usage, and network bandwidth.
    -   Faster response times: Users experience quicker synchronization operations.
-   **[Granular roles in Install Base Management](https://www.servicenow.com/docs/access?context=r_rolesinstalledwithcustaccessmgmt&family=zurich&ft:locale=en-US)**

Added new granular roles with the sn\_install\_base.install\_base\_admin admin role, which is installed with Customer Service Install Base Management \[com.snc.install\_base\] plugin.

    -   sn\_install\_base.install\_base\_read
    -   sn\_install\_base.install\_base\_write
    -   sn\_install\_base.install\_base\_create
    -   sn\_install\_base.install\_base\_delete
    -   sn\_customerservice.customer\_data\_viewer
    -   sn\_customerservice.case.viewer
These roles provide you with more control over administrative tasks like read, write, create, delete, data view, and case view related to install base and sold product related entities.

-   **[Billing account store application](https://www.servicenow.com/docs/access?context=configuring-billing-accounts&family=zurich&ft:locale=en-US)**

Install the new CSM Billing Account Core store application, which introduces a foundational data model and hierarchy for managing billing accounts. It enables you to define billing relationships, establish account hierarchies, and track financial responsibility across your organization.

-   **[Sold product form](https://www.servicenow.com/docs/access?context=sold-product-form&family=zurich&ft:locale=en-US)**

The following enhancements are added for the Sold Product in this release:

    -   Billing Account: Enables direct reference to the associated Billing Account on the Sold Product entity within ServiceNow® CRM allowing agents to access financial information instantly during service delivery. This provides visibility into payment terms and conditions linked to the product, builds customer trust through transparent and predictable billing, and supports accurate revenue recognition for businesses.
    -   Start and end Dates: Provides full lifecycle state‑transition support \(**In preparation, Active, Expired, Cancelled**\) with automated date‑driven updates.

</td></tr><tr><td>

Australia

</td><td>

-   **[Configuring a contact as a consumer](https://www.servicenow.com/docs/access?context=configuring-a-contact-as-a-unified-consumer&family=australia&ft:locale=en-US)**

Model a single user who functions as both a contact and a consumer within your customer data structure. This capability improves administrative efficiency by reducing the overhead of creating and maintaining multiple user records for the same individual. It also provides a unified experience, eliminating the need to switch logins across different personas.

-   **[Granular administrative roles for Customer Data Foundation](https://www.servicenow.com/docs/access?context=customer-data&family=australia&ft:locale=en-US)**

Implemented administrative roles that provide fine-grained access control across CDF. These roles can be assigned to administrators and other personas based on job functions and security requirements. It includes the following capabilities:

    -   Added 25 admin roles with specific read, write, create, and delete permissions.
    -   Updated Before you begin sections across all Customer Data Foundation configuration topics with role prerequisites.
    -   Improved security compliance through role-based access segregation.
-   **[New fields in the Customer Account table](https://www.servicenow.com/docs/access?context=customer-data&family=australia&ft:locale=en-US)**

Added the following fields to the Customer Account \(customer\_account\) table to improve business identification and record management:

    -   DUNS Number: Store the Data Universal Numbering System \(DUNS\) identifier for business accounts to support data enrichment and third-party integrations.
    -   Active: Indicates whether an account record is active for filtering and workflow purposes.
-   **[Description field added Customer Data Foundation configuration tables](https://www.servicenow.com/docs/access?context=csm-cust-access-mgmt-tables&family=australia&ft:locale=en-US)**

Added a Description field to the following Customer Data Foundation \(CDF\) configuration tables to capture additional details about each record:

    -   Related Party Configuration \[sn\_customerservice\_related\_party\_configuration\] table
    -   Responsibility Definition \[sn\_customerservice\_responsibility\_def\] table
    -   Responsibility Access Configuration \[sn\_customerservice\_responsibility\_access\_config\] table
-   **[Billing accounts data model enhancements](https://www.servicenow.com/docs/access?context=add-related-parties-to-a-billing-account&family=australia&ft:locale=en-US)**

Grant contacts and consumers access to billing accounts through the related parties data model, using out of base system responsibilities and roles.

-   **[Service Model Foundation Granular admin roles](https://www.servicenow.com/docs/access?context=granular-admin-roles&family=australia&ft:locale=en-US)**

Added new granular admin roles to enable targeted permission assignments based on functional responsibilities, replacing broad admin access.

-   **[Add related parties to an install base item](https://www.servicenow.com/docs/access?context=add-related-party-install-base&family=australia&ft:locale=en-US)**

The Sold product is enhanced to support Related pricing.

-   **[Adding related parties to a sold product](https://www.servicenow.com/docs/access?context=add-related-parties-to-sp&family=australia&ft:locale=en-US)**

Use flexible price and quantity ramps that adapt over a product’s lifecycle, enabling time-based pricing, segment modifications during post-sale workflows, and accurate calculations across multi-year contracts.

-   **[Sold product form](https://www.servicenow.com/docs/access?context=sold-product-form&family=australia&ft:locale=en-US)**

Use scheduled jobs to update the state of the Sold product based on start and end dates. Ensure that sold products follow clear start and end dates with automatic state updates, giving customers fair access, predictable billing, and reducing errors through accurate lifecycle management and delta pricing.

-   **[Sold product form](https://www.servicenow.com/docs/access?context=sold-product-form&family=australia&ft:locale=en-US)**

Billing Account support on Sold Products to give agents immediate financial context, streamline billing‑related case resolution, and improve billing accuracy and transparency for customers and enterprises.

-   **[Business Organization Self Contributor persona](https://www.servicenow.com/docs/access?context=csm-data-model-roles&family=australia&ft:locale=en-US)**

Create and track service cases for themselves, and for sold products and install base items at a business location that are assigned to them, using the Business Organization Self Contributor \[sn\_bus\_loc.business\_org\_self\_contributor\] role. This role is available to frontline, field, and location-based workers. A new Buyer Organization Member field on the sold product and install base item lets managers associate these records with specific members.

-   **[Hierarchy-scoped access for business organization members](https://www.servicenow.com/docs/access?context=csm-assign-responsibilities&family=australia&ft:locale=en-US)**

Grant business organization members hierarchy-scoped access across child locations with administrator or manager-controlled exclusions using a new organization hierarchy responsibility, Organization Hierarchy Contributor \[org\_hierarchy\_contributor\]. Two new fields control the scope: Excluded Locations on the assignment, and Restricted on the business location.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Data Management for CSM features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **[Enhancements to the declarative responsibility framework](https://www.servicenow.com/docs/access?context=declarative-resposibility-framework&family=zurich&ft:locale=en-US)**

Introduced several key improvements to enhance the flexibility and usability of the declarative responsibility framework:

    -   Enabled responsibility access configurations to support more granular access control.
    -   Updated the data model by adding new fields and renaming select field labels for improved clarity.
    -   Refreshed associated forms and lists to reflect the latest framework updates.
-   **[Updated account manager responsibility access configuration](https://www.servicenow.com/docs/access?context=list-of-reponsibilities-provided-with-base-system&family=zurich&ft:locale=en-US)**

Enhanced access configurations for account manager responsibilities by creating a unified entity that defines access based on record and role for more consistent and streamlined access control.

-   **[Managing account addresses](https://www.servicenow.com/docs/access?context=associate-address-account&family=zurich&ft:locale=en-US)**

Manage account addresses by associating locations with accounts where the Update access is granted to confirm tracking of address information and support account management.

-   **[Updating location records associated with account](https://www.servicenow.com/docs/access?context=delete-address-location-form&family=zurich&ft:locale=en-US)**

Restricts users from updating a shared location record unless they have the Update access to all associated accounts, confirming location details can only be modified with the necessary permissions across every linked account.

-   **[Delta price enhancements](https://www.servicenow.com/docs/access?context=sold-product-form&family=zurich&ft:locale=en-US)**

The following are enhancements added in Delta pricing:

    -   Added pricing fields that reference sales agreements and captures base prices on sold products to verify consistent pricing during modifications, such as quantity changes or attribute updates. New fields are added to enhance the traceability for subscription-based products.
    -   Added columns to the Sold Product base table. Use the Split from and Split from root to track lineage during upsells, downsells, and expiration date changes ensuring accurate order management, compliance, and analytics.
-   **[Install base data model enhancements](https://www.servicenow.com/docs/access?context=create-install-base-item&family=zurich&ft:locale=en-US)**

Improve traceability and product life cycle management with the **Install Base Identifier** field on the install base form. Base install base items are mapped directly to model categories to support industry-specific product configurations.

Added **Provider Service Org** field on the install base form to support tracking, recall workflows, and post-sale engagement with dealers and partners.

-   **[Access control improvements](https://www.servicenow.com/docs/access?context=sold-product-form&family=zurich&ft:locale=en-US)**

Provide hierarchical access to Install Base items for location managers and staff to manage assets sold by or associated with their service organizations.

-   **[Entity configuration and mapping](https://www.servicenow.com/docs/access?context=entity-configuration-and-mapping&family=zurich&ft:locale=en-US)**

Gain precision in sales entity setup with three new columns in the Lead to Cash Entity Definition table: Filter Conditions, Enable Post Processing, and Post Processing Script. These columns enable targeted data filtering and post-processing logic execution.

-   **[Explore partial sync](https://www.servicenow.com/docs/access?context=about-partial-sync&family=zurich&ft:locale=en-US)**

Partial sync processes the data sections you specify instead of the entire structure, significantly improving performance and reducing resource consumption.

The partial sync enhancement includes improved error handling that provides clear, actionable error messages when mandatory fields are missing from synchronization requests.

-   **[Associate products and services](https://www.servicenow.com/docs/access?context=products-services-at-bus-loc&family=zurich&ft:locale=en-US)Support for service-related capabilities in business locations**

Enable service-related capabilities for business locations by activating the optional Customer Service Case Types \(sn\_csm\_case\_types\) plugin.


</td></tr><tr><td>

Australia

</td><td>

-   **[Enhanced Customer Data Viewer role](https://www.servicenow.com/docs/access?context=business-stakeholder-for-csm&family=australia&ft:locale=en-US)**

The Customer Data Viewer \(sn\_customerservice.customer\_data\_viewer\) role includes expanded access to additional data tables and menu items. These enhancements enable users to view a broader range of customer data while maintaining read-only access restrictions. With this enhancement, you can:

    -   Extend access to additional tables for the customer data viewer role
        -   Inherit household role in customer data viewer role
    -   Explore additional menu items now accessible to the customer data viewer role.

-   **[Household plugin migration to ServiceNow Store](https://www.servicenow.com/docs/access?context=activate-customer-service-household&family=australia&ft:locale=en-US)**

Starting with the Australia release, the Household family plugin \(com.snc.household\) has been migrated to the ServiceNow Store as a standalone application. Any new enhancements to this application are delivered through the Household store app. This change provides improved packaging, versioning, and deployment flexibility for B2C implementations that require household relationship management.


-   **[Guided setup access for granular admin roles](https://www.servicenow.com/docs/access?context=import-csm-accounts&family=australia&ft:locale=en-US)**

Access to foundation data steps in guided setup now aligns with CDF admin roles. This access change enables administrators to delegate specific configuration tasks to users based on their assigned roles, providing greater flexibility in managing setup responsibilities.

-   **[Extensible account code support](https://www.servicenow.com/docs/access?context=csm-account-code-account-path&family=australia&ft:locale=en-US)**

Updated the account code generation logic to support dynamic length scalability. Account codes now automatically expand from 4 digits to 5 or more as needed, ensuring unlimited account growth without manual intervention. Administrators can resolve invalid insert errors by clearing the system property to regenerate codes based on the maximum existing code.

-   **[Declarative Responsibility Framework enhancements](https://www.servicenow.com/docs/access?context=declarative-resposibility-framework&family=australia&ft:locale=en-US)**

Introduced usability and functional enhancements to the Customer Access Management \(CAM\) Declarative Responsibility Framework. These updates streamline access configuration management and improve flexibility for responsibility definitions. With this enhancement, you can now:

    -   Import or copy access configurations from one responsibility definition to another.
    -   Manage CAM-related assets through improved cleanup capabilities.
    -   Reference any field name in the Responsibility Definition field configuration.
-   **[Unified User configuration enhancements](https://www.servicenow.com/docs/access?context=configuring-unified-user&family=australia&ft:locale=en-US)**

Added a system property \(sn\_customerservice.consumer.allowed\_user\_types\) to enhance unified user management. This property specifies which user types \(classes\) can be associated with consumers.

-   **[Customer Life Cycle Management Workflows](https://www.servicenow.com/docs/access?context=customer-life-cycle-management-workflows&family=australia&ft:locale=en-US)**

Added core primitives to support price and quantity ramps, enabling flexible, time‑based changes across the sold product lifecycle. The feature delivers scalable pricing aligned with usage, simplifies post-sale workflows, and improves revenue forecasting without custom scripts.

-   **[Install base data model enhancements](https://www.servicenow.com/docs/access?context=create-install-base-item&family=australia&ft:locale=en-US)**

Improve traceability and product life cycle management with the **Install Base Identifier** field on the install base form. Base install base items are mapped directly to model categories to support industry-specific product configurations.

Added **Provider Service Org** field on the install base form to support tracking, recall workflows, and post-sale engagement with dealers and partners.

-   **[Sold product form](https://www.servicenow.com/docs/access?context=sold-product-form&family=australia&ft:locale=en-US)**

Create future‑dated subscription products in a **Pending Activation** state to improve the Add‑Order‑to‑Sold‑Product process. It also ensures lifecycle accuracy, predictable billing, and fair access for customers while improving revenue recognition for businesses.


-   **[Renamed entities](https://www.servicenow.com/docs/access?context=renamed-entities&family=australia&ft:locale=en-US)**

Renamed Service Model Foundation entities to improve clarity and maintain consistency across the platform. Review your existing configurations, scripts, or integrations that reference these entities and update them accordingly.

**Note:** The entity name changes are available in the Business Location 5.2.0 store app.


-   **[\[Placeholder link text to key use-hierarchial-list-view-for-sold-products\]](https://www.servicenow.com/docs/access?context=use-hierarchial-list-view-for-sold-products&family=australia&ft:locale=en-US)[Use hierarchical list view for sold products](https://www.servicenow.com/docs/access?context=use-hierarchial-list-view-for-sold-products&family=australia&ft:locale=en-US)**

Visualize the structure of a customer's sold products and product inventories as an expandable hierarchy directly on the account workspace.


-   **[Modify action limited to parent sold products](https://www.servicenow.com/docs/access?context=modify-a-sold-product&family=australia&ft:locale=en-US)**

Perform the **Modify** action for only root sold products.The **Modify** action is inactive for child sold products across the list view, detail view, and hierarchical list.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Data Management for CSM features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Data Management for CSM features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

The following legacy base system workflows have been deprecated:

-   Escalation Master-Approval
-   Escalation-Approval

Custom workflows remain supported, and you can continue to create them as needed. However, any new business requirements must be implemented using the new or updated flow-based framework rather than with the legacy workflows.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Data Management for CSM.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

CSM is a ServiceNow AI Platform application that is available with activation of the Customer Service Management plugin \(com.sn\_customerservice\). For details, see [Activate Customer Service Management](https://www.servicenow.com/docs/access?context=t_ActivateCustomerService&family=zurich&ft:locale=en-US).

 Additional CSM features are available with the activation of other plugins. For details, see [Additional plugins for Customer Service Management](https://www.servicenow.com/docs/access?context=r_CustServMgmtAddtlPluginsTable&family=zurich&ft:locale=en-US).

 Sales Customer Relationship Management is a ServiceNow AI Platform feature that is available with the activation of the Lead to Cash Core plugin \(com.snd.l2c.core\). For details, see [Explore](https://www.servicenow.com/docs/access?context=som-exploring&family=zurich&ft:locale=en-US).

 Starting in the Yokohama release, the following plugins are available on the ServiceNow Store for:

-   Install Base Management \(com.snc.install\_base\)
-   Install base characteristics \(com.snc.install\_base\_characteristics\)
-   Customer Service with Service Portfolio management \(com.snc.csm\_spm\)

For details, see [Configure Install base](https://www.servicenow.com/docs/access?context=configure-install-base&family=zurich&ft:locale=en-US).

 Starting from the Yokohama release, the Business Location plugin \(com.snc.business\_location\) is available on the ServiceNow Store. For details, see [Activate business locations](https://www.servicenow.com/docs/access?context=activate-business-location&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

CSM is a ServiceNow AI Platform application that is available with activation of the Customer Service Management \(CSM\) plugin \(com.sn\_customerservice\). For details, see [Activate Customer Service Management](https://www.servicenow.com/docs/access?context=t_ActivateCustomerService&family=australia&ft:locale=en-US).

 Additional CSM features are available with the activation of other plugins. For details, see [Additional plugins for Customer Service Management](https://www.servicenow.com/docs/access?context=r_CustServMgmtAddtlPluginsTable&family=australia&ft:locale=en-US).

 Sales Customer Relationship Management is a ServiceNow AI Platform feature that is available with the activation of the Lead to Cash Core plugin \(com.snd.l2c.core\). For details, see [Explore](https://www.servicenow.com/docs/access?context=som-exploring&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Data Management for CSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Data Management for CSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

Starting with the Zurich release, data management for Customer Service Management doesn't support mobile devices and Internet Explorer. For more information, see [Browser support](https://www.servicenow.com/docs/access?context=browser-support&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

Starting with the Australia release, data management for Customer Service Management doesn't support mobile devices and Internet Explorer. For more information, see [Browser support](https://www.servicenow.com/docs/access?context=browser-support&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Data Management for CSM, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   ****

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Data Management for CSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Data Management for CSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   Simplify your experience in viewing and applying protections to sensitive data by identifying, categorizing, and securing sensitive customer relationship management \(CRM\) data.
-   Streamline access management through an enhanced UI-based configuration, using the declarative framework enhancements in Customer Access Management \(CAM\).
-   Integrate Service Model Foundation with Order Management and Quote Management to enable enterprises to track orders and quotes that are generated by channel partners.
-   Add pricing fields based on sales agreements to capture base prices for sold products and verify consistent pricing.
-   Improve traceability with serial numbers on Install Base items and direct links to model categories for industry-specific configurations.
-   Enable partial sync using `allowedContextTypes` to sync specific sections with preserved structure and recursive filtering, and deliver clear, actionable error messages with consistent API responses.

 See [Data management](https://www.servicenow.com/docs/access?context=csm-data-management&family=zurich&ft:locale=en-US) feature for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Implement granular administrative roles across the Customer Data Foundation \(CDF\) for better access control over user permissions and data.
-   Support unified user modeling with Contact as Consumer functionality, enabling the user to function as both a business-to-business \(B2B\) and a business-to-consumer \(B2C\).
-   Migrate the Household \(com.snc.household\) plugin to ServiceNow Store for improved packaging and deployment flexibility.
-   Renamed Service Model Foundation entities for clarity and consistency. Update any configurations, scripts, or integrations that reference these entities.
-   Enable billing account support on Sold Products to give agents instant financial context, accelerate billing case resolution, and improve billing accuracy and transparency.

 See [Data management](https://www.servicenow.com/docs/access?context=csm-data-management&family=australia&ft:locale=en-US) feature for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-yokohama-australia/rn-combined-intro.md)

