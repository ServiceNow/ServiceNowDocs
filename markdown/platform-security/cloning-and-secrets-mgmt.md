---
title: Cloning and Secrets Management
description: Learn how to reconfigure secrets groups and client secrets groups after a clone.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring client accessible secrets, Secrets Management, Platform Security]
---

# Cloning and Secrets Management

Learn how to reconfigure secrets groups and client secrets groups after a clone.

After you clone an instance, your secrets groups and client secrets groups may require reconfiguration to operate as expected.

|Secrets group origin|Behavior after a clone|
|--------------------|----------------------|
|Original instance secrets groups from the target instance|Works as expected after manually importing the missing cryptographic module. See [Exporting and importing data via XML](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/c_ExportAndImportXMLFiles.md).|
|Original client secrets groups from target instance|Works as expected after manually importing the missing cryptographic module. See [Exporting and importing data via XML](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/c_ExportAndImportXMLFiles.md).|
|Cloned instance secrets groups from source instance|Doesn’t work unless manually set up|
|Cloned client secrets groups from source instance|Work if manually config sg/identity group/alias/mid|

**Parent Topic:**[Configuring client accessible secrets](../concept/client-access-secret-landing.md)

