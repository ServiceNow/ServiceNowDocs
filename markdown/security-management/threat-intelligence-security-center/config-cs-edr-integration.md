---
title: Configure Crowdstrike Falcon EDR integration
description: Download and configure the CrowdStrike Falcon EDR integration to enable endpoint detection and response capabilities in your ServiceNow instance.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-04-21"
reading_time_minutes: 2
breadcrumb: [CrowdStrike Falcon EDR integration, TISC Security Tools integrations, TISC Integrations, Integrate, Threat Intelligence Security Center, Security Operations]
---

# Configure Crowdstrike Falcon EDR integration

Download and configure the CrowdStrike Falcon EDR integration to enable endpoint detection and response capabilities in your ServiceNow instance.

## Before you begin

Role required: sn\_sec\_tisc.admin

**Important:**

-   Threat Intelligence Security Center application must be installed and activated.
-   Obtain the API Client ID and API Client Secret from CrowdStrike Falcon console.
-   In the CrowdStrike Falcon portal API Scopes, enable the **IOC Management: read and write access**.

## Procedure

1.  Navigate to **Threat Intelligence Security Center**.

2.  [Download the integration from the ServiceNow Store](../../security-incident-response/reference/download-app-first-time.md).

3.  Select **Integrations** &gt; **Security Tools** &gt; **EDR**.

4.  Select **Configure New Security Tool** to configure CrowdStrike Falcon EDR integration.

5.  Select **CrowdStrike Falcon EDR**.

6.  On the Configure new security tool form, fill in the fields as appropriate.

<table id="table_iqf_n4p_tzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the new security tool integration. For example, CrowdStrike Falcon EDR.

</td></tr><tr><td>

Vendor Name

</td><td>

Name of the vendor. The details of the selected vendor are populated by default. For example, CrowdStrike Falcon EDR.

</td></tr><tr><td>

Description

</td><td>

Description for the new security tool integration.

</td></tr><tr><td>

Integration Type

</td><td>

Type of integration.

</td></tr><tr><td>

Integration Category

</td><td>

Category of integration.

</td></tr><tr><td colspan="2">

**Integration Configuration**

</td></tr><tr><td>

Base URL

</td><td>

The base URL is the CrowdStrike API base URL. The default value is [https://api.crowdstrike.com](https://api.crowdstrike.com). For more information, see [https://falcon.crowdstrike.com/documentation/page/a2a7fc0e/crowdstrike-oauth2-based-apis\#k9578c40](https://falcon.crowdstrike.com/documentation/page/a2a7fc0e/crowdstrike-oauth2-based-apis#k9578c40)

</td></tr><tr><td>

Client ID

</td><td>

The client ID that you obtained from CrowdStrike. For more information, see [https://falcon.crowdstrike.com/documentation/page/a2a7fc0e/crowdstrike-oauth2-based-apis](https://falcon.crowdstrike.com/documentation/page/a2a7fc0e/crowdstrike-oauth2-based-apis).

</td></tr><tr><td>

Client Secret

</td><td>

The client secret key that you obtained from CrowdStrike. For more information, see [https://falcon.crowdstrike.com/documentation/page/a2a7fc0e/crowdstrike-oauth2-based-apis](https://falcon.crowdstrike.com/documentation/page/a2a7fc0e/crowdstrike-oauth2-based-apis).

</td></tr><tr><td>

Expiration period in days for any type of observables

</td><td>

The expiry period in days that is applied for any type of observable\(s\) when they are sent to CrowdStrike EDR.**Note:** This option is a fall back expiration period when the expiration time is not set for any specific observable type.

</td></tr><tr><td>

IP Observable Expiration Time

</td><td>

The expiry period in days that is applied for the IP type of observable when they are sent to CrowdStrike EDR.

</td></tr><tr><td>

Domain Observable Expiration Time

</td><td>

The expiry period in days that is applied for the domain type of observable when they are sent to CrowdStrike EDR.

</td></tr><tr><td>

Hash Observable Expiration Time

</td><td>

The expiry period in days that is applied for the Hash type of observable when they are sent to CrowdStrike EDR.

</td></tr></tbody>
</table>7.  Select **Save** to apply the changes.

    The integration details are validated, and by default the CrowdStrike EDR integration's status is turned off.

8.  Select **Enable** to enable the CrowdStrike EDR integration.

    **Note:** Multiple configurations are allowed for CrowdStrike Falcon EDR integration.


**Parent Topic:**[CrowdStrike Falcon EDR integration](../concept/crowdstrike-edr-integration.md)

**Related topics**  


[Send observables to EDR](send-to-edr.md)

