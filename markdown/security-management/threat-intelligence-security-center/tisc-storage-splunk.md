---
title: Data storage in Splunk
description: This section outlines how TISC utilizes lookups during the integration within Splunk's Key-Value store for data storage. It details how these lookups are configured and retrieved within Splunk.
locale: en-US
release: xanadu
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2025-01-15"
reading_time_minutes: 1
keywords: [data, storage, lookups, key-value, splunk, tisc, tisc integrations]
breadcrumb: [Configuring TISC add-on in Splunk, TISC add-on for Splunk overview, Configure Sighting Search, Sighting Search, TISC Enrichment Integrations, TISC Integrations, Integrating Threat Intelligence Security Center, Threat Intelligence Security Center, Security Operations]
---

# Data storage in Splunk

This section outlines how TISC utilizes lookups during the integration within Splunk's Key-Value store for data storage. It details how these lookups are configured and retrieved within Splunk.

<table id="table_izm_vzw_12c"><thead><tr><th>

Lookup

</th><th>

Lookup Description

</th></tr></thead><tbody><tr><td>

```
threat_intel_store_lookup_test_instance_test
```

</td><td>

Name of the KV lookup to be used for searching the incoming records.

</td></tr><tr><td>

```
threat_intel_store_test_instance_test
```

</td><td>

Name of the KV store where the data resides.

</td></tr><tr><td>

```
inputlookup <lookup_name>" example : | inputlookup threat_intel_store_lookup_test_instance_test
```

</td><td>

Query to lookup records in the KV store.

</td></tr></tbody>
</table>**Parent Topic:**[Configuring TISC add-on in Splunk](../task/tisc-configure-splunk.md)

