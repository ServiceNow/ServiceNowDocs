---
title: Yokohama Patch 5 Hotfix 1
description: The Yokohama Patch 5 Hotfix 1 release contains fixes to these problems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/release-notes/yokohama-patch-5-hf-1-PO.html
release: yokohama
topic_type: reference
last_updated: "2025-07-04"
reading_time_minutes: 1
breadcrumb: [Available patches and hotfixes, Learn about the Yokohama release, Yokohama release notes]
---

# Yokohama Patch 5 Hotfix 1

The Yokohama Patch 5 Hotfix 1 release contains fixes to these problems.

-   **Build information:**

    Build date: 07-01-2025\_0630

    Build tag: glide-yokohama-12-18-2024\_\_patch5-hotfix1-06-30-2025


**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

## Fixed problem

<table id="all-other-fixes"><thead><tr><th>

Problem

</th><th>

Short description

</th><th>

Description

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

Asynchronous Message Bus \(AMB\)

 PRB1910946

</td><td>

The Record Watcher \(RW\) Asynchronous Message Bus \(AMB\) message censor doesn't work when AMB lazy load is disabled

</td><td>

When glide.amb.message. lazy.load is set to 'false', having a record open in two browsers and updating it in one doesn't update it in the other browser.

</td><td>

1.  Set glide.amb.message. lazy.load to 'false'.
2.  Open a record in two different browsers.
3.  Update the record in one browser.

 Notice that the **Record** field in the other browser window isn't updated.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Yokohama Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-5.md)
-   [Yokohama Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-4.md)
-   [Yokohama Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-3.md)
-   [Yokohama Patch 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-2.md)
-   [Yokohama Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-1.md)
-   [Yokohama security and notable fixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-security-notables.md)
-   [All other Yokohama fixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/available-versions.md)

