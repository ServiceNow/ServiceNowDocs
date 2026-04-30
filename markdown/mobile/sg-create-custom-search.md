---
title: Configure search criteria
description: Create a custom search for your launcher screen to help your users find related information quickly. Administrators can configure which search sources the search uses, as well as options like search result limits.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Global search, Launcher screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure search criteria

Create a custom search for your launcher screen to help your users find related information quickly. Administrators can configure which search sources the search uses, as well as options like search result limits.

Configuration for search consist of linking the following records:

-   **Launcher screen**

    The launcher screen is where the search bar appears within your mobile application.

-   **Global search configuration**

    The global search configuration \[sys\_sg\_global\_search\] record is what associates your launcher screen with a search context configuration and an item configuration. This record is also where you can configure placeholder text, and enable photo search.

-   **Item configuration**

    Item configurations provide a pattern for data in your screen, and control how your data appears within a segment. In this case, the appearance of your search results.

-   **Search application configuration**

    The search application configuration \[sys\_search\_context\_config\] record connects your search source with your search configuration. This record is also where you can set limits on search results and search suggestions.

-   **Search source**

    Search source \[sys\_search\_source\] records determine what tables on your instance are included in your searches.


![Diagram showing relationship of records used in search.](../image/search-diagram.png "Records used in search")

-   **[Create a search source](../task/sg-create-search-source.md)**  
Create a search source to define what records can be found in your search bar.
-   **[Create a search configuration](../task/sg-mobile-search-e2e.md)**  
Create a search configuration. This record connects your launcher screen with the other records used to configure search.
-   **[Add your search configuration to a launcher screen](../task/sg-mobile-search-alp-config.md)**  
Update your launcher screen to use your custom search configuration.

