---
title: Alert tags
description: Alert tags allow consolidation for all normalized fields and improve the admin experience to transform and normalize alert fields \(key/value\)​ enabling reuse of normalized fields across different sources.​ This improves alert quality for correlation and provides more out-of-the-box TBAC \(Tag Based Automatic Correlation\) definitions​.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Processing Events, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Alert tags

Alert tags allow consolidation for all normalized fields and improve the admin experience to transform and normalize alert fields \(key/value\)​ enabling reuse of normalized fields across different sources.​ This improves alert quality for correlation and provides more out-of-the-box TBAC \(Tag Based Automatic Correlation\) definitions​.

## Example: Field normalization in alert management

In some cases, the same information may exist under different field names across data sources. For instance, an incoming event from one source has the location stored under the field **region**, but in other source, the same information is captured under **impacted\_region**. To avoid confusion and enable consistent grouping, filtering, or automation, we normalize these fields by creating a unified field — for example,**t\_region**. This field pulls the value from **region** or from **impacted\_region** depending what field is present in the event. This way, the normalized field **t\_region** always holds the location value in a consistent manner, regardless of the original source field.

Alert tags field appears in the Alerts form. These tags are created by Event Rules and in Event mapping and are saved in the alert tags' table \[em\_alert\_tags\]. The naming convention used to create key/value pairs is t\_&lt;tag name&gt;.​ This enables reusing tags in the event rules by allowing users to select tags that were previously defined.​ When new alert tags are defined, TBAC \(Tag Based Alert Clustering\) tags are automatically created.​ Using these TBAC tags, you can create new TBAC alert clustering definitions from the new source of tags​.

