---
title: Sitemap Generator for the Consumer Service Portal
description: The ServiceNow Sitemap Generator application enables you to efficiently define and automatically generate XML sitemaps.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure the Customer and Consumer Service Portals, Set up self-service, Configuring Customer Service Management, Customer Service Management]
---

# Sitemap Generator for the Consumer Service Portal

The ServiceNow® Sitemap Generator application enables you to efficiently define and automatically generate XML sitemaps.

## Sitemap Generator configuration requirements for the Consumer Service Portal

The sitemap is generated from a script or static XML. Validating sitemaps isn't handled automatically, so verify when creating a sitemap that its contents meet the following requirements:

-   Includes only the knowledge base and catalogs configured for the Consumer Service Portal
-   Includes only Consumer Service Portal pages with unauthenticated user access
-   Excludes Consumer Service Portal URLs that aren't publicly accessible
-   Excludes pages that respond with a 301 redirect
-   Excluded retired and expired knowledge base articles
-   Includes hreflang support for knowledge articles

For information about sitemap requirements for search engine optimization \(SEO\), see [Build and submit a sitemap](https://developers.google.com/search/docs/crawling-indexing/sitemaps/build-sitemap) in the Google documentation.

