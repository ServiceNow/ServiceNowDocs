---
title: Archive firewall rule audit, rule requests, and audit tasks
description: Archive firewall rule requests, audit requests, and audit tasks that are older than a specific time period to enhance system performance. At a later time, you can delete them from the archive table altogether to reduce the size of that table.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Visibility to Firewall inventory, Configuring Firewall Audits and Reporting, Firewall Audits and Reporting, ITOM Visibility, IT Operations Management]
---

# Archive firewall rule audit, rule requests, and audit tasks

Archive firewall rule requests, audit requests, and audit tasks that are older than a specific time period to enhance system performance. At a later time, you can delete them from the archive table altogether to reduce the size of that table.

## Before you begin

Ensure that the Data Archiver \[com.glide.auxdb\] plugin is activated and enabled.

Role required: firewall\_admin

## Procedure

1.  Activate one or more of the **Firewall Archival Rules**.

    The following archival rules come with the Firewall Audits and Reporting application, but are inactive by default. You must activate any rules if you want to use them.

    -   Archive Firewall Audit Request
    -   Archival Firewall Audit Request Security Policy M2M
    -   Archive Firewall Audit Task
    -   Archival Firewall Audit Task Security Policy M2M
    -   Archive Firewall Rule Task
    -   Archival Firewall Rule Task Security Policy M2M
2.  Navigate to **Archive Rules** &gt; **Select a Firewall Archive rule**.

3.  Select the **Active** check box.

    The Data Archiver \[com.glide.auxdb\] plugin moves data that is no longer needed from the primary tables to a set of archive tables daily. It checks for and archives requests and tasks based on the archival rule activated and chosen. The rule archives data from the primary table when the following two conditions are met:

    -   State is Closed Complete
    -   Update before Last 12 months

**Parent Topic:**[Visibility to Firewall inventory](../concept/use-firewall-audit-rep.md)

