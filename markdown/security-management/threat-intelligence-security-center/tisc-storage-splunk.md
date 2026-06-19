---
title: Data storage in Splunk
description: Configure and retrieve Key-Value store lookups used by TISC during its integration with Splunk.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/threat-intelligence-security-center/tisc-storage-splunk.html
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [data, storage, lookups, key-value, splunk, tisc, tisc integrations]
breadcrumb: [TISC add-on for Splunk overview, TISC Security Tools integrations, TISC Integrations, Integrate, Threat Intelligence Security Center, Security Operations]
---

# Data storage in Splunk

Configure and retrieve Key-Value store lookups used by TISC during its integration with Splunk.

<table id="table_izm_vzw_12c"><thead><tr><th>

Lookup

</th><th>

Description

</th></tr></thead><tbody><tr><td>

```
tisc_kv_store
```

</td><td>

Name of the KV store where the data resides.

</td></tr><tr><td>

```
tisc_store_lookup
```

</td><td>

Name of the KV lookup to be used for searching the incoming records.

</td></tr><tr><td>

```
inputs_metadata_lookup
```

</td><td>

KV lookup that stores the status of recent executions for each configured input. Each record captures the configuration name, input name, last successful execution time, status, status message, and historical fetch date. Use this lookup to verify whether an input is running on schedule and to diagnose failures.

</td></tr><tr><td>

```
inputlookup <tisc_store_lookup>" example : | inputlookup tisc_store_lookup
```

</td><td>

Query to lookup records in the KV store.

</td></tr></tbody>
</table>**Parent Topic:**[TISC add-on for Splunk overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-addon-splunk.md)

