---
title: Australia Patch 6 W40 Hotfix 1
description: The Australia Patch 6 W40 Hotfix 1 release contains fixes to these problems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/release-notes/australia-patch-6-W40-hf-1-PO.html
release: australia
topic_type: reference
last_updated: "2026-10-09"
reading_time_minutes: 2
breadcrumb: [Available patches and hotfixes, Learn about the Australia release, Australia release notes]
---

# Australia Patch 6 W40 Hotfix 1

The Australia Patch 6 W40 Hotfix 1 release contains fixes to these problems.

-   **Build information:**

    Build date: 10-06-2026\_1730

    Build tag: glide-australia-02-11-2026\_\_patch6w40-hotfix1-10-05-2026


**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/upgrade.md).

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

AI Search \(Glide\)

 PRB2095865

</td><td>

AIS deleteSingleRecord's unconditional attachment deleteByQuery blocks the event processor, causing queue backlog and auto-shutoff

</td><td>

AIS indexing was auto-paused because the update event queue backlog grew past 1M due to IngestService.deleteSingleRecord stalling the AIS event processor. During this pause window, updated cases and records were not searchable until the backlog drained and indexing resumed.

</td><td>

1.  Open an instance with AIS/glide-ais.
2.  Configure a datasource/table pair where AIS responds slowly to deleteByQuery \(for example, a very large index or 100M+ docs\) or is intermittently unavailable, which triggers the exponential backoff retry path.
3.  Trigger a sustained burst of record deletes on that table via a retention/cleanup policy's bulk delete, or a scripted bulk delete through the normal GlideRecord delete path, so business rules/listeners fire normally.

 Observe that each deleted record produces one AIS delete event; the AIS event processor calls IngestService.deleteSingleRecord once per event, which unconditionally calls deleteAttachmentDocumentsByQuery to InternalContentIngestionApi.deleteByQuery. This runs synchronously and blocks the event-processing thread on the AIS network call \(and on retry backoff sleeps\) even when the deleted records have no attachments at all. If AIS is slow/unavailable long enough, the queueShouldNotBeWritable\(\) safeguard disables the update event queue \(glide.ais.update\_event\_queue\_writable=false\), and any record changes during the pause window are not reflected in Global Search until the queue is manually re-enabled and the backlog drains.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB2095766

</td><td>

KittyScopedEvaluator rejects the CMDB Search tokenized utterance, breaking the CI name search in the global search

</td><td>

An error occurs in the logs after attempting to search for a CI name in the Global Search box.

</td><td>

1.  Activate the deprecated CMDB Search plugin.
2.  After indexing, attempt to search for a CI name in the Global Search box, such as 'lnux100'.

 Observe that in the logs, an error occurs: 'ReferenceError: 'text\_search' is not defined' or 'Illegal use of while loop in sandbox scope'.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Australia Patch 6 W40](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3220853)
-   [Australia Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-5.md)
-   [Australia Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-4.md)
-   [Australia Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-3.md)
-   [Australia Patch 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-2.md)
-   [Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-1.md)
-   [Australia security and notable fixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-security-notables.md)
-   [All other Australia fixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/available-versions.md)

