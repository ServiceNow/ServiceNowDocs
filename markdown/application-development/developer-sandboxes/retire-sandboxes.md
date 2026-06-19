---
title: Retire Developer Sandboxes
description: Retire sandboxes that are outdated or no longer needed to make room for new sandboxes in your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/developer-sandboxes/retire-sandboxes.html
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

**Warning:** Because sandboxes are retired automatically after an upgrade or clone, ensure any work that you want to keep is preserved before upgrading. You must manually recreate sandboxes after an upgrade or clone.

-   For Zurich Patch 5 or later, uncommitted work in existing sandboxes is automatically exported as remote update sets on the base instance, which you must commit to sandboxes created after the upgrade.
-   For clones, you must manually save and restore all work in sandboxes.
-   Any custom table configuration changes or fixes must be reapplied after an upgrade. Contact Now Support to open a case.

For more information, see [Cloning and upgrading considerations for Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/developer-sandboxes/dev-sbx-clone-upgrade-info.md).

## Before you begin

Commit any changes if you're using source control.

Role required: admin or delegated developer

## Procedure

1.  Navigate to **All** &gt; **Sandbox Management** &gt; **Sandbox Management Home**.

2.  Select the More options icon in the Developer Sandboxes dashboard, and then select **Retire sandbox**.

    \[Omitted image "dev-sbx-retire-home-2.png"\] Alt text: Select to Retire sandbox

3.  Confirm the retirement by selecting **Retire**.


## Result

After it's retired, the sandbox is no longer available for use. However, you can allocate new sandboxes as needed. For more information, see [Allocate a sandbox](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/developer-sandboxes/allocating-sandboxes.md).

