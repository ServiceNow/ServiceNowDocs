---
title: Threat Intelligence Security Center Catalog
description: The Threat Intelligence Security Center Catalog is a curated list of Threat Intelligence feeds and enrichment integrations available in the application. You can enable them after adding the required information and schedule the feed to automatically ingest Threat Intelligence data on a set frequency.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrate, Threat Intelligence Security Center, Security Operations]
---

# Threat Intelligence Security Center Catalog

The Threat Intelligence Security Center Catalog is a curated list of Threat Intelligence feeds and enrichment integrations available in the application. You can enable them after adding the required information and schedule the feed to automatically ingest Threat Intelligence data on a set frequency.

As a sn\_sec\_tisc.admin, you can search and edit existing source configurations, enable or disable them, and delete configurations from the Catalog. When you add a data source to the Catalog, it appears as a new configuration card.

Role required:

-   sn\_sec\_tisc.admin \(create/update\)
-   sn\_sec\_tisc.analyst \(read\)

![TISC Catalog](../image/tisc-catolog.png)

**Note:** The cards on the catalog are differentiated by their label at the top of the card: **Threat Feed/Enrichment**.

## Actions on the Catalog view

You can perform the following actions:

<table id="table_ols_yx1_nzb"><thead><tr><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Filter items

</td><td>

Use this **dropdown menu** to filter feeds and integrations based on their current state. You can filter based on the following states:-   **All**: Displays all the feeds and integrations on the page. This is the default option.
-   **Enabled**: Displays all the feeds and integrations that are in an enabled state.
-   **Disabled**: Displays all the feeds and integrations that are in an inactive state.
-   **Draft**: Displays all the feeds and integrations that are in a draft state.

</td></tr><tr><td>

Refresh list

</td><td>

Use the refresh icon ![Refresh](../image/enrich-refresh-icon.png) to refresh the list.

</td></tr><tr><td>

![Sort](../image/enrich-sort-icon.png)

</td><td>

Use this action to sort all the feeds and integrations based on the following:-   **Last Modified \(recent\)**
-   **Last Modified \(oldest\)**
-   **Name \(A-Z\)**
-   **Name \(Z-A\)**

</td></tr><tr><td>

Search in catalog

</td><td>

Use this action to search for feeds and integrations based on the name and description within the catalog.

</td></tr></tbody>
</table>**Parent Topic:**[Integrate](integrating-threat-intelligence-security-center.md)

**Related topics**  


[Threat Intelligence Feeds](threat-intelligence-feeds.md)

[TISC Integrations](tisc-integrations.md)

