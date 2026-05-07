---
title: Components installed with synthetic monitoring
description: Several types of components are installed with activation of the synthetic monitoring plugin, including tables and user roles.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Synthetic monitoring reference, Synthetic monitoring, ITOM AIOps, IT Operations Management]
---

# Components installed with synthetic monitoring

Several types of components are installed with activation of the synthetic monitoring plugin, including tables and user roles.

## Roles installed

<table id="table_hgx_ljr_qdc"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Synthetic monitor viewer\[sn\_sow\_synthetics.synthetics\_viewer\]

</td><td>

Views test configurations and their results.

</td><td>

-   cmdb\_read
-   sn\_sow.sow\_user
-   agent\_client\_collector\_user
-   sn\_sow\_synthetics.credential\_reader

</td></tr><tr><td>

Synthetic monitor editor \[sn\_sow\_synthetics.synthetics\_editor\]

</td><td>

Creates and edits tests. Views test configurations and their results.

</td><td>

-   credential\_admin
-   sn\_cmdb\_editor
-   sn\_sow\_synthetics.synthetics\_viewer

</td></tr><tr><td>

Synthetic monitor admin \[sn\_sow\_synthetics.synthetics\_admin\]

</td><td>

Assigns roles. Creates and edits tests. Views test configurations and their results.

</td><td>

-   agent\_client\_collector\_admin
-   sn\_sow\_synthetics.synthetics\_editor
-   sn\_sow\_itsm\_admin.sow\_admin\_user


</td></tr><tr><td>

Synthetic monitor credential reader\[sn\_sow\_synthetics.credential\_reader\]

</td><td>

Used internally to read from the Credentials \[discovery\_credentials\] table.

</td><td>

None

</td></tr><tr><td>

Synthetic monitor event writer\[sn\_sow\_synthetics.synthetics\_event\_writer\]

</td><td>

Used internally to communicate with the MID Server.

</td><td>

None

</td></tr></tbody>
</table>## Tables installed

<table id="table_fwf_y3r_qdc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Check

 \[sn\_sow\_synthetics\_check\]

</td><td>

Configuration information for synthetic checks.

</td></tr><tr><td>

Check Execution Location

 \[sn\_\_sow\_synthetics\_check\_execution\_location\]

</td><td>

Execution location configuration for synthetic checks.

</td></tr><tr><td>

Single API

 \[sn\_sow\_synthetics\_check\_single\_api\]

</td><td>

Additional configuration information and last run results for single API synthetic checks.

</td></tr><tr><td>

Single API Header

 \[sn\_sow\_synthetics\_check\_single\_api\_header\]

</td><td>

Key value pairs of requests headers for single API synthetic checks.

</td></tr><tr><td>

Single API to Policy

 \[sn\_sow\_synthetics\_check\_single\_api\_policy\]

</td><td>

Single API synthetic test data and its corresponding Agent Client Collector \(ACC\) policies.

</td></tr><tr><td>

Single API Result

 \[sn\_sow\_synthetics\_check\_single\_api\_result\]

</td><td>

Results from each synthetic check run.

</td></tr><tr><td>

sn\_sow\_synthetics\_recommendation\_state

</td><td>

Per-endpoint creation state, idempotency\_key, error tracking

</td></tr><tr><td>

sn\_sow\_synthetics\_recommendation\_telemetry

</td><td>

Aggregate workflow metrics: card\_shown, endpoints\_discovered, monitors\_created, workflow\_status

</td></tr><tr><td>

Synthetic Private Locations

 \[sn\_sow\_synthetics\_private\_location\]

</td><td>

Definitions of the ACC Agent Proxy Clusters available for synthetic monitoring. Extends the Proxy Agent Cluster \[sn\_agent\_cluster\] table.

</td></tr><tr><td>

sn\_sow\_synthetics\_bulk\_job

</td><td>

Provides async bulk job tracking.

</td></tr><tr><td>

sn\_sow\_synthetics\_bulk\_job\_governance

</td><td>

Defines governance metadata for rate limiting and auditing for bulk jobs.

</td></tr></tbody>
</table>**Parent Topic:**[Synthetic monitoring reference](synthetic-monitoring-reference.md)

