---
title: Zurich Patch 1 Hotfix 2
description: The Zurich Patch 1 Hotfix 2 release contains fixes to these problems.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-10-16"
reading_time_minutes: 1
breadcrumb: [Available patches and hotfixes, Learn about the Zurich release, Zurich release notes]
---

# Zurich Patch 1 Hotfix 2

The Zurich Patch 1 Hotfix 2 release contains fixes to these problems.

-   **Build information:**

    Build date: 10-11-2025\_2320

    Build tag: glide-zurich-07-01-2025\_\_patch1-hotfix2-10-11-2025


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

OneExtend

 PRB1944861

</td><td>

Revert NASK licensing charge by token to not include input tokens

</td><td>

The assist charge logged in sys\_gen\_ai\_usage\_log is based on 1 assist per 1000 tokens, where tokens = input tokens + 3 \* output tokens.

</td><td>

Invoke the custom skill created in the NA Skill Kit.

 Observe that the assist charge logged in sys\_gen\_ai\_usage\_log is based on 1 assist per 1000 tokens, where tokens = input tokens + 3 \* output tokens.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Zurich Patch 1 Hotfix 1](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2524158)
-   [Zurich security and notable fixes](zurich-security-notables.md)
-   [All other Zurich fixes](zurich-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

