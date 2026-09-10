---
title: Software filter tables
description: The following table lists the software filter tables and the purpose each one serves.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/agent-client-collector/sw-filter-tables.html
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2026-08-23"
reading_time_minutes: 1
breadcrumb: [ACC-VC reference, Agent Client Collector reference, Agent Client Collector, IT Operations Management]
---

# Software filter tables

The following table lists the software filter tables and the purpose each one serves.

|Table|Who edits it|Purpose|
|-----|------------|-------|
|Software Install Filter \(samp\_sw\_install\_filter\)|ServiceNow|Base-system rules maintained by ServiceNow that cover common, well-known filtered software across all customers. Read-only.|
|Software Install Custom Filter \(samp\_sw\_install\_custom\_filter\)|SAM admin|Where you create, edit, and manage your own organization-specific exclusion rules for internal tools, custom shortcuts, or anything the base-system rules don't cover.|
|Software Install Filter Staging \(samp\_sw\_install\_filter\_staging\)|System-generated|An audit log of every software install that has been excluded, which rule excluded it, and the last date it was reconfirmed as irrelevant. Use this table to review and validate what is being filtered. Read-only.|

**Parent Topic:**[Agent Client Collector for Visibility Content reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/agent-client-collector-for-visibility-references.md)

