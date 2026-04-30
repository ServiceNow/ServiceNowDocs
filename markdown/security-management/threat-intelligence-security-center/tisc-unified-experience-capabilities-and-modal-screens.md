---
title: Run Enrichment operations in TISC
description: The following table below describes the interactions involved in running different enrichment operations from TISC.
locale: en-US
release: yokohama
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Observables, TISC Library Repository, Threat Intelligence Security Center Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Run Enrichment operations in TISC

The following table below describes the interactions involved in running different enrichment operations from TISC.

## TISC modal screens

<table id="table_z5p_bk5_g1c"><thead><tr><th>

Capability

</th><th>

UX Frameworks interactions

</th><th>

Integrations supported

</th></tr></thead><tbody><tr><td>

Run Threat Look Up

</td><td>

On Screen 1 – Select the implementation\(s\) and submit.There are no common inputs or implementation specific inputs applicable for Run Threat Look Up.

</td><td>

-   Virus Total
-   Crowd Strike Falcon Intelligence

</td></tr><tr><td>

Run Sighting Search

</td><td>

Screen 1 – Select Implementations and Screen 2 – Common Inputs are applicable.Sighting search takes date and time frequency as common inputs across multiple implementations of Splunk and other integrations.

</td><td>

-   Elastic search
-   Splunk Sighting

</td></tr><tr><td>

Run Observable Enrichment

</td><td>

Only Screen 1 – Select Implementations.There are no common inputs or implementation specific inputs applicable for Run Observable Enrichment.

</td><td>

-   WHOIS
-   Shodan

</td></tr></tbody>
</table>-   **[Observable Enrichment](../concept/tisc-observable-enrichment.md)**  
The Enrich Observable WhoIs workflow performs enrichment on selected observables. If the observables are of a type recognized by the WhoisXML API Integration, the observables are enriched.
-   **[Run Threat Lookup](tisc-run-threat-lookup.md)**  
Select one or more implementations as applicable to run threat lookup on observables.
-   **[Run Sighting Search](tisc-run-sighting-search.md)**  
Perform Run Sighting Search related integration.
-   **[Run Observable Enrichment](tisc-run-observable-enrichment.md)**  
Select one or more implementations as applicable to run threat lookup on observables.

**Parent Topic:**[Observables](../concept/observables.md)

