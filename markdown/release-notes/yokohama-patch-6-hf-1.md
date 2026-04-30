---
title: Yokohama Patch 6 Hotfix 1
description: The Yokohama Patch 6 Hotfix 1 release contains fixes to these problems.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-08-08"
reading_time_minutes: 3
breadcrumb: [Available patches and hotfixes, Learn about the Yokohama release, Yokohama release notes]
---

# Yokohama Patch 6 Hotfix 1

The Yokohama Patch 6 Hotfix 1 release contains fixes to these problems.

-   **Build information:**

    Build date: 08-05-2025\_2351

    Build tag: glide-yokohama-12-18-2024\_\_patch6-hotfix1-08-01-2025


**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](../upgrades/reference/upgrade.md).

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

Activity Stream

 PRB1923345

</td><td>

Activity Response Generation \(ARG\) updates for workspace are not included in Yokohama

</td><td>

ARG changes are missing in workspace.

</td><td>

1.  Set up Activity Response Generation.
2.  Enable the configuration.

</td></tr><tr><td>

Analytics Data API

 PRB1845187

 [KB2238953](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2238953)

</td><td>

Drilling down on KPIs in a Performance Analytics dashboard produces the error 'No internet connection'

</td><td>

Drilling down on any value redirects the user to the KPI details page with a 'No Internet connection' error.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Application Manager

 PRB1924202

 [KB2397128](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2397128)

</td><td>

'My Company Application' \($mycompany appsmgmt.do\) page isn't found

</td><td>

The 'My Company Application' page isn't found after upgrading Yokohama.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Cache

 PRB1922845

</td><td>

File handlers are left open if a LazyInputStream is closed before being read by LargeContentDiskCache

</td><td>

If LazyInput\#close is called before the internal StreamSupplier is opened by LazyInput Stream\#stream, the InputStream remains open until finalizers are calling during garbage collection. File handles are leaked when using LargeContent DiskCache and only call getMetadata\(\) or contentExists\(\). Because the supplier is never invoked and the stream is never opened, closing the LazyInputStream doesn't close the underlying FileInputStream. These leaked file handles are only released when the garbage collector runs finalizers.

</td><td>

1.  Start glide.
2.  Run java Process Status \(JPS\).
3.  Get the Process ID \(PID\) of the glide process.
4.  Run LSOF.
5.  Take note of the file descriptor entries.
6.  Flush the cache.
7.  Load the Service Operations Workspace home page.
8.  Repeat step 3 through step 6.

 Expected behavior: File descriptor entries is close to the original number.

 Actual behavior: Notice the 10's or 100's of additional file descriptor entries, indicating that the file handlers are left open.

</td></tr><tr><td>

UX Framework

 PRB1923311

</td><td>

UX dependency tracing should use LargeContentDiskCache. getMetadata to avoid file touching

</td><td>

File descriptors should not increase when there is a cache hit.

</td><td>

1.  Access a workspace homepage \(for example: CSM, SOW, or Case Record\).
2.  Re-load the page multiple times.
3.  Monitor open file descriptors for LSOF.
4.  Notice the file descriptor entries.

 Notice that the file descriptors increase even when there's a cache hit.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Yokohama Patch 6](yokohama-patch-6.md)
-   [Yokohama Patch 5](yokohama-patch-5.md)
-   [Yokohama Patch 4](yokohama-patch-4.md)
-   [Yokohama Patch 3](yokohama-patch-3.md)
-   [Yokohama Patch 2](yokohama-patch-2.md)
-   [Yokohama Patch 1](yokohama-patch-1.md)
-   [Yokohama security and notable fixes](yokohama-security-notables.md)
-   [All other Yokohama fixes](yokohama-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

