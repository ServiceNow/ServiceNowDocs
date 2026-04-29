---
title: Improving search engine optimization for portals
description: Search engine optimization \(SEO\) helps portal users find the information they need and be more engaged with your portal. Adding SEO information to your public portal pages improves how external search engines index and rank pages to make them more findable.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Service Portal, Configure UIs and portals, Configure user experiences]
---

# Improving search engine optimization for portals

Search engine optimization \(SEO\) helps portal users find the information they need and be more engaged with your portal. Adding SEO information to your public portal pages improves how external search engines index and rank pages to make them more findable.

You can add the following types of information to Service Portal pages to improve SEO:

-   Human readable keywords in URLs.
-   Meta tags that include information about the page or portal in the `<head>` section of a page.
-   Dynamic page titles that are descriptive of the page contents.
-   **hreflang** tags that specify all the available languages of a page.
-   Canonical URLs that specify which pages to index from sets of duplicate URLs.

To improve SEO for your portal further, you can also define and automatically generate XML sitemaps for search engines to index using the Sitemap Generator application.

Some portal pages load data from a record that's specified by a parameter in the URL. For these pages, you can use dynamic page variables to add meta tags, page titles, and human readable URL keywords that vary depending on the record loaded in the page.

Using a Service Catalog page as an example, the following URL includes a sys\_id parameter in addition to the page ID. Different content loads on the page depending on the value of the sys\_id parameter, which specifies a catalog item record.

`https://<instance>/sp?id=sc_cat_item&sys_id=c3b9cbf29716cd1021983d1e6253afad`

In this example, the sys\_id is for the iPad pro catalog item. The sc\_cat\_item page has been configured to generate a dynamic title and dynamic keywords in the URL based on the **Name** field of the catalog item record.

![Dynamic page title and URL keywords based on the catalog item sys_id specified by the URL parameter](../image/dyn-page-ex.png)

-   **[Add human readable keywords to page URLs](../task/add-human-readable-keywords-page-urls.md)**  
Add human readable keywords to the URLs of portal pages to improve search engine optimization \(SEO\) and click-through rates and help users understand what to expect on the page.
-   **[Add meta tags to a public page](../task/seo-tags.md)**  
Improve the searchability of Service Portal pages by adding meta tags. You can add the meta name and description attributes to a page, define the robots attribute, or create dynamic meta tags for pages that load record data based on a URL parameter.
-   **[Add dynamic titles to a page](../task/add-page-title.md)**  
Create variables to generate descriptive titles depending on the content loaded into a page.
-   **[Configure the main tag on a page](../task/configure-main-tag-on-page.md)**  
Specify the main content of a page to include in the **&lt;main&gt;** tag to improve search engine optimization and accessibility.
-   **[Enable SEO for localized versions of a portal page](../task/seo-header-tags.md)**  
Allow users to discover portal pages in their preferred language by adding **hreflang** tags.
-   **[Sitemap Generator](sitemap-generator.md)**  
Use the ServiceNow® Sitemap Generator application to define and automatically generate XML sitemaps to improve search engine optimization of public portal pages.

**Parent Topic:**[Service Portal](c_ServicePortal.md)

