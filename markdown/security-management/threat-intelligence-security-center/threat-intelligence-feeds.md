---
title: Threat Intelligence Feeds
description: Configure threat intelligence data sources to automatically import security indicators into your ServiceNow instance. Use feeds to keep threat data current and enhance security monitoring capabilities.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Integrate, Threat Intelligence Security Center, Security Operations]
---

# Threat Intelligence Feeds

Configure threat intelligence data sources to automatically import security indicators into your ServiceNow instance. Use feeds to keep threat data current and enhance security monitoring capabilities.

Use Threat Intelligence Feeds to add, edit, or remove threat intelligence feed data sources. Access data source feeds from the Threat Intel Catalog under the Integrations section.

The catalog for threat intelligence feeds displays available feed data sources as tiles. You can filter, search, and navigate to source configuration details to perform various actions.

## All Feeds

You can enable and use feeds displayed as cards in the base system.

To view feeds, navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Integrations** &gt; **Threat Intel Feeds** &gt; **All Feeds**.

![Threat Intelligence Feeds](../image/tisc-all-feeds.png)

## Actions on the All Feeds view

You can perform the following actions in the All Feeds section.

<table id="table_ols_yx1_nzb"><thead><tr><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

All

</td><td>

Filter feeds by current state using this drop-down menu. Available filter states:-   **All**: Displays all the feeds on the page. This is the default option.
-   **Enabled**: Displays all the feeds that are in an enabled state.
-   **Disabled**: Displays all the feeds that are in a inactive state.
-   **Draft**: Displays all the feeds that are in a draft state.

</td></tr><tr><td>

![Card view](../image/enrich-card-view.png)

</td><td>

View all feeds as cards.

</td></tr><tr><td>

![List view](../image/enrich-list-view.png)

</td><td>

View all feeds as a list.

</td></tr><tr><td>

![Refresh](../image/enrich-refresh-icon.png)

</td><td>

Refresh the page.

</td></tr><tr><td>

![Sort](../image/enrich-sort-icon.png)

</td><td>

Sort integrations by:-   **Last Modified \(recent\)**
-   **Last Modified \(oldest\)**
-   **Name \(A-Z\)**
-   **Name \(Z-A\)**

</td></tr><tr><td>

All items

</td><td>

Filter threat intelligence feed tiles by source type or feed type.**Source Type**:

-   Open Source
-   Other Source
-   Premium Source

**Feed Type**:

-   CSV
-   Custom Feed
-   JSON
-   MISP
-   RSS
-   STIX HTTPs
-   Text

</td></tr><tr><td>

Search in catalog

</td><td>

Search for feeds by name and description within the catalog.

</td></tr></tbody>
</table>## Threat Intelligence feed types

You can configure and enable the following threat intelligence feed types:

<table id="table_y2y_rnd_pyb"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

TAXII Feeds

</td><td>

Feeds in STIX/TAXII Collections format.

</td></tr><tr><td>

STIX HTTPS

</td><td>

Threat intelligence feeds in STIX format accessible through REST APIs on HTTPS protocol.

</td></tr><tr><td>

MISP

</td><td>

Feeds in MISP Format Feeds.

</td></tr><tr><td>

Text

</td><td>

Feeds hosted as text files.**Note:** Only URLs, domains, file names, hashes, and IP addresses are extracted.

</td></tr><tr><td>

CSV

</td><td>

Feeds hosted as CSV files.**Note:** Only URLs, domains, file names, hashes, and IP addresses are extracted.

</td></tr><tr><td>

JSON

</td><td>

Feeds hosted as JSON files.**Note:** Only URLs, domains, file names, hashes, and IP addresses are extracted.

</td></tr><tr><td>

RSS

</td><td>

Feeds in RSS format. The application will store the data as RSS Feed Records.

</td></tr><tr><td>

Custom

</td><td>

Feeds configured with custom parsers.**Note:** Only URLs, domains, file names, hashes, and IP addresses are extracted.

</td></tr></tbody>
</table>For configuration steps, refer to the respective topic for your feed type.

-   **[Configure a new threat intelligence feed](../task/tisc-new-data-source.md)**  
Add external threat intelligence sources to your TISC environment. Configure feed parameters, authentication, scheduling, and data processing to automatically ingest threat indicators from various sources.
-   **[Configure Custom Field Mapping](../task/tisc-field-mapping.md)**  
Field Mapping allows you to configure how each field in a data feed such as Text, CSV or JSON is interpreted and assigned to the corresponding observable.
-   **[View Threat Intel Feeds](base-system-threat-intel-feeds.md)**  
View threat intelligence feeds that automatically imports security data into your TISC ServiceNow instance. This enables real-time threat detection and response capabilities.
-   **[About STIX TAXII](threat-intelligence-security-center-feeds.md)**  
Structured Threat Information Expression \(STIX\) is a language and serialization format used to exchange cyberthreat intelligence \(CTI\). Trusted Automated Exchange of Intelligence Information \(TAXII\) is a protocol used to exchange cyberthreat intelligence \(CTI\) over HTTPS.
-   **[Duplicate threat intelligence feeds](../task/tisc-duplicate-feeds.md)**  
Duplicate a threat feed to create an exact copy with all associated observables, indicators, and actors when you want to modify settings without affecting the original feed.

**Parent Topic:**[Integrate](integrating-threat-intelligence-security-center.md)

**Related topics**  


[Threat Intelligence Security Center Catalog](threat-intelligence-security-center-catalogue.md)

[TISC Integrations](tisc-integrations.md)

