---
title: Service Portal events
description: View Service Portal events to get insight into how a portal is being used in your organization.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Usage Insights for Service Portal, Analytics and Reporting Solutions for Service Portal, Analyzing portal performance and usage, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Service Portal events

View Service Portal events to get insight into how a portal is being used in your organization.

Usage Insights automatically detects the gestures and actions of portal users. You can view each occurrence of these events in the Usage Insights application.

<table id="table_ls1_gl5_rlb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Submit Catalog Request

</td><td>

Tracks when a user submits a request through the SC Catalog Item widget. You can view the request ID and the number of items in each request.

 Use these analytics to optimize the Service Catalog.

</td></tr><tr><td>

Order Catalog Item

</td><td>

Tracks when a user orders a catalog item through the SC Catalog Item widget. You can view the name and ID of each ordered item. You can also view the associated request ID.

 Use these analytics to optimize the Service Catalog.

</td></tr><tr><td>

Submit Record Producer Request

</td><td>

Tracks when a user submits a request through any record producer.

 Use these analytics to optimize the Service Catalog.

</td></tr><tr><td>

View Knowledge Article

</td><td>

Tracks when a user views a knowledge article. You can view the name, ID, and language of each viewed article.

 Use these analytics to optimize the knowledge base.

</td></tr><tr><td>

Initiate Search

</td><td>

Tracks when a user searches the portal using the Faceted Search and Typeahead Search widgets. You can view the search keywords that users enter. You can also compare usage of the two search widgets.

 Use these analytics to improve search in Service Portal.

</td></tr><tr><td>

Search Result Selected

</td><td>

Tracks when a user selects a search result when using the Faceted Search widget. You can view the click rank and sys\_id of the selected search item.

 Use these analytics to improve search in Service Portal.

</td></tr><tr><td>

Successful Login

</td><td>

Tracks when a user logs in to Service Portal.

 Use these analytics to monitor login activity within a given time period.

</td></tr><tr><td>

PortalPageLoad

</td><td>

Tracks which pages users visit and in which languages.

 Use these analytics to understand your user base and the pages they interact with.

</td></tr><tr><td>

SP File Attach

</td><td>

Tracks how users attach files to records from portal pages: by navigating the file system, pasting files from the clipboard, or dragging and dropping files.

 Use these analytics to optimize how users can attach files to records from portal pages.

</td></tr></tbody>
</table>You can create custom events to be triggered. For more information, see [SNAnalytics - Client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/SNAnalyticsClientAPI.md)

**Parent Topic:**[Usage Insights for Service Portal](../concept/sp-analytics.md)

**Related topics**  


[SC Catalog Item widget](../concept/sc-catalog-item-widget.md)

[Faceted Search widget](../concept/faceted-search.md)

[Typeahead Search widget](../concept/typeahead-search-widget.md)

