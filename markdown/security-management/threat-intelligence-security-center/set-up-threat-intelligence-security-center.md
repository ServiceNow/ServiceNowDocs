---
title: Set up Threat Intelligence Security Center
description: Before you use the Threat Intelligence Security Center, you must download it from the ServiceNow Store.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, Threat Intelligence Security Center, Security Operations]
---

# Set up Threat Intelligence Security Center

Before you use the Threat Intelligence Security Center, you must download it from the ServiceNow Store.

## Roles installed

Review the following information and verify that you’ve completed all the tasks for a smooth integration. Following is the list of different user persona defined to access and work with the application:

-   Threat Intelligence analyst \(sn\_sec\_tisc.analyst\)
-   Threat Intelligence administrator \(sn\_sec\_tisc.admin\)

<table id="table_lfk_hkv_21c"><thead><tr><th>

Setup

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assign and verify the required ServiceNow AI Platform and Threat Intelligence Security Center roles.

</td><td>

The following roles are required for configuration and verification of the expected results:-   As an admin, you must install the TISC application from the ServiceNow Store and assign the role as sn\_sec\_tisc.admin.
-   This sn\_sec\_tisc.admin role performs the following tasks:

    -   Configures the Data Sources to ingest the data. For more information, see [Threat Intelligence Feeds](../concept/threat-intelligence-feeds.md).
    -   Configured the integrations required to enrich observables in TISC. For more information, see [TISC Enrichment integrations](../concept/tisc-enrichment-integrations.md).
    -   Configures data import approvals to import the intelligence data using Import Intelligence. For more information, see [Working with Data Imports](../concept/working-with-data-imports.md).
    -   Configures Threat Score Calculator using required criteria for automatic calculation of Threat Score of observables. For more information, see [Define Threat Score Calculator](../task/threat-score-calculator.md).
    -   Configures required Taxonomies and Taxonomy Values. For more information, see [Creating Taxonomies](../concept/create-taxonomies.md).
    -   Configure the MITRE-ATT&amp;CK repository relevant to your organization. For more information, see [MITRE-ATT&amp;CK Repository](../concept/tisc-mitre-att-ck-framework-overview.md).
**Note:** As a sn\_sec\_tisc.admin, you can also assign the sn\_sec\_tisc.analyst role.

-   The sn\_sec\_tisc.analyst role performs the following tasks:
    -   Views the overview of intelligence data in the TISC Home page. For more information, see [TISC Workspace](../task/view-threat-intelligence-security-center-homepage.md).
    -   Import data into TISC using **Import Intelligence** button in **Threat Library** page. For more information, see [Threat Intelligence Security Center Library](../concept/threat-intelligence-security-center-library.md).
    -   -   Search across the data present in the application using search provided in **Threat Library** page.
-   Manages the data ingested from various sources in **Threat Library**.
-   Performs various enrichment actions on Observables.
-   Creates and manages Cases. For more information, see [Creating cases using Threat Analyst Workbench](../concept/create-cases-using-threat-analyst-workbench.md).

</td></tr></tbody>
</table>## Plugins

<table id="table_d51_dlv_21c"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

This following applications are required to installTISC:-   Security Case Management common workspace components \[com.snc.escm.ws\_commons\].
-   Threat Intelligence Support Common \[com.snc.threat\].
-   Column Level Encryption \(com.glide.encryption\)
-   Large JSON and XML Payload Builder API \(com.glide.streaming\_builder\)
-   Security Support Core \(com.snc.security\_support.core\)

</td><td>

Verify that the ServiceNow core applications that are required to support the integration are installed and activated before you configure this integration.

</td></tr></tbody>
</table>## What to do next

[Set Threat Intelligence Security Center properties](tisc-set-properties.md).

