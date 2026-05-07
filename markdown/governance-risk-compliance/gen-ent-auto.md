---
title: Generate entities automatically using a scheduled job
description: Generate entities automatically via scheduled job once pillars, entity types, and entity filters are active. Entities are individual records matching your filter criteria. For actual entity creation, you should run the GRC Profile Generation scheduled job in the GRC: Profiles application rather than using entity filters.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up pillars, entity types, entity filters, and entities, Configure, Operational Resilience, Governance, Risk, and Compliance]
---

# Generate entities automatically using a scheduled job

Generate entities automatically via scheduled job once pillars, entity types, and entity filters are active. Entities are individual records matching your filter criteria. For actual entity creation, you should run the **GRC Profile Generation** scheduled job in the GRC: Profiles application rather than using entity filters.

## Before you begin

Role required: sn\_oper\_res.manager

## About this task

Entities can be generated using two methods. This section describes the automatic generation method, which is recommended for most scenarios.

## Procedure

1.  Navigate to **Admin** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Find the **GRC Profile Generation** scheduled job in the GRC: Profiles application.

    The **GRC Profile Generation** scheduled job is shown in the example.

    ![GRC Profile Generation scheduled job.](../image/sch-job-grc-profile-gen.png)

3.  Select **Execute Now**.

4.  Wait for job completion \(time varies based on data volume\).

5.  Check the entity types to verify that entities are created.

6.  Open an entity type and check the entities related list.

    **Note:** Generate entities automatically using the scheduled job. Use manual addition from the Operational Resilience Workspace for exceptions or one-off additions that don't fit the filter criteria. For adding entities from the Operational Resilience Workspace using the **Add to OpRes** UI action, see [Add entities manually](gen-ent-manually.md).


