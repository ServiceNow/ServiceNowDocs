---
title: Log history
description: The system uses table rotation and table extension to archive older logs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/r\_LogHistory.html
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [System logs, Logs, Platform Security]
---

# Log history

The system uses table rotation and table extension to archive older logs.

By default, the system uses the following schedule to archive common logs:

|Table|Archive schedule|Rotations|Type|
|-----|----------------|---------|----|
|Event \[ecc\_event\]|Every day|7|Rotation|
|Queue \[ecc\_queue\]|Every day|7|Rotation|
|Event \[sysevent\]|Every day|7|Rotation|
|Log \[syslog\]|Every week|8|Rotation|
|Transaction Log \[syslog\_transaction\]|Every week|8|Rotation|

**Note:** The Email \[sys\_email\] table is not managed using table rotation or extension. Instead, use the [Email retention](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/email-retention.md) plugin to archive and destroy email records. By default, email records are archived after one year and destroyed after an additional year in the archive.

