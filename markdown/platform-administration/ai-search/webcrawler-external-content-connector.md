---
title: Webcrawler external content connector
description: The Webcrawler external content connector retrieves pages and subdomains from a public website and makes their content and metadata searchable in AI Search applications. This connector can crawl content from predefined public web sources or your own custom web sources.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Webcrawler external content connector

The Webcrawler external content connector retrieves pages and subdomains from a public website and makes their content and metadata searchable in AI Search applications. This connector can crawl content from predefined public web sources or your own custom web sources.

Connector administrators can run or schedule content crawls to retrieve updated content from pages and subdomains found on the selected website. Scheduled content crawls can run on a daily, weekly, or monthly basis. Content crawls feed their data to AI Search for indexing.

The indexed content and metadata are stored as records in a connector-specific indexed source. Search administrators can create search sources from this indexed source and link them to search profiles to make the indexed records searchable in AI Search applications.

Each Webcrawler connector can retrieve up to 50,000 items \(URLs\) from its source system when running content crawls.

**Note:** This is an exception to the general content crawl limit of ten million \(10,000,000\) items.

By default, you can configure up to three Webcrawler connectors for custom web sources. If you need to retrieve items from more than three custom web sources, you can create a Customer Service and Support case at [https://support.servicenow.com/now](https://support.servicenow.com/now) to request a limit increase for the Webcrawler connector.

-   **[Predefined web sources for the Webcrawler external content connector](../reference/predefined-websources-webcrawler-ext-cont-connector.md)**  
List of predefined public web sources that search administrators can retrieve searchable content from using the Webcrawler external content connector.
-   **[Create a Webcrawler external content connector](../task/create-ext-cont-connector-webcrawler.md)**  
Create an external content connector to retrieve searchable content from pages and subdomains in a public web source system. Select from a list of predefined web sources or specify your own web source.
-   **[Configure crawl settings for a Webcrawler external content connector](../task/configure-crawl-settings-webcrawler-external-content-connector.md)**  
Specify the pages and subdomains you want your Webcrawler external content connector to retrieve from your specified web source.

**Parent Topic:**[Configuring External Content Connectors](configuring-ext-cont-connectors.md)

**Related topics**  


[Create a content crawl for an external content connector](../task/create-content-crawl-external-content-connector.md)

