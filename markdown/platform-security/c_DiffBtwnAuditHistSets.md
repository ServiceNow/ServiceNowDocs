---
title: Differences Between Audit and History Sets
description: The Audit \[sys\_audit\], History Sets \[sys\_history\_set\], and History \[sys\_history\_line\] tables store the same data, but they serve different purposes and manage data differently.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Knowing about History sets, Auditing, Platform Security]
---

# Differences Between Audit and History Sets

The Audit \[sys\_audit\], History Sets \[sys\_history\_set\], and History \[sys\_history\_line\] tables store the same data, but they serve different purposes and manage data differently.

## Audit \[sys\_audit\] table

The Audit \[sys\_audit\] table is where the system stores historical information for all records. These records are intended to be kept forever so that administrators can always track the history of audited records. As the number of auditing records grows over time, it becomes more inefficient to directly query the Audit table for historical information. It is much more efficient to run queries only on the smaller subset records you actually want to view historical information for.

## History Set \[sys\_history\_set\] table

The History Set \[sys\_history\_set\] table identifies which particular records from an audited table have historical information. The History \[sys\_history\_line\] table stores the actual changes to field values that occurred.

-   The system automatically generates History Set and History records as needed from the Audit table when a user either creates a record or requests its history.
-   Rather than containing a complete history of all changes in the system, History Set and History records only contain a recent subset of historical information for records where users have created or requested such information.
-   In addition to audit data, history sets also include the information that is set during record insert, including journal field entries. Journal field entries you create before creating a record are handled in the same manner as journal entries created at the time of record creation. These journal entries appear in history sets with the same creation time and created by data as the associated record itself.

The system limits History Set and History records by:

-   Having the table cleaner delete History Set records that have not been updated in 30 days.
-   Using table rotation to rotate between four History tables every seven days. The system drops History records that are older than 28 days.

Should someone need historical information again at a later date, the system can regenerate it from auditing source records.

After the system generates History Set records, the context menu choice **History** uses the History Set rather than Audit records. From the user's perspective, the same historical data is available in the same user interface, but the way the information is stored is different.

