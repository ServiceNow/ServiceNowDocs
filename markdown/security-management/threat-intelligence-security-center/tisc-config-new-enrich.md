---
title: Configure new enrichment
description: Set up threat intelligence enrichment integrations to automatically gather additional context about observables, search for sightings, or perform threat lookups from external security vendors.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-04-27"
reading_time_minutes: 2
breadcrumb: [TISC Enrichment integrations, TISC Integrations, Integrate, Threat Intelligence Security Center, Security Operations]
---

# Configure new enrichment

Set up threat intelligence enrichment integrations to automatically gather additional context about observables, search for sightings, or perform threat lookups from external security vendors.

## Before you begin

Role required: sn\_sec\_tisc.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Select the **Integrations** icon.

    ![Configure new enrichment from All Integrations view](../image/enrich-all-integrations.png)In the **All Integrations** section, select the **Configure new enrichment** action.

3.  Choose an enrichment type from the Configure new enrichment dialog.

    The Configure new enrichment dialog displays three enrichment types: Observable Enrichment, Sighting Search, and Threat Lookup.

    ![Configure the enrichment type](../image/enrich-popup-observables.png)

4.  From the enrichment types, select your preferred option and select **Next**.

    The system displays available integrations.

5.  Select an integration from the list of available integrations.

    The system opens the Create Enrichment Integration page with pre-filled details for the selected integration, such as WHOIS integration.

6.  Complete the Create Integration form fields.

<table id="table_zvp_mjl_bjc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the new enrichment integration. For example, `WHOIS1`.

</td></tr><tr><td>

Vendor Name

</td><td>

Name of the vendor. This field is automatically populated. For example, `WHOIS`.

</td></tr><tr><td>

Integration Type

</td><td>

Type of integration selected, such as Observable Enrichment. This field is automatically populated.The following Integration Types are supported:

-   Observable Enrichment
-   Sighting Search
-   Threat Lookup


</td></tr><tr><td>

Description

</td><td>

Unique description for the new enrichment integration.

</td></tr></tbody>
</table>7.  In the Integration Configuration section, configure the integration details.

    The Integration Configuration section includes details such as API key, API Client ID or secret, username, and password. These details vary for different integrations.

8.  To create the enrichment integration configuration, select **Save**.

    The system validates the provided details and sets the enrichment integration status to inactive by default.

9.  To store the integration configurations as draft only, select **Save as Draft**.

    You cannot enable an integration when it is saved as draft. If you're not sure about the configuration details, you can use the **Save as Draft** option. After you get the configuration details, you can complete the draft version and create it.

10. To enable the enrichment integration, select **Enable**.

    The integration status changes to enabled.

    **Note:** You can also enable, disable, or delete an enrichment integration using the Actions menu on the integration tile.


**Parent Topic:**[TISC Enrichment integrations](../concept/tisc-enrichment-integrations.md)

**Related topics**  


[TISC Security Tools integrations](../concept/tisc-edr-integrations.md)

