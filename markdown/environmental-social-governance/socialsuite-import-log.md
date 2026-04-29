---
title: Socialsuite import log
description: The Socialsuite import log table \(sn\_osm\_ma\_import\_log\) tracks material topic data imported from Socialsuite into your ServiceNow instance. When you sync material topics, the assessment data is first imported into this table before the system creates corresponding material topic records. The import log is read-only and automatically maintained by the system.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Operational Sustainability Management \(formerly ESG\) reference, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Socialsuite import log

The Socialsuite import log table \(sn\_osm\_ma\_import\_log\) tracks material topic data imported from Socialsuite into your ServiceNow instance. When you sync material topics, the assessment data is first imported into this table before the system creates corresponding material topic records. The import log is read-only and automatically maintained by the system.

|Field|Description|
|-----|-----------|
|Assessment name|Name of the materiality assessment from Socialsuite.|
|Topic name|Name of the material topic being imported.|
|Reporting period ID|Identifier for the reporting period associated with the assessment.|
|Sync status|Current status of the import process.|
|Data record|Reference to the material topic record created from the imported data.|
|Comments|Additional information or error messages about the import.|

**Parent Topic:**[Operational Sustainability Management \(formerly ESG\) reference](../concept/reference-data-esg.md)

