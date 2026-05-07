---
title: Configure and enable CrowdStrike Falcon Intelligence integration
description: Set up CrowdStrike Falcon Intelligence integration to perform threat lookups on observables in Threat Intelligence Security Center.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [TISC CrowdStrike Falcon Intelligence integration, Threat Lookup, TISC Enrichment integrations, TISC Integrations, Integrate, Threat Intelligence Security Center, Security Operations]
---

# Configure and enable CrowdStrike Falcon Intelligence integration

Set up CrowdStrike Falcon Intelligence integration to perform threat lookups on observables in Threat Intelligence Security Center.

## Before you begin

Role required: sn\_sec\_tisc.admin

**Note:** The Threat Intelligence Security Center and VirusTotal Threat Lookup plugins must be installed and active.

Download the VirusTotal integration from the ServiceNow Store. Confirm you have a valid VirusTotal account before use. For more information, see [Download the integration from the ServiceNow Store](../../security-incident-response/reference/download-app-first-time.md).

## About this task

This integration requires downloading the app from the ServiceNow Store and configuring API credentials from your CrowdStrike account.

Obtain the API Client ID and API Client Secret under your CrowdStrike Falcon Intelligence profile. In the CrowdStrike Falcon Intelligence portal API Scopes, enable the **Read** setting for Indicators \(Falcon Intelligence\).

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Integrations** &gt; **Enrichment Integrations** &gt; **All Integrations** &gt; **Threat Lookup**.

2.  Select **Configure New Enrichment** to configure **CrowdStrike Falcon Intelligence** integration.

3.  Fill in the fields on the Configure New Enrichment form.

    |Field|Description|
    |-----|-----------|
    |Name|Name for the new enrichment integration. For example, CrowdStrike Falcon Intelligence.|
    |Vendor Name|Name of the vendor. The details of the selected vendor is populated by default. For example, CrowdStrike Falcon Intelligence.|
    |Integration Type|Type of integration that you selected. For example, Threat Lookup.|
    |Description|Description for the new enrichment integration.|
    |**Integration Configuration**|
    |Client ID|The client ID that you obtained from CrowdStrike.|
    |Client Secret|The client secret key that you obtained from CrowdStrike.|

4.  Select **Save** to apply the changes.

    The integration details are validated, and by default the CrowdStrike Falcon Intelligence integration's status is inactive.

5.  Select **Enable** to enable the CrowdStrike Falcon Intelligence integration.


## Result

After you configure it, CrowdStrike Falcon Intelligence can be selected for performing lookups on observables in Threat Intelligence Security Center.

**Parent Topic:**[TISC CrowdStrike Falcon Intelligence integration](../concept/tisc-crowdstrike-falcon-intelligence-integration.md)

**Related topics**  


[Threat Lookup](../concept/tisc-threat-lookup.md)

[Configure and enable VirusTotal Integration](tisc-virustotal-integration.md)

