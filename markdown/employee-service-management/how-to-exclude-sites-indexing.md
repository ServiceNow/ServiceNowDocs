---
title: Exclude sites from indexing
description: Index sites and subsites selectively by excluding some URLs and subsites, which have confidential information.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Index sites for search, SharePoint Online Search Connector, Employee Service Management]
---

# Exclude sites from indexing

Index sites and subsites selectively by excluding some URLs and subsites, which have confidential information.

## Before you begin

Specify a list of subsites that you want to exclude from the SharePoint Online Search Connector indexing. Work with a Microsoft SharePoint administrator to understand the set of sites to exclude from indexing.

Role required: AI search administrator

## Procedure

1.  Navigate to **SharePoint Online Search Connector** &gt; **SharePoint Connectors**.

2.  Click **New**.

3.  Follow the instructions [Index sites for search](../concept/sharepoint-how-to-configure-search.md).

4.  Specify the URLs list in the **Exclude Subsites** field.

    **Note:** Specify the complete URLs and not relative URLs. You can add multiple sites with **\|** as a separator.


## Result

These URLs are not indexed by the AI Search and are not displayed in the search results.

## What to do next

**Remove Index**: Select the indexed site and click Remove Index to remove the site from indexing. On success, all the sites, drivers, and files are removed from the respective tables and the connector is updated to read only with the Deleted status.

