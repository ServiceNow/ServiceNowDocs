---
title: Configure crawl settings for a Webcrawler external content connector
description: Specify the pages and subdomains you want your Webcrawler external content connector to retrieve from your specified web source.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/search-administration/configure-crawl-settings-webcrawler-external-content-connector.html
release: australia
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2026-05-28"
reading_time_minutes: 5
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Webcrawler external content connector, Configure, External Content Connectors, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure crawl settings for a Webcrawler external content connector

Specify the pages and subdomains you want your Webcrawler external content connector to retrieve from your specified web source.

## Before you begin

A connector administrator must have already created the Webcrawler external content connector that you want to configure crawl settings for. To learn about this procedure, see [Create a Webcrawler external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/create-ext-cont-connector-webcrawler.md).

Role required: sn\_ext\_conn.xcc\_admin

## About this task

This task is optional. By default, the Webcrawler external content connector crawls all pages and subdomains from its specified source system. Only perform this task if you want to specify inclusion or exclusion filters for the subdomains to crawl or pages to retrieve when running content crawls.

Content is only retrieved from the source system if it passes all of your configured crawl setting filters. If any crawl setting filter excludes a content item, the external content connector doesn't retrieve it.

Each Webcrawler connector can retrieve up to 50,000 items \(URLs\) from its source system when running content crawls.

**Note:** This is an exception to the general content crawl limit of one million \(1,000,000\) items.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  In the Connectors list, select the record for the Webcrawler external content connector whose settings you want to modify.

3.  In the connector editor's Settings tab, select **Crawl settings**.

4.  To load content crawl URLs from the source system's sitemaps, select the **Use sitemap** option.

    If you select this option, content crawls for the Webcrawler external content connector retrieve content and links from URLs found in the source system's sitemaps that include the specified start point URL. The connector reads matching URLs from all sitemaps referenced in the source system's `robots.txt` file and all sitemaps located in common sitemap locations.

    As an example, suppose you select the **Use sitemap** option and then specify `https://example.com/mysite` as the start point URL for a content crawl. When you run the content crawl, the Webcrawler connector retrieves content and links from sitemap URLs that include `https://example.com/mysite`. In this case, the connector retrieves content and links from sitemap URLs `https://example.com/mysite/a` and `https://example.com/mysite/b` but ignores sitemap URLs `https://example.com/othersite/c` and `https://example.com/yoursite/d` because they don't include the start point URL.

5.  Select one of the following **Content** options:

    -   To crawl all pages and subdomains from the source system, select **Crawl all content**.
    -   To crawl only a specified set of pages and subdomains from the source system, select **Include only these URLs**, then use the **Add URL** field and **Add** button to enter URLs or wildcard URL expressions for pages and subdomains that you want to include in the crawl.

        For example, you might enter `https://support.apple.com/ipad` to include only searchable content from the specified page or subdomain. Alternately, you might enter `https://support.apple.com/ipad**` to include every page or subdomain with a URL that matches the specified wildcard expression.

    -   To crawl all except a specified set of pages and subdomains from the source system, select **Exclude only these URLs**, then use the **Add URL** field and **Add** button to enter URLs or wildcard URL expressions for pages and subdomains that you want to exclude from the crawl.

        For example, you might enter `https://knowledgebase.paloaltonetworks.com/KCSArticleDetail` to exclude searchable content from the specified page or subdomain. Alternately, you might enter `https://knowledgebase.paloaltonetworks.com/KCSArticleDetail**` to exclude every page or subdomain with a URL that matches the specified wildcard expression.

    **Note:** Wildcard URL expressions can include a URL prefix followed by the `**` suffix. They match all URLs that begin with the specified prefix.

6.  In the **Include only these pages and subdomains** section, use the **Add URL to include** field and **Add** button to enter URLs or URL wildcard expressions for the pages and subdomains that you want to include in content crawls.

    As an example, you might enter `https://www.example.com/products*` and `https://www.example.com/newsroom*` to only retrieve searchable content and metadata from pages and subdomains that match one of the specified URL wildcard expressions.

7.  In the **Exclude only these pages and subdomains** section, use the **Add URL to exclude** field and **Add** button to enter URLs or URL wildcard expressions for the pages and subdomains that you want to exclude from content crawls.

    As an example, you might enter `*contact*` to exclude pages and subdomains with URLs that match the specified URL wildcard expression.

8.  If you want AI Search to automatically generate captions for content in attachments and files retrieved by the connector, select the **Multimodal captions** option.

    When you select this option, the Platform Multimodal Service automatically generates descriptive captions for images, tables, charts, and other visual elements found in retrieved attachments and files. You can discover these retrieved attachments and files by searching for terms from their generated captions.

    This option is only available when the Platform Multimodal Service plugin is activated on your instance.

    -   For details on activating the plugin, see [Activate the Platform Multimodal Service plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/activate-platform-multimodal-service-plugin.md).
    -   To learn how to select the VLM \(visual learning model\) provider and model used for the Platform Multimodal Service, see [Configure multimodal captioning for AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/configure-multimodal-captioning-for-ai-search.md).
9.  Select **Save and validate**.


## Result

The Webcrawler external content connector is updated with your modified crawl settings.

## What to do next

To retrieve content from the public web source using your modified crawl settings, create and run a one-time content crawl for your Webcrawler external content connector. To learn about creating and running one-time content crawls, see [Create a content crawl for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/create-content-crawl-external-content-connector.md).

**Parent Topic:**[Webcrawler external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/webcrawler-external-content-connector.md)

