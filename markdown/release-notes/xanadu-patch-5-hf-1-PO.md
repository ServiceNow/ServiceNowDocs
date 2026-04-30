---
title: Xanadu Patch 5 Hotfix 1
description: The Xanadu Patch 5 Hotfix 1 release contains fixes to these problems.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2025-01-29"
reading_time_minutes: 1
breadcrumb: [Available patches and hotfixes, Learn about the Xanadu release, Xanadu release notes]
---

# Xanadu Patch 5 Hotfix 1

The Xanadu Patch 5 Hotfix 1 release contains fixes to these problems.

-   **Build information:**

    Build date: 01-24-2025\_0005

    Build tag: glide-xanadu-07-02-2024\_\_patch5-hotfix1-01-21-2025


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

Antivirus Scanning

 PRB1835660

</td><td>

The antivirus job updates all columns instead of only the 'State' column

</td><td>

The antivirus job updates all columns in some scenarios. It should only update the state column when attachment.setState\(advice\) is called. However a forceUpdate is occurs, which ultimately updates the entire row, including the state data. Additionally, when the old table name and table sys\_id are updated, the attached file is moved to the previous table.

</td><td>

1.  Log in to a Washington DC instance.
2.  Navigate to **All** &gt; **Self service** &gt; **Service catalog** &gt; **Select Mobiles** &gt; **Add to cart**.
3.  Upload a 10MB file.
4.  Select **Order now**.
5.  Navigate to sys\_attachment.list.

 Expected behavior: The table name should be sc\_req\_item on the available 'State'.

 Actual behavior: The antivirus job updates all columns instead of only the 'State' column.

</td></tr><tr><td>

Stream Connect Core

 PRB1845639

</td><td>

Kafka Consumer stops consuming messages once it receives a 'null' message from Producer

</td><td>

When a 'null' message error is observed from the source, the Kafka stream no longer consumes the messages.

</td><td>

 

</td></tr></tbody>
</table>## Fixes included

-   [Xanadu Patch 5](xanadu-patch-5.md)
-   [Xanadu Patch 4](xanadu-patch-4.md)
-   [Xanadu Patch 3](xanadu-patch-3.md)
-   [Xanadu Patch 2](xanadu-patch-2.md)
-   [Xanadu Patch 1](xanadu-patch-1.md)
-   [Xanadu security and notable fixes](xanadu-security-notables.md)
-   [All other Xanadu fixes](xanadu-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

