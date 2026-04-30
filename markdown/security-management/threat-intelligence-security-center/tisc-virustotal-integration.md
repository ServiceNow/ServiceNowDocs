---
title: Configure and Enable VirusTotal Integration
description: Before you can use the VirusTotal integration, you must download it from the ServiceNow Store.
locale: en-US
release: xanadu
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [TISC VirusTotal integration, Threat Lookup, TISC Enrichment Integrations, TISC Integrations, Integrating Threat Intelligence Security Center, Threat Intelligence Security Center, Security Operations]
---

# Configure and Enable VirusTotal Integration

Before you can use the VirusTotal integration, you must download it from the ServiceNow Store.

## Before you begin

Role required: sn\_sec\_tisc.admin

The Threat Intelligence Security Center plugin is required in order to activate VirusTotal integration.

## Procedure

1.  Using your instance, access **Threat Intelligence Security Center**.

2.  [Download the integration from the ServiceNow Store](../../security-incident-response/reference/download-app-first-time.md).

3.  When the installation is complete, access VirusTotal and obtain the API Key under your VirusTotal profile.

4.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

5.  Select **Integrations** &gt; **Enrichment Integrations** &gt; **All Integrations**.

6.  Alternatively, you can navigate to **Integrations** &gt; **Enrichment Integrations** &gt; **All Integrations** &gt; **Threat Lookup**

7.  Click **Configure New Enrichment** to configure **VirusTotal** integration.

8.  Fill in the fields on the Configure New Enrichment form.

    |Field|Description|
    |-----|-----------|
    |Name|Enter a name for the new enrichment integration. For example, VirusTotal.|
    |Vendor Name|Name of the vendor. The details of the selected vendor is populated by default. For example, VirusTotal.|
    |Integration Type|Type of integration that you selected. For example, Threat Lookup.|
    |Description|Enter the description for the new enrichment integration.|

9.  Drill down to **Integration Configuration** section.

10. Enter \(or paste\) the **API Key** you acquired from the VirusTotal site.

11. Click **Save**.

    The integration details are validated, and by default the VirusTotal integration's status is disabled.

12. Click **Enable** to enable the VirusTotal integration.


## Result

After it is configured, VirusTotal can be selected for performing lookups on observables in Threat Intelligence Security Center.

**Parent Topic:**[TISC VirusTotal integration](../concept/tisc-virustotal-integration_0.md)

