---
title: Combined External Content Connectors release notes for upgrades from Xanadu to Australia
description: Consolidated page of all release notes for External Content Connectors from Xanadu to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-australia/australia-xanadu-externalcontentconnectors-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 11
breadcrumb: [Products combined by family]
---

# Combined External Content Connectors release notes for upgrades from Xanadu to Australia

Consolidated page of all release notes for External Content Connectors from Xanadu to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family External Content Connectors release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading External Content Connectors to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Beginning with version 2 of the External Content Connectors application, external content connectors implement semantic vector indexing for crawled items. When you upgrade to a version that supports semantic vector indexing, your existing connectors will reindex all previously retrieved items the next time they're visited by a crawl, even if those items' content is unchanged. To force semantic vector indexing of your external content items as soon as possible after upgrading, cancel any running crawls, then restart the canceled crawls manually.

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

Between your current release family and Australia, new features were introduced for External Content Connectors.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Atlassian Jira Cloud external content connector](https://www.servicenow.com/docs/access?context=create-ext-cont-connector-jira&family=xanadu&ft:locale=en-US)**

Retrieve searchable content and user permissions from projects in your Atlassian Jira Cloud source system.

-   **[Google Drive external content connector](https://www.servicenow.com/docs/access?context=create-ext-cont-connector-gdrive&family=xanadu&ft:locale=en-US)**

Retrieve searchable content and user permissions from shared drives in your Google Drive source system.

-   **[Microsoft Teams external content connector](https://www.servicenow.com/docs/access?context=create-ext-cont-connector-msteams&family=xanadu&ft:locale=en-US)**

Retrieve searchable content and user permissions from teams in your Microsoft Teams source system.

-   **[Predefined web sources external content connector](https://www.servicenow.com/docs/access?context=create-ext-cont-connector-websources&family=xanadu&ft:locale=en-US)**

Retrieve searchable content from pages and subdomains in predefined public web sites.

-   **[ServiceNow product documentation external content connectors](https://www.servicenow.com/docs/access?context=create-ext-cont-connector-snowdoc&family=xanadu&ft:locale=en-US)**

Retrieve searchable content from the ServiceNow product documentation site.

-   **[Slack external content connector](https://www.servicenow.com/docs/access?context=create-ext-cont-connector-slack&family=xanadu&ft:locale=en-US)**

Retrieve searchable content and user permissions from public channels in your Slack source system.

-   **[Warning messages for indexed document counts](https://www.servicenow.com/docs/access?context=exploring-ext-cont-connectors&family=xanadu&ft:locale=en-US)**

When an external content connector's indexed document count exceeds 800,000, a warning message appears in the connector's UI to indicate that it's approaching the indexing limit of 1,000,000 documents.

-   **[Add external content search results to Now Assist in Virtual Agent conversations](https://www.servicenow.com/docs/access?context=add-ext-cont-srch-src-na-va&family=xanadu&ft:locale=en-US)**

Expand the range of information available to Virtual Agent users by adding external content search results to Now Assist in Virtual Agent conversations.


-   **[Semantic vector indexing for crawled content](https://www.servicenow.com/docs/access?context=semantic-search-ais&family=xanadu&ft:locale=en-US)**

Improve recall for external content searches with support for semantic vector indexing of crawled content. Semantic vector indexing is supported for all external content connectors.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Semantic vector indexing for crawled content](https://www.servicenow.com/docs/access?context=semantic-search-ais&family=yokohama&ft:locale=en-US)**

Improve recall for external content searches with support for semantic vector indexing of crawled content. Semantic vector indexing is supported for all external content connectors.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Amazon S3 external content connector](https://www.servicenow.com/docs/access?context=amazon-s3-external-content-connector&family=zurich&ft:locale=en-US)**

Retrieve searchable content and metadata from buckets in your Amazon S3 source system.

-   **[Box external content connector](https://www.servicenow.com/docs/access?context=box-external-content-connector&family=zurich&ft:locale=en-US)**

Retrieve searchable content and metadata from user boxes in your Box source system.

-   **[GitLab external content connector](https://www.servicenow.com/docs/access?context=gitlab-external-content-connector&family=zurich&ft:locale=en-US)**

Retrieve searchable content and metadata from issues, wikis, merge requests, tags, branches, and commits in your GitLab source system's groups, projects, and repositories.

-   **[Microsoft OneDrive external content connector](https://www.servicenow.com/docs/access?context=microsoft-onedrive-external-content-connector&family=zurich&ft:locale=en-US)**

Retrieve searchable content and metadata from individual drives in your Microsoft OneDrive source system.

-   **[Microsoft Viva Engage external content connector](https://www.servicenow.com/docs/access?context=microsoft-viva-engage-external-content-connector&family=zurich&ft:locale=en-US)**

Retrieve searchable content and metadata from conversations in your Microsoft Viva Engage source system's communities.

-   **[ServiceNow instance external content connector](https://www.servicenow.com/docs/access?context=servicenow-instance-external-content-connector&family=zurich&ft:locale=en-US)**

Retrieve searchable content and metadata from KB articles in your ServiceNow AI Platform instance.

-   **[Webcrawler external content connector](https://www.servicenow.com/docs/access?context=webcrawler-external-content-connector&family=zurich&ft:locale=en-US)**

Retrieve searchable content and metadata from pages and subdomains in public web sources. Select a predefined web source or specify a custom web source.

-   **[Zendesk Guide external content connector](https://www.servicenow.com/docs/access?context=zendesk-guide-external-content-connector&family=zurich&ft:locale=en-US)**

Retrieve searchable content and metadata from articles in your Zendesk Guide source system's knowledge bases.

-   **[Statistics for content crawls](https://www.servicenow.com/docs/access?context=document-statistics-external-content-connectors&family=zurich&ft:locale=en-US)**

Review statistics for searchable items retrieved by a content crawl.

-   **[Statistics for user permission crawls](https://www.servicenow.com/docs/access?context=permission-statistics-external-content-connectors&family=zurich&ft:locale=en-US)**

Review statistics for user and group permissions retrieved by a user permission crawl.


</td></tr><tr><td>

Australia

</td><td>

-   **[SAP SuccessFactors external content connector](https://www.servicenow.com/docs/access?context=sap-successfactors-external-content-connector&family=australia&ft:locale=en-US)**

Retrieve searchable content and metadata exported from your SAP SuccessFactors Learning source system.

-   **[Configuring crawl settings for external content connectors](https://www.servicenow.com/docs/access?context=cfg-crawl-settings-ext-cont-connector&family=australia&ft:locale=en-US)**

Activate multimodal captioning for attachments and files retrieved by your external content connector's content crawls. The multimodal service automatically generates captions for images, tables, charts, and complex layouts in the retrieved attachments and files. Searches can match attachment and file results using keywords from the generated captions.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing External Content Connectors features.

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

-   **[Connector creation UI](https://www.servicenow.com/docs/access?context=creating-ext-cont-connectors&family=yokohama&ft:locale=en-US)**

The connector creation UI now includes optional steps for configuring user permission crawls \(for connectors that support them\) and for linking connector search sources to your search profiles. If you want to change these settings for an existing connector, you can configure these settings from the connector editor.


 -   **[Analytics](https://www.servicenow.com/docs/access?context=analytics-external-content-connectors&family=yokohama&ft:locale=en-US)**

Analyze connector performance and behavior in a selected time period using the redesigned Analytics page. You can access this page from the connector editor.

-   **[Atlassian Jira Cloud connection settings](https://www.servicenow.com/docs/access?context=create-ext-cont-connector-jira&family=yokohama&ft:locale=en-US)**

The Atlassian Jira Cloud external content connector no longer requires your Atlassian Jira Cloud instance ID as a connection setting.

-   **[Microsoft OneDrive connection settings](https://www.servicenow.com/docs/access?context=create-ext-cont-connector-microsoft-onedrive&family=yokohama&ft:locale=en-US)**

The Microsoft OneDrive external content connector now accepts certificate SHA1 thumbprint hashes in hexadecimal format as well as in base64-encoded format.

-   **[Microsoft SharePoint Online connection settings](https://www.servicenow.com/docs/access?context=create-ext-cont-connector-mspo&family=yokohama&ft:locale=en-US)**

The Microsoft SharePoint Online external content connector now accepts certificate SHA1 thumbprint hashes in hexadecimal format as well as in base64-encoded format.

-   **[Microsoft Teams connection settings](https://www.servicenow.com/docs/access?context=create-ext-cont-connector-msteams&family=yokohama&ft:locale=en-US)**

The Microsoft Teams external content connector now accepts certificate SHA1 thumbprint hashes in hexadecimal format as well as in base64-encoded format.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Connector creation UI](https://www.servicenow.com/docs/access?context=creating-ext-cont-connectors&family=zurich&ft:locale=en-US)**

The connector creation UI now includes optional steps for configuring the new connector's crawl settings and creating and scheduling crawls for it. You can still configure these settings from the connector's editor, so you can skip these steps during connector creation if you want to configure crawl settings and create crawls later on.


 -   **[Webcrawler external content connector](https://www.servicenow.com/docs/access?context=webcrawler-external-content-connector&family=zurich&ft:locale=en-US)**

The predefined web sources external content connector has been subsumed into the new Webcrawler external content connector, which enables you to specify a custom web source or select a predefined one.


</td></tr><tr><td>

Australia

</td><td>

-   **[ServiceNow instance external content connector](https://www.servicenow.com/docs/access?context=servicenow-instance-external-content-connector&family=australia&ft:locale=en-US)**

You can now create and run multiple ServiceNow instance connectors on a single ServiceNow AI Platform instance.

-   **[Webcrawler external content connector](https://www.servicenow.com/docs/access?context=webcrawler-external-content-connector&family=australia&ft:locale=en-US)**

Connector admins can now schedule crawls on a daily, weekly, or monthly basis for all Webcrawler external content connectors.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some External Content Connectors features or functionality were removed.

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

Between your current release family and Australia, some External Content Connectors features or functionality were deprecated.

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

Review information on how to activate External Content Connectors.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Install External Content Connectors by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

-   **Activation information**

Install External Content Connectors by requesting the External Content Connectors Application Suite plugin from the ServiceNow Store. If you want to activate the ServiceNow product documentation external content connector or the Webcrawler external content connector, you must request activation of those plugins after the Application Suite is activated.

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).


</td></tr><tr><td>

Zurich

</td><td>

-   **Activation information**

Install External Content Connectors by requesting the External Content Connectors Application Suite plugin from the ServiceNow Store. If you want to activate the ServiceNow product documentation external content connector or the Webcrawler external content connector, you must request activation of those plugins after the Application Suite is activated.

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).


</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

Install External Content Connectors by requesting the External Content Connectors Application Suite plugin from the ServiceNow Store. If you want to activate the ServiceNow product documentation external content connector or the Webcrawler external content connector, you must request activation of those plugins after the Application Suite is activated.

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for External Content Connectors we have noted them here.

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

-   **Additional requirements**

Your instance needs inbound mTLS support to run external content connector crawls. If inbound mTLS support isn't already activated for your instance, it should be automatically activated after you install the External Content Connectors Application Suite plugin.


</td></tr><tr><td>

Zurich

</td><td>

-   **Additional requirements**

Your instance needs inbound mTLS support to run external content connector crawls. If inbound mTLS support isn't already activated for your instance, it should be automatically activated after you install the External Content Connectors Application Suite plugin.


</td></tr><tr><td>

Australia

</td><td>

-   **Additional requirements**

Your instance needs inbound mTLS support to run external content connector crawls. If inbound mTLS support isn't already activated for your instance, it should be automatically activated after you install the External Content Connectors Application Suite plugin.


</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for External Content Connectors we have noted them here.

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

-   **Browser requirements**

For optimal performance, use External Content Connectors in the latest release of Google Chrome or Mozilla Firefox. Internet Explorer isn't supported.


</td></tr><tr><td>

Zurich

</td><td>

-   **Browser requirements**

For optimal performance, use External Content Connectors in the latest release of Google Chrome or Mozilla Firefox. Internet Explorer isn't supported.


</td></tr><tr><td>

Australia

</td><td>

-   **Browser requirements**

For optimal performance, use External Content Connectors in the latest release of Google Chrome or Mozilla Firefox. Internet Explorer isn't supported.


</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for External Content Connectors, such as specific requirements or compliance levels.

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
</table>## Localization information

If there are specific localization considerations for External Content Connectors we have noted them here.

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

If there are specific highlight considerations for External Content Connectors we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Expand your search by indexing searchable content and user permissions from your Atlassian Jira Cloud, Google Drive, Microsoft Teams, and Slack source systems.
-   Make web content locally searchable by indexing pages from predefined public web sites or from the ServiceNow product documentation site.
-   Know when your external content connectors are approaching their crawl limits with new warning messages.
-   Expand the range of information available to Virtual Agent users by adding external content search results to Now Assist in Virtual Agent conversations.
-   Improve recall for external content searches with support for semantic vector indexing of crawled content.

 See [External Content Connectors](https://www.servicenow.com/docs/access?context=ext-cont-connectors-landing-page&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Make content and metadata from your external document repositories searchable in AI Search applications.
-   Map your source system users to their ServiceNow AI Platform user accounts to preserve their access permissions for crawled content.
-   Schedule content and user permission crawls or run them manually as needed.

 See [External Content Connectors](https://www.servicenow.com/docs/access?context=ext-cont-connectors-landing-page&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Make content and metadata from your external document repositories searchable in AI Search applications.
-   Map your source system users to their ServiceNow AI Platform user accounts to preserve their access permissions for crawled content.
-   Schedule content and user permission crawls or run them manually as needed.

 See [External Content Connectors](https://www.servicenow.com/docs/access?context=ext-cont-connectors-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Make content and metadata from your external document repositories searchable in AI Search applications.
-   Map your source system users to their ServiceNow AI Platform user accounts to preserve their access permissions for crawled content.
-   Schedule content and user permission crawls or run them manually as needed.

 See [External Content Connectors](https://www.servicenow.com/docs/access?context=ext-cont-connectors-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-xanadu-australia/rn-combined-intro.md)

