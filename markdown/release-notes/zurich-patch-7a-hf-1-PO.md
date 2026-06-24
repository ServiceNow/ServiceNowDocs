---
title: Zurich Patch 7a Hotfix 1
description: The Zurich Patch 7a Hotfix 1 release contains fixes to these problems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/release-notes/zurich-patch-7a-hf-1-PO.html
release: zurich
topic_type: reference
last_updated: "2026-04-29"
reading_time_minutes: 2
breadcrumb: [Available patches and hotfixes, Learn about the Zurich release, Zurich release notes]
---

# Zurich Patch 7a Hotfix 1

The Zurich Patch 7a Hotfix 1 release contains fixes to these problems.

-   **Build information:**

    Build date: 04-23-2026\_1103

    Build tag: glide-zurich-07-01-2025\_\_patch7a-hotfix1-04-21-2026


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

Now Assist in AI Search

 PRB1920760

</td><td>

GenAI log IDs are not returned for Now Assist Genius Results

</td><td>

This issue occurs in Virtual Agent, portal, Now Assist Actions, Now Assist Q&amp;A, Synthesized Response, or anywhere a Now Assist Genius Result \(GR\) can be returned. Feedback is not logged even though there should be a value after the user selects the **Thumbs up** icon or **Thumbs down** icon on the Genius Result \(GR\).

</td><td>

1.  Open Virtual Agent.
2.  Perform a search that returns at least one Now Assist Genius Result \(GR\).
3.  Select the **Thumbs up** icon or the **Thumbs down** icon on the GR.
4.  Run the background job to process queued signals.
5.  Open the sys\_generative\_ai\_log table.
6.  Inspect the **Feedback** field for the transactions relevant to the Genius Result the user provided feedback on.

 Expected behavior: There should be a value such as 'Rejected' for negative feedback or 'Accepted' for positive feedback.

 Actual behavior: The feedback is not logged.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Zurich Patch 7a](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2935961)
-   [Zurich Patch 6](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-6.md)
-   [Zurich Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-5.md)
-   [Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)
-   [Zurich Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-3.md)
-   [Zurich Patch 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-2.md)
-   [Zurich Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-1.md)
-   [Zurich security and notable fixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-security-notables.md)
-   [All other Zurich fixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/available-versions.md)

