---
title: Set up Threat Intelligence Security Center
description: Before you use the Threat Intelligence Security Center, you must download it from the ServiceNow Store.
locale: en-US
release: yokohama
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2025-08-21"
reading_time_minutes: 3
breadcrumb: [Configure, Threat Intelligence Security Center, Security Operations]
---

# Set up Threat Intelligence Security Center

Before you use the Threat Intelligence Security Center, you must download it from the ServiceNow Store.

## Roles installed

Review the following information and verify that you’ve completed all the tasks for a smooth integration. Below is the list of different user persona defined to access and work with the application:

-   Threat Intelligence Analyst \(sn\_sec\_tisc.analyst\)
-   Threat Intelligence Administrator \(sn\_sec\_tisc.admin\)

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
    -   Configured the integrations required for Enriching Observable data in TISC. For more information, see [TISC Enrichment integrations](../concept/tisc-enrichment-integrations.md).
    -   Configures Data Import Approval Roles for importing data using Import Assistant. For more information, see [Working with Data Imports](../concept/working-with-data-imports.md).
    -   Configures Threat Score Calculator using required criteria for automatic calculation of Threat Score of observables. For more information, see [Define Threat Score Calculator](../task/threat-score-calculator.md).
    -   Configures required Taxonomies and Taxonomy Values. For more information, see [Creating Taxonomies](../concept/create-taxonomies.md).
    -   Configure the MITRE ATT&amp;CK repository relevant to your organization. For more information, see [MITRE-ATT&amp;CK Repository](../concept/tisc-mitre-att-ck-framework-overview.md).
**Note:** As a sn\_sec\_tisc.admin, you can also assign the sn\_sec\_tisc.analyst role.

-   The sn\_sec\_tisc.analyst role performs the following tasks:
    -   Views the overview of data in the system using the application homepage. For more information, see [Home page in TISC Workspace](../task/view-threat-intelligence-security-center-homepage.md).
    -   Import data into system using Import Intelligence button in Threat Library Page. For more information, see [Threat Intelligence Security Center Library](../concept/threat-intelligence-security-center-library.md).
    -   -   Searches across the data present in the application using search provided in Threat Library page.
-   Manages the data ingested from various sources in Threat Library.
-   Performs various Enrichment actions on Observables.
-   Creates and Manages Cases. For more information, see [Creating cases using Threat Analyst Workbench](../concept/create-cases-using-threat-analyst-workbench.md).

</td></tr></tbody>
</table>## Granular roles in TISC with scripting access

The following roles provide scripting access to the listed tables:

|Role|Table|
|----|-----|
|sn\_sec\_tisc.integration\_write|sn\_sec\_tisc\_enrichment\_integration|
|sn\_sec\_tisc.rules\_write|sn\_sec\_tisc\_threat\_score\_calculator\_rule|

## Dependency Plugins

<table id="table_d51_dlv_21c"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

This following applications are required for installation of this application:-   Security Case Management common workspace components \[com.snc.escm.ws\_commons\].
-   Threat Intelligence Support Common \[com.snc.threat\].
-   Column Level Encryption \(com.glide.encryption\)
-   Large JSON and XML Payload Builder API \(com.glide.streaming\_builder\)
-   Security Support Core \(com.snc.security\_support.core\)
-   Node map Experience Component \(sn\_node\_map\)
-   Reporting UI Component for Workspace\(sn\_sec\_reporting\)
-   Rich Text Editor Component for Security Operations\(sn\_escm\_rte\)
-   Security Integration Framework\(sn\_sec\_int\)
-   Security Support Common\(sn\_sec\_cmn\)
-   Security Support Orchestration\(sn\_sec\_cmn\_orch\)

</td><td>

Verify that the ServiceNow core applications that are required to support the integration are installed and activated before you configure this integration.

</td></tr></tbody>
</table>