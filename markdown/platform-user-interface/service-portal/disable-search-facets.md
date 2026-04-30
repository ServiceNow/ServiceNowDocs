---
title: Disable facets for a search source
description: Disable facets for one or more search sources by adding a system property. Once disabled, the search source does not display search facets in the Faceted Search widget on the sp\_search page. You can disable facets for simple or advanced search sources.
locale: en-US
release: xanadu
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Zing search in Service Portal, Configuring search in a portal, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Disable facets for a search source

Disable facets for one or more search sources by adding a system property. Once disabled, the search source does not display search facets in the Faceted Search widget on the sp\_search page. You can disable facets for simple or advanced search sources.

## Before you begin

Role required: admin or sp\_admin

## Procedure

1.  Enter `sys_properties.list` in the Application Navigator to navigate to the System Properties table.

2.  Click **New**.

3.  In the **Name** field, enter `glide.service_portal.disable_facets_for_search_sources`.

4.  In the **Value** field, enter a comma-separated list of search source Sys IDs to disable facets for.

    Do not include spaces. For example, `c6170ae86721220023c82e08f585efe6,c96eb1686721220023c82e08f585efff`.

5.  Click **Submit**.


## Result

Facets do not display when the defined search source is selected in the sp\_seach page.

**Parent Topic:**[Zing search in Service Portal](../concept/zing-search-service-portal.md)

