---
title: Configure and enable Whois integration
description: Set up WHOIS integration with TISC to perform domain and URL lookups for threat intelligence enrichment. This integration provides context on observables to help determine potential threats.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Whois integration, Configure Observable Enrichment, TISC Enrichment integrations, TISC Integrations, Integrate, Threat Intelligence Security Center, Security Operations]
---

# Configure and enable Whois integration

Set up WHOIS integration with TISC to perform domain and URL lookups for threat intelligence enrichment. This integration provides context on observables to help determine potential threats.

## Before you begin

Role required: sn\_sec\_tisc.admin

**Important:** The Threat Intelligence Security Center and Whois Observable Enrichment plugins must be installed and active.

Download the Whois integration from the ServiceNow Store and confirm you have a valid Whois account before use. For more information see, [Download the integration from the ServiceNow Store](../../security-incident-response/reference/download-app-first-time.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Integrations** &gt; **Enrichment Integrations** &gt; **All Integrations** &gt; **Observable Enrichment**.

2.  In the **WHOIS** card, select **Configure New Enrichment** to configure **WHOIS** integration.

3.  Fill in the fields on the Configure New Enrichment form.

<table id="table_iqf_n4p_tzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a name for the new enrichment integration. For example, Whois.

</td></tr><tr><td>

Vendor Name

</td><td>

Name of the vendor. The details of the selected vendor populate by default. For example, Whois.

</td></tr><tr><td>

Integration Type

</td><td>

Type of integration that you selected. For example, Threat Lookup.

</td></tr><tr><td>

Description

</td><td>

Enter the description for the new enrichment integration.For example, the description for Whois integration is, The Whois Integration for Threat Intelligence Security Center enables users to submit Whois lookups on domain names and URLs to obtain context on URL observables, and to make better determination on threats.

</td></tr></tbody>
</table>4.  Drill down to **Integration Configuration** section.

5.  Enter \(or paste\) the **API Key** you acquired from the Whois site.

6.  Select **Save** to apply the changes.

    The integration details are validated, and by default the Whois integration's status is inactive.

7.  Select **Enable** to enable the Whois integration.


## Result

After it is configured, Whois can be selected for performing enrichment on observables in Threat Intelligence Security Center.

**Parent Topic:**[Whois integration](../concept/tisc-whoisxml-integration.md)

**Related topics**  


[Configure Observable Enrichment](configure-observable-enrichment.md)

