---
title: Content Management meta tags
description: Meta tags are special tags in web pages that contain information about the page but are not rendered with the page. You can define custom meta tags for content pages.
locale: en-US
release: xanadu
product: Content Management System
classification: content-management-system
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure Content Management sites, Content Management System, Configure UIs and portals, Configure user experiences]
---

# Content Management meta tags

Meta tags are special tags in web pages that contain information about the page but are not rendered with the page. You can define custom meta tags for content pages.

Meta tags are not noticeable to a page visitor unless the visitor looks at the page source code. Web search engines read meta tags as they "crawl" the web, identifying and organizing content. Modern website designers often use meta tags to embed "hints" to search engines about how to index or otherwise crawl the site.

Structurally, a meta tag consists of a tag and a name/content pair and looks similar to the following code.

```
<meta name="generator" content="MediaWiki 1.16wmf4" />
```

The Content Management System allows you to define both site level and page level tags.

-   **[Configure a page level meta tag](../task/t_AddAPageLevelMetaTag.md)**  
A page level tag is a meta tag defined on a specific page and included on only that page.
-   **[Configure a site level meta tag](../task/t_AddASiteLevelMetaTag.md)**  
A site level tag is a meta tag is defined on a site and included on every page within that site.
-   **[Configure DIV-based layouts](../task/t_ConfigureDivBasedLayouts.md)**  
After you create your site, you can change the site layout with DIV tags.
-   **[Content meta tag hierarchy](../reference/r_ContentMetaTagHierarchy.md)**  
Page and site level meta tags are included in a content meta tag hierarchy.

**Parent Topic:**[Configure Content Management sites](../task/t_CreateASite.md)

**Related topics**  


[Content sites](c_ContentSite.md)

[Content pages in CMS](c_ContentPages.md)

[Content Management templates](c_ContentManagementTemplates.md)

[Content types](c_ContentTypes.md)

[Content blocks](c_ContentBlocks.md)

[Style in Content Management](c_StyleInContentManagement.md)

