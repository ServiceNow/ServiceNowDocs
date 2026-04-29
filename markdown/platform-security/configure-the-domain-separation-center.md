---
title: Configure the Domain Separation Center
description: Specify which tables in domains are large and whether you want detailed logging.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Domain Separation Center, Domain separation for service providers, Access Management]
---

# Configure the Domain Separation Center

Specify which tables in domains are large and whether you want detailed logging.

## Before you begin

Role required: admin

## About this task

You can schedule audits to run on a daily, weekly, or monthly basis. Audits run on large tables can take a significant amount of time. For that reason, avoid running audits daily on large tables. Starting a new audit on one that is taking more than a day to run can have negative consequences.

Detailed logging can provide greater insights into problems found during audits, however might cause performance issues.

## Procedure

1.  In the Domain Separation Center, select **Configure Domain Center**.

    The Configure Domain Center page appears.

2.  Select **Yes** for **Enables detail domain logging**, to store detailed logs that help diagnose domain-related issues.

    These logs refer to server-side logs in the Domain Log \[syslog\_domain\] table. For information about viewing the logs, see the View audits with warnings and failures section.

3.  In the list, move all of your large tables into the **Selected** column.

    Daily audits should not run on large tables. Grayed-out table names in the **Selected** column are large and cannot be moved to the **Available** column.

4.  Select **Update**.

5.  If you have large tables that should never be audited, set the **com.glide.domain.audit.big\_tables.additional** system property to a comma-separated list of those table names.


