---
title: Archive rules in the Industrial Connected Workforce
description: Archiving rules in the Industrial Connected Workforce \(ICW\) helps maintain system efficiency by automatically managing outdated records. These rules verify that only relevant and current data remains active.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Industrial Connected Workforce Core, Industrial Connected Workforce]
---

# Archive rules in the Industrial Connected Workforce

Archiving rules in the Industrial Connected Workforce \(ICW\) helps maintain system efficiency by automatically managing outdated records. These rules verify that only relevant and current data remains active.

The system applies archiving rules to the following record types:

-   Deviations
-   Actions
-   Root cause analyses \(RCAs\)

The system automatically archives records that haven’t been updated in two years \(both active and inactive\).

By default, archiving rules are active in the ICW. You can manage these rules by going to **All** &gt; **System Archiving** &gt; **Archive Rules** and deactivating rules as needed.

The ICW includes the following predefined rules:

-   Archive stale actions after 2 years: Archives actions that haven’t been updated in two years.
-   Archive stale deviations after 2 years: Archives deviations that haven’t been updated in two years.
-   Archive stale RCAs after 2 years: Archives root cause analysis tasks that haven’t been updated in two years.

These archiving rules support data hygiene and system usability by making sure that outdated records don’t interfere with active workflows.

For more information on archive rules, see [Create an archive rule in Core UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_CreateAnArchiveRule.md).

**Parent Topic:**[Configuring ICW Core](configuring-icw-core.md)

