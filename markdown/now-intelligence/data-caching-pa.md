---
title: Data caching in Platform Analytics
description: Data caching can help data visualizations load faster by reusing older responses when available. Users can always get the latest data by refreshing the dashboard manually.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
keywords: [Prefetch, Prefetching]
breadcrumb: [Reference, Platform Analytics experience, Platform Analytics]
---

# Data caching in Platform Analytics

Data caching can help data visualizations load faster by reusing older responses when available. Users can always get the latest data by refreshing the dashboard manually.

Data caching could potentially speed up the load time of dashboards and data visualizations, especially for large datasets, for the following reasons:

-   Caching can avoid long aggregation calculations when there have been no changes to the data.
-   Caching can avoid aggregation calculations for users who have access to the same aggregated result data.
-   Caching can reduce the toll on the instance from long-running requests piling up.
-   Caching may be suitable for use cases where users are more interested in the speed with which their dashboard loads than in the freshness of the data.

## Supported data sources

Table and indicator data support caching.

## Activating data caching

Before you activate data caching, the property **glide.analytics.cache.enabled** must be set to `true`.

In the inline dashboard editor, you can activate or deactivate data caching per dashboard. Caching then applies to all data visualizations on that dashboard that have a data source that supports it. For more information, see [Configure Platform Analytics dashboard settings](../../dashboards/task/configure-ac-db-settings.md).

In the UI Builder, you can activate or deactivate data caching per data visualization. For an example, see the **useDataCache** property for either table or indicator data sources in [Single Score UIB Setup](https://developer.servicenow.com/dev.do#!/reference/next-experience/xanadu/now-components/now-vis-score-wrapper/uib-setup).

In the UI Builder, you can also enable data caching for a local data instance of the table or indicator type. For more information, see [Enable data caching for a local data instance](../../dashboards/task/enable-caching-local-data-instance.md).

## Default dashboard caching

By default, new dashboards that you create in the inline editor do not have caching enabled. You have to enable caching per dashboard, as described in the previous section. However, you can change the default behavior so that all new dashboards that you create in the inline editor have caching enabled. To do so, set the property **glide.analytics.cache.enable\_dashboard\_default** to `true`.

If you set the default behavior to have caching enabled on new dashboards, consider whether you want to change the default expiration time. The default value for the default expiration time is 24 hours. You can set this value in the property **glide.analytics.cache.dashboard\_default\_value**. The options are 1, 2, 4, 8, 12, or 24 hours. When setting this value, consider the impact on data prefetching.

It is not possible to enable caching by default for data visualizations created in the UI Builder.

## Prefetching data

The first loading of a dashboard does not have cached data to use, so can be subject to a slow load time. For example, the first time an IT agent logs in for the day, their cached data from the previous day has expired, so they must wait for the system to fetch data before any of their dashboards load. The prefetch mechanism addresses this issue for frequently used dashboards and data visualizations with long cache expiry times.

Prefetching keeps cache entries alive by refreshing the data automatically as the cache approaches expiry time, without any user interaction. A scheduled job looks for cache entries with prefetch enabled where the entry is due to expire in the next 30 minutes. The job collects all such records and queues them to be refreshed. After refreshing, the expiry time is reset. This scheduled job runs every 15 minutes, so that the table cleaner will not delete a valid cache entry that has not yet been processed.

## Prefetch settings and defaults

Prefetching is activated by default with settings chosen to balance minimizing system load with maximizing value to the user. An admin can change these values, but should do so with great caution and only for pressing reasons.

|Property|Setting|Value|Notes|
|--------|-------|-----|-----|
|glide.analytics.cache.prefetch.min\_age\_in\_seconds|Lower limit of cache expiration time \[cacheExpirationTime\] for data to be subject to prefetching|8 hours|Eight hours is the minimum safe lifespan of cached data for it to be prefetched. You may need to increase this value but should not decrease it.|
|glide.analytics.cache.prefetch.max\_refresh\_counter|Number of consecutive times data is prefetched without a cache hit before prefetching stops for this data|10|Prefetching is meant for frequently used data. In order to reduce system load, if data is prefetched 10 times in a row without a user looking at the data, prefetching ceases. The data then follows default cache behavior and will reload when next viewed. The default value was selected to cover weekends. You may need to decrease this value but should not increase it.|

**Parent Topic:**[Platform Analytics experience reference](platform-analytics-exp-reference.md)

