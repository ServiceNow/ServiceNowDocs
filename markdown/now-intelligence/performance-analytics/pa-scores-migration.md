---
title: Migrating Performance Analytics scores
description: The Performance Analytics Scores \[pa\_scores\] table was split into two tables. This structure helps with processing large numbers of scores. You can migrate your scores from the old table structure to the new, using the score migration tool.Schedule the automated migration process to move existing scores to the new table structure.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure Performance Analytics advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Migrating Performance Analytics scores

The Performance Analytics Scores \[pa\_scores\] table was split into two tables. This structure helps with processing large numbers of scores. You can migrate your scores from the old table structure to the new, using the score migration tool.

**Warning:** The new table structure is not supported on Oracle databases.

In Istanbul, the Scores \[pa\_scores\] table was split into Scores Level 1 \[pa\_scores\_l1\] and Scores Level 2 \[pa\_scores\_l2\]. The pa\_scores\_l2 table contains the second-level breakdown matrix of scores and the pa\_scores\_l1 table contains all other scores. This separation of scores ensures optimal performance when collecting and analyzing scores, and enables larger sets of scores. New instances created on the Istanbul release or later use the new scores tables by default.

Instances created prior to Istanbul still use the original Scores \[pa\_scores\] table after upgrading.

**Important:** For full details on migrating Performance Analytics scores to the new table structure, see [KB1294371](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1294371).

## Migration Monitor

After beginning the migration, you can track the migration status by navigating to **Performance Analytics** &gt; **Scores Migration Monitor.**

If any errors occur during migration, contact Customer Service and Support to resolve the issue.

## Delays in starting score migration

If any of the following processes are running, score migration remains in the Waiting state until they stop:

-   Data collector jobs
-   Collection cleaner jobs
-   Scoresheet editing

**Parent Topic:**[Configure Performance Analytics advanced features](c_PADataArchitecture.md)

## Schedule the Performance Analytics scores migration

Schedule the automated migration process to move existing scores to the new table structure.

### Before you begin

Role required: admin. Users with the pa\_admin role can view the migration monitor page but cannot schedule the migration.

### About this task

Migrating scores improves performance and scalability of Performance Analytics. Migration should be performed during off-peak hours.

During migration you cannot collect, modify, or delete scores. Scheduled data collection jobs do not run during migration. After migration completes, check any data collection jobs that were scheduled to run during the migration, as these jobs were suspended.

**Note:**

-   The scores migration can take several hours to complete, depending on the number of scores. Schedule the migration in a non-production instance and then carefully plan the migration in production.
-   The original Scores \[pa\_scores\] table is truncated 10 days after successful migration.

### Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Scores Migration Monitor**.

2.  Click the **Schedule Scores Migration** button.

    The scores migration is scheduled. The page displays the time that the migration is scheduled to start, and the estimated completion time.

3.  Click the **Logs** or **Active Jobs** links to view additional information about the migration.

    If there are any data collection or cleanup jobs running when you start the migration, the migration waits for those jobs to complete before beginning. All scheduled collection and cleanup jobs are paused during the migration.


### What to do next

If the migration fails for any reason, contact Customer Service and Support for assistance. Existing scores remain in place.

