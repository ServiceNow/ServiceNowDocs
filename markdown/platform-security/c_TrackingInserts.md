---
title: Tracking inserts
description: By default, the system does not create Audit records for inserts because in a typical instance, inserts can account for over 80% of the size of the Audit table.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Knowing about History sets, Auditing]
---

# Tracking inserts

By default, the system does not create Audit records for inserts because in a typical instance, inserts can account for over 80% of the size of the Audit table.

Not tracking inserts allows for better performance and a much smaller Audit table. Administrators can enable auditing of inserts by setting the **glide.sys.audit\_inserts** property to true.

