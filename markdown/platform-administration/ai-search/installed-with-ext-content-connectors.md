---
title: Components installed with External Content Connectors
description: The External Content Connectors plugin installs a connector admin role and a scheduled job to remove unused OAuth 2.0 credentials for deleted external content connectors.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2025-11-13"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Reference, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Components installed with External Content Connectors

The External Content Connectors plugin installs a connector admin role and a scheduled job to remove unused OAuth 2.0 credentials for deleted external content connectors.

## Roles installed

<table id="table_xst_3bf_pgc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

External Content Connectors administrator \[sn\_ext\_conn.xcc\_admin\]

</td><td>

Manages configuration settings for the External Content Connectors application, including the following:-   Creates, reads, updates, and deletes external content connectors
-   Creates, reads, updates, and deletes crawl settings for external content connectors
-   Tests and validates external content connector configuration and crawl settings
-   Schedules and runs external content connectors
-   Views external content connector crawl logs

This is a granular admin role that allows you to complete external content connector configuration tasks without requiring the full admin role. To learn more about how granular admin roles improve security and efficiency, see [Granular admin roles required to secure your instance](https://www.servicenow.com/docs/access?context=roles-within-platform-security&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

</td><td>

-   ais\_admin
-   connection\_admin
-   sn\_kmf.cryptographic\_manager

</td></tr></tbody>
</table>## Scheduled jobs installed

<table id="table_azz_5cm_w2c"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Clean orphan external content oauth credential

</td><td>

Deletes stored OAuth 2.0 credentials for external content connectors that have been deleted. By default, this job runs once per day. Users with the admin role can change the schedule for this job:

1.  Navigate to **All** &gt; **System Scheduler** &gt; **Scheduled Jobs** &gt; **Scheduled Jobs**.
2.  Open the **Clean orphan external content oauth credential** record.
3.  Set the desired schedule for the job by modifying the **Trigger type**, **Time zone**, and **Run time** field values.
4.  Select **Update**.

</td></tr></tbody>
</table>**Parent Topic:**[External Content Connectors reference](../concept/reference-ext-cont-connectors.md)

