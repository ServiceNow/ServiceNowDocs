---
title: Configure Search Sources available on a page
description: Use contextual search to limit search results for an instance of the type-ahead search widget.
locale: en-US
release: xanadu
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Zing search in Service Portal, Configuring search in a portal, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Configure Search Sources available on a page

Use contextual search to limit search results for an instance of the type-ahead search widget.

With contextual search enabled, users only see type-ahead results for specific search sources. For example, searching on the Service Catalog page only shows results from the Service Catalog search source when contextual search is enabled.

1.  In the Service Portal Designer \(**Service Portal** &gt; **Service Portal Configuration** &gt; **Service Portal Designer**, find an instance of the type-ahead search widget.
2.  Point to the widget and click the edit icon \(![Edit icon from a widget in the Service Portal Designer](../image/IconEditOption.png)\).

    Alternatively, in any preview page containing the type-ahead search widget, for example the Service Catalog homepage, control + right-click to open the widget context menu. Then click **Instance Options**.

3.  In the Contextual Search Sources field, select search sources from the list.

    Search sources listed for contextual search can be limited to just one, several, or all search sources.


Default search sources are defined in the **glide.service\_portal.default\_search\_sources** property, so even if you do not have search sources configured, type-ahead search widget still shows type-ahead suggestions. For more information on default search sources, see [Set the default portal search source](../task/default-search-sources.md).

**Parent Topic:**[Zing search in Service Portal](zing-search-service-portal.md)

