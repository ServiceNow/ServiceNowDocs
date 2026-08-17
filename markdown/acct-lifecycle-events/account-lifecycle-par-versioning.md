---
title: Product adoption roadmap versioning
description: Versioning preserves a snapshot of your roadmap each time you publish it, creating a complete history you can review or restore when plans change.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/acct-lifecycle-events/account-lifecycle-par-versioning.html
release: australia
topic_type: concept
last_updated: "2026-07-26"
reading_time_minutes: 2
keywords: [product adoption roadmap, versioning, roadmap history, version control]
breadcrumb: [View a product adoption roadmap, Product adoption, Customer success, Use, Customer Success Management]
---

# Product adoption roadmap versioning

Versioning preserves a snapshot of your roadmap each time you publish it, creating a complete history you can review or restore when plans change.

Product adoption roadmaps evolve over time as priorities shift and new products are introduced. Versioning lets you preserve a snapshot of the roadmap every time you publish it, giving you a complete history of how the adoption plan has changed. If you need to go back to an earlier plan, you can revert the roadmap to any previous published version without losing the current state permanently.

Publishing a roadmap creates a version record that stores a read-only snapshot of the roadmap header, lanes, and items at that point in time. Version records can't be copied or edited. You can update only the version label.

## How versioning works

Publishing a roadmap creates a new version record linked to that roadmap. The version record stores snapshots of the header, lanes, and items as JSON. When you revert to a previous version, the lanes and items are restored from that version's snapshots. The roadmap header state \(Draft or Published\) is not affected when you revert to a previous version.

The version label in the roadmap header reflects the most recently published version and updates whenever you publish a new version.

## Version record fields

A version record includes the following fields:

-   Version: Identifies the version of the roadmap. By default, the first version has the format **1.0 &lt;roadmap name&gt;**. Every time a new version is published, the version increments \(1.0, 1.1, 1.2, and so on\). You can edit the label to use a custom name suitable for your engagement.
-   Roadmap: The product adoption roadmap that this version belongs to.
-   Previous version: The previous version of the roadmap. This field links versions together so you can track the complete history of roadmap changes.
-   PAR snapshot: A read-only JSON snapshot of the roadmap header at the time of publishing.
-   Lane snapshot: A read-only JSON snapshot of the lane configuration at the time of publishing, including the name and details of each lane.
-   Item snapshot: A read-only JSON snapshot of all items within the lanes at the time of publishing.

**Note:** Snapshots store the complete roadmap state as JSON. A visual comparison between versions is not available in this release.

## View version history

The current version label is displayed in the roadmap header. To view all versions for a roadmap, open the roadmap record and scroll to the **Versions** related list. The list displays all published versions in chronological order.

To restore a roadmap to an earlier state, see [Revert a product adoption roadmap to a previous version](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-revert-par-roadmap.md).

**Parent Topic:**[View a product adoption roadmap](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-view-par-roadmap.md)

**Related topics**  


[Product adoption roadmap](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-par-roadmap.md)

[View a product adoption roadmap](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-view-par-roadmap.md)

[Revert a product adoption roadmap to a previous version](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-revert-par-roadmap.md)

[Create a product adoption roadmap](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-create-par-roadmap.md)

