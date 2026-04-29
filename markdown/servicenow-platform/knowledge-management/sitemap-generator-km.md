---
title: Sitemap Generator for the Knowledge Portal
description: The ServiceNow Sitemap Generator application enables you to efficiently define and automatically generate XML sitemaps.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Exploring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Sitemap Generator for the Knowledge Portal

The ServiceNow® Sitemap Generator application enables you to efficiently define and automatically generate XML sitemaps.

## Sitemap Generator configuration requirements for the Knowledge Portal

The sitemap is generated from a script or static XML. Validating sitemaps isn't handled automatically, so verify when creating a sitemap that its contents meet the following requirements:

-   Includes only the knowledge base configured for the Knowledge Portal
-   Includes only Knowledge Portal pages with unauthenticated user access
-   Excludes Knowledge Portal URLs that aren't publicly accessible
-   Excludes pages that respond with a 301 redirect
-   Excluded retired and expired knowledge base articles

For information about sitemap requirements for search engine optimization \(SEO\), see [Build and submit a sitemap](https://developers.google.com/search/docs/crawling-indexing/sitemaps/build-sitemap) in the Google documentation.

**Parent Topic:**[Knowledge Management](knowledge-management.md)

