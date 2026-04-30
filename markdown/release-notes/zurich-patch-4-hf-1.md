---
title: Zurich Patch 4 Hotfix 1
description: The Zurich Patch 4 Hotfix 1 release contains fixes to these problems.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-12-23"
reading_time_minutes: 1
breadcrumb: [Available patches and hotfixes, Learn about the Zurich release, Zurich release notes]
---

# Zurich Patch 4 Hotfix 1

The Zurich Patch 4 Hotfix 1 release contains fixes to these problems.

-   **Build information:**

    Build date: 12-20-2025\_0947

    Build tag: glide-zurich-07-01-2025\_\_patch4-hotfix1-12-19-2025


**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](../upgrades/reference/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform® major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

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

Mobile Studio

 PRB1974465

</td><td>

Mobile AI Builder \(id = sn\_maib\) plugin oob\_apps/now-mobile-ai-builder.properties should have mode = optional to ensure it is not installed in base instance

</td><td>

Mobile AI Builder \(id = sn\_maib\) is installed as it is marked as mode = core in oob\_apps/now-mobile-ai-builder.properties.

</td><td>

 

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Zurich Patch 4](zurich-patch-4.md)
-   [Zurich Patch 3](zurich-patch-3.md)
-   [Zurich Patch 2](zurich-patch-2.md)
-   [Zurich Patch 1](zurich-patch-1.md)
-   [Zurich security and notable fixes](zurich-security-notables.md)
-   [All other Zurich fixes](zurich-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

