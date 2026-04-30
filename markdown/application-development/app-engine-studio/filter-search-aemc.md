---
title: Filter and search for requests in AEMC
description: The App Engine Management Center \(AEMC\) application provides tools for locating requests. You can perform a global search for request records or filter the list of current requests to locate the ones you want to work on.
locale: en-US
release: yokohama
product: App Engine Studio
classification: app-engine-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Managing requests using AEMC, Managing app development using the App Engine Management Center, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Filter and search for requests in AEMC

The App Engine Management Center \(AEMC\) application provides tools for locating requests. You can perform a global search for request records or filter the list of current requests to locate the ones you want to work on.

## Filtering requests

On the Requests, Pipelines, Custom apps, and Developers pages, you can filter the list of requests by several different criteria.

To create a filter, select the filter icon \(![Filter icon.](../image/aemc-filter.png)\), select **Advanced view**, and add criteria. Build a filter by adding conditions that contain a field, operator, and value\(s\). You can use an existing filter, save what you create, and limit who can use the filter. Build more complex filters by using the **or** and **and** connectors. Add as many filters as you need, and select **Update**.

When you filter on the Pipelines tab, only instances with requests that match the filtering criteria display information. For example, if your pipeline shows request data in three instances and you filter by an app name used in only one of those instances, only that instance returns results.

## Searching for requests

You can use the **Search** field at the top of any AEMC screen to search for submitted requests. Simply type all or a portion of a request number using an asterisk wild card character, and select **View results**.

![Search field](../image/search.png "Search")

For example, you can type DEV0001\* and select **View results** \(or simply press **Enter**\), and a list of all collaboration requests that begin with DEV0001 are returned.

![Search results](../image/search-results.png "Search results")

You can then select the record you want to review.

**Parent Topic:**[Managing requests using AEMC](manage-aemc-requests.md)

