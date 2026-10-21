---
title: Live Archive
description: Live Archive moves records and attachments from primary tables to object storage, freeing primary storage while keeping the data queryable in the same way as live data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/live-archive.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Explore, RaptorDB Professional, Extend ServiceNow AI Platform capabilities]
---

# Live Archive

Live Archive moves records and attachments from primary tables to object storage, freeing primary storage while keeping the data queryable in the same way as live data.

Live Archive reuses your existing archive rules, so no rule changes or rule migration are required. When records match the conditions in an archive rule, Live Archive moves those records and their attachments out of primary tables. The data is stored in object storage in a compressed columnar format. Archived records remain searchable and queryable on the ServiceNow AI Platform, so historical data stays available for reporting and conformance.

Live Archive applies the same security controls to archived records as to live records. Access control lists, role-based access, and row-level security continue to apply, and object storage data is encrypted at rest and in transit without additional configuration.

**Note:** Live Archive and backup serve different purposes and are configured independently. Live Archive does not replace backup and recovery procedures.

## Where to go next

For instructions on installing and configuring Live Archive, see [Install Live Archive](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/install-data-archiving-plugin.md).

