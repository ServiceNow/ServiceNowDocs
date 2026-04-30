---
title: Review the MISP integration settings
description: Review the MISP integration for Security Operations settings and modify the default system properties to suit your environment.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [MISP administration, MISP integration for Security Operations, Threat Intelligence integrations, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Review the MISP integration settings

Review the MISP integration for Security Operations settings and modify the default system properties to suit your environment.

## Before you begin

Role required: sn\_si.admin, sn\_ti.admin

## Procedure

1.  Navigate to **All** &gt; **MISP Integration** &gt; **Integration Settings**.

2.  Modify the following settings as required.

<table id="table_smd_tdf_kqb"><thead><tr><th colspan="2">

Property name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Observable Enrichment

</td><td>

Time \(in hours\) before fetching new data

</td><td>

Time in hours before you can fetch new data.Type: integer

 Default value: 24

</td></tr><tr><td rowspan="2">

Sighting Search

</td><td>

Run Sighting Search automatically when new observables are associated with the security incident

</td><td>

Sighting search that runs whenever a new observable is associated with a security incident.Default value: Yes

</td></tr><tr><td>

Search Interval \(in days\) for sighting search in MISP

</td><td>

Number of days that the sighting search data is searched in MISP. Use this option only for the automatic sighting search feature.Default value: 90

</td></tr><tr><td rowspan="3">

Data synchronization

</td><td>

Interval period \(in minutes\) for tags to be fetched and synchronized with MISP

</td><td>

MISP tags that are fetched at the time of the integration configuration. After the data is in the ServiceNow AI Platform, this property defines the frequency at which the data with the MISP server is synchronized. The value is defined in minutes.Default value: 1440 \(minutes or 24 hours\)

</td></tr><tr><td>

Interval period \(in minutes\) to refresh MISP galaxies from configured sources

</td><td>

MISP galaxies that are fetched at the time of the integration configuration. After the data is in the ServiceNow AI Platform, this property defines the frequency at which the data with the MISP server is synchronized. The value is defined in minutes.Default value: 1440 \(minutes or 24 hours\)

</td></tr><tr><td>

Interval period \(in minutes\) for organizations to be fetched and synchronized with MISP

</td><td>

MISP organizations that are fetched at the time of the integration configuration. After the data is in the ServiceNow AI Platform, this property defines the frequency at which the data with the MISP server is synchronized. The value is defined in minutes.Default value: 1440 \(minutes or 24 hours\)

</td></tr><tr><td rowspan="2">

MITRE™ Technique Extraction

</td><td>

Rollup MITRE-ATT&amp;CK techniques automatically from MISP Observable Enrichment Results \(Tags\) to security incident

</td><td>

Rollup of MITRE-ATT&amp;CK information from MISP observable enrichment results \(tags\) to the security incident.Default value: Yes

</td></tr><tr><td>

Rollup MITRE-ATT&amp;CK techniques automatically from MISP Observable Enrichment Results \(Galaxies\) to security incident

</td><td>

Rollup of MITRE-ATT&amp;CK information from the MISP observable enrichment results \(galaxies\) to the security incident.Default value: Yes

</td></tr></tbody>
</table>    **Note:**

    -   To use the MITRE™ technique extraction features in MISP, you must [enable the MITRE-ATT&amp;CK feature in the Threat Intelligence module](../../threat-intelligence/reference/get-started-with-mitre.md).
    -   The MISP integration for Security Operations introduces two base system MITRE-ATT&amp;CK technique extraction rules for MISP - MISP galaxies and MISP tags. For more information on auto-extraction rules in MITRE-ATT&amp;CK, see [auto-extract technique rules for importing MITRE-ATT&amp;CK information](../../threat-intelligence/concept/auto-extract-technique-rules.md#).
3.  Click **Save**.


## Result

Your modified integration settings are saved and applied.

**Parent Topic:**[MISP administration](../concept/misp-administration.md)

**Related topics**  


[Getting started with MISP integration for Security Operations](../reference/get-started-with-misp-integration-for-security-operations.md)

[Install and configure the MISP integration for Security Operations](install-and-configure-misp.md)

[Configure MISP sighting searches](configure-sightings-search.md)

[Configure how an automatic event is created](configure-automatic-event-creation-profile.md#)

[MISP event data](../concept/misp-event-data.md)

[Associated MISP events](../reference/associated-misp-events.md)

[MISP user information](../reference/misp-user-information.md)

[Domain separation and MISP](../reference/domain-separation-and-misp.md)

[Troubleshooting MISP integration](../reference/troubleshooting-misp-integration.md)

