---
title: Combined Data Management for CSM release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for Data Management for CSM from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-datamanagementforcsm-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 7
breadcrumb: [Products combined by family]
---

# Combined Data Management for CSM release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for Data Management for CSM from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Data Management for CSM release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Data Management for CSM to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

Zurich

</td><td>

-   **[Create return merchandise authorization case lines](https://www.servicenow.com/docs/access?context=som.create-return-merchandise-authorization-case-lines&family=zurich&ft:locale=en-US)**

Enable agents to initiate return requests directly from sold product records along with the install base items. Return cases automatically map order and product details to the case, giving users an end-to-end visibility into their returns and reducing processing time.

-   **[Synchronizing life-cycle values](https://www.servicenow.com/docs/access?context=cmdb-asset-CI-IBI-sync-options&family=zurich&ft:locale=en-US)**

Configure a model category as a product instance to enable the system to synchronize the life cycle values between asset and install base item using the life cycle stage and life cycle state status values.

-   **[Proactive Customer Service Operations](https://www.servicenow.com/docs/access?context=proactive-service-operations&family=zurich&ft:locale=en-US)**

Event management operators now have a dedicated customer service management role for access control when setting up new installations. The access to customer data for event management operators is granted through a limited scoped role \( sn\_pro\_cs\_ops.csm\_evt\_mgmt\_stakeholder\) instead of the global platform role \(evt\_mgmt\_operator role\).


</td></tr><tr><td>

Australia

</td><td>

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


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Data Management for CSM features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Entity configuration and mapping](https://www.servicenow.com/docs/access?context=entity-configuration-and-mapping&family=zurich&ft:locale=en-US)**

Gain precision in sales entity setup with three new columns in the Lead to Cash Entity Definition table: Filter Conditions, Enable Post Processing, and Post Processing Script. These columns enable targeted data filtering and post-processing logic execution.

-   **[Associate products and services](https://www.servicenow.com/docs/access?context=products-services-at-bus-loc&family=zurich&ft:locale=en-US)Support for service-related capabilities in business locations**

Enable service-related capabilities for business locations by activating the optional Customer Service Case Types \(sn\_csm\_case\_types\) plugin.


</td></tr><tr><td>

Australia

</td><td>

-   **[Renamed entities](https://www.servicenow.com/docs/access?context=renamed-entities&family=australia&ft:locale=en-US)**

Renamed Service Model Foundation entities to improve clarity and maintain consistency across the platform. Review your existing configurations, scripts, or integrations that reference these entities and update them accordingly.

**Note:** The entity name changes are available in the Business Location 5.2.0 store app.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Data Management for CSM features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Data Management for CSM.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Data Management for CSM we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

Zurich

</td><td>

-   **Browser requirements**

Starting with the Zurich release, data management for Customer Service Management doesn't support mobile devices and Internet Explorer. For more information, see [Browser support](https://www.servicenow.com/docs/access?context=browser-support&family=zurich&ft:locale=en-US).


</td></tr><tr><td>

Australia

</td><td>

-   **Browser requirements**

Starting with the Australia release, data management for Customer Service Management doesn't support mobile devices and Internet Explorer. For more information, see [Browser support](https://www.servicenow.com/docs/access?context=browser-support&family=australia&ft:locale=en-US).


</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Data Management for CSM, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **Accessibility information**
    -   **Dark theme**

The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


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
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)

