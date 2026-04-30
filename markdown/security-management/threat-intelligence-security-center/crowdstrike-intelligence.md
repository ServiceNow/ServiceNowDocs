---
title: Configure and Enable CrowdStrike Falcon Intelligence integration
description: Before you can use the CrowdStrike Falcon Intelligence, you must download it from the ServiceNow Store and add the appropriate Client ID and Client Secret.
locale: en-US
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [TISC CrowdStrike Falcon Intelligence integration, Threat Lookup, TISC Enrichment Integrations, TISC Integrations, Integrate, Threat Intelligence Security Center, Security Operations]
---

# Configure and Enable CrowdStrike Falcon Intelligence integration

Before you can use the CrowdStrike Falcon Intelligence, you must download it from the ServiceNow Store and add the appropriate Client ID and Client Secret.

## Before you begin

Role required: sn\_sec\_tisc.admin

-   Threat Intelligence Security center application must be installed and activated.
-   Obtain the API Client ID and API Client Secret under your CrowdStrike Falcon Intelligence profile.
-   In the CrowdStrike Falcon Intelligence portal API Scopes, enable the Read setting for Indicators \(Falcon Intelligence\).

## Procedure

1.  Using your instance, access **Threat Intelligence Security Center**.

2.  [Download the integration from the ServiceNow Store](../../security-incident-response/reference/download-app-first-time.md).

3.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

4.  Select **Integrations** &gt; **Enrichment Integrations** &gt; **All Integrations**.

5.  Alternatively, you can navigate to **Integrations** &gt; **Enrichment Integrations** &gt; **All Integrations** &gt; **Threat Lookup**.

6.  Click **Configure New Enrichment** to configure **CrowdStrike Falcon Intelligence** integration.

7.  Fill in the fields on the Configure New Enrichment form.

    |Field|Description|
    |-----|-----------|
    |Name|Enter a name for the new enrichment integration. For example, CrowdStrike Falcon Intelligence.|
    |Vendor Name|Name of the vendor. The details of the selected vendor is populated by default. For example, CrowdStrike Falcon Intelligence.|
    |Integration Type|Type of integration that you selected. For example, Threat Lookup.|
    |Description|Enter the description for the new enrichment integration.|
    |**Integration Configuration**|
    |Client ID|The client ID that you obtained from CrowdStrike.|
    |Client Secret|The client secret key that you obtained from CrowdStrike.|

8.  Click **Save**.

    The integration details are validated, and by default the CrowdStrike Falcon Intelligence integration's status is disabled.

9.  Click **Enable** to enable the CrowdStrike Falcon Intelligence integration.


## Result

After it is configured, CrowdStrike Falcon Intelligence can be selected for performing lookups on observables in Threat Intelligence Security Center.

**Parent Topic:**[TISC CrowdStrike Falcon Intelligence integration](../concept/tisc-crowdstrike-falcon-intelligence-integration.md)

