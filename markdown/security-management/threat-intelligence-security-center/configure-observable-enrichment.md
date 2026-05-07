---
title: Configure Observable Enrichment
description: Enrich one or more observables to identify whether they're associated with known threats. The results are based on the enrichment integrations active in your environment.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-04-27"
reading_time_minutes: 2
breadcrumb: [TISC Enrichment integrations, TISC Integrations, Integrate, Threat Intelligence Security Center, Security Operations]
---

# Configure Observable Enrichment

Enrich one or more observables to identify whether they're associated with known threats. The results are based on the enrichment integrations active in your environment.

## Before you begin

Role required: sn\_sec\_tisc.admin

The Threat Intelligence Security Center supports Observable Enrichment only for the WHOIS Integration currently. For more information, see [Configure and enable Whois integration](tisc-whoisxml-api-integration.md).

**Note:** Enrichment Integrations module is only shown if at least one of the integration supporting any of the capability is installed in the application.

## About this task

The Observable Enrichment section contains only the integrations with the integration type as observable enrichment. This section displays cards for each of the configured integration implementations that you can activate and use.

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Select the **Integrations** icon, and select the **Observable Enrichment** section.

    ![Observable Enrichment integrations](../image/enrich-observables.png)

3.  Select **Configure new enrichment**.

4.  Select an integration from the list of available integrations.

    This takes you to the Create Enrichment Integration page of the selected integration. This page is pre-filled with details of the selected integration by default. For example, WHOIS integration.

    ![Select and integration from the list of available integrations](../image/enrich-observable-config.png)

5.  On the Create Integration form, fill the fields.

    |Field|Description|
    |-----|-----------|
    |**Enrichment Integration**| |
    |**Name**|Enter a name for the new enrichment integration. For example, `WHOIS1`.|
    |**Vendor Name**|Name of the vendor. The details of the selected vendor is pre-filled by default. For example, `WHOIS`.|
    |**Integration Type**|Type of integration that you selected, which is Observable Enrichment. The details of the selected integration type is pre-filled by default.|
    |**Description**|Enter a unique description for the new enrichment integration.|

    ![Create enrichment integration form](../image/enrich-whois-new.png)

6.  In the Integration Configuration section, configure the integration details based on your requirements.

    The Integration Configuration section includes configuration details like API key, API Client ID or secret, username, password, and so on, which you must fill in. These configuration details vary for different apps.

7.  Select the **Save** action to store and create the new enrichment integration configuration.

    After you select the **Save** or **Enable** action, the integration is validated using the given integration configurations. By default, the enrichment integration's status is set to inactive.

8.  Select **Save as Draft** action to only store the updates made to the enrichment configuration and not create it.

    If you're not sure about the configuration details, you can use the **Save as Draft** option. After you get the configuration details, you can fill the remaining information in the draft version and create it.

9.  To enable the enrichment integration, select **Enable**.

    The enrichment integration is enabled successfully. You can also enable, disable, or delete a particular enrichment integration by using the **Actions** menu of the required integration tile on the **Catalog** or the **Enrichment Integrations** page.


-   **[Have I Been Pwned integration](../concept/tisc-hibp-integration.md)**  
The Have I Been Pwned \(HIBP\) integration enables you to enrich email address and domain observables with breach data directly within the TISC.
-   **[Whois integration](../concept/tisc-whoisxml-integration.md)**  
Submit Whois lookups on domain names and URLs to gather threat intelligence and assess potential security risks. Use this integration to obtain registration details, ownership information, and other contextual data for suspicious domains.
-   **[Shodan integration](tisc-shodan.md)**  
Configure Shodan integration to enable automated discovery and analysis of internet-connected devices in your network infrastructure.

**Parent Topic:**[TISC Enrichment integrations](../concept/tisc-enrichment-integrations.md)

