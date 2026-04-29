---
title: Granular admin roles for Logging tables
description: Granular admin roles replace broad admin access with targeted, feature-specific permissions. Use these roles to grant the administrative capabilities needed for specific tasks without assigning the admin role.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Logs, Platform Security]
---

# Granular admin roles for Logging tables

Granular admin roles replace broad admin access with targeted, feature-specific permissions. Use these roles to grant the administrative capabilities needed for specific tasks without assigning the admin role.

|Role name|Feature|Plugin|Description|
|---------|-------|------|-----------|
|syslog\_viewer|System Logs \(Log Entry\)|com.snc.system\_security|Provides read access to Log Entry \(syslog\) records.|
|syslog\_admin|System Logs \(Log Entry\)|com.snc.system\_security|Provides create/write access to Log Entry \(syslog\) records. The previous admin role ACL bindings on the syslog table are deleted and replaced with these new granular roles.|
|txn\_part\_metrics\_viewer|Transaction Part Metrics Logs|com.glide.transaction\_part\_metrics\_log|Provides read and report\_view access to the syslog\_transaction\_part\_metrics table.|
|txn\_part\_metrics\_admin|Transaction Part Metrics Logs|com.glide.transaction\_part\_metrics\_log|Provides create, write, and delete access to the syslog\_transaction\_part\_metrics table. The previous admin role ACL bindings on this table are deleted and replaced with these new granular roles. New ACLs for all five operations \(read, create, write, delete, report\_view\) are introduced, each gated by the appropriate new role.|

**Parent Topic:**[Logs](../../security/concept/logs.md)

