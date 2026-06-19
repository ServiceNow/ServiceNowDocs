---
title: Associate input form attachments to the activity stream in offline
description: Attachments added through input forms aren't displayed in the record activity stream by default, when working offline. Configure the write-back action step to associate attachments with the activity stream, so they appear immediately alongside other record updates.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/mobile-platform/input-form-attach-activity-stream.html
release: australia
product: Mobile Platform
classification: mobile-platform
topic_type: concept
last_updated: "2026-06-01"
reading_time_minutes: 1
breadcrumb: [Input forms in offline, Offline mode setup options, Offline mode, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Associate input form attachments to the activity stream in offline

Attachments added through input forms aren't displayed in the record activity stream by default, when working offline. Configure the write-back action step to associate attachments with the activity stream, so they appear immediately alongside other record updates.

Input forms create and update records, while inheriting the context of the record from which they are opened. When working offline, form changes and attachments are stored locally and queued in the Outbox, then synced automatically once connectivity is restored. By default, attachments added offline aren't shown in the record activity stream while the user is offline.

To display attachments immediately in the activity stream, configure the write-back-action step field **Associate attachments to current record** to include any relevant attachment inputs in the input form. This verifies that attachments added offline are also reflected in the record’s activity stream. This configuration is applicable when the offline step is set to apply to offline only or both offline and online.

**Parent Topic:**[Input forms in offline](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/offline-input-form.md)

