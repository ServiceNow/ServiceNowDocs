---
title: Combined Data Management for CSM release notes for upgrades from Australia to Brazil
description: Consolidated page of all release notes for Data Management for CSM from Australia to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-australia-brazil/brazil-australia-datamanagementforcsm-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 15
breadcrumb: [Products combined by family]
---

# Combined Data Management for CSM release notes for upgrades from Australia to Brazil

Consolidated page of all release notes for Data Management for CSM from Australia to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Data Management for CSM release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Australia to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Data Management for CSM to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for Data Management for CSM.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[External staff can resolve customer cases at their locations](https://www.servicenow.com/docs/access?context=access-limitations-for-ext-loc-customer-agent&family=australia&ft:locale=en-US)**

The external location consumer agents \(having sn\_customerservice.svc\_location\_consumer\_agent and snc\_external roles\) at external organization \(formerly external business location\) can create, view, update, and close customer cases directly from the classic environment, the same way internal location staff already can. This extends consistent, timely customer service across company-owned and third-party locations.

-   **[External staff can view colleague contact details at their location](https://www.servicenow.com/docs/access?context=csm-data-model-tables&family=australia&ft:locale=en-US)**

An external staff member with sn\_customerservice.service\_organization\_contributor role, can view the business phone number, mobile phone number, and email address of other external staff members at their organization in the classic environment.


 -   **[Create Return Merchandise Authorization case lines](https://www.servicenow.com/docs/access?context=create-return-merchandise-authorization-case-lines&family=australia&ft:locale=en-US)**

Enable agents to initiate return requests directly from sold product records along with install base items. Return cases automatically map order and product details to the case, giving users an end-to-end visibility into their returns and reducing processing times.

-   **[Proactive Customer Service Operations](https://www.servicenow.com/docs/access?context=proactive-service-operations&family=australia&ft:locale=en-US)**

Event management operators now have a dedicated customer service management role for access control when setting up new installations. The access to customer data for event management operators is granted through a limited scope role \(sn\_pro\_cs\_ops.csm\_evt\_mgmt\_stakeholder\) instead of the global platform role \(evt\_mgmt\_operator\) role.

-   **[Synchronizing life-cycle values](https://www.servicenow.com/docs/access?context=cmdb-asset-CI-IBI-sync-options&family=australia&ft:locale=en-US)**

Configure a model category as a product instance to enable the system to synchronize life cycle values between asset and install base item. The synchronization uses the life cycle stage and life cycle state status values.


 -   **[Business Organization Self Contributor persona](https://www.servicenow.com/docs/access?context=csm-data-model-roles&family=australia&ft:locale=en-US)**

Create and track service cases for themselves and for sold products and install base items at a business location that are assigned to them. Use the Business Organization Self Contributor \[sn\_bus\_loc.business\_org\_self\_contributor\] role. This role is available to frontline, field, and location-based workers. A new Buyer Organization Member field on the sold product and install base item lets managers associate these records with specific members.

-   **[Hierarchy-scoped access for business organization members](https://www.servicenow.com/docs/access?context=csm-assign-responsibilities&family=australia&ft:locale=en-US)**

Grant business organization members hierarchy-scoped access across child locations with administrator or manager-controlled exclusions using a new organization hierarchy responsibility, Organization Hierarchy Contributor \[org\_hierarchy\_contributor\]. Two new fields control the scope: Excluded Locations on the assignment, and Restricted on the business location.


 -   **[Configuring a contact as a consumer](https://www.servicenow.com/docs/access?context=configuring-a-contact-as-a-unified-consumer&family=australia&ft:locale=en-US)**

Model a single user who functions as both a contact and a consumer within your customer data structure. This capability improves administrative efficiency by reducing the overhead of creating and maintaining multiple user records for the same individual. It also provides a unified experience, eliminating the must switch logins across different personas.

-   **[Billing accounts data model enhancements](https://www.servicenow.com/docs/access?context=add-related-parties-to-a-billing-account&family=australia&ft:locale=en-US)**

Grant contacts and consumers access to billing accounts through the related parties data model, using out of base system responsibilities and roles.

-   **[Service Model Foundation Granular admin roles](https://www.servicenow.com/docs/access?context=granular-admin-roles&family=australia&ft:locale=en-US)**

Added new granular admin roles to enable targeted permission assignments based on functional responsibilities, replacing broad admin access.

-   **[Add related parties to an install base item](https://www.servicenow.com/docs/access?context=add-related-party-install-base&family=australia&ft:locale=en-US)**

The Sold product is enhanced to support Related pricing.

-   **[Adding related parties to a sold product](https://www.servicenow.com/docs/access?context=add-related-parties-to-sp&family=australia&ft:locale=en-US)**

Use flexible price and quantity ramps that adapt over a product’s lifecycle, enabling time-based pricing, segment modifications during post-sale workflows, and accurate calculations across multi-year contracts.

-   **[Sold product form](https://www.servicenow.com/docs/access?context=sold-product-form&family=australia&ft:locale=en-US)**

Use scheduled jobs to update the state of the Sold product based on start and end dates. Automatic state updates ensure fair access and predictable billing. This reduces errors through accurate lifecycle management and delta pricing.

-   **[Sold product form](https://www.servicenow.com/docs/access?context=sold-product-form&family=australia&ft:locale=en-US)**

Billing Account support on Sold Products to give agents immediate financial context, streamline billing‑related case resolution, and improve billing accuracy and transparency for customers and enterprises.


 -   **[Granular administrative roles for Customer Data Foundation](https://www.servicenow.com/docs/access?context=customer-data&family=australia&ft:locale=en-US)**

Implemented administrative roles that provide fine-grained access control across CDF. These roles can be assigned to administrators and other personas based on job functions and security requirements. It includes the following capabilities:

    -   Added 25 admin roles with specific read, write, create, and delete permissions.
    -   Updated Before you begin sections across all Customer Data Foundation configuration topics with role prerequisites.
    -   Improved security compliance through role-based access segregation.
-   **[New fields in the Customer Account table](https://www.servicenow.com/docs/access?context=customer-data&family=australia&ft:locale=en-US)**

Added the following fields to the Customer Account \(customer\_account\) table to improve business identification and record management:

    -   DUNS Number: Store the Data Universal Numbering System \(DUNS\) identifier for business accounts to support data enrichment and third party integrations.
    -   Active: Indicates whether an account record is active for filtering and workflow purposes.
-   **[Description field added Customer Data Foundation configuration tables](https://www.servicenow.com/docs/access?context=csm-cust-access-mgmt-tables&family=australia&ft:locale=en-US)**

Added a Description field to the following Customer Data Foundation \(CDF\) configuration tables to capture additional details about each record:

    -   Related Party Configuration \[sn\_customerservice\_related\_party\_configuration\] table
    -   Responsibility Definition \[sn\_customerservice\_responsibility\_def\] table
    -   Responsibility Access Configuration \[sn\_customerservice\_responsibility\_access\_config\] table

</td></tr><tr><td>

Brazil

</td><td>

-   **[Restricted Customer Access now controls visibility](https://www.servicenow.com/docs/access?context=associate-customers-or-bus-loc-to-so&family=brazil&ft:locale=en-US)**

Extended the organization customer criteria for a business organization with a new **Restricted Customer Access** check box that controls visibility of customer records. When enabled, business organization staff can view only the customer and consumer records that satisfy the configured criteria at their business organization. This applies to both service and sales personas. Upgrade customers must run the one-time scheduled job, **Remove Legacy roles from Loc Mgr Contrib** to enable restricted customer access configuration.

-   **[New business organization-scoped contributor personas](https://www.servicenow.com/docs/access?context=csm-contributor-user-roles&family=brazil&ft:locale=en-US)**

Added two new roles, Business Org Account Contributor \[sn\_bus\_loc.business\_org\_account\_contributor\] and Business Org Consumer Contributor \[sn\_bus\_loc.business\_org\_account\_contributor\] that grant location-scoped equivalents of the existing Account Contributor and Consumer Contributor roles. With Business Org Account Contributor role, you can create cases for accounts supported by your business organization. You can also track and manage cases created by you for the accounts associated with your organization. With Business Org Consumer Contributor role, you can create cases for consumers or households supported by your business organization. You can also track and manage cases created by you for the consumers or households associated with your organization.

-   **[Proactive Customer Service extended to business organizations](https://www.servicenow.com/docs/access?context=configure-flow-designer-bo&family=brazil&ft:locale=en-US)**

Extended proactive customer service and major case management to business organizations, alongside the existing support for accounts and consumers. When a network alert affects install base items belonging to a business organization, the system can propose a major case and build a recipient list of the affected business organizations. If the major case manager accepts the proposal, they can create a child case for each affected business organization, so all affected business organizations are tracked and updated under a single major case. Business Organization staff can track cases from Business Organization Support Portal.

-   **[Billing account address](https://www.servicenow.com/docs/access?context=associate-location-with-billing-account&family=brazil&ft:locale=en-US)**

Associate one or more locations with a billing account using the new Billing Account Address \[sn\_billing\_account\_address\] table. Each address record captures the address type, identifies the primary address, and tracks whether the address is active or inactive.

-   **[Billing account payment profile](https://www.servicenow.com/docs/access?context=add-payment-profile-to-billing-account&family=brazil&ft:locale=en-US)**

Define payment information for a billing account using the new Billing Account Payment Profile \[sn\_billing\_account\_payment\_profile\] table, which captures the payment method and related payment details for the account.

-   **[Payment responsibility on billing accounts](https://www.servicenow.com/docs/access?context=add-payment-profile-to-billing-account&family=brazil&ft:locale=en-US)**

Specify who pays for a billing account with the new Paying party and Paying billing account fields, supporting self, parent, and designated-account payment relationships.

-   **[Billing schedules on billing accounts](https://www.servicenow.com/docs/access?context=set-up-billing-schedule-for-billing-account&family=brazil&ft:locale=en-US)**

Define when billing occurs for a billing account with the new Billing Schedule field, which links the account to a platform schedule and its schedule entry records. The new billing account schedule viewer \[sn\_billing\_account.schedule\_viewer\] and writer \[sn\_billing\_account.schedule\_writer\] roles control read and write access to these schedules.

-   **New fields across the Customer Data Foundation tables**

Added fields to the core customer data model tables to support segmentation, life cycle tracking, and external-system integration:

    -   **Account table**: Account stage, Account status, Customer since, Relationship tier, Market segment, Total ACV, and External ID
    -   **Contact table**: External ID
    -   **Consumer table**: Consumer stage, Consumer status, Customer since, Relationship tier, and External ID
    -   **Account Team Member table**: Active, Start date, and End date

</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Data Management for CSM features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Modify action limited to parent sold products](https://www.servicenow.com/docs/access?context=modify-a-sold-product&family=australia&ft:locale=en-US)**

Perform the **Modify** action for only root sold products.The **Modify** action is inactive for child sold products across the list view, detail view, and hierarchical list.


 -   **[Renamed entities](https://www.servicenow.com/docs/access?context=renamed-entities&family=australia&ft:locale=en-US)**

Renamed Service Model Foundation entities to improve clarity and maintain consistency across the platform. Review your existing configurations, scripts, or integrations that reference these entities and update them accordingly.

**Note:** The entity name changes are available in the Business Location 5.2.0 store app.


 -   **[Household plugin migration to ServiceNow Store](https://www.servicenow.com/docs/access?context=activate-customer-service-household&family=australia&ft:locale=en-US)**

Starting with the Australia release, the Household family plugin \(com.snc.household\) has been migrated to the ServiceNow Store as a standalone application. Any new enhancements to this application are delivered through the Household store app. This change provides improved packaging, versioning, and deployment flexibility for B2C implementations that require household relationship management.


 -   **[Customer Life Cycle Management Workflows](https://www.servicenow.com/docs/access?context=customer-life-cycle-management-workflows&family=australia&ft:locale=en-US)**

Added core primitives to support price and quantity ramps, enabling flexible, time‑based changes across the sold product lifecycle. The feature delivers scalable pricing aligned with usage, simplifies post-sale workflows, and improves revenue forecasting without custom scripts.

-   **[Sold product form](https://www.servicenow.com/docs/access?context=sold-product-form&family=australia&ft:locale=en-US)**

Create future‑dated subscription products in a **Pending Activation** state to improve the Add‑Order‑to‑Sold‑Product process. It also ensures lifecycle accuracy, predictable billing, and fair access for customers while improving revenue recognition for businesses.


 -   **[Enhanced Customer Data Viewer role](https://www.servicenow.com/docs/access?context=business-stakeholder-for-csm&family=australia&ft:locale=en-US)**

The Customer Data Viewer \(sn\_customerservice.customer\_data\_viewer\) role includes expanded access to additional data tables and menu items. These enhancements enable users to view a broader range of customer data while maintaining read-only access restrictions. With this enhancement, you can:

    -   Extend access to additional tables for the customer data viewer role
        -   Inherit household role in customer data viewer role
    -   Explore additional menu items now accessible to the customer data viewer role.

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

-   **[Configuring billing accounts](https://www.servicenow.com/docs/access?context=configuring-billing-accounts&family=australia&ft:locale=en-US)**

Visualize a billing account's hierarchy directly from the account, making large parent-and-child account structures easier to navigate. The default view now adapts to the billing account type. The **Billing account type** field is populated automatically from the source customer to reduce manual setup and keep records consistent.


</td></tr><tr><td>

Brazil

</td><td>

-   **[Project task assignment access for business organization staff](https://www.servicenow.com/docs/access?context=csm-data-model-roles&family=brazil&ft:locale=en-US)**

Gain write access to the Assignment group and Assigned to field, and read access to the Priority field, on business organization project tasks with the Location Project Member \[sn\_bus\_loc.location\_project\_stakeholder\] or Location Project Manager Contributor \[sn\_bus\_loc.location\_manager\_project\_stakeholder\] role.

-   **[Billing account roles and responsibility access](https://www.servicenow.com/docs/access?context=granular-roles-and-supported-entities-CAM&family=brazil&ft:locale=en-US)**

Updated billing account roles and responsibility access to align with the expanded billing account capabilities. Extended access to Billing Account Address, Billing Account Payment Profile, and Billing Schedule \(schedule and schedule entry\) through:

    -   Billing Account platform granular and CRM granular roles
    -   Billing Account responsibilities through the customer access management \(CAM\) framework
-   **[Create a sold product](https://www.servicenow.com/docs/access?context=create-sold-item&family=brazil&ft:locale=en-US)**

Edit and view multiple related parties in the sold product enable users to review the details of a deal and review deal context without leaving the record. **Deal type** and **Route to Market** aren't captured on the sold product, with route to market options filtered automatically based on the selected deal type.

-   **[Create return merchandize authorization \(RMA\) cases directly from the business portal](https://www.servicenow.com/docs/access?context=rma-case-self-service&family=brazil&ft:locale=en-US)**

Initiate an RMA case from the business portal without contacting an agent to reduce the back-and-forth for returns and replacements.

    -   Enable customer contacts to view the list of their RMA cases from the **Request** menu on the portal to track their requests in progress.
    -   Customer contacts can open individual RMA cases and drill into case lines to review its status and details.

</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Data Management for CSM features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some Data Management for CSM features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   As part of the CAM Declarative Responsibility Framework enhancements, the following legacy fields have been marked deprecated:
    -   **Restrict access to** field from the Responsibility Access Configuration \[sn\_customerservice\_responsibility\_access\_config\] table
    -   **Applicable to** field from the Responsibility Definition \[sn\_customerservice\_responsibility\_def\] table
-   Starting with the Australia release, the Household plugin \(com.snc.household\) is available as a store plugin. The family version of the plugin is being prepared for future deprecation. On upgrading, customers will automatically move to the store version of the plugin. It will be hidden from the family plugins and no longer installed on new instances but will continue to be supported as a store plugin. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

 -   **Restrict access to** field from the Responsibility Access Configuration \[sn\_customerservice\_responsibility\_access\_config\] table
-   **Applicable to** field from the Responsibility Definition \[sn\_customerservice\_responsibility\_def\] table

</td></tr><tr><td>

Brazil

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

Australia

</td><td>

-   **Activation information**

CSM is a ServiceNow AI Platform application that is available with activation of the Customer Service Management \(CSM\) plugin \(com.sn\_customerservice\). For details, see [Activate Customer Service Management](https://www.servicenow.com/docs/access?context=t_ActivateCustomerService&family=australia&ft:locale=en-US).

Additional CSM features are available with the activation of other plugins. For details, see [Additional plugins for Customer Service Management](https://www.servicenow.com/docs/access?context=r_CustServMgmtAddtlPluginsTable&family=australia&ft:locale=en-US).

Sales Customer Relationship Management is a ServiceNow AI Platform feature that is available with the activation of the Lead to Cash Core plugin \(com.snd.l2c.core\). For details, see [Explore](https://www.servicenow.com/docs/access?context=som-exploring&family=australia&ft:locale=en-US).


**Important:** Business Location and Install Base Management are available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr><tr><td>

Brazil

</td><td>

-   **Activation information**

CSM is a ServiceNow AI Platform application that is available with activation of the Customer Service Management \(CSM\) plugin \(com.sn\_customerservice\). For details, see [Activate Customer Service Management](https://www.servicenow.com/docs/access?context=t_ActivateCustomerService&family=brazil&ft:locale=en-US).

Additional CSM features are available with the activation of other plugins. For details, see [\[Placeholder link text to key bundle-csm.r\_CustServMgmtAddtlPluginsTable\]](https://www.servicenow.com/docs/access?context=r_CustServMgmtAddtlPluginsTable&family=brazil&ft:locale=en-US).

Sales Customer Relationship Management is a ServiceNow AI Platform feature that is available with the activation of the Lead to Cash Core plugin \(com.snd.l2c.core\). For details, see [Explore](https://www.servicenow.com/docs/access?context=som-exploring&family=brazil&ft:locale=en-US).


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Data Management for CSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Australia

</td><td>

-   **Browser requirements**

Starting with the Australia release, data management for Customer Service Management doesn't support mobile devices and Internet Explorer. For more information, see [Browser support](https://www.servicenow.com/docs/access?context=browser-support&family=australia&ft:locale=en-US).


</td></tr><tr><td>

Brazil

</td><td>

-   **Browser requirements**

Starting with the Brazil release, data management for Customer Service Management doesn't support mobile devices and Internet Explorer. For more information, see [Browser support](https://www.servicenow.com/docs/access?context=browser-support&family=brazil&ft:locale=en-US).


</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Data Management for CSM, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Australia

</td><td>

-   Implement granular administrative roles across the Customer Data Foundation \(CDF\) for better access control over user permissions and data.
-   Support unified user modeling with Contact as Consumer functionality, enabling the user to function as both a business-to-business \(B2B\) and a business-to-consumer \(B2C\).
-   Migrate the Household \(com.snc.household\) plugin to ServiceNow Store for improved packaging and deployment flexibility.
-   Renamed Service Model Foundation entities for clarity and consistency. Update any configurations, scripts, or integrations that reference these entities.
-   Enable billing account support on Sold Products to give agents instant financial context, accelerate billing case resolution, and improve billing accuracy and transparency.

 See [Data management](https://www.servicenow.com/docs/access?context=csm-data-management&family=australia&ft:locale=en-US) feature for more information.

</td></tr><tr><td>

Brazil

</td><td>

-   Unify billing schedules and payment profiles across all billing accounts, with visibility into when each account is billed, who is responsible for payment, and how payments are collected.
-   Manage related parties and deal context on sold products, and enable customers to create and track Return Merchandise Authorization \(RMA\) cases directly from the portal.
-   Track business organization outages efficiently. As a major case manager, get auto-proposed major cases and child cases for every affected organization, ensuring consistent updates across all impacted accounts.

 See [Data management](https://www.servicenow.com/docs/access?context=csm-data-management&family=brazil&ft:locale=en-US) feature for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-australia-brazil/rn-combined-intro.md)

