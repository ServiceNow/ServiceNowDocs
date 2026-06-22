---
title: Combined Financial Services Operations Core release notes for upgrades from Xanadu to Australia
description: Consolidated page of all release notes for Financial Services Operations Core from Xanadu to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-australia/australia-xanadu-financialservicesoperationscore-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 5
breadcrumb: [Products combined by family]
---

# Combined Financial Services Operations Core release notes for upgrades from Xanadu to Australia

Consolidated page of all release notes for Financial Services Operations Core from Xanadu to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Financial Services Operations Core release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Financial Services Operations Core to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Financial Services Operations Core.

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

-   **[Payment card application](https://www.servicenow.com/docs/access?context=payment-card-application&family=zurich&ft:locale=en-US)**

Store the details of physical payment cards across the entire card life cycle, from issuance to servicing. You can also store tokenized values for sensitive data, such as the primary account number \(PAN\).

-   **[Deny-Unless ACL](https://www.servicenow.com/docs/access?context=acl-denial-behavior&family=zurich&ft:locale=en-US)**

Use Deny-Unless access control lists \(ACLs\) on FSO tables for non-authenticated users, such as users with public roles. With this minimum-security setting, only your authenticated users can read, write, delete, or create actions on these tables. For more information about the Deny-Unless ACLs, see the [Deny-Unless ACL](https://www.servicenow.com/docs/access?context=acl-denial-behavior&family=zurich&ft:locale=en-US) topic in the ServiceNow® Platform Security documentation.


</td></tr><tr><td>

Australia

</td><td>

-   The FSO tables `sn_bom_m2m_service_definition_user_criteria` and `sn_bom_m2m_service_definition_customer_condition` are deprecated. If you're on an upgraded instance, you can continue to reference these tables, but they're no longer maintained. Use `sn_csm_case_types_service_user_criteria` and `sn_csm_case_types_service_customer_criteria` instead. For more information, see [Banking tables](https://www.servicenow.com/docs/access?context=fso-core-banking-tables&family=australia&ft:locale=en-US).
-   The **Show in Interceptor** field \(`show_in_interceptor`\) on the `sn_bom_service_definition` table is deprecated. Use agent criteria in the `sn_csm_case_types_service_user_criteria` table to control which service definitions appear in the case type selector.

User criteria mappings control the visibility of new service definitions. To hide a service definition, map it to the **No User** user criteria. To make it visible, map it to the **Users with sn\_bom.service\_definition\_read** user criteria. Both user criteria records are predefined in Financial Services Operations Core.

For more information, see [Components installed with case types](https://www.servicenow.com/docs/access?context=service-definitions-components&family=australia&ft:locale=en-US).


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Financial Services Operations Core features.

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

-   **[Added fields to Claim Base table](https://www.servicenow.com/docs/access?context=fso-core-insurance-tables&family=yokohama&ft:locale=en-US)**

Added the following fields to the Claim Base \[sn\_bom\_claim\_base\] table:

    -   SIU review
    -   Claim validation decision
    -   Claim fraud decision

</td></tr><tr><td>

Zurich

</td><td>

-   **[Added field to Financial transaction table](https://www.servicenow.com/docs/access?context=fso-core-banking-tables&family=zurich&ft:locale=en-US)**

Added the **Payment Card** field to the Financial transaction \[sn\_bom\_transaction\] table as part of the Payment card application.


</td></tr><tr><td>

Australia

</td><td>

-   **[Case type selector](https://www.servicenow.com/docs/access?context=csm-case-type-select-modals&family=australia&ft:locale=en-US)**

Filter service definitions using the case type selector in FSO with the predefined CSM implementation. For upgraded instances, existing agent criteria and customer condition data is automatically migrated from the deprecated FSO tables to the CSM tables during upgrade. No manual migration is required.

To configure agent criteria or customer conditions for the case type selector, use the following CSM tables:

    -   `sn_csm_case_types_service_user_criteria`: for agent criteria
    -   `sn_csm_case_types_service_customer_criteria`: for customer conditions

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Financial Services Operations Core features or functionality were removed.

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

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Financial Services Operations Core features or functionality were deprecated.

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

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Financial Services Operations Core.

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

Install Financial Services Operations Core by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Install Financial Services Operations Core by requesting it from the ServiceNow Store. 

</td></tr><tr><td>

Australia

</td><td>

Install Financial Services Operations Core by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Financial Services Operations Core we have noted them here.

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

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Financial Services Operations Core we have noted them here.

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

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Financial Services Operations Core, such as specific requirements or compliance levels.

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

-   ****

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Financial Services Operations Core we have noted them here.

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

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Financial Services Operations Core we have noted them here.

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

The Claim Base \[sn\_bom\_claim\_base\] table has been updated in this release with additional fields. These fields were previously available only to specific applications. They're available in the Claim Base table and can be used across all other claim applications in this release.

 See [Financial Services Operations Core](https://www.servicenow.com/docs/access?context=financial-services-operations-core-data-model&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Leverage a payment card data model application in FSO workflows, such as disputes, which can be used across an entire card life cycle, from issuance to servicing.
-   Support multiple payment card types, including credit and debit cards.

 See [Payment Card](https://www.servicenow.com/docs/access?context=payment-card-application&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

The case type selector in Financial Services Operations now uses the predefined Customer Service Management \(CSM\) implementation, replacing the previous FSO-specific override.

 See [Case type selector](https://www.servicenow.com/docs/access?context=csm-case-type-select-modals&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-xanadu-australia/rn-combined-intro.md)

