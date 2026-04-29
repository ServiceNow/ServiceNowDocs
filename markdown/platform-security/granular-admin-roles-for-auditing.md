---
title: Granular admin roles for Audit tables
description: Granular admin roles replace broad admin access with targeted, feature-specific permissions. Use these roles to grant the administrative capabilities needed for specific tasks without assigning the admin role.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Auditing]
---

# Granular admin roles for Audit tables

Granular admin roles replace broad admin access with targeted, feature-specific permissions. Use these roles to grant the administrative capabilities needed for specific tasks without assigning the admin role.

|Role name|Feature|Description|
|---------|-------|-----------|
|audit\_viewer|Audit, History and Journal|Provides read access to the sys\_audit, sys\_journal\_field, and sys\_history\_set tables.|
|audit\_admin|Audit, History and Journal|Provides write and delete access to sys\_audit. Manual record modifications should be avoided. For bulk deletions, use system jobs rather than direct deletion.|

