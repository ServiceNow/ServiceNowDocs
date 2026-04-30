---
title: Content lookup
description: The Content library portal gives you visibility into the data stored in the Software Asset Management Content Service via an intuitive user interface.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Content lookup

The Content library portal gives you visibility into the data stored in the Software Asset Management Content Service via an intuitive user interface.

The Software Asset Management Content Service is a repository of software product names and all additional information such as software product lifecycle dates, discovery maps, model numbers, publisher part numbers \(PPNs\). This information is stored in different tables in the Content Service. For more details on the Content Service, see [Software Asset Management Content Service](c_SAMContentService.md).

To access the Content library portal, navigate to the Software Asset Workspace and click the Content lookup view icon on the left hand side of the page.

![Content library portal](../image/contentlookup.png "Content lookup")

The Content library portal application is available in the ServiceNow Store. Once you install the application, ensure that the AI Search \(com.glide.ais\) plugin is activated. For details on installing the Content library portal application, see [Install Content library portal for Software Asset Management](../task/install-contentlookup.md).

The Content library portal uses the AI search functionality and helps you to:

-   Search for specific software product, PPNs, or model IDs.
-   View the entire list of software products, PPNs, and model IDs in the Content Service.
-   View additional details related to software products such as software version, software product life cycles.
-   View the days remaining for the next content update.

Once you enter your search criteria in the search bar, the search results are listed with the most relevant matches at the top. Filters on the left-hand side of the page assist you in further narrowing down your results.

Based on your search criteria the information in the Content Service is pulled from multiple tables, such as:

-   Software Product \[samp\_sw\_product\]
-   Discovery Map \[samp\_sw\_entitlement\_definition\]
-   Publisher part numbers \[samp\_sw\_product\_definition\]

Click the search result that matches your criteria to display the product details page along with the related lists. The product details page opens in a read-only mode. For example, if you click the Microsoft SQL Server 2008 Enterprise product result, the Microsoft SQL Server 2008 Enterprise page appears with the related lists such as software version, software life cycle data, and PPN.

