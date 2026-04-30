---
title: Global search in Content Management
description: When you add global search to a CMS site, two different search result blocks can display, depending on the user role: global or no global.
locale: en-US
release: yokohama
product: Content Management System
classification: content-management-system
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Content Management System, Configure UIs and portals, Configure user experiences]
---

# Global search in Content Management

When you add global search to a CMS site, two different search result blocks can display, depending on the user role: global or no global.

Roles are defined at **System Properties** &gt; **Global Text Search**.

-   Search Results \(Global\): For users with permission to use the global search within the normal frame set. The normal frame set is defined as the default, non-CMS user interface with the set of frames.
-   Search Results \(No Global\): For users without permission to use the global search. Searches only the knowledge base and the catalog.

The header search bar and the Search dynamic block in the base system both automatically handle the permissions and direct the user to the appropriate search results. In the base system, the search result blocks are deployed on the same Search Results content page.

In order for the global search to work properly, it is important to ensure that the DEFAULT directs users to a working content page. If not, the results from the global search link back to the frame set, not to pages within the CMS site.

**Note:** The global search is similar to the normal frame set user interface and ties to the same roles \([Set global text search properties](https://www.servicenow.com/docs/access?context=set-global-text-search-properties&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)\).

## Search Results \(Global\)

Before you use the **Search Results \(Global\)** dynamic block, define Configure content types to control the behavior a search result is clicked. If no content type is defined for a table, selecting a link on that table renders the results according to the **DEFAULT** content type. It is good practice to point the **DEFAULT** content type to a page with a normal "Current Document" detailed block. Set the content type detail \(**Detail Template** field\) to have just an iFrame.

The **Search Results \(No Global\)** dynamic block does not require any additional configuration.

**Parent Topic:**[Content Management System](c_ContentManagementSystem.md)

**Related topics**  


[Content Management design](c_ContentManagementPlanning.md)

[Domain separation and the Content Management System](domain-separation-content-management.md)

[Configure Content Management sites](../task/t_CreateASite.md)

[Content Management integration points](c_CMSIntegrationPoints.md)

[Content Management testing](c_ContentManagementTesting.md)

[CMS translation](c_CMSTranslation.md#)

