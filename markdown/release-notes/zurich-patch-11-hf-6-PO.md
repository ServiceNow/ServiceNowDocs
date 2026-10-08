---
title: Zurich Patch 11 Hotfix 6
description: The Zurich Patch 11 Hotfix 6 release contains fixes to these problems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/release-notes/zurich-patch-11-hf-6-PO.html
release: zurich
topic_type: reference
last_updated: "2026-09-17"
reading_time_minutes: 2
breadcrumb: [Available patches and hotfixes, Learn about the Zurich release, Zurich release notes]
---

# Zurich Patch 11 Hotfix 6

The Zurich Patch 11 Hotfix 6 release contains fixes to these problems.

-   **Build information:**

    Build date: 09-14-2026\_1101

    Build tag: glide-zurich-07-01-2025\_\_patch11-hotfix6-09-10-2026


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

Service Catalog Variables

 PRB2072938

</td><td>

The 'Lists and Platform Analytics' visualization shows encrypted responses for record producer variables

</td><td>

The variables in the incident list view should show decrypted values. The issue occurs because the form and the list view retrieve the variable's value in two different ways.

</td><td>

1.  Create an encrypted field configuration on the question\_answer table and **Value** field.
2.  Define a module access policy based on the crypto module of type 'Role'.
3.  Set the target role as snc\_internal and the result as track.
4.  Create a record producer on the incident with one variable.
5.  Create an incident via the record producer.
6.  Add the record producer variable to the incident list view.
7.  Load incident.list.

 Expected behavior: The variables in the list view show decrypted values.

 Actual behavior: The variables in the list view show encrypted values.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Zurich Patch 11 Hotfix 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-11-hf-5-PO.md)
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

