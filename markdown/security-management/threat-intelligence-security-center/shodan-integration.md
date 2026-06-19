---
title: Configure and enable Shodan integration
description: Before you use Shodan integration, you must download it from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/threat-intelligence-security-center/shodan-integration.html
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Shodan integration, Configure Observable Enrichment, TISC Enrichment Integrations, TISC Integrations, Integrate, Threat Intelligence Security Center, Security Operations]
---

# Configure and enable Shodan integration

Before you use Shodan integration, you must download it from the ServiceNow Store.

## Before you begin

Role required: sn\_sec\_tisc.admin

## Procedure

1.  Using your instance, access **Threat Intelligence Security Center**.

2.  [Download the integration from the ServiceNow Store](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/download-app-first-time.md).

3.  When the installation is complete, navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

4.  Select **Integrations** &gt; **Enrichment Integrations** &gt; **All Integrations**.

5.  Alternatively, you can navigate to **Integrations** &gt; **Enrichment Integrations** &gt; **All Integrations** &gt; **Observable Enrichment**.

6.  In the **Shodan** card, click **Configure New Enrichment** to configure the integration.

7.  Fill in the fields on the Configure New Enrichment form.

    |Field|Description|
    |-----|-----------|
    |Name|Enter a name for the new enrichment integration. For example, Shodan.|
    |Vendor Name|Name of the vendor. The details of the selected vendor is auto populated and by default this field will be read only. For example, Shodan.|
    |Integration Type|Type of integration that you selected. For example, Observable Enrichment.|
    |Description|Enter the description for the new enrichment integration. For example, the description for Shodan integration is, Shodan helps you to analyze banner information from connected devices all around the globe.|

8.  Drill down to **Integration Configuration** section.

9.  Enter \(or paste\) the **API Key** you acquired from the Shodan portal.

10. Click **Save**.

    The integration details are validated, and by default the status is disabled.

11. Click **Enable** to enable the integration.


**Parent Topic:**[Shodan integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/threat-intelligence-security-center/tisc-shodan.md)

