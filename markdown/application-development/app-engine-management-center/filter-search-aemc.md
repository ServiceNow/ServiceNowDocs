---
title: Filter and search for requests in AEMC
description: The App Engine Management Center \(AEMC\) application provides tools for locating requests. You can perform a global search for request records or filter the list of current requests to locate the ones you want to work on.
locale: en-US
release: australia
product: App Engine Management Center
classification: app-engine-management-center
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage requests, Manage app development, Use, App Engine Management Center, Governing app development, Building applications]
---

# Filter and search for requests in AEMC

The App Engine Management Center \(AEMC\) application provides tools for locating requests. You can perform a global search for request records or filter the list of current requests to locate the ones you want to work on.

## Filtering requests

On the Requests, Pipelines, Release Management, Custom apps, and Developers pages, you can filter the list of requests by several different criteria.

To create a filter, select the filter icon \( ![Filter icon.](../image/aemc-filter.png)\), select **Advanced view**, and add criteria. Build a filter by adding conditions that contain a field, operator, and value\(s\). You can use an existing filter, save what you create, and limit who can use the filter. Build more complex filters by using the **or** and **and** connectors. Add as many filters as you need, and select **Update**.

**Note:** On the **Requests** and **Release Management** tabs, you can use the **Saved filters** option \(![Saved filter option](../image/saved-filter-icon.png)\) which provides default filtering capabilities along with advanced features and real time filtering options. Saved filters can be stored and shared with individual users or user groups..

When you filter on the Pipelines tab, only instances with requests that match the filtering criteria display information. For example, if your pipeline shows request data in three instances and you filter by an app name used in only one of those instances, only that instance returns results.

## Searching for requests

You can use the **Search** field at the top of any AEMC screen to search for submitted requests. Simply type all or a portion of a request number using an asterisk wild card character, and select **View results**.

![Search field](../image/search.png "Search")

For example, you can type DEV0001\* and select **View results** \(or simply press **Enter**\), and a list of all collaboration requests that begin with DEV0001 are returned.

You can then select the record you want to review.

**Parent Topic:**[Managing requests using AEMC](manage-aemc-requests.md)

