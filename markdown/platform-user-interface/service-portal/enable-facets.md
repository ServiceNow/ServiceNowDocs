---
title: Enable search facets
description: In new instances, search facets are enabled by default. If upgrading from a previous release, enable search facets by activating a record in the Page Route Maps \[sp\_page\_route\_map\] table.
locale: en-US
release: xanadu
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Zing search in Service Portal, Configuring search in a portal, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Enable search facets

In new instances, search facets are enabled by default. If upgrading from a previous release, enable search facets by activating a record in the Page Route Maps \[sp\_page\_route\_map\] table.

## Before you begin

Role required: admin or sp\_admin

## About this task

Search facets render in the Faceted Search widget on the sp\_search page. To enable search facets after upgrade, activate the page route map record to route your search results to render in the sp\_search page.

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Page Route Maps**.

2.  Locate the Search record in the list.

    This record redirects users from the search page to the sp\_search page when viewing search results in Service Portal. The sp\_search page includes the Faceted Search widget, which supports search facets in both desktop and mobile environments.

3.  Set the **Active** field to true.


## Result

When using search in Service Portal, results render in the sp\_search page. Add facets to the search source to enable end users to filter search results. To learn more about facets, see [Add facets to a simple search source](create-search-filter.md).

**Parent Topic:**[Zing search in Service Portal](../concept/zing-search-service-portal.md)

