---
title: Xanadu Patch 3 Hotfix 1
description: The Xanadu Patch 3 Hotfix 1 release contains fixes to these problems.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-11-21"
reading_time_minutes: 1
breadcrumb: [Available patches and hotfixes, Learn about the Xanadu release, Xanadu release notes]
---

# Xanadu Patch 3 Hotfix 1

The Xanadu Patch 3 Hotfix 1 release contains fixes to these problems.

-   **Build information:**

    Build date: 11-19-2024\_1208

    Build tag: glide-xanadu-07-02-2024\_\_patch3-hotfix1-11-13-2024


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

Attachments to Records

 PRB1823698

 [KB1709552](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1709552)

</td><td>

Out Of Memory \(OOM\) caused by the misuse of BuffetedInputStream when creating attachments

</td><td>

Attachments created from previously prepared TMP files are read with BufferedInputStream and have an internal buffer of 512M.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1784967

 [KB1706117](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1706117)

</td><td>

A Null Pointer Exception \(NPE\) is thrown while invoking the getAvailableConnection

</td><td>

Failure to load the script's DB because the returned value of com.glide.db.pool .DBConnectionPool .getDBConnection\(int\) is null.

</td><td>

 

</td></tr><tr><td>

Health Log Analytics \(Family\)

 PRB1825365

</td><td>

Health Log Analytics breaks after upgrading to Xanadu

</td><td>

MID Server distribution is missing a bundled dependency \(mid-loom.jar\).

</td><td>

1.  Open an instance with the HLA app installed.
2.  Upgrade the instance to Xanadu.
3.  Provision Occultus and ElasticSearch.
4.  Create a Data Input.Associate the Data Input to a MID.
5.  Attempt to start the Data Input.

 Notice that there is a ClassNotFoundException on the Data Input form.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Xanadu Patch 3](xanadu-patch-3.md)
-   [Xanadu Patch 2 Hotfix 1](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1705551)
-   [Xanadu Patch 1 Hotfix 3](xanadu-patch-1-hf-3-PO.md)
-   [Xanadu Patch 2](xanadu-patch-2.md)
-   [Xanadu Patch 1](xanadu-patch-1.md)
-   [Xanadu security and notable fixes](xanadu-security-notables.md)
-   [All other Xanadu fixes](xanadu-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

