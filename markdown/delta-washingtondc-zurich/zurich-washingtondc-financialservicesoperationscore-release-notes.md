---
title: Combined Financial Services Operations Core release notes for upgrades from Washington DC to Zurich
description: Consolidated page of all release notes for Financial Services Operations Core from Washington DC to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-washingtondc-zurich/zurich-washingtondc-financialservicesoperationscore-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 6
breadcrumb: [Products combined by family]
---

# Combined Financial Services Operations Core release notes for upgrades from Washington DC to Zurich

Consolidated page of all release notes for Financial Services Operations Core from Washington DC to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Financial Services Operations Core release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Financial Services Operations Core to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

During the upgrade to Washington DC, the Financial Services Operations Core plugin reparents the following tables:

**Note:** You may experience a longer time for the upgrade to complete if your upgraded instance has a large number of records.

-   The Service Definition \[sn\_bom\_service\_definition\] table extends from the Service Definition \[sn\_case\_type\_selection\] table instead of the Request Definition \[sn\_ind\_request\_definition.
-   The Financial task \[sn\_bom\_task\] table extends from the Customer Service Task \[sn\_customerservice\_task\] table instead of the Global Task \[task\] table.
-   The Policy Participant \[sn\_bom\_policy\_participant\] table extends from the Sold Product Related Party \[sn\_install\_base\_sold\_product\_related\_party\] table.

Reparenting enables leveraging of the benefits and advancements introduced by ServiceNow® Customer Service Management \(CSM\) while preserving the functionality of existing applications.

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

Between your current release family and Zurich, new features were introduced for Financial Services Operations Core.

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

-   **[Payment card application](https://servicenow-staging.fluidtopics.net/access?context=payment-card-application&family=zurich&ft:locale=en-US)**

Store the details of physical payment cards across the entire card life cycle, from issuance to servicing. You can also store tokenized values for sensitive data, such as the primary account number \(PAN\).

-   **[Deny-Unless ACL](https://servicenow-staging.fluidtopics.net/access?context=acl-denial-behavior&family=zurich&ft:locale=en-US)**

Use Deny-Unless access control lists \(ACLs\) on FSO tables for non-authenticated users, such as users with public roles. With this minimum-security setting, only your authenticated users can read, write, delete, or create actions on these tables. For more information about the Deny-Unless ACLs, see the [Deny-Unless ACL](https://servicenow-staging.fluidtopics.net/access?context=acl-denial-behavior&family=zurich&ft:locale=en-US) topic in the ServiceNow® Platform Security documentation.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Financial Services Operations Core features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Case creation enhancements](https://servicenow-staging.fluidtopics.net/access?context=configure-service-definitions&family=washingtondc&ft:locale=en-US)**

The FSO interceptor is replaced with the Customer Service Management Product Service select version of the case type selector. This enhancement enables customer service agents to easily create new case records by selecting the appropriate case type from a list of available services. For details, see the [Service type selector for Financial Services Operations](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1638995) article in the Now Support knowledge base.


</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Added fields to Claim Base table](https://servicenow-staging.fluidtopics.net/access?context=fso-core-insurance-tables&family=yokohama&ft:locale=en-US)**

Added the following fields to the Claim Base \[sn\_bom\_claim\_base\] table:

    -   SIU review
    -   Claim validation decision
    -   Claim fraud decision

</td></tr><tr><td>

Zurich

</td><td>

-   **[Added field to Financial transaction table](https://servicenow-staging.fluidtopics.net/access?context=fso-core-banking-tables&family=zurich&ft:locale=en-US)**

Added the **Payment Card** field to the Financial transaction \[sn\_bom\_transaction\] table as part of the Payment card application.


</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Financial Services Operations Core features or functionality were removed.

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

Between your current release family and Zurich, some Financial Services Operations Core features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

As part of the Customer Service Management \(CSM\) service definition uptake initiative, the FSO service definition category table is now deprecated and no longer supported or available for new activation. Instead, the FSO service definitions category data has been migrated to CSM's service category and service category relation tables. For more information, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base and the[Service type selector for Financial Services Operations](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1638995) article.

 Starting with the Washington DC release, the following requestor roles and the related UI actions are now deprecated and no longer supported or available for new activation.

-   sn\_bom\_loan.b2c\_requestor
-   sn\_bom\_credit\_card.requestor
-   sn\_bom\_deposit\_b2b.requestor
-   sn\_bom\_loan\_b2b.requestor
-   sn\_bom\_compl.requestor
-   sn\_ins\_policy\_b2c.requestor
-   sn\_bom\_payment.requestor
-   sn\_bom\_deposit\_b2c.requestor
-   sn\_ins\_policy\_b2b.requestor
-   sn\_bom.fs\_requestor
-   sn\_bom.b2c\_requestor
-   sn\_bom.b2b\_requestor
-   sn\_bom.requestor

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
</table>## Activation information

Review information on how to activate Financial Services Operations Core.

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

Install Financial Services Operations Core by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Install Financial Services Operations Core by requesting it from the ServiceNow Store. 

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Financial Services Operations Core we have noted them here.

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

If any specific browser requirements were introduced or changed for Financial Services Operations Core we have noted them here.

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
</table>## Accessibility information

Review details on accessibility information for Financial Services Operations Core, such as specific requirements or compliance levels.

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

If there are specific localization considerations for Financial Services Operations Core we have noted them here.

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

If there are specific highlight considerations for Financial Services Operations Core we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   Utilize the updated data model with reparented tables to enhance data alignment.
-   Seamlessly transfer and update data to newer product model tables using efficient fix scripts.

 See [Financial Services Operations Core](https://servicenow-staging.fluidtopics.net/access?context=financial-services-ops-data-model&family=washingtondc&ft:locale=en-US) for more information.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

The Claim Base \[sn\_bom\_claim\_base\] table has been updated in this release with additional fields. These fields were previously available only to specific applications. They're available in the Claim Base table and can be used across all other claim applications in this release.

 See [Financial Services Operations Core](https://servicenow-staging.fluidtopics.net/access?context=financial-services-operations-core-data-model&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Leverage a payment card data model application in FSO workflows, such as disputes, which can be used across an entire card life cycle, from issuance to servicing.
-   Support multiple payment card types, including credit and debit cards.

 See [Payment Card](https://servicenow-staging.fluidtopics.net/access?context=payment-card-application&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-washingtondc-zurich/rn-combined-intro.md)

