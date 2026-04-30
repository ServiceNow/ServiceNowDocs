---
title: Log history
description: The system uses table rotation and table extension to archive older logs.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
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
|Email \[sys\_email\]|Every 30 days|8|Extension|

