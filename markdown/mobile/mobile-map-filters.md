---
title: Mobile map screen filters
description: Use mobile filters in map screens to enable your users to find what they need in the records on your instance.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Map screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Mobile map screen filters

Use mobile filters in map screens to enable your users to find what they need in the records on your instance.

Choose one of the following options when configuring your mobile map screens:

## Default filters

By default, the instance automatically creates a filter and sorting functionality. This filter is based on the fields selected in your map pattern. No further configuration is needed Users can filter and sort the list based on any of these fields.

## Custom filters

If the default filters do not fit your requirements, consider creating a customer filter experience for your users. You can manually select the fields available to the map filter, as well as enable keyword filtering. Custom filters can include fields that are not in the map pattern. For more details on creating custom filters, see [Configure a custom filter](../task/config-mobile-list-filter.md).

**Note:** For those who have upgraded to the Rome release, consider the following:

-   If you did not define filters and are using the default setup, you automatically use the default filters and sorting capabilities after the upgrade.
-   If you defined filters in earlier versions, then after the upgrade your defined filters are still available. However, you must manually configure the sorting capabilities. See, [Configure sorting capabilities within mobile filters](../task/list-filter-sorting.md).

## Disable filters

To disable filters and sorting on map screen, open the map screen record, click the **Filter** tab, and disable the **Show or hide filters for this list screen** option. When filtering is turned off, users are unable to filter or sort records.

