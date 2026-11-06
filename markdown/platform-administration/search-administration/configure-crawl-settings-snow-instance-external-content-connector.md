---
title: Configure crawl settings for a ServiceNow instance external content connector
description: Specify the content types that you want your ServiceNow instance external content connector to retrieve when running content crawls.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-administration/search-administration/configure-crawl-settings-snow-instance-external-content-connector.html
release: australia
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2026-10-28"
reading_time_minutes: 7
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [ServiceNow instance external content connector, Configure, External Content Connectors, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure crawl settings for a ServiceNow instance external content connector

Specify the content types that you want your ServiceNow instance external content connector to retrieve when running content crawls.

## Before you begin

A connector administrator must have already created the ServiceNow® instance external content connector that you want to configure crawl settings for. To learn about this procedure, see [Create a ServiceNow instance external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/create-ext-cont-connector-snow-instance.md).

To specify inclusion and exclusion filters, you must be familiar with Java regular expression patterns. For information on the syntax of Java regular expression patterns, see [the Javadoc for the java.regex.util.Pattern class](https://docs.oracle.com/en/java/javase/21/docs/api/java.base/java/util/regex/Pattern.html).

Role required: sn\_ext\_conn.xcc\_admin

## About this task

This task is optional. By default, the ServiceNow instance external content connector retrieves all KB article, Service Catalog item, and incident records, plus attachments on those records, from your ServiceNow AI Platform instance. Only perform this task if you want the connector to use any of the following non-default settings:

-   Inclusion or exclusion filters for the KB articles to retrieve from the source instance when running content crawls
-   Inclusion or exclusion filters for the Service Catalog items to retrieve from the source instance when running content crawls
-   Inclusion or exclusion filters for the incidents to retrieve from the source instance when running content crawls
-   Inclusion or exclusion of attachments from all retrieved records

Content is only retrieved from the source system if it passes all of your configured crawl setting filters. If any crawl setting filter excludes a content item, the external content connector doesn't retrieve it.

**Important:**

By default, each external content connector can index up to one million \(1,000,000\) content items from its source system. When a connector exceeds this limit, it continues to crawl the source system, but only sends content item deletions and updates to AI Search for indexing, ignoring new content items. The connector logs an error message for every 10,000 content items it crawls beyond the indexing limit.

When a connector's indexed content item count exceeds 800,000, a warning message appears in the connector's UI to indicate that it's approaching the indexing limit. If the connector reaches the indexing limit, an error message appears in its UI.

External content connectors that support user permissions crawls can handle permissions for up to five hundred thousand \(500,000\) users and their groups. If a connector retrieves users in excess of this limit, user and group permissions may not be correctly applied to the connector's retrieved content. As a result, the content may not be searchable.

If one of your connectors reaches the content indexing limit, you can update its crawl settings and file inclusion/exclusion filters to reduce the number of content items it retrieves. If you need to index more content items than the limit allows, you can create a Customer Service and Support case at [https://support.servicenow.com/now](https://support.servicenow.com/now) to request a limit increase for the connector.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  In the Connectors list, select the record for the ServiceNow instance external content connector whose settings you want to modify.

3.  In the connector editor's **Settings** tab, select **Crawl settings**.

4.  To crawl knowledge base articles from the source instance, activate the **Crawl KB articles** option in the KB articles section, then select one of the following filtering options in that section.

    -   To crawl all KB articles from the source instance, select **Crawl all short descriptions**.
    -   To crawl only a specified set of KB articles from the source instance, select **Include only these short descriptions**, then use the **Add short description patterns to include** field and **Add** button to enter Java regular expression patterns that match the short descriptions for the KB articles that you want to include in the crawl.

        As an example, you might enter `Beginner's [Gg]uide` to include all KB articles with short descriptions that contain the terms `Beginner's Guide` or `Beginner's guide`.

    -   To crawl all except a specified set of KB articles from the source instance, select **Exclude only these short descriptions**, then use the **Add short description patterns to exclude** field and **Add** button to enter Java regular expression patterns that match the short descriptions for the KB articles that you want to exclude from the crawl.

        As an example, you might enter `(?i)\[Legacy\]` to exclude all KB articles with short descriptions that contain the terms `[Legacy]` or `[legacy]`.

5.  To crawl Service Catalog items from the source instance, activate the **Crawl service catalog items** option in the Service catalog items section, then select one of the following filtering options in that section.

    -   To crawl all Service Catalog items from the source instance, select **Crawl all names**.
    -   To crawl only a specified set of Service Catalog items from the source instance, select **Include only these names**, then use the **Add name patterns to include** field and **Add** button to enter Java regular expression patterns that match the names for the Service Catalog items that you want to include in the crawl.

        As an example, you might enter `(?i)\blaptop\b` to include all Service Catalog items with names that contain `Laptop` or `laptop` surrounded by word breaks.

    -   To crawl all except a specified set of Service Catalog items from the source instance, select **Exclude only these names**, then use the **Add name patterns to exclude** field and **Add** button to enter Java regular expression patterns that match the names for the Service Catalog items that you want to exclude from the crawl.

        As an example, you might enter `1[3-5] inch laptop` to exclude all Service Catalog items with names that contain `13 inch laptop`, `14 inch laptop`, or `15 inch laptop`.

6.  To crawl Incident records from the source instance, activate the **Crawl incidents** option in the Incidents section, then select one of the following filtering options in that section.

    -   To crawl all incidents from the source instance, select **Crawl all short descriptions**.
    -   To crawl only a specified set of incidents from the source instance, select **Include only these short descriptions**, then use the **Add short description patterns to include** field and **Add** button to enter Java regular expression patterns that match the short descriptions for the incidents that you want to include in the crawl.

        As an example, you might enter `Release2025Q[1-4]` to include all incidents with short descriptions that contain the terms `Release2025Q1`, `Release2025Q2`, `Release2025Q3`, or `Release2025Q4`.

    -   To crawl all except a specified set of incidents from the source instance, select **Exclude only these short descriptions**, then use the **Add short description patterns to exclude** field and **Add** button to enter Java regular expression patterns that match the short descriptions for the incidents that you want to exclude from the crawl.

        As an example, you might enter `sprint\d{1,3}` to exclude incidents with short descriptions that contain the term `sprint` followed by a one-digit, two-digit, or three-digit numeral.

7.  To crawl attachments from retrieved records, activate the **Crawl attachments** option in the Attachments section.

8.  If you want AI Search to automatically generate captions for content in attachments and files retrieved by the connector, select the **Multimodal captions** option.

    When you select this option, the Platform Multimodal Service automatically generates descriptive captions for images, tables, charts, and other visual elements found in retrieved attachments and files. You can discover these retrieved attachments and files by searching for terms from their generated captions.

    This option is only available when the Platform Multimodal Service plugin is activated on your instance.

    -   For details on activating the plugin, see [Activate the Platform Multimodal Service plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/ai-search/activate-platform-multimodal-service-plugin.md).
    -   To learn how to select the VLM \(visual learning model\) provider and model used for the Platform Multimodal Service, see [Configure multimodal captioning for AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/configure-multimodal-captioning-for-ai-search.md).
9.  Select **Save and validate**.


## Result

The ServiceNow instance external content connector is updated with your modified crawl settings.

## What to do next

To retrieve content from your ServiceNow AI Platform instance using your modified crawl settings, create and run a one-time content crawl for your ServiceNow instance external content connector. To learn about creating and running one-time content crawls, see [Create a content crawl for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/create-content-crawl-external-content-connector.md).

**Parent Topic:**[ServiceNow instance external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/servicenow-instance-external-content-connector.md)

