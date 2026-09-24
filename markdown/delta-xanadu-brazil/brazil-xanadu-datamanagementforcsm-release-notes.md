---
title: Combined Data Management for CSM release notes for upgrades from Xanadu to Brazil
description: Consolidated page of all release notes for Data Management for CSM from Xanadu to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-brazil/brazil-xanadu-datamanagementforcsm-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 14
breadcrumb: [Products combined by family]
---

# Combined Data Management for CSM release notes for upgrades from Xanadu to Brazil

Consolidated page of all release notes for Data Management for CSM from Xanadu to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Data Management for CSM release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Data Management for CSM to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Billing account store application](https://www.servicenow.com/docs/access?context=configuring-billing-accounts&family=yokohama&ft:locale=en-US)**

Use the new CSM Billing Account Core store app that provides a foundational data model for managing billing accounts across organizations and users. It enables businesses to define, organize, and maintain billing relationships, supporting accurate billing, payments, and scalable financial operations.


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


</td></tr><tr><td>

Australia

</td><td>

-   **[External staff can resolve customer cases at their locations](https://www.servicenow.com/docs/access?context=access-limitations-for-ext-loc-customer-agent&family=australia&ft:locale=en-US)**

The external location consumer agents \(having sn\_customerservice.svc\_location\_consumer\_agent and snc\_external roles\) at external organization \(formerly external business location\) can create, view, update, and close customer cases directly from the classic environment, the same way internal location staff already can. This extends consistent, timely customer service across company-owned and third-party locations.

-   **[External staff can view colleague contact details at their location](https://www.servicenow.com/docs/access?context=csm-data-model-tables&family=australia&ft:locale=en-US)**

An external staff member with sn\_customerservice.service\_organization\_contributor role, can view the business phone number, mobile phone number, and email address of other external staff members at their organization in the classic environment.


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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Product Inventories configurations for Customer Life Cycle Management workflows](https://www.servicenow.com/docs/access?context=product_inventory_configurations&family=yokohama&ft:locale=en-US)**

Perform the Modify, Suspend, Resume, and Disconnect operations on product inventory records directly from the Product Inventory related list on the Accounts page.

-   **[Grant write access to account relationships](https://www.servicenow.com/docs/access?context=t_CreateAcctRelationshipRecord&family=yokohama&ft:locale=en-US)**

Enable administrators and customer service managers to update account relationship records.

-   **[Enable write access to contact relationships](https://www.servicenow.com/docs/access?context=t_CreateAContactRelationship&family=yokohama&ft:locale=en-US)**

Enable administrators and customer service managers to update the contact relationship records.

-   **[Populate the Type field in relationship tables using the fix script](https://www.servicenow.com/docs/access?context=migration-of-account-manager-responsibility-access&family=yokohama&ft:locale=en-US)**

Migrate the account manager responsibilities from the account team member relationships to the new responsibility access configurations. The updated framework enables you to manage access settings more efficiently.

-   **[Update roles within relationship agent and relationship contributor](https://www.servicenow.com/docs/access?context=features-supp-and-unsupp-by-unified-consumer&family=yokohama&ft:locale=en-US)**

Modify the roles of the relationship agent and relationship contributor to include the new granular roles that can grant access by responsibilities.


</td></tr><tr><td>

Zurich

</td><td>

-   **Coral theme**

Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


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


</td></tr><tr><td>

Australia

</td><td>

-   **[Modify action limited to parent sold products](https://www.servicenow.com/docs/access?context=modify-a-sold-product&family=australia&ft:locale=en-US)**

Perform the **Modify** action for only root sold products.The **Modify** action is inactive for child sold products across the list view, detail view, and hierarchical list.


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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   Escalation Master-Approval
-   Escalation-Approval

</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **Activation information**

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

-   **Activation information**

CSM is a ServiceNow AI Platform application that is available with activation of the Customer Service Management \(CSM\) plugin \(com.sn\_customerservice\). For details, see [Activate Customer Service Management](https://www.servicenow.com/docs/access?context=t_ActivateCustomerService&family=australia&ft:locale=en-US).

Additional CSM features are available with the activation of other plugins. For details, see [Additional plugins for Customer Service Management](https://www.servicenow.com/docs/access?context=r_CustServMgmtAddtlPluginsTable&family=australia&ft:locale=en-US).

Sales Customer Relationship Management is a ServiceNow AI Platform feature that is available with the activation of the Lead to Cash Core plugin \(com.snd.l2c.core\). For details, see [Explore](https://www.servicenow.com/docs/access?context=som-exploring&family=australia&ft:locale=en-US).


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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **Browser requirements**

Starting with the Zurich release, data management for Customer Service Management doesn't support mobile devices and Internet Explorer. For more information, see [Browser support](https://www.servicenow.com/docs/access?context=browser-support&family=zurich&ft:locale=en-US).


</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **Accessibility information**
    -   **Dark theme**

The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr><tr><td>

Brazil

</td><td>

-   Unify billing schedules and payment profiles across all billing accounts, with visibility into when each account is billed, who is responsible for payment, and how payments are collected.
-   Manage related parties and deal context on sold products, and enable customers to create and track Return Merchandise Authorization \(RMA\) cases directly from the portal.
-   Track business organization outages efficiently. As a major case manager, get auto-proposed major cases and child cases for every affected organization, ensuring consistent updates across all impacted accounts.

 See [Data management](https://www.servicenow.com/docs/access?context=csm-data-management&family=brazil&ft:locale=en-US) feature for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-xanadu-brazil/rn-combined-intro.md)

