---
title: Configure Threat Lookup
description: Scan selected observables for malware using Threat Intelligence to determine if they are malicious. Use this lookup to assess security threats from IP addresses, URLs, file hashes, and other observable types.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [TISC Enrichment integrations, TISC Integrations, Integrate, Threat Intelligence Security Center, Security Operations]
---

# Configure Threat Lookup

Scan selected observables for malware using Threat Intelligence to determine if they are malicious. Use this lookup to assess security threats from IP addresses, URLs, file hashes, and other observable types.

## Before you begin

Role required: sn\_sec\_tisc.admin

**Note:** The Enrichment Integrations module appears only if at least one integration supporting any capability is installed in the application.

The Threat Intelligence Security Center supports Threat Lookup only for the following integrations:

-   VirusTotal
-   CrowdStrike Intelligence

For more information, see [Threat Lookup](../concept/tisc-threat-lookup.md).

## About this task

The Threat Lookup section contains only the integrations with the integration type as threat lookup.

This section displays cards for each of the configured integration implementations that you can activate and use.

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Select the **Integrations** icon, and select the **Threat Lookup** section.

    ![Threat Lookup integrations](../image/enrich-threatlook.png)

3.  Select the **Configure new enrichment** action.

    A pop-up displays the available integrations.

4.  Select an integration from the list of available integrations, and select **Select**.

    The Create Enrichment Integration page opens with pre-filled details for the selected integration.

    ![Select an integration from the list of available integrations](../image/enrich-threat-config.png)

5.  On the Create Integration form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |**Name**|Enter a name for the new enrichment integration. For example, `VirusTotal-1`.|
    |**Vendor Name**|Name of the vendor. This field is automatically set to the selected vendor. For example, `VirusTotal`.|
    |**Integration Type**|Type of integration. This field is automatically set to Threat Lookup.|
    |**Description**|Enter a unique description for the new enrichment integration.|

    ![Create enrichment integration form](../image/enrich-threatlook-new.png)

6.  In the Integration Configuration section, configure the integration details based on your requirements.

    The Integration Configuration section includes configuration details like API key, API Client ID or secret, username, and password. These configuration details vary for different apps.

7.  Select the **Save** action to store and create the new enrichment integration configuration.

    The system validates the provided details and sets the enrichment integration status to inactive by default.

8.  Select **Save as Draft** action to only store the updates made to the enrichment configuration and not create it.

    If you aren't sure about the configuration details, you can use the **Save as Draft** option. After you get the configuration details, you can fill the remaining information in the draft version and create it.

9.  To enable the enrichment integration, select **Enable**.

    The system enables the enrichment integration. You can also enable, disable, or delete a particular enrichment integration by using the Actions menu of the required integration tile on the Catalog page or the Enrichment Integrations page.


-   **[View Threat Lookup Reputation Calculators](view-threat-lookup-reputation-calculators.md)**  
You can view the Threat Lookup Finding Calculator to calculate the observable findings for your integration.

**Parent Topic:**[TISC Enrichment integrations](../concept/tisc-enrichment-integrations.md)

**Related topics**  


[View Threat Lookup Reputation Calculators](view-threat-lookup-reputation-calculators.md)

