---
title: Requirements for querying archive data
description: Confirm these requirements before working with archive data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/working-with-archive-data.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Live Archive, Explore, RaptorDB Professional, Extend ServiceNow AI Platform capabilities]
---

# Requirements for querying archive data

Confirm these requirements before working with archive data.

## Platform requirements

|Requirement|Details|
|-----------|-------|
|RaptorDB Professional V2|Live Archive requires RaptorDB Professional V2. Confirm your entitlement with your account representative before installation.|
|Live Archive installed|Live Archive must be installed on the instance. Archive tables don't exist until at least one archive rule has run after installation. For installation steps, see [Install Live Archive](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/install-data-archiving-plugin.md).|
|Archive rule configured and run|At least one archive rule must have run so that an archive table exists on the instance. An archive table is created the first time an archive rule moves records out of its corresponding live table. For archive rule setup, see [Create an archive rule in Data Management Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/dmc-create-archive-rule.md).|

## Access control requirements

Live Archive applies the same security controls to archived records as to live records. Access control lists, role-based access, and row-level security continue to apply. A user who can't see a record in the live table can't see it in the archive.

No separate ACL configuration is required for archive tables. Access granted on `incident` applies to `ar_incident`

.

