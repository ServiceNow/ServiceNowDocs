---
title: Live Archive with RaptorDB Professional V2
description: Live Archive \(formerly Data Archiving\) moves records and attachments to object storage, freeing up space in the primary database while keeping data accessible for compliance and reporting. This capability improves query performance and provides scalable storage for large archives.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-14"
reading_time_minutes: 3
breadcrumb: [Explore, Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Live Archive with RaptorDB Professional V2

Live Archive \(formerly Data Archiving\) moves records and attachments to object storage, freeing up space in the primary database while keeping data accessible for compliance and reporting. This capability improves query performance and provides scalable storage for large archives.

When you upgrade to RaptorDB Professional V2 and install Live Archive, you can migrate archived records and attachments from the primary instance to a dedicated object storage. The archived data remains accessible in the same way as regular tables. This capability is exclusive to RaptorDB Professional.

Object storage doesn't require additional configuration beyond plugin installation.

During the migration to object storage, data management processes that interact with archive tables are temporarily paused. However, no downtime is required for the upgrade itself. For more information about upgrading to RaptorDB Professional, contact your account representative.

## Key benefits

-   Moves data to object storage in a compressed columnar format, freeing up primary storage.
-   Improves query performance on active data by reducing the primary database size.
-   Reuses existing archive rules without requiring changes.
-   Retains closed records for compliance and audit purposes.
-   Provides scalable storage capacity for larger archives without impacting primary database performance.
-   Keeps archived data accessible and searchable to users on the ServiceNow AI Platform so historical data can be queried and reported on as needed.
-   Applies the same security controls, ACLs, and role-based access to archived records as to live records.
-   Enables you to monitor live and archive table volumes in the Data Management Console.

## Live Archive architecture

Live Archive extends the existing archive rules framework. When records match the archive rule conditions, they move from primary tables to archive tables.

-   **S3 facade**

    To keep archived data accessible even if a datacenter is unavailable, Live Archive uses an S3 facade, which is a communication layer between RaptorDB Professional and object storage. It handles authentication, routing, and resilience.

    Live Archive automatically creates two S3 facade endpoints, one per datacenter in your instance's datacenter pair. If one datacenter is unavailable, the other endpoint keeps the archived records remain accessible. The S3 facade is verified during Live Archive installation.

    ![Live Archive routes archived data through the S3 facade.](../image/s3-facade-data-archiving.png "Archiving with S3 facade")

-   **Archive rules**

    Use archive rules to define which records should be archived. Time-based conditions are common. For example, to archive incidents closed more than two years ago. However, any field-based condition is supported.

    Existing archive rules operate without changes or migration. For guidance on creating and managing archive rules, see [Create an archive rule in Core UI](../task/t_CreateAnArchiveRule.md#).

    When an archive rule runs, records and attachments move from live tables to archive tables through the S3 facade.

-   **Monitoring storage**

    Track object storage volume in the Data Management Console. Storage stats refresh once daily and reflect compressed sizes.

    Data appears in the console only after an archive table exceeds 512 MB or 2 million rows.

-   **Primary database space reclamation**

    As records move to object storage, RaptorDB reclaims space in the primary database.

    The primary database might not shrink immediately in absolute size, especially when new records continue to be created, but archiving slows primary database growth and reduces the volume of data processed on every query. The performance and operational benefits of archiving appear in faster query times and instance responsiveness.

-   **Security**

    Live Archive maintains all ServiceNow AI Platform security controls. ACLs, role-based access, and row-level security apply to archived records the same way as live records. Users without access to live records cannot access the corresponding archived records.

    Object storage data is encrypted at rest and in transit without requiring additional configuration.


To install Live Archive after upgrading to RaptorDB Professional V2, see [Install Live Archive](../../managing-data/task/install-data-archiving-plugin.md).

