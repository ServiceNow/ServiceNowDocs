---
title: Remove a product from a multi-product release
description: Remove an included product from a multi-product release when the product is no longer part of the release plan.
locale: en-US
release: zurich
product: Digital Product Release
classification: digital-product-release
topic_type: task
last_updated: "2026-02-13"
reading_time_minutes: 1
keywords: [remove product from release, remove included product, cancel child release]
breadcrumb: [Manage releases for digital products and services, Use, Digital Product Release, IT Service Management]
---

# Remove a product from a multi-product release

Remove an included product from a multi-product release when the product is no longer part of the release plan.

## Before you begin

Role required: sn\_dpr\_model.release\_admin or sn\_dpr\_model.product\_manager

## About this task

You can only remove included products. The primary product can’t be removed. Products can be removed one at a time.

## Procedure

1.  Navigate to **Workspaces** &gt; **Digital Product Release Workspace**.

2.  Select the releases icon \(![Releases icon.](../image/dpr-icon-release.png)\).

3.  Select a release from the list to open.

4.  Select the **Products** tab.

5.  Select the product from the list that you want to remove.

    The primary product selection is turned off because it can’t be removed from the release.

6.  Select **Remove product** and confirm.


## Result

-   The product is removed from the product list on the dashboard. Its version will still be available for future use.
-   The child release for the removed product is cancelled and the cancellation reason is recorded on the release record.
-   All pending and in-progress phases and tasks within those phases on the product release are cancelled.
-   Policy mappings for the child release are marked inactive. Policy counts on the main release are recalculated to exclude the removed product.

**Parent Topic:**[Manage releases for digital products and services](dpr-manage-releases.md)

