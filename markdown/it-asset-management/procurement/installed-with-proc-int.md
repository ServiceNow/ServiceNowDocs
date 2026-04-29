---
title: Components installed with Asset Management - Procurement Integration
description: Several types of components are installed with activation of the Asset Management - Procurement Integration application, such as tables and scheduled jobs.
locale: en-US
release: australia
product: Procurement
classification: procurement
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Install Asset Management - Procurement Integration, Integrating with external procurement applications, Procurement, IT Asset Management]
---

# Components installed with Asset Management - Procurement Integration

Several types of components are installed with activation of the Asset Management - Procurement Integration application, such as tables and scheduled jobs.

## Scheduled jobs installed

<table id="table_dqd_23n_wwb"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ITAM - Sync &lt;procurement\_integration\_profile\_name&gt; purchase orders

</td><td>

Fetches the status of the already created requisitions daily.

This scheduled job is automatically created when you publish the integration profile.

</td></tr></tbody>
</table>## Tables installed

<table id="table_fqd_23n_wwb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Procurement Integration Profile\[itam\_procurement\_integration\_profile\]

</td><td>

Includes the details of the third-party procurement integrations that are connected to the Procurement application in ServiceNow.

</td></tr><tr><td>

Procurement Integration Jobs\[itam\_procurement\_integration\_job\]

</td><td>

Includes the mapping information of a procurement integration profile with its associated scheduled jobs.

</td></tr><tr><td>

Integration Scheduled Job Results\[itam\_procurement\_integration\_job\_log\]

</td><td>

Includes the details of the failure of the scheduled job execution.

</td></tr></tbody>
</table>