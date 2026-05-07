---
title: Generate XML sitemaps for SEO indexing
description: Create XML sitemaps for web crawlers to index your public portal pages and improve search engine optimization for your portals.
locale: en-US
release: australia
product: Sitemap Generator
classification: sitemap-generator
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Sitemap Generator, Improving search engine optimization for portals, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Generate XML sitemaps for SEO indexing

Create XML sitemaps for web crawlers to index your public portal pages and improve search engine optimization for your portals.

## Before you begin

Add SEO information to portal pages, such as meta tags that improve the searchability of Service Portal pages. For more information, see [Improving search engine optimization for portals](../concept/seo-sp.md).

Review the "Sitemap requirements" section of the [Sitemap Generator](../concept/sitemap-generator.md) documentation topic to determine what content should be in the sitemap.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Sitemap Generator** &gt; **Sitemap Configuration**.

2.  In the UX Sitemap Configurations \[sys\_ux\_seo\_sitemap\_config\] table, select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Sitemap Name|A unique name for the sitemap.|
    |Description|A description of the sitemap contents.|
    |Active|Option for whether the sitemap is automatically generated.|

4.  From the form context menu, select **Save**.

5.  From the **Sitemap Config Definition** tab, select **New**.

    **Important:**

    -   You must ensure that the contents of your sitemap meet the [Sitemap requirements](../concept/sitemap-generator.md#section_w52_vbq_ytb).
    -   You don’t need to add the header and footer of the sitemap XML. These are added automatically when the sitemap is generated.
6.  In the **Type** field of the UX Sitemap Definition form, select one of the following options to define the contents of the sitemap either with a script or by specifying static URL elements.

<table id="choicetable_fff_fps_gtb"><thead><tr><th align="left" id="d117896e211">

Type

</th><th align="left" id="d117896e214">

Action

</th></tr></thead><tbody><tr><td id="d117896e220">

**Script**

</td><td>

Dynamically generate the content from a script.

 **Note:** If special characters such as &lt;,&gt;, &amp;, or " are included in URLs, you must replace them with their equivalent escape characters.

</td></tr><tr><td id="d117896e235">

**Static**

</td><td>

Specify the static URL elements to include in the sitemap.

 -   **loc**

The full page URL.

-   **lastmod**

The date the page was last modified.

-   **changefreq**

The approximate frequency at which the page is updated.

 For more information about valid values for these elements, see the [Sitemaps XML format](https://www.sitemaps.org/protocol.html) topic on the sitemaps.org website.

</td></tr></tbody>
</table>7.  Select **Active** and then select **Submit**.

8.  Repeat steps [5](generate-xml-sitemaps-seo-indexing.md#new-sitemap-def) through [7](generate-xml-sitemaps-seo-indexing.md#save-definition-type) to define additional content to include in the sitemap.

    You can create multiple sitemap definitions with any combination of types that combine to create the sitemap. For example, you could include both static XML and dynamic content from a script or you could include content from multiple scripts.

9.  Configure the number of URL elements to include per sitemap page to control how many pages are in your sitemap.

    By default, 750 URLs are included per sitemap page. For URLs with **hreflang** tags, you should limit the number of URLs per page to the default value of 750 URLs.

    1.  Enter `sys_properties.list` in the navigation filter.

    2.  Open the **glide.sitemap.page.count** property and set the value to the number of URLs to include per page.

        The maximum value is 5,000.

    3.  Select **Update**.

10. From the UX Sitemap Configuration record, select **Generate Sitemap**.

    If a sitemap includes more than the number of URL elements specified with the **glide.sitemap.page.count** system property, a sitemap index file that specifies the URLs of the sitemap pages is generated. The sitemap index file naming structure is `sitemap-<sitemap-config-sysid>.xml` and the sitemap page naming structure is `sitemap-<page>-<sitemap-config-sysid>.xml`.

11. Select **Copy Sitemap URL** and add the sitemap URL in Google Search Console or to your `robots.txt` file with the Google Custom Search integration.

    **Note:** This URL accesses the latest sitemap or, if the sitemap is paginated, the latest sitemap index. It doesn’t execute scripts on the fly to regenerate the sitemap.

    For information about using Google Search Console, see [Manage your sitemaps using the Sitemaps report](https://support.google.com/webmasters/answer/7451001) in the Google documentation. For information about the Google Custom Search integration, see [ServiceNow provided integrations](https://www.servicenow.com/docs/access?context=r_ServiceNowProvidedintegrations&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

12. Review any portals URLs that were excluded from the sitemap because they aren't publicly accessible.

    1.  Navigate to **All** &gt; **System Logs** &gt; **System Log** &gt; **Application Logs**.

    2.  In the condition builder, enter the filter **\[App Scope\] \[is\] \[Sitemap Generator\] AND \[Message\] \[starts with\] \[The given URL\]**.

        The **Message** field includes the excluded URLs. For example, "The given URL `https://<instance>/kb?id=kb_article_view` is not public".


## Result

All active sitemaps automatically regenerate once a day and include content from any of their active sitemap definitions. Previous versions of the sitemap are deleted. You can check the status of the daily job at **All** &gt; **System Logs** &gt; **System Log** &gt; **Application Logs** using the filter **\[App Scope\] \[is\] \[Sitemap Generator\]**.

**Parent Topic:**[Sitemap Generator](../concept/sitemap-generator.md)

