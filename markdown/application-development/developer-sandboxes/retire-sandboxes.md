---
title: Retire a sandbox
description: Retire sandboxes that are outdated or no longer needed to make room for new Developer Sandboxes in your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/developer-sandboxes/retire-sandboxes.html
release: brazil
product: Developer Sandboxes
classification: developer-sandboxes
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Administering, Developer Sandboxes, Developing your application, Building applications]
---

# Retire a sandbox

Retire sandboxes that are outdated or no longer needed to make room for new Developer Sandboxes in your instance.

## Before you begin

Save your work, for example commit it to source control or export update sets. For more information, see [Update sets transfer between sandboxes and base instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/developer-sandboxes/dsb-update-sets.md).

Role required: admin or sandbox\_manager

## About this task

You should manually retire sandboxes when your work is complete to maintain a healthy development lifecycle.

**Warning:** Because sandboxes are retired automatically after an upgrade or clone, ensure any work that you want to keep is preserved before upgrading or cloning.

-   For upgrades, you can restore work from the remote update sets that Developer Sandboxes automatically created from prior sandboxes.
-   For clones, you must manually save and restore all work in sandboxes.
-   Any custom table configuration changes or fixes must be reapplied after an upgrade. Contact Now Support to open a case.

## Procedure

1.  Navigate to **All** &gt; **Sandbox Management** &gt; **Sandbox Management Home**.

2.  Select the more options icon \[Omitted image "sn-studio-more-options-icon.png"\]in the Developer Sandboxes dashboard, and then select **Retire sandbox**.

    \[Omitted image "dev-sbx-retire-home-2.png"\] Alt text: Select to Retire sandbox

3.  Confirm the retirement by selecting **Retire**.


## Result

After it's retired, the sandbox is no longer available for use. However, you can allocate new sandboxes as needed. For more information, see [Allocate a sandbox](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/developer-sandboxes/allocating-sandboxes.md).

The update set sources associated with the sandbox are automatically removed during retirement. The source on the base instance pointing to the sandbox is deleted, and the source on the sandbox is dropped along with the rest of the sandbox data. No manual cleanup is needed.

