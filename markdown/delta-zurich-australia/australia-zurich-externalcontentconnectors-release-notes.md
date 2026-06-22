---
title: Combined External Content Connectors release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for External Content Connectors from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-externalcontentconnectors-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 12
breadcrumb: [Products combined by family]
---

# Combined External Content Connectors release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for External Content Connectors from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family External Content Connectors release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading External Content Connectors to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

Beginning with version 2 of the External Content Connectors application, external content connectors implement semantic vector indexing for crawled items. When you upgrade to a version that supports semantic vector indexing, your existing connectors will reindex all previously retrieved items the next time they're visited by a crawl, even if those items' content is unchanged. To force semantic vector indexing of your external content items as soon as possible after upgrading, cancel any running crawls, then restart the canceled crawls manually.

 When you upgrade to version 4 of the External Content Connectors application from an earlier version, searches may not show all previously crawled content until you've completed both a content crawl and a user mapping crawl for each upgraded connector. The first content crawl run after the upgrade will reindex all searchable content from the source system, and the user mapping crawl will reindex all security principals from the source system. All crawled content should be shown in searches after both of these crawls are complete.

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

Zurich

</td><td>

-   **[Adobe Acrobat Sign external content connector](https://www.servicenow.com/docs/access?context=adobe-acrobat-sign-external-content-connector&family=zurich&ft:locale=en-US)**

Retrieve searchable content and metadata from your Adobe Acrobat Sign source system.

-   **[Aha! Roadmaps external content connector](https://www.servicenow.com/docs/access?context=aha-roadmaps-external-content-connector&family=zurich&ft:locale=en-US)**

Retrieve searchable content and metadata from your Aha! Roadmaps source system.

-   **[Cornerstone external content connector](https://www.servicenow.com/docs/access?context=cornerstone-external-content-connector&family=zurich&ft:locale=en-US)**

Retrieve searchable content and metadata from your Cornerstone source system.

-   **[Fluid Topics external content connector](https://www.servicenow.com/docs/access?context=fluid-topics-external-content-connector&family=zurich&ft:locale=en-US)**

Retrieve searchable content and metadata from your Fluid Topics source system.

-   **[ManageEngine external content connector](https://www.servicenow.com/docs/access?context=manageengine-external-content-connector&family=zurich&ft:locale=en-US)**

Retrieve searchable content and metadata from your ManageEngine source system.

-   **[Workvivo external content connector](https://www.servicenow.com/docs/access?context=workvivo-external-content-connector&family=zurich&ft:locale=en-US)**

Retrieve searchable content and metadata from your Workvivo source system.


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


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing External Content Connectors features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Sitemap support in the Webcrawler external content connector](https://www.servicenow.com/docs/access?context=webcrawler-external-content-connector&family=zurich&ft:locale=en-US)**

Retrieve content and links from URLs found in sitemaps defined for your web source system when running content crawls for the Webcrawler external content connector. A content crawl only retrieves sitemap URLs that include the crawl's starting point URL.

-   **[Start point links for scheduled partial content crawls](https://www.servicenow.com/docs/access?context=create-content-crawl-external-content-connector&family=zurich&ft:locale=en-US)**

View the start point for a scheduled partial content crawl via a link in its entry in the the external content connector's list of crawls.

-   **[Start point links in partial content crawl history entries](https://www.servicenow.com/docs/access?context=review-crawl-ext-cont-connector&family=zurich&ft:locale=en-US)**

View the start point for a scheduled partial content crawl via a link in its crawl history entries.

-   **[Limited Role-Based Access Control \(RBAC\) support in the Atlassian](https://www.servicenow.com/docs/access?context=atlassian-confluence-cloud-external-content-connector&family=zurich&ft:locale=en-US) Confluence Cloud external content connector**

Map source system user and group permissions assigned via RBAC roles to users in your ServiceNow AI Platform instance.


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


-   **[Webcrawler external content connector](https://www.servicenow.com/docs/access?context=webcrawler-external-content-connector&family=zurich&ft:locale=en-US)**

The predefined web sources external content connector has been subsumed into the new Webcrawler external content connector, which enables you to specify a custom web source or select a predefined one.


</td></tr><tr><td>

Australia

</td><td>

-   **[ServiceNow instance external content connector](https://www.servicenow.com/docs/access?context=servicenow-instance-external-content-connector&family=australia&ft:locale=en-US)**

You can now create and run multiple ServiceNow instance connectors on a single ServiceNow AI Platform instance.

-   **[Webcrawler external content connector](https://www.servicenow.com/docs/access?context=webcrawler-external-content-connector&family=australia&ft:locale=en-US)**

Connector admins can now schedule crawls on a daily, weekly, or monthly basis for all Webcrawler external content connectors.


-   **[Sitemap support in the Webcrawler external content connector](https://www.servicenow.com/docs/access?context=webcrawler-external-content-connector&family=australia&ft:locale=en-US)**

Retrieve content and links from URLs found in sitemaps defined for your web source system when running content crawls for the Webcrawler external content connector. A content crawl only retrieves sitemap URLs that include the crawl's starting point URL.

-   **[Start point links for scheduled partial content crawls](https://www.servicenow.com/docs/access?context=create-content-crawl-external-content-connector&family=australia&ft:locale=en-US)**

View the start point for a scheduled partial content crawl via a link in its entry in the the external content connector's list of crawls.

-   **[Start point links in partial content crawl history entries](https://www.servicenow.com/docs/access?context=review-crawl-ext-cont-connector&family=australia&ft:locale=en-US)**

View the start point for a scheduled partial content crawl via a link in its crawl history entries.

-   **[Limited Role-Based Access Control \(RBAC\) support in the Atlassian](https://www.servicenow.com/docs/access?context=atlassian-confluence-cloud-external-content-connector&family=australia&ft:locale=en-US) Confluence Cloud external content connector**

Map source system user and group permissions assigned via RBAC roles to users in your ServiceNow AI Platform instance.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some External Content Connectors features or functionality were removed.

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

Between your current release family and Australia, some External Content Connectors features or functionality were deprecated.

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
</table>## Activation information

Review information on how to activate External Content Connectors.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

Install External Content Connectors by requesting the External Content Connectors Application Suite from the ServiceNow Store. 

</td></tr><tr><td>

Australia

</td><td>

Install External Content Connectors by requesting the External Content Connectors Application Suite from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for External Content Connectors we have noted them here.

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

If any specific browser requirements were introduced or changed for External Content Connectors we have noted them here.

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
</table>## Accessibility information

Review details on accessibility information for External Content Connectors, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   ****

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

Zurich

</td><td>

[Zurich Patch 7](https://www.servicenow.com/docs/access?context=zurich-patch-7&family=zurich&ft:locale=en-US)

-   Expand your search experience with external content connectors for Adobe Acrobat Sign, Aha! Roadmaps, Cornerstone, Fluid Topics, ManageEngine, and Workvivo source systems.
-   Retrieve content and links from URLs found in sitemaps defined for your web source system when running content crawls for the Webcrawler external content connector.
-   View a content crawl's start point via links in the content crawl list and in content crawl history entries.

 [Zurich Patch 4](https://www.servicenow.com/docs/access?context=zurich-patch-4&family=zurich&ft:locale=en-US)

-   Expand your search experience with external content connectors for Adobe Experience Manager as a Cloud Service, Asana, Docusign, Dropbox, GitHub Enterprise Cloud, HubSpot, Lucidchart, Miro, monday.com, Notion, SAP DMS, Smartsheet, Trello, WordPress, Workday, and Zoom source systems.
-   Customize user permission settings, choosing the fields you want to compare when mapping source system users to ServiceNow AI Platform® users.
-   Make external content connector crawl results searchable by linking connector search sources to search profiles from the connector editor.
-   Monitor connector behavior on individual crawl runs and over time with improved crawl statistics and analytics.

 [Zurich Patch 1](https://www.servicenow.com/docs/access?context=zurich-patch-1&family=zurich&ft:locale=en-US)

-   Expand your search experience by indexing searchable content from your Amazon S3, Box, GitLab, Microsoft OneDrive, Microsoft Viva Engage, and Zendesk Guide source systems.
-   Search KB articles from your ServiceNow instance.
-   Make web content locally searchable by indexing pages from predefined or custom public web sites with the Webcrawler external content connector.
-   Configure connector settings and schedule crawls as part of connector creation using the revamped UI.

 See [External Content Connectors](https://www.servicenow.com/docs/access?context=ext-cont-connectors-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

[Australia Patch 3](https://www.servicenow.com/docs/access?context=australia-patch-3&family=australia&ft:locale=en-US)

-   Expand your search experience to include content and metadata from your SAP SuccessFactors Learning source system.
-   Improve search recall with automatic multimodal caption generation for images, tables, charts, and complex layouts in attachments and files retrieved by your external content connector's content crawls.
-   Make more content searchable by creating and running multiple ServiceNow instance connectors on a single ServiceNow AI Platform instance.
-   Increase flexibility by scheduling crawls on a daily, weekly, or monthly basis for your Webcrawler external content connectors.

 [Australia Patch 1](https://www.servicenow.com/docs/access?context=australia-patch-1&family=australia&ft:locale=en-US)

-   Expand your search experience with external content connectors for Adobe Acrobat Sign, Aha! Roadmaps, Cornerstone, Fluid Topics, ManageEngine, and Workvivo source systems.
-   Retrieve content and links from URLs found in sitemaps defined for your web source system when running content crawls for the Webcrawler external content connector.
-   View a content crawl's start point via links in the content crawl list and in content crawl history entries.

 See [External Content Connectors](https://www.servicenow.com/docs/access?context=ext-cont-connectors-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)

