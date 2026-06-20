---
title: Combined Data Management for CSM release notes for upgrades from Washington DC to Zurich
description: Consolidated page of all release notes for Data Management for CSM from Washington DC to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-washingtondc-zurich/zurich-washingtondc-datamanagementforcsm-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 11
breadcrumb: [Products combined by family]
---

# Combined Data Management for CSM release notes for upgrades from Washington DC to Zurich

Consolidated page of all release notes for Data Management for CSM from Washington DC to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Data Management for CSM release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Data Management for CSM to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Data Management for CSM.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

-   **Naming customer relationship records for [Consumer team member relationship tables](https://servicenow-staging.fluidtopics.net/access?context=assign-team-member-to-consumer&family=zurich&ft:locale=en-US) and [Household team member relationship tables](https://servicenow-staging.fluidtopics.net/access?context=assign-team-member-to-household&family=zurich&ft:locale=en-US)**

Use the **Type** field through related party configurations to name records in the consumer team member and household team member relationship tables. This functionality enables you to label relationships based on the purpose of the association and relevant industry use cases.

-   **[Migrating legacy workflow to low code](https://servicenow-staging.fluidtopics.net/access?context=create-escalation-template&family=zurich&ft:locale=en-US)**

Added an **Escalation Approval Flow** field to the Escalation Template \[sn\_customerservice\_escalation\_template\] table where existing customers can continue using their current escalation workflows or migrate to the new flows, depending on their customizations.

As part of this update:

    -   The legacy Escalation-Approval workflow has been migrated to the low-code flow designer.
    -   The Escalation Master–Approval workflow has been converted into a business rule.
-   **[Account address enhancements](https://servicenow-staging.fluidtopics.net/access?context=account-address-access-for-contacts&family=zurich&ft:locale=en-US)**

Enable contacts to access the account addresses that permit contacts to view both account-address records and the associated location information for accounts they’re authorized to access.

-   **Using [CSM Data Classification application](https://servicenow-staging.fluidtopics.net/access?context=using-csm-data-classification&family=zurich&ft:locale=en-US)**

Use the new CSM Data Classification \(com.snc.csm\_data\_privacy\) Store app that delivers base system classifications for CRM data, categorizing it as internal, personally identifiable information \(PII\), confidential, and more. The solution uses the ServiceNow AI Platform data privacy capabilities, such as data classification, to apply protection measures and enhance data security.

-   **Support indirect sales through Business Locations with [Order Management for business location](https://servicenow-staging.fluidtopics.net/access?context=order-managment-for-business-location&family=zurich&ft:locale=en-US), [Quote Management for business location](https://servicenow-staging.fluidtopics.net/access?context=quote-management-for-business-location&family=zurich&ft:locale=en-US).**

Use the Sales and Order Management capabilities for both internal and external business organizations to enable Order Management, and Quote Management systems for business locations. Support channel sales and indirect sales by enabling business location staff to collaborate with an enterprise in managing customer orders, quotes, and performing the following actions:

    -   Permit enterprise sales agents to associate business locations as channel partners to create and fulfill customer orders and quotes.
    -   Enable self-service order tracking for internal and external business location staff through the Business Location Service Portal to track and manage customer orders.
    -   Support the tracking of multiple business locations for a single order or quote, either at the order line item level, order related party, quote line item level, or the quote related party.
    -   Improve the indirect sales cycle efficiency by converting approved channel quotes into customer orders.
-   **Support indirect sales through Business Locations with [Opportunity Management for business location](https://servicenow-staging.fluidtopics.net/access?context=opportunity-management-for-business-location&family=zurich&ft:locale=en-US).**

Use the Sales and Order Management capabilities with both internal and external business organizations using Opportunity Management for business locations. Support channel sales by enabling business location staff to create and modify business opportunities and to track end-to-end life cycle of opportunities.

-   **ServiceNow CPQ integration with MACD workflows**

Introduced new data model changes to enable ServiceNow CPQ configurator usage for MACD workflows.

-   **[Sales and Service API Core](https://servicenow-staging.fluidtopics.net/access?context=sales-and-services-api-core&family=zurich&ft:locale=en-US) and [Lead to Cash Core](https://servicenow-staging.fluidtopics.net/access?context=entity-configuration-and-mapping&family=zurich&ft:locale=en-US)**

Granular admin roles introduced in Lead to Cash Core and Sales and Service API core.

-   **[Explore Partial sync](https://servicenow-staging.fluidtopics.net/access?context=about-partial-sync&family=zurich&ft:locale=en-US)**

Synchronize only specific sections of your data structure using the new partial sync capability in the create instance flow. This enhancement introduces the `allowedContextTypes` parameter, which enables you to specify exactly which types should be processed during synchronization operations. This leads to the following benefits:

    -   Improved performance: Reduction in processing time for targeted updates.
    -   Reduced resource consumption: Lower database queries, memory usage, and network bandwidth.
    -   Faster response times: Users experience quicker synchronization operations.
    -   Better scalability: System handles higher volumes with lower resource requirements.
    -   Flexible configuration: Adapt sync behavior to your specific use case.
-   **[Improved error handling for synchronization operations](https://servicenow-staging.fluidtopics.net/access?context=about-partial-sync&family=zurich&ft:locale=en-US)**

The partial sync enhancement includes improved error handling that provides clear, actionable error messages when mandatory fields are missing from synchronization requests. Benefits:

    -   Faster troubleshooting with clear error messages.
    -   Reduced configuration errors through validation.
    -   Improved system stability with graceful handling.
    -   Better developer experience with helpful guidance.
-   **[Recursive filtering and structure preservation](https://servicenow-staging.fluidtopics.net/access?context=about-partial-sync&family=zurich&ft:locale=en-US)**

The partial sync enhancement implements advanced filtering logic to maintain data integrity while optimizing performance.

    -   Consistent API responses across all operations
    -   Predictable data structure for client applications
    -   Reduced integration errors from missing fields
    -   Simplified error handling in consuming systems
-   **[Granular roles in Install Base Management](https://servicenow-staging.fluidtopics.net/access?context=r_rolesinstalledwithcustaccessmgmt&family=zurich&ft:locale=en-US)**

Added new granular roles with the sn\_install\_base.install\_base\_admin admin role, which is installed with Customer Service Install Base Management \[com.snc.install\_base\] plugin.

    -   sn\_install\_base.install\_base\_read
    -   sn\_install\_base.install\_base\_write
    -   sn\_install\_base.install\_base\_create
    -   sn\_install\_base.install\_base\_delete
    -   sn\_customerservice.customer\_data\_viewer
    -   sn\_customerservice.case.viewer
These roles provide you with more control over administrative tasks like read, write, create, delete, data view, and case view related to install base and sold product related entities.

-   **[Billing account store application](https://servicenow-staging.fluidtopics.net/access?context=configuring-billing-accounts&family=zurich&ft:locale=en-US)**

Install the new CSM Billing Account Core store application, which introduces a foundational data model and hierarchy for managing billing accounts. It enables you to define billing relationships, establish account hierarchies, and track financial responsibility across your organization.

-   **[Sold product form](https://servicenow-staging.fluidtopics.net/access?context=sold-product-form&family=zurich&ft:locale=en-US)**

The following enhancements are added for the Sold Product in this release:

    -   Billing Account: Enables direct reference to the associated Billing Account on the Sold Product entity within ServiceNow® CRM allowing agents to access financial information instantly during service delivery. This provides visibility into payment terms and conditions linked to the product, builds customer trust through transparent and predictable billing, and supports accurate revenue recognition for businesses.
    -   Start and end Dates: Provides full lifecycle state‑transition support \(**In preparation, Active, Expired, Cancelled**\) with automated date‑driven updates.

</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Data Management for CSM features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

-   **[Enhancements to the declarative responsibility framework](https://servicenow-staging.fluidtopics.net/access?context=declarative-resposibility-framework&family=zurich&ft:locale=en-US)**

Introduced several key improvements to enhance the flexibility and usability of the declarative responsibility framework:

    -   Enabled responsibility access configurations to support more granular access control.
    -   Updated the data model by adding new fields and renaming select field labels for improved clarity.
    -   Refreshed associated forms and lists to reflect the latest framework updates.
-   **[Updated account manager responsibility access configuration](https://servicenow-staging.fluidtopics.net/access?context=list-of-reponsibilities-provided-with-base-system&family=zurich&ft:locale=en-US)**

Enhanced access configurations for account manager responsibilities by creating a unified entity that defines access based on record and role for more consistent and streamlined access control.

-   **[Managing account addresses](https://servicenow-staging.fluidtopics.net/access?context=associate-address-account&family=zurich&ft:locale=en-US)**

Manage account addresses by associating locations with accounts where the Update access is granted to confirm tracking of address information and support account management.

-   **[Updating location records associated with account](https://servicenow-staging.fluidtopics.net/access?context=delete-address-location-form&family=zurich&ft:locale=en-US)**

Restricts users from updating a shared location record unless they have the Update access to all associated accounts, confirming location details can only be modified with the necessary permissions across every linked account.

-   **[Delta price enhancements](https://servicenow-staging.fluidtopics.net/access?context=sold-product-form&family=zurich&ft:locale=en-US)**

The following are enhancements added in Delta pricing:

    -   Added pricing fields that reference sales agreements and captures base prices on sold products to verify consistent pricing during modifications, such as quantity changes or attribute updates. New fields are added to enhance the traceability for subscription-based products.
    -   Added columns to the Sold Product base table. Use the Split from and Split from root to track lineage during upsells, downsells, and expiration date changes ensuring accurate order management, compliance, and analytics.
-   **[Install base data model enhancements](https://servicenow-staging.fluidtopics.net/access?context=create-install-base-item&family=zurich&ft:locale=en-US)**

Improve traceability and product life cycle management with the **Serial Number** field on the install base form. Base install base items are mapped directly to model categories to support industry-specific product configurations.

Added **Provider Service Org** field on the install base form to support tracking, recall workflows, and post-sale engagement with dealers and partners.

-   **[Access control improvements](https://servicenow-staging.fluidtopics.net/access?context=sold-product-form&family=zurich&ft:locale=en-US)**

Provide hierarchical access to Install Base items for location managers and staff to manage assets sold by or associated with their service organizations.

-   **[Entity configuration and mapping](https://servicenow-staging.fluidtopics.net/access?context=entity-configuration-and-mapping&family=zurich&ft:locale=en-US)**

Gain precision in sales entity setup with three new columns in the Lead to Cash Entity Definition table: Filter Conditions, Enable Post Processing, and Post Processing Script. These columns enable targeted data filtering and post-processing logic execution.

-   **[Explore Partial sync](https://servicenow-staging.fluidtopics.net/access?context=about-partial-sync&family=zurich&ft:locale=en-US)**

Partial sync processes the data sections you specify instead of the entire structure, significantly improving performance and reducing resource consumption.

The partial sync enhancement includes improved error handling that provides clear, actionable error messages when mandatory fields are missing from synchronization requests.

-   **[Associate products and services](https://servicenow-staging.fluidtopics.net/access?context=products-services-at-bus-loc&family=zurich&ft:locale=en-US)Support for service-related capabilities in business locations**

Enable service-related capabilities for business locations by activating the optional Customer Service Case Types \(sn\_csm\_case\_types\) plugin.


</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Data Management for CSM features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Data Management for CSM features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

The following legacy base system workflows have been deprecated:

-   Escalation Master-Approval
-   Escalation-Approval

Custom workflows remain supported, and you can continue to create them as needed. However, any new business requirements must be implemented using the new or updated flow-based framework rather than with the legacy workflows.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Data Management for CSM.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

CSM is a ServiceNow AI Platform application that is available with activation of the Customer Service Management plugin \(com.sn\_customerservice\). For details, see [Activate Customer Service Management](https://servicenow-staging.fluidtopics.net/access?context=t_ActivateCustomerService&family=zurich&ft:locale=en-US).

 Additional CSM features are available with the activation of other plugins. For details, see [Additional plugins for Customer Service Management](https://servicenow-staging.fluidtopics.net/access?context=r_CustServMgmtAddtlPluginsTable&family=zurich&ft:locale=en-US).

 Sales and Order Management is a ServiceNow AI Platform feature that is available with the activation of the Lead to Cash Core plugin \(com.snd.l2c.core\). For details, see [Explore](https://servicenow-staging.fluidtopics.net/access?context=som-exploring&family=zurich&ft:locale=en-US).

 Starting in the Yokohama release, the following plugins are available on the ServiceNow Store for:

-   Install Base Management \(com.snc.install\_base\)
-   Install base characteristics \(com.snc.install\_base\_characteristics\)
-   Customer Service with Service Portfolio management \(com.snc.csm\_spm\)

For details, see [Configure Install base](https://servicenow-staging.fluidtopics.net/access?context=configure-install-base&family=zurich&ft:locale=en-US).

 Starting from the Yokohama release, the Business Location plugin \(com.snc.business\_location\) is available on the ServiceNow Store. For details, see [Activate business locations](https://servicenow-staging.fluidtopics.net/access?context=activate-business-location&family=zurich&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Data Management for CSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Data Management for CSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Starting with the Zurich release, data management for Customer Service Management doesn't support mobile devices and Internet Explorer. For more information, see [Browser support](https://servicenow-staging.fluidtopics.net/access?context=browser-support&family=zurich&ft:locale=en-US).

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Data Management for CSM, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

-   ****

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Data Management for CSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Data Management for CSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

 See [Data management](https://servicenow-staging.fluidtopics.net/access?context=csm-data-management&family=zurich&ft:locale=en-US) feature for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-washingtondc-zurich/rn-combined-intro.md)

