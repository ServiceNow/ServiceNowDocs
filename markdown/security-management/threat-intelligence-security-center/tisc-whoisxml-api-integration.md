---
title: Configure and enable Whois integration
description: Before you use the Whois integration, you must download it from the ServiceNow Store, and must have a valid account from Whois.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/threat-intelligence-security-center/tisc-whoisxml-api-integration.html
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Whois integration, Configure Observable Enrichment, TISC Enrichment Integrations, TISC Integrations, Integrate, Threat Intelligence Security Center, Security Operations]
---

# Configure and enable Whois integration

Before you use the Whois integration, you must download it from the ServiceNow Store, and must have a valid account from Whois.

## Before you begin

Role required: sn\_sec\_tisc.admin

The Threat Intelligence Security Center and Whois observable integration plugins are required.

## Procedure

1.  Using your instance, access **Threat Intelligence Security Center**.

2.  [Download the integration from the ServiceNow Store](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/download-app-first-time.md).

3.  When the installation is complete, navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

4.  Select **Integrations** &gt; **Enrichment Integrations** &gt; **All Integrations**.

5.  Alternatively, you can navigate to **Integrations** &gt; **Enrichment Integrations** &gt; **All Integrations** &gt; **Observable Enrichment**.

6.  In the **WHOIS** card, click **Configure New Enrichment** to configure **WHOIS** integration.

7.  Fill in the fields on the Configure New Enrichment form.

    |Field|Description|
    |-----|-----------|
    |Name|Enter a name for the new enrichment integration. For example, WHOIS.|
    |Vendor Name|Name of the vendor. The details of the selected vendor is populated by default. For example, WHOIS.|
    |Integration Type|Type of integration that you selected. For example, Threat Lookup.|
    |Description|Enter the description for the new enrichment integration. For example, the description for WHOIS integration is, The WHOIS Integration for Threat Intelligence Security Center enables users to submit Whois lookups on domain names and URLs to obtain context on URL observables, and to make better determination on threats.|

8.  Drill down to **Integration Configuration** section.

9.  Enter \(or paste\) the **API Key** you acquired from the WHOIS site.

10. Click **Save**.

    The integration details are validated, and by default the WHOIS integration's status is disabled.

11. Click **Enable** to enable the WHOIS integration.


## Result

After it is configured, WHOIS can be selected for performing enrichments on observables in Threat Intelligence Security Center.

**Parent Topic:**[Whois integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/threat-intelligence-security-center/tisc-whoisxml-integration.md)

