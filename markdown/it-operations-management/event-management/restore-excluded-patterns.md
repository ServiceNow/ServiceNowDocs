---
title: Restore excluded patterns
description: Restoring excluded patterns to the learned patterns report lets you reintegrate valuable insights lost due to incorrect alerts. This flexibility maintains accurate alert aggregation and enhances monitoring. For example, if you excluded a pattern due to an incorrect alert, you can restore it without that alert, ensuring relevant data remains accessible for analysis and decision-making.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/event-management/restore-excluded-patterns.html
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Automated alert grouping, Alert grouping types and creation methods, Alert grouping, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Restore excluded patterns

Restoring excluded patterns to the learned patterns report lets you reintegrate valuable insights lost due to incorrect alerts. This flexibility maintains accurate alert aggregation and enhances monitoring. For example, if you excluded a pattern due to an incorrect alert, you can restore it without that alert, ensuring relevant data remains accessible for analysis and decision-making.

## Before you begin

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Administration** &gt; **Excluded patterns**.

    \[Omitted image "em-restore-pattern-nav.png"\] Alt text: Restore pattern navigation

2.  On the Excluded Patterns page, expand or select a pattern to view its alerts.

    \[Omitted image "em-pattern-excluded.png"\] Alt text: Expanded patterns

3.  Select the patterns you want to restore.

4.  In the **Actions on selected rows** drop-down menu, select **Delete**.

    \[Omitted image "em-excluded-patterns-delete.png"\] Alt text: Delete patterns that you want to restore

5.  In the confirmation window, select **Delete**.

6.  Run the Learned Patterns scheduled job.

    1.  Select **System Definition** &gt; **Scheduled Job**.

    2.  On the Scheduled Jobs page, search for the Service Analytics Alert Aggregation Learner - Daily job.

    3.  Open the Service Analytics Alert Aggregation Learner - Daily job.

        \[Omitted image "em-learned-patterns-job.png"\] Alt text: Scheduled job

    4.  Select **Execute Now**.


## Result

The pattern appears with its restored alerts on the Learned Patterns report page. To access this page, navigate to **Event Management** &gt; **Reporting** &gt; **Learned Patterns**.

