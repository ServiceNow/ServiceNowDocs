---
title: Retire Developer Sandboxes
description: Retire sandboxes that are outdated or no longer needed to make room for new sandboxes in your instance.
locale: en-US
release: zurich
product: Developer Sandboxes
classification: developer-sandboxes
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Allocating and retiring, Developer Sandboxes, Developing your application, Building applications]
---

# Retire Developer Sandboxes

Retire sandboxes that are outdated or no longer needed to make room for new sandboxes in your instance.

## About this task

You should manually retire sandboxes when your work is complete to maintain a healthy lifecycle.

**Note:** Because sandboxes are retired automatically after an upgrade or clone, you should ensure any work that you want to keep is preserved before upgrading. However, if you are on Zurich Patch 5 or later, update sets on the instance may be automatically backed up.For more information, see [Cloning and upgrading considerations for Developer Sandboxes](../concept/dev-sbx-clone-upgrade-info.md).

## Before you begin

Commit any changes if you're using source control.

Role required: admin or delegated developer

## Procedure

1.  Navigate to **All** &gt; **Sandbox Management** &gt; **Sandbox Management Home**.

2.  Select the More options icon in the Developer Sandboxes dashboard, and then select **Retire sandbox**.

    ![Select to Retire sandbox](../image/dev-sbx-retire-home-2.png "Retire a sandbox")

3.  Confirm the retirement by selecting **Retire**.


## Result

After it's retired, the sandbox is no longer available for use. However, you can allocate new sandboxes as needed. For more information, see [Allocate a sandbox](allocating-sandboxes.md).

