---
title: Zurich Patch 11 Hotfix 4
description: The Zurich Patch 11 Hotfix 4 release contains fixes to these problems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/release-notes/zurich-patch-11-hf-4-PO.html
release: zurich
topic_type: reference
last_updated: "2026-08-13"
reading_time_minutes: 2
breadcrumb: [Available patches and hotfixes, Learn about the Zurich release, Zurich release notes]
---

# Zurich Patch 11 Hotfix 4

The Zurich Patch 11 Hotfix 4 release contains fixes to these problems.

-   **Build information:**

    Build date: 08-10-2026\_1957

    Build tag: glide-zurich-07-01-2025\_\_patch11-hotfix4-08-06-2026


**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/upgrade.md).

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

Flow Engine

 PRB1943894

</td><td>

Looping over records using 'built in iterator' is significantly slower than the normal GlideRecord iteration

</td><td>

Flow engine should take a similar amount of time to iterate over records and script or Java when no quiescing occurs, but run times are 16.8x - 73.6x slower.

</td><td>

 

</td></tr><tr><td>

Service Catalog

 PRB2040266

</td><td>

g\_form.clearValue should clear the value of the **Lookup select box**, even when there are no reference qualifiers

</td><td>

When loading the XML files, this creates **Lookup select boxes**. One file creates an item option named 'user\_group' under the 'AWS account request' catalog item, which is a is a **Lookup select box** that references the sys\_user\_group table and its reference qualifier is 'javascript: 'manager=' + current.variables.user'. Another file creates an item option named 'user' under the 'AWS account request' catalog item, which is a **Lookup select box** that references the sys\_user table. The next file is a catalog script for the 'AWS account request' catalog item, which logs the value of the **user\_group** field when there is a change to the **User** field.

</td><td>

1.  Load the XML files.

Notice that these XML files create a item options named 'user\_group' and 'user' under the 'AWS account request' catalog item, and that **Lookup select boxes** are created.

2.  Navigate to the catalog item.
3.  Change the **User** field to any value.

 Expected behavior: The **User Group** field should be cleared, and the alert should show an empty value.

 Actual behavior: The **User Group** field is cleared in the UI, but the alert shows the previous value.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Zurich Patch 11 Hotfix 3](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3146433)
-   [Zurich Patch 10](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-10.md)
-   [Zurich Patch 9](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-9.md)
-   [Zurich Patch 8](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-8.md)
-   [Zurich Patch 7](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-7.md)
-   [Zurich Patch 6](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-6.md)
-   [Zurich Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-5.md)
-   [Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)
-   [Zurich Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-3.md)
-   [Zurich Patch 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-2.md)
-   [Zurich Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-1.md)
-   [Zurich security and notable fixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-security-notables.md)
-   [All other Zurich fixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/available-versions.md)

