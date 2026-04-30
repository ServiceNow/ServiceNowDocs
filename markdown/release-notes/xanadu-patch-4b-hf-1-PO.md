---
title: Xanadu Patch 4b Hotfix 1
description: The Xanadu Patch 4b Hotfix 1 release contains fixes to these problems.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2025-02-27"
reading_time_minutes: 1
breadcrumb: [Available patches and hotfixes, Learn about the Xanadu release, Xanadu release notes]
---

# Xanadu Patch 4b Hotfix 1

The Xanadu Patch 4b Hotfix 1 release contains fixes to these problems.

-   **Build information:**

    Build date: 02-23-2025\_2130

    Build tag: glide-xanadu-07-02-2024\_\_patch4b-hotfix1-02-20-2025


**Important:** For more information about how to upgrade an instance, see [ServiceNow Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0547244).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0743854&_ga=2.238511747.200430442.1684856845-2052949275.1611611591).

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

Workflow Contexts

 PRB1820829

</td><td>

A fix causes a query to be executed when module access is requested

</td><td>

A SQL query against sys\_kmf\_crypto\_module is run whenever access to a module is checked with CallerPolicyAccessManager .isModuleAccessible. For a field with a Column Level Encryption \(CLE\) configuration, this API is called one or more times for each canRead\|canWrite\|canCreate call that is made. When canRead is called multiple times for each form load, the query is run many times when loading a single record.

</td><td>

 

</td></tr></tbody>
</table>## Fixes included

-   [Xanadu Patch 4b](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1915138)
-   [Xanadu Patch 4](xanadu-patch-4.md)
-   [Xanadu Patch 3](xanadu-patch-3.md)
-   [Xanadu Patch 2](xanadu-patch-2.md)
-   [Xanadu Patch 1](xanadu-patch-1.md)
-   [Xanadu security and notable fixes](xanadu-security-notables.md)
-   [All other Xanadu fixes](xanadu-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

