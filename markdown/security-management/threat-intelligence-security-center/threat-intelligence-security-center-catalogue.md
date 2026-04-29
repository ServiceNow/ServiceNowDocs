---
title: Threat Intelligence Security Center Catalog
description: The Threat Intelligence Security Center Catalog is a curated list of Threat Intelligence feeds and enrichment integrations available in the application for you to enable them after adding the required information, and schedule the feed to automatically ingest Threat Intelligence data on a set frequency.
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

The Threat Intelligence Security Center Catalog is a curated list of Threat Intelligence feeds and enrichment integrations available in the application for you to enable them after adding the required information, and schedule the feed to automatically ingest Threat Intelligence data on a set frequency.

As a sn\_sec\_tisc.admin, you can also search and edit the existing source configurations, enable or disable, and delete the configurations from the Catalog. Any new data source is added to the Catalog, that will appear as a new configuration card on the Catalog.

Role required:

-   sn\_sec\_tisc.admin \(create/update\)
-   sn\_sec\_tisc.analyst \(read\)

![TISC Catalog](../image/tisc-catolog.png)

**Note:** The cards on the catalog are differentiated by its label which is present at the top of the card Threat Feed/Enrichment.

## Actions on the Catalog view

The Catalog view enables you to perform the following actions.

<table id="table_ols_yx1_nzb"><thead><tr><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

All

</td><td>

Use this dropdown menu to filter feeds and integrations based on their current state. You can filter based on the following states:-   **All**: Displays all the feeds and integrations on the page. This is the default option.
-   **Enabled**: Displays all the feeds and integrations that are in an enabled state.
-   **Disabled**: Displays all the feeds and integrations that are in a disabled state.
-   **Draft**: Displays all the feeds and integrations that are in a draft state.

</td></tr><tr><td>

![Refresh](../image/enrich-refresh-icon.png)

</td><td>

Use this action to refresh the Catalog.

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

Use this action to search for feeds/ integrations based on the name and description within the catalog.

</td></tr></tbody>
</table>**Parent Topic:**[Integrating Threat Intelligence Security Center](integrating-threat-intelligence-security-center.md)

**Related topics**  


[Threat Intelligence Feeds](threat-intelligence-feeds.md)

[TISC Integrations](tisc-integrations.md)

