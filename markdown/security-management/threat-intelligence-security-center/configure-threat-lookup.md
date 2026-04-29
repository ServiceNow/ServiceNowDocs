---
title: Configure Threat Lookup
description: You can configure the threat lookup to perform a lookup on selected observables. If the observables are of a type recognized by Threat Intelligence, the observables are scanned for malware, and the results are returned. You can perform threat lookup on one or more observables to determine maliciousness of an observable.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Sighting Search, TISC Enrichment integrations, TISC Integrations, Integrate, Threat Intelligence Security Center, Security Operations]
---

# Configure Threat Lookup

You can configure the threat lookup to perform a lookup on selected observables. If the observables are of a type recognized by Threat Intelligence, the observables are scanned for malware, and the results are returned. You can perform threat lookup on one or more observables to determine maliciousness of an observable.

## Before you begin

Role required: sn\_sec\_tisc.admin

**Note:** Enrichment Integrations module is only shown if at least one of the integration supporting any of the capability is installed in the application.

The Threat Intelligence Security Center supports Threat Lookup only for the following integrations:

-   VirusTotal
-   CrowdStrike Intelligence

For more information, see [Threat Lookup](../concept/tisc-threat-lookup.md).

## About this task

The Threat Lookup section contains only the integrations with the integration type as threat lookup.

This section displays cards for each of the configured integration implementations that you can activate and use.

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Click the **Integrations** icon, and select the **Threat Lookup** section.

    ![Threat Lookup integrations](../image/enrich-threatlook.png)

3.  Click the **Configure new enrichment** action.

    This takes you to the pop-up that displays the available integrations. You need to choose the integration that you need to configure.

4.  Select and integration from the list of available integrations, and click **Select**.

    This takes you to the Create New Enrichment Integration page of the selected integration. This page is pre-filled with details of the selected integration by default. For example, VirusTotal integration.

    ![Select and integration from the list of available integrations](../image/enrich-threat-config.png)

5.  On the Create New Integration form, fill the fields.

    |Field|Description|
    |-----|-----------|
    |**Name**|Enter a name for the new enrichment integration. For example, `VirusTotal-1`.|
    |**Vendor Name**|Name of the vendor. The details of the selected vendor is pre-filled by default. For example, `VirusTotal`.|
    |**Integration Type**|Type of integration that you selected, which is Threat Lookup. The details of the selected integration type is pre-filled by default.|
    |**Description**|Enter a unique description for the new enrichment integration.|

    ![Create new enrichment integration form](../image/enrich-threatlook-new.png)

6.  In the Integration Configuration section, configure the integration details based on your requirements.

    The Integration Configuration section includes configuration details like API key, API Client ID or secret, username, password, and so on, which you need to fill in. These configuration details vary for different apps.

7.  Click the **Save** action to store and create the new enrichment integration configuration.

    The provided details are validated, and by default the enrichment integration's status is disabled.

8.  Click **Save as Draft** action to only store the updates made to the enrichment configuration and not create it.

    If you're not sure about the configuration details, you can use the **Save as Draft** option. After you get the configuration details, you can fill the remaining information in the draft version and create it.

9.  To enable the enrichment integration, click **Enable**.

    The enrichment integration is enabled successfully. You can also enable, disable, or delete a particular enrichment integration by using the Actions menu of the required integration tile on the Catalog page or the Enrichment Integrations page.


-   **[View Threat Lookup Reputation Calculators](view-threat-lookup-reputation-calculators.md)**  
You can view the Threat Lookup Finding Calculator to calculate the observable findings for your integration.

**Parent Topic:**[Sighting Search](../concept/tisc-sighting-search.md)

