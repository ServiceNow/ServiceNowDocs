---
title: Mobile list screen filters
description: Use mobile filters in list screens to enable your users to find what they need in your instance's records.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [List screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Mobile list screen filters

Use mobile filters in list screens to enable your users to find what they need in your instance's records.

Choose one of the following options when configuring your mobile list screens:

## Default filters

By default, the instance automatically creates a filter and sorting functionality. This filter is based on the fields selected in your list pattern. No further configuration is needed. Users can filter and sort the list based on any of these fields.

## Custom filters

If the default filters do not fit your requirements, consider creating a customer filter experience for your users. You can manually select the fields available to the list filter, as well as enable keyword filtering. Custom filters can include fields that are not in the list pattern. For more details on creating custom filters, see [Configure a custom filter](../task/config-mobile-list-filter.md).

**Note:** For those who have upgraded to the Rome release, consider the following:

-   If you did not define filters and are using the default setup, you automatically use the default filters and sorting capabilities after the upgrade.
-   If you defined filters in earlier versions, then after the upgrade your defined filters are still available. However, you must manually configure the sorting capabilities. See, [Configure sorting capabilities within mobile filters](../task/list-filter-sorting.md).

## Disabling filters

To disable filters and sorting on list screens, open the list screen record in Mobile App Builder and disable the **Hide filters** option. When filtering is turned off, users are unable to filter or sort records.

![List screen record in Mobile App Builder.](../image/mab-disable-filters.png)

