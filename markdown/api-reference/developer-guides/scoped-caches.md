---
title: ScopedCacheManager API Developer Guide
description: Scoped caches allow customers to store custom data in memory for faster access, and define when it becomes invalidated. This can be useful when working with data takes longer to obtainthat from scratch, such as the results of a query across multiple tables. Use the ScopedCacheManager API to retrieve, set, and flush cache data for scoped applications.Create a scoped cache and define its cache pair.
locale: en-US
release: zurich
product: Developer Guides
classification: developer-guides
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Developer guides, API implementation and reference]
---

# ScopedCacheManager API Developer Guide

Scoped caches allow customers to store custom data in memory for faster access, and define when it becomes invalidated. This can be useful when working with data takes longer to obtainthat from scratch, such as the results of a query across multiple tables. Use the ScopedCacheManager API to retrieve, set, and flush cache data for scoped applications.

This guide includes instructions for creating a scoped cache and table pair to use with the [ScopedCacheManager API](../../../../app-store/dev_portal/API_reference/ScopedCacheManager/concept/ScopedCacheManagerAPI.md#).

You can assign the following types of table pairs to a scoped cache:

-   **Table pair cache**: When you need to perform any update operation in the table, all the entries in the cache are also flushed.
-   **Table row pair cache**: When you need to perform any update operation in the table, only the entries that have the same sys\_id as the edited record get flushed from the cache. The other entries remain the same.
-   **Table column pair cache**: When you edit a field in the list of selected columns, the entire cache is flushed.
-   **Table column and row pair cache**: When you edit a field in the list of selected columns, the entries that have the same sys\_id as the edited record get flushed from the cache.

## Creating a scoped cache and table pair

Create a scoped cache and define its cache pair.

### Before you begin

Role required: admin

### Procedure

1.  Create a scoped cache. Go to **All** &gt; **System Definition** &gt; **Scoped Caches**.

2.  Click **New** and enter a meaningful name in the **Cache Name** field.

3.  Enter a number in the **Max Entries** field. This value represents the maximum number of entries allowed for this cache. The maximum value is 100.

    **Note:** The **Application** field should automatically include the name of the scoped application for which this cache is being created.

4.  Make sure the **Active** check box is selected.

5.  Check the **Always Compress** check box if you want the scoped cache values to occupy less memory space by compressing it.

6.  Click **Submit**.

    The scoped cache has been created.

7.  Create a cache pair. Go to **All** &gt; **System Definition** &gt; **Scoped Cache Pairs**.

8.  Click **New** and click the magnifying glass to select a cache in the **Scoped Cache** field.

9.  Select a table from the **Table** menu.

10. Select an option from the **Pair type** menu.

    -   **Table pair cache**: When you need to perform any update operation in the table, all the entries in the cache are also flushed.
    -   **Table row pair cache**: When you need to perform any update operation in the table, only the entries that have the same sys\_id as the edited record get flushed from the cache. The other entries remain the same.
    -   **Table column pair cache**: When you edit a field in the list of selected columns, the entire cache is flushed.
    -   **Table column and row pair cache**: When you edit a field in the list of selected columns, the entries that have the same sys\_id as the edited record get flushed from the cache.
11. Click **Submit**.

    The scoped cache table pair has been created and is ready to use with the ScopedCacheManager API.


