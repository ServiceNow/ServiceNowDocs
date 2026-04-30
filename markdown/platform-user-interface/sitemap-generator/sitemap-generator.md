---
title: Sitemap Generator
description: Use the ServiceNow Sitemap Generator application to define and automatically generate XML sitemaps to improve search engine optimization of public portal pages.
locale: en-US
release: zurich
product: Sitemap Generator
classification: sitemap-generator
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Improving search engine optimization for portals, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Sitemap Generator

Use the ServiceNow® Sitemap Generator application to define and automatically generate XML sitemaps to improve search engine optimization of public portal pages.

## Activation information

You can activate the Sitemap Generator application \(sn\_ux\_seo\_sitemap\) from your instance. For more information, see [Activate Sitemap Generator](../task/activate-sitemap-generator.md).

You can also activate Sitemap Generator from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Sitemap requirements

The sitemap is generated from a script or static XML. When creating a sitemap, you must ensure that its contents meet the following requirements because validating them isn’t handled automatically:

-   Includes only pages with unauthenticated user access.

    Sitemap Generator automatically excludes portal URLs that aren’t publicly accessible from sitemaps. However, this doesn’t apply for URLs with custom domains instead of the ServiceNow domain. URLs that are excluded from the sitemap are listed in the Application Log \[syslog\_app\_scope\] table.

-   Excludes pages that respond with a 301 redirect.
-   Excludes pages with the NOINDEX meta tag, such as retired or expired pages. If you use a script to create the sitemap, include logic similar to that of the SEO script include you used to add NOINDEX meta tags to pages to exclude those pages from the sitemap. For more information, see [Configure custom SEO tags for canonical URLs and localized knowledge articles](https://www.servicenow.com/docs/access?context=configure-seo-knowledge&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).
-   For any pages with canonical URLs or **hreflang** tags, the sitemap includes those canonical URLs or URLs with **hreflang** tags returned by the SEO script include for that page. If you use a script to create the sitemap, include logic similar to that of the SEO script include you used to return canonical URLs or URLs with **hreflang** tags. For more information, see [SEO for canonical URLs and localized versions of knowledge articles](https://www.servicenow.com/docs/access?context=seo-knowledge&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).
-   For any pages with human readable keywords in URLS, the sitemap includes those URLs with human readable keywords. If you use a script to create the sitemap, use one of the getHumanReadableUrl methods in the SPSEOUtilsSNC class to return the human readable keywords and include them in the sitemap URLs. For more information, see [Add human readable keywords to page URLs](../task/add-human-readable-keywords-page-urls.md).

**Note:** Guidance on how to meet these requirements is included in the code templates in the **Script** and **Static XML** fields where the sitemap contents are defined. For more information, see [Generate XML sitemaps for SEO indexing](../task/generate-xml-sitemaps-seo-indexing.md).

For more information about sitemap requirements for SEO, refer to the following resources:

-   [Build and submit a sitemap](https://developers.google.com/search/docs/advanced/sitemaps/build-sitemap) in the Google documentation
-   [XML schema for the Sitemap protocol](https://www.sitemaps.org/protocol.html) on the sitemaps.org website

-   **[Activate Sitemap Generator](../task/activate-sitemap-generator.md)**  
You can activate the Sitemap Generator plugin \(sn\_ux\_seo\_sitemap\) for Service Portal if you have the admin role.
-   **[Generate XML sitemaps for SEO indexing](../task/generate-xml-sitemaps-seo-indexing.md)**  
Create XML sitemaps for web crawlers to index your public portal pages and improve search engine optimization for your portals.

**Parent Topic:**[Improving search engine optimization for portals](seo-sp.md)

