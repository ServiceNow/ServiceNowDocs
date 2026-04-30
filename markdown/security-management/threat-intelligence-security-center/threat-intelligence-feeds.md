---
title: Threat Intelligence Feeds
description: Use Threat Intelligence Feeds to add, edit, or remove Threat Intelligence feed data source.
locale: en-US
release: yokohama
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Integrate Threat Intelligence Security Center, Threat Intelligence Security Center, Security Operations]
---

# Threat Intelligence Feeds

Use Threat Intelligence Feeds to add, edit, or remove Threat Intelligence feed data source.

The data source feeds are available from the Threat Intel Catalog under Integrations section.

The catalog for threat intelligence feeds is built to show the available feed data sources in the form of tiles and has the ability to filter, search, and navigate to the details of the source configuration and perform various actions.

## All Feeds

The base system includes a series of cards for each of the feeds that you can enable and use.

The Feeds can be viewed by navigating to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Integrations** &gt; **Threat Intel Feeds** &gt; **All Feeds**.

![Threat Intelligence Feeds](../image/tisc-all-feeds.png)

## Actions on the All Feeds view

The All Feeds section enables you to perform the following actions.

<table id="table_ols_yx1_nzb"><thead><tr><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

All

</td><td>

Use this drop-down menu to filter feeds based on their current state. You can filter based on the following states:-   **All**: Displays all the feeds on the page. This is the default option.
-   **Enabled**: Displays all the feeds that are in an enabled state.
-   **Disabled**: Displays all the feeds that are in a disabled state.
-   **Draft**: Displays all the feeds that are in a draft state.

</td></tr><tr><td>

![Card view](../image/enrich-card-view.png)

</td><td>

Use this action to view all the feeds in the form of cards.

</td></tr><tr><td>

![List view](../image/enrich-list-view.png)

</td><td>

Use this action to view all the feeds in the form of a list view.

</td></tr><tr><td>

![Refresh](../image/enrich-refresh-icon.png)

</td><td>

Use this action to refresh the page.

</td></tr><tr><td>

![Sort](../image/enrich-sort-icon.png)

</td><td>

Use this action to sort all the integrations based on the following:-   **Last Modified \(recent\)**
-   **Last Modified \(oldest\)**
-   **Name \(A-Z\)**
-   **Name \(Z-A\)**

</td></tr><tr><td>

All items

</td><td>

Use this action to filter and list the threat intelligence feed tiles by source type or feed type.**Source Type**:

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

Use this action to search for feeds based on the name and description within the catalog.

</td></tr></tbody>
</table>## Types of Threat Intel Feeds

The following are the types of threat intelligence feeds which can be configured and enabled:

<table id="table_y2y_rnd_pyb"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

TAXII Feeds

</td><td>

Feeds that are available as STIX/TAXII Collections format.

</td></tr><tr><td>

STIX HTTPS

</td><td>

Threat Intelligence feeds in STIX format that can be accessed through REST APIs on HTTPS protocol.

</td></tr><tr><td>

MISP

</td><td>

Feeds that are in the MISP Format Feeds.

</td></tr><tr><td>

Text

</td><td>

Feeds that are available as hosted files in text format.**Note:** Only URLs, domains, file names, hashes, and IP addresses are extracted.

</td></tr><tr><td>

CSV

</td><td>

Feeds that are available as hosted files in CSV format.**Note:** Only URLs, domains, file names, hashes, and IP addresses are extracted.

</td></tr><tr><td>

JSON

</td><td>

Feeds that are available as hosted files in JSON format.**Note:** Only URLs, domains, file names, hashes, and IP addresses are extracted.

</td></tr><tr><td>

RSS

</td><td>

Feeds that are available in RSS format. The application will store the data as RSS Feed Records.

</td></tr><tr><td>

Custom

</td><td>

Feeds that are configured using custom parsers.**Note:** Only URLs, domains, file names, hashes, and IP addresses are extracted.

</td></tr></tbody>
</table>For the next steps in the procedure, refer to the respective section for configuring a each specific feed type. [Threat Intelligence Feeds](threat-intelligence-feeds.md).

-   **[Configure a new threat intelligence feed](../task/tisc-new-data-source.md)**  
Configure new threat intelligence feed.
-   **[Configure Custom Field Mapping](../task/tisc-field-mapping.md)**  
Field Mapping allows you to configure how each field in a data feed such as Text, CSV or JSON is interpreted and assigned to the corresponding observable.
-   **[View Threat Intel Feeds](base-system-threat-intel-feeds.md)**  
This section provides you the threat intel feeds that are configured in the base system.
-   **[Understanding STIX TAXII](threat-intelligence-security-center-feeds.md)**  
Structured Threat Information Expression \(STIX\) is a language and serialization format used to exchange cyber threat intelligence \(CTI\). Trusted Automated Exchange of Intelligence Information \(TAXII\) is a protocol used to exchange cyber threat intelligence \(CTI\) over HTTPS.
-   **[Duplicate threat intelligence feeds](../task/tisc-duplicate-feeds.md)**  
Duplicating a threat feed allows you to create an exact copy of an existing feed, including all associated observables, indicators, actors, and so on.

**Parent Topic:**[Integrate Threat Intelligence Security Center](integrating-threat-intelligence-security-center.md)

**Related topics**  


[Threat Intelligence Security Center Catalog](threat-intelligence-security-center-catalogue.md)

[TISC Integrations](tisc-integrations.md)

