---
title: Configure and enable Have I Been Pwned integration
description: Configure API credentials and enrichment behavior through the dedicated Have I Been Pwned \(HIBP\) configuration tile in TISC integration settings.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Have I Been Pwned, HIBP, observable enrichment, integration, breach detection]
breadcrumb: [Have I Been Pwned integration, Configure Observable Enrichment, TISC Enrichment integrations, TISC Integrations, Integrate, Threat Intelligence Security Center, Security Operations]
---

# Configure and enable Have I Been Pwned integration

Configure API credentials and enrichment behavior through the dedicated Have I Been Pwned \(HIBP\) configuration tile in TISC integration settings.

## Before you begin

Role required: sn\_sec\_tisc.admin

Prerequisites

-   The Have I Been Pwned integration depends on the Threat Intelligence Security Center \(TISC\) application. To enrich email and domain observables, verify that the TISC plugin \(`sn_sec_tisc`\) is installed.
-   Obtain a valid API key from the Have I Been Pwned portal before you begin.

## About this task

The HIBP integration is an observable enrichment integration that determines whether a submitted email address or domain name has been part of a publicly known data breach.

When an analyst submits a supported observable, the integration queries the HIBP database and returns breach details, including the total number of breaches found and the type of data compromised.

The integration supports the following observable types:

-   Email address
-   Domain name

**Note:** Before you begin, [Download the integration from the ServiceNow Store](../../security-incident-response/reference/download-app-first-time.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Enrichment Integrations** &gt; **All Integrations** &gt; **Observable Enrichment**.

2.  Select **Configure New Enrichment**.

3.  Select the integration.

    For example, Have I Been Pwned to configure the HIBP integration.

4.  Fill in the fields on the Configure New Enrichment form.

    |Field|Description|
    |-----|-----------|
    |**Enrichment Integration**|
    |Name|Name for the new enrichment integration. For example, Have I Been Pwned.|
    |Integration Category|Integration category that you selected.|
    |Vendor Name|Name of the vendor. The details of the selected vendor is populated by default. For example, Have I Been Pwned.|
    |Integration Type|Type of integration that you selected.|
    |Description|Description for the new enrichment integration.|
    |**Integration Configuration**|
    |API Key|API key that you obtained from the Have I Been Pwned site.|

5.  Navigate to the **Integration Configuration** section.

6.  Enter \(or paste\) the **API Key** you acquired from the Have I Been Pwned site.

7.  Select **Save**.

    The integration details are validated, and by default the Have I Been Pwned integration status is set to inactive.

8.  Select **Enable** to enable the Have I Been Pwned integration.

    **Important:** Only one Have I Been Pwned integration card can exist per instance. Attempting to create a second card results in an error.


## Result

After configuration, you can select Have I Been Pwned for performing enrichment on observables in Threat Intelligence Security Center.

## What to do next

To run observable enrichment, see [Run Have I Been Pwned enrichment integration](tisc-hibp-enrichment-integration.md) for the detailed procedure.

**Parent Topic:**[Have I Been Pwned integration](../concept/tisc-hibp-integration.md)

