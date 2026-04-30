---
title: Components installed with External Content Connectors
description: The External Content Connectors plugin installs a scheduled job to remove unused OAuth 2.0 credentials for deleted external content connectors.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2025-04-05"
reading_time_minutes: 1
breadcrumb: [Reference, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Components installed with External Content Connectors

The External Content Connectors plugin installs a scheduled job to remove unused OAuth 2.0 credentials for deleted external content connectors.

## Scheduled jobs installed

<table id="table_azz_5cm_w2c"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Clean orphan external content oauth credential

</td><td>

Deletes stored OAuth 2.0 credentials for external content connectors that have been deleted. By default, this job runs once per day.

 Users with the admin role can change the schedule for this job:

1.  Navigate to **All** &gt; **System Scheduler** &gt; **Scheduled Jobs** &gt; **Scheduled Jobs**.
2.  Open the **Clean orphan external content oauth credential** record.
3.  Set the desired schedule for the job by modifying the **Trigger type**, **Time zone**, and **Run time** field values.
4.  Select **Update**.

</td></tr></tbody>
</table>**Parent Topic:**[External Content Connectors reference](../concept/reference-ext-cont-connectors.md)

