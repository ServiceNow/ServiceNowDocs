---
title: Configure and enable Shodan integration
description: Before you use Shodan integration, you must download it from the ServiceNow Store.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Shodan integration, Configure Observable Enrichment, TISC Enrichment integrations, TISC Integrations, Integrate, Threat Intelligence Security Center, Security Operations]
---

# Configure and enable Shodan integration

Before you use Shodan integration, you must download it from the ServiceNow Store.

## Before you begin

Role required: sn\_sec\_tisc.admin

**Important:** The Threat Intelligence Security Center and Whois Observable Enrichment plugins must be installed and active.

Download the Whois integration from the ServiceNow Store and verify you have a valid Whois account before use. For more information see, [Download the integration from the ServiceNow Store](../../security-incident-response/reference/download-app-first-time.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Integrations** &gt; **Enrichment Integrations** &gt; **All Integrations** &gt; **Observable Enrichment**.

2.  In the **Shodan** card, select **Configure New Enrichment** to configure the integration.

3.  Complete the Configure New Enrichment form.

<table id="table_iqf_n4p_tzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the new enrichment integration. For example, Shodan.

</td></tr><tr><td>

Vendor Name

</td><td>

Name of the vendor.The details of the selected vendor are auto-populated and by default this field will be read only. For example, Shodan.

</td></tr><tr><td>

Integration Type

</td><td>

Type of integration that you selected. For example, Observable Enrichment.

</td></tr><tr><td>

Description

</td><td>

Description for the new enrichment integration.For example, the description for Shodan integration is, Shodan helps you to analyze banner information from connected devices all around the globe.

</td></tr></tbody>
</table>4.  Navigate to the **Integration Configuration** section.

5.  Enter \(or paste\) the **API Key** you acquired from the Shodan portal.

6.  Select **Save** to apply the changes.

    The integration details are validated, and by default the status is inactive.

7.  Select **Enable** to enable the integration.


## Result

After configuration, Shodan can be selected for performing enrichment on observables in Threat Intelligence Security Center.

**Parent Topic:**[Shodan integration](tisc-shodan.md)

**Related topics**  


[Configure Observable Enrichment](configure-observable-enrichment.md)

