---
title: Roll back patch upgrades or plugin activations
description: Use the Rollback Contexts module to roll back patch upgrades and plugin activations.
locale: en-US
release: australia
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Roll back and delete recovery, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Roll back patch upgrades or plugin activations

Use the **Rollback Contexts** module to roll back patch upgrades and plugin activations.

## Before you begin

Role required: admin

Review this information and requirements before performing rollback:

-   Rolling back is possible only between patches in the same software release. For example, Rolling back is possible from Orlando patch 2 to patch 1, but not from Orlando to New York.
-   The rollback must be done within 10 days of the most recent upgrade or plugin activation. If you need to retain a rollback context for more than 10 days, you can do so by adding a system property. See [Rollback context properties](../reference/rollback-context-properties.md).
-   You can only roll back to the previous version.

    For example, rolling back from patch 3 to patch 1 requires two rollbacks.

-   You must have the Restore Deleted Records \(com.snc.undelete\) and Delete Recovery \(com.glide.delete\_recovery\) plugins activated.
-   You can only roll back one active instance at a time.

    Rolling back contexts on multiple nodes is not supported.

-   A rollback deletes data and may remove evidence of an upgrade or activation record, which makes it difficult to debug the problem that made the rollback necessary.
-   To roll back to a patch version before the Assigned WAR, submit a request for Customer Service and Support to do the rollback.

## Procedure

1.  Navigate to **All** &gt; **Rollback &amp; Recovery** &gt; **Rollback Contexts**.

2.  Select the context that you want to rollback.

3.  Roll back by selecting the **Rollback** related link.

4.  Confirm the rollback.

    An indicator appears showing the progress of the rollback. **glide.war** updates to the rolled-back version. The log shows the stages of the rollback process.

5.  After the rollback is complete, log out of your instance and log back in again.

6.  Open a new tab and see if the context state changed to **Rolled back**.

    If not, contact Customer Service and Support.


**Parent Topic:**[Roll back and delete recovery](../concept/rollback-delete-recovery.md)

