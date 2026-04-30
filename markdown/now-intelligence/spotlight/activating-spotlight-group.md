---
title: Schedule Item \[sys\_trigger\] records for Spotlight
description: Setting a Spotlight group to Active creates a Schedule Item \[sys\_trigger\] record. As an administrator, access this record to troubleshoot scheduling. This record contains the scheduling information that is set on the Spotlight group.
locale: en-US
release: zurich
product: Spotlight
classification: spotlight
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Administering Spotlight, Ranking records with Spotlight, Configure advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Schedule Item \[sys\_trigger\] records for Spotlight

Setting a Spotlight group to Active creates a Schedule Item \[sys\_trigger\] record. As an administrator, access this record to troubleshoot scheduling. This record contains the scheduling information that is set on the Spotlight group.

Editing the schedule in the Spotlight group record replaces the Schedule Item \[sys\_trigger\] record with a new one. Deactivating or deleting the Spotlight group deletes the Schedule Item record. If you reactivate the Spotlight group, you create a new Schedule Item record.

**Note:** As an administrator, you can access the Schedule Item \[sys\_trigger\] record for a Spotlight group by clicking **Show Scheduler** on the Spotlight Group form.

The process of creating, editing, and deleting Schedule Item \[sys\_trigger\] records uses business rules as follows:

|Action|Business rule|Effect on Schedule Item record|
|------|-------------|------------------------------|
|Activating a Spotlight group|Create Schedule Item \[sys\_trigger\] record|A new Schedule Item \[sys\_trigger\] record is created with the scheduling information.|
|Editing a schedule in a Spotlight group record|Create Schedule Item \[sys\_trigger\] record|The existing Schedule Item \[sys\_trigger\] record is replaced with a new record, with the new scheduling information.|
|Deactivating a Spotlight group|Delete Schedule Item \[sys\_trigger\] record|The existing Schedule Item \[sys\_trigger\] record associated with that Spotlight group is deleted.|
|Reactivating a Spotlight group|Create Schedule Item \[sys\_trigger\] record|A new Schedule Item \[sys\_trigger\] record is created with the scheduling information.|
|Deleting a Spotlight group|Delete Schedule Item \[sys\_trigger\] record|The existing Schedule Item \[sys\_trigger\] record associated with that Spotlight group is deleted.|

**Parent Topic:**[Administering Spotlight](administering-spotlight.md)

