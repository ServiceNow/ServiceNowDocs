---
title: Combined External Content Connectors release notes for upgrades from Xanadu to Brazil
description: Consolidated page of all release notes for External Content Connectors from Xanadu to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-brazil/brazil-xanadu-externalcontentconnectors-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 16
breadcrumb: [Products combined by family]
---

# Combined External Content Connectors release notes for upgrades from Xanadu to Brazil

Consolidated page of all release notes for External Content Connectors from Xanadu to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family External Content Connectors release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading External Content Connectors to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for External Content Connectors.

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

-   **[Connector admin role](https://www.servicenow.com/docs/access?context=installed-with-ext-content-connectors&family=yokohama&ft:locale=en-US)**

Users with the sn\_ext\_conn.xcc\_admin role can create, configure, and review details for external content connectors and crawls.

-   **[Adobe Experience Manager as a Cloud Service external content connector](https://www.servicenow.com/docs/access?context=adobe-expmgr-cs-external-content-connector&family=yokohama&ft:locale=en-US)**

Retrieve searchable content and metadata from your Adobe Experience Manager as a Cloud Service source system.

-   **[Asana external content connector](https://www.servicenow.com/docs/access?context=asana-external-content-connector&family=yokohama&ft:locale=en-US)**

Retrieve searchable content and metadata from your Asana source system.

-   **[Docusign external content connector](https://www.servicenow.com/docs/access?context=docusign-external-content-connector&family=yokohama&ft:locale=en-US)**

Retrieve searchable content and metadata from your Docusign source system.

-   **[Dropbox external content connector](https://www.servicenow.com/docs/access?context=dropbox-external-content-connector&family=yokohama&ft:locale=en-US)**

Retrieve searchable content and metadata from your Dropbox source system.

-   **[GitHub Enterprise Cloud external content connector](https://www.servicenow.com/docs/access?context=github-enterprise-cloud-external-content-connector&family=yokohama&ft:locale=en-US)**

Retrieve searchable content and metadata from your GitHub Enterprise Cloud source system.

-   **[HubSpot external content connector](https://www.servicenow.com/docs/access?context=hubspot-external-content-connector&family=yokohama&ft:locale=en-US)**

Retrieve searchable content and metadata from your HubSpot source system.

-   **[Lucidchart external content connector](https://www.servicenow.com/docs/access?context=lucidchart-external-content-connector&family=yokohama&ft:locale=en-US)**

Retrieve searchable content and metadata from your Lucidchart source system.

-   **[Miro external content connector](https://www.servicenow.com/docs/access?context=miro-external-content-connector&family=yokohama&ft:locale=en-US)**

Retrieve searchable content and metadata from your Miro source system.

-   **[monday.com external content connector](https://www.servicenow.com/docs/access?context=monday-com-external-content-connector&family=yokohama&ft:locale=en-US)**

Retrieve searchable content and metadata from your monday.com source system.

-   **[Notion external content connector](https://www.servicenow.com/docs/access?context=notion-external-content-connector&family=yokohama&ft:locale=en-US)**

Retrieve searchable content and metadata from your Notion source system.

-   **[SAP DMS external content connector](https://www.servicenow.com/docs/access?context=sap-dms-external-content-connector&family=yokohama&ft:locale=en-US)**

Retrieve searchable content and metadata from your SAP DMS source system.

-   **[Smartsheet external content connector](https://www.servicenow.com/docs/access?context=smartsheet-external-content-connector&family=yokohama&ft:locale=en-US)**

Retrieve searchable content and metadata from your Smartsheet source system.

-   **[Trello external content connector](https://www.servicenow.com/docs/access?context=trello-external-content-connector&family=yokohama&ft:locale=en-US)**

Retrieve searchable content and metadata from your Trello source system.

-   **[WordPress external content connector](https://www.servicenow.com/docs/access?context=wordpress-external-content-connector&family=yokohama&ft:locale=en-US)**

Retrieve searchable content and metadata from your WordPress source system.

-   **[Workday external content connector](https://www.servicenow.com/docs/access?context=workday-external-content-connector&family=yokohama&ft:locale=en-US)**

Retrieve searchable content and metadata from your Workday source system.

-   **[Zoom external content connector](https://www.servicenow.com/docs/access?context=zoom-external-content-connector&family=yokohama&ft:locale=en-US)**

Retrieve searchable content and metadata from your Zoom source system.

-   **[Configure user mapping permission settings](https://www.servicenow.com/docs/access?context=configure-user-mapping-settings-external-content-connector&family=yokohama&ft:locale=en-US)**

Specify the source system and User \[sys\_user\] table fields to examine for matches when an external content connector maps source system users to your ServiceNow AI Platform users.

-   **[Statistics for content crawls](https://www.servicenow.com/docs/access?context=document-statistics-external-content-connectors&family=yokohama&ft:locale=en-US)**

Review statistics about the documents \(items or files with searchable content and metadata\) retrieved by a content crawl.

-   **[Statistics for user permission crawls](https://www.servicenow.com/docs/access?context=permission-statistics-external-content-connectors&family=yokohama&ft:locale=en-US)**

Review statistics about the permissions \(user and group-membership security principals\) retrieved by a user permission crawl.

-   **[Analytics](https://www.servicenow.com/docs/access?context=analytics-external-content-connectors&family=yokohama&ft:locale=en-US)**

Review metrics that show how your external content connector has run over time.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Connector admin role](https://www.servicenow.com/docs/access?context=installed-with-ext-content-connectors&family=zurich&ft:locale=en-US)**

Users with the sn\_ext\_conn.xcc\_admin role can create, configure, and review details for external content connectors and crawls.

-   **[Adobe Experience Manager as a Cloud Service external content connector](https://www.servicenow.com/docs/access?context=adobe-expmgr-cs-external-content-connector&family=zurich&ft:locale=en-US)**

Retrieve searchable content and metadata from your Adobe Experience Manager as a Cloud Service source system.

-   **[Asana external content connector](https://www.servicenow.com/docs/access?context=asana-external-content-connector&family=zurich&ft:locale=en-US)**

Retrieve searchable content and metadata from your Asana source system.

-   **[Docusign external content connector](https://www.servicenow.com/docs/access?context=docusign-external-content-connector&family=zurich&ft:locale=en-US)**

Retrieve searchable content and metadata from your Docusign source system.

-   **[Dropbox external content connector](https://www.servicenow.com/docs/access?context=dropbox-external-content-connector&family=zurich&ft:locale=en-US)**

Retrieve searchable content and metadata from your Dropbox source system.

-   **[GitHub Enterprise Cloud external content connector](https://www.servicenow.com/docs/access?context=github-enterprise-cloud-external-content-connector&family=zurich&ft:locale=en-US)**

Retrieve searchable content and metadata from your GitHub Enterprise Cloud source system.

-   **[HubSpot external content connector](https://www.servicenow.com/docs/access?context=hubspot-external-content-connector&family=zurich&ft:locale=en-US)**

Retrieve searchable content and metadata from your HubSpot source system.

-   **[Lucidchart external content connector](https://www.servicenow.com/docs/access?context=lucidchart-external-content-connector&family=zurich&ft:locale=en-US)**

Retrieve searchable content and metadata from your Lucidchart source system.

-   **[Miro external content connector](https://www.servicenow.com/docs/access?context=miro-external-content-connector&family=zurich&ft:locale=en-US)**

Retrieve searchable content and metadata from your Miro source system.

-   **[monday.com external content connector](https://www.servicenow.com/docs/access?context=monday-com-external-content-connector&family=zurich&ft:locale=en-US)**

Retrieve searchable content and metadata from your monday.com source system.

-   **[Notion external content connector](https://www.servicenow.com/docs/access?context=notion-external-content-connector&family=zurich&ft:locale=en-US)**

Retrieve searchable content and metadata from your Notion source system.

-   **[SAP DMS external content connector](https://www.servicenow.com/docs/access?context=sap-dms-external-content-connector&family=zurich&ft:locale=en-US)**

Retrieve searchable content and metadata from your SAP DMS source system.

-   **[Smartsheet external content connector](https://www.servicenow.com/docs/access?context=smartsheet-external-content-connector&family=zurich&ft:locale=en-US)**

Retrieve searchable content and metadata from your Smartsheet source system.

-   **[Trello external content connector](https://www.servicenow.com/docs/access?context=trello-external-content-connector&family=zurich&ft:locale=en-US)**

Retrieve searchable content and metadata from your Trello source system.

-   **[WordPress external content connector](https://www.servicenow.com/docs/access?context=wordpress-external-content-connector&family=zurich&ft:locale=en-US)**

Retrieve searchable content and metadata from your WordPress source system.

-   **[Workday external content connector](https://www.servicenow.com/docs/access?context=workday-external-content-connector&family=zurich&ft:locale=en-US)**

Retrieve searchable content and metadata from your Workday source system.

-   **[Zoom external content connector](https://www.servicenow.com/docs/access?context=zoom-external-content-connector&family=zurich&ft:locale=en-US)**

Retrieve searchable content and metadata from your Zoom source system.

-   **[Configure user mapping permission settings](https://www.servicenow.com/docs/access?context=configure-user-mapping-settings-external-content-connector&family=zurich&ft:locale=en-US)**

Specify the source system and User \[sys\_user\] table fields to examine for matches when an external content connector maps source system users to your ServiceNow AI Platform users.

-   **[Statistics for content crawls](https://www.servicenow.com/docs/access?context=document-statistics-external-content-connectors&family=zurich&ft:locale=en-US)**

Review statistics about the documents \(items or files with searchable content and metadata\) retrieved by a content crawl.

-   **[Statistics for user permission crawls](https://www.servicenow.com/docs/access?context=permission-statistics-external-content-connectors&family=zurich&ft:locale=en-US)**

Review statistics about the permissions \(user and group-membership security principals\) retrieved by a user permission crawl.

-   **[Analytics](https://www.servicenow.com/docs/access?context=analytics-external-content-connectors&family=zurich&ft:locale=en-US)**

Review metrics that show how your external content connector has run over time.


</td></tr><tr><td>

Australia

</td><td>

-   **[Adobe Acrobat Sign external content connector](https://www.servicenow.com/docs/access?context=adobe-acrobat-sign-external-content-connector&family=australia&ft:locale=en-US)**

Retrieve searchable content and metadata from your Adobe Acrobat Sign source system.

-   **[Aha! Roadmaps external content connector](https://www.servicenow.com/docs/access?context=aha-roadmaps-external-content-connector&family=australia&ft:locale=en-US)**

Retrieve searchable content and metadata from your Aha! Roadmaps source system.

-   **[Cornerstone external content connector](https://www.servicenow.com/docs/access?context=cornerstone-external-content-connector&family=australia&ft:locale=en-US)**

Retrieve searchable content and metadata from your Cornerstone source system.

-   **[Fluid Topics external content connector](https://www.servicenow.com/docs/access?context=fluid-topics-external-content-connector&family=australia&ft:locale=en-US)**

Retrieve searchable content and metadata from your Fluid Topics source system.

-   **[ManageEngine external content connector](https://www.servicenow.com/docs/access?context=manageengine-external-content-connector&family=australia&ft:locale=en-US)**

Retrieve searchable content and metadata from your ManageEngine source system.

-   **[Workvivo external content connector](https://www.servicenow.com/docs/access?context=workvivo-external-content-connector&family=australia&ft:locale=en-US)**

Retrieve searchable content and metadata from your Workvivo source system.


</td></tr><tr><td>

Brazil

</td><td>

-   **[Connector health dashboard](https://www.servicenow.com/docs/access?context=resolve-health-issues-external-content-connector&family=brazil&ft:locale=en-US)**

View and resolve connector health issues using the connector health dashboard.

-   **[Index inspector tool](https://www.servicenow.com/docs/access?context=review-indexing-status-content-items&family=brazil&ft:locale=en-US)**

Verify indexing status and error counts for individual content items using the index inspector tool. Optionally review additional item details, see which users and groups can view the item in secure search, and view retrieval and indexing errors for the item.

-   **[Advanced connection settings for the Amazon S3 external content connector](https://www.servicenow.com/docs/access?context=create-ext-cont-connector-amazon-s3&family=brazil&ft:locale=en-US)**

Optionally specify advanced connection settings including the AWS region and Amazon S3 endpoint you want the connector to use. You can also specify a list of Amazon S3 buckets to retrieve content from, or leave this list empty to enable auto-discovery of buckets.

-   **[Delta content crawls for the Google Drive connector](https://www.servicenow.com/docs/access?context=delta-content-crawls-external-content-connectors&family=brazil&ft:locale=en-US)**

Reduce content crawl time with delta content crawls. Unlike full content crawls, delta content crawls ignore unchanged content items in a connector's source system. Delta content crawls are supported for the Google Drive external content connector.


</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing External Content Connectors features.

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

The connector creation UI now includes optional steps for configuring user permission crawls \(for connectors that support them\) and for linking connector search sources to your search profiles. If you want to change these settings for an existing connector, you can configure these settings from the connector editor.


 -   **[Analytics](https://www.servicenow.com/docs/access?context=analytics-external-content-connectors&family=zurich&ft:locale=en-US)**

Analyze connector performance and behavior in a selected time period using the redesigned Analytics page. You can access this page from the connector editor.

-   **[Atlassian Jira Cloud connection settings](https://www.servicenow.com/docs/access?context=create-ext-cont-connector-jira&family=zurich&ft:locale=en-US)**

The Atlassian Jira Cloud external content connector no longer requires your Atlassian Jira Cloud instance ID as a connection setting.

-   **[Microsoft OneDrive connection settings](https://www.servicenow.com/docs/access?context=create-ext-cont-connector-microsoft-onedrive&family=zurich&ft:locale=en-US)**

The Microsoft OneDrive external content connector now accepts certificate SHA1 thumbprint hashes in hexadecimal format as well as in base64-encoded format.

-   **[Microsoft SharePoint Online connection settings](https://www.servicenow.com/docs/access?context=create-ext-cont-connector-mspo&family=zurich&ft:locale=en-US)**

The Microsoft SharePoint Online external content connector now accepts certificate SHA1 thumbprint hashes in hexadecimal format as well as in base64-encoded format.

-   **[Microsoft Teams connection settings](https://www.servicenow.com/docs/access?context=create-ext-cont-connector-msteams&family=zurich&ft:locale=en-US)**

The Microsoft Teams external content connector now accepts certificate SHA1 thumbprint hashes in hexadecimal format as well as in base64-encoded format.


</td></tr><tr><td>

Australia

</td><td>

-   **[Sitemap support in the Webcrawler external content connector](https://www.servicenow.com/docs/access?context=webcrawler-external-content-connector&family=australia&ft:locale=en-US)**

Retrieve content and links from URLs found in sitemaps defined for your web source system when running content crawls for the Webcrawler external content connector. A content crawl only retrieves sitemap URLs that include the crawl's starting point URL.

-   **[Start point links for scheduled partial content crawls](https://www.servicenow.com/docs/access?context=create-content-crawl-external-content-connector&family=australia&ft:locale=en-US)**

View the start point for a scheduled partial content crawl via a link in its entry in the the external content connector's list of crawls.

-   **[Start point links in partial content crawl history entries](https://www.servicenow.com/docs/access?context=review-crawl-ext-cont-connector&family=australia&ft:locale=en-US)**

View the start point for a scheduled partial content crawl via a link in its crawl history entries.

-   **[Limited Role-Based Access Control \(RBAC\) support in the Atlassian](https://www.servicenow.com/docs/access?context=atlassian-confluence-cloud-external-content-connector&family=australia&ft:locale=en-US) Confluence Cloud external content connector**

Map source system user and group permissions assigned via RBAC roles to users in your ServiceNow AI Platform instance.


</td></tr><tr><td>

Brazil

</td><td>

-   **Crawl schedules tab renamed**

In the external content connector editor, the **Crawl schedules** tab has been renamed to **Manage crawls**.


</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some External Content Connectors features or functionality were removed.

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

Between your current release family and Brazil, some External Content Connectors features or functionality were deprecated.

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


</td></tr><tr><td>

Brazil

</td><td>

-   **Activation information**

Install External Content Connectors by requesting the External Content Connectors Application Suite plugin from the ServiceNow Store. If you want to activate the ServiceNow product documentation external content connector or the Webcrawler external content connector, you must request activation of those plugins after the Application Suite is activated.

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=brazil&ft:locale=en-US).


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


</td></tr><tr><td>

Brazil

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


</td></tr><tr><td>

Brazil

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

</td></tr><tr><td>

Brazil

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

</td></tr><tr><td>

Brazil

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

</td></tr><tr><td>

Brazil

</td><td>

-   Make content and metadata from your external document repositories searchable in AI Search applications.
-   Map your source system users to their ServiceNow AI Platform user accounts to preserve their access permissions for crawled content.
-   Schedule content and user permission crawls or run them manually as needed.

 See [External Content Connectors](https://www.servicenow.com/docs/access?context=ext-cont-connectors-landing-page&family=brazil&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-xanadu-brazil/rn-combined-intro.md)

