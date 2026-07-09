---
title: Configure CrowdStrike EDR integration
description: Before you can use the CrowdStrike Falcon EDR integration, you must download it from the ServiceNow Store Store and add the appropriate Client ID and Client Secret.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/threat-intelligence-security-center/config-cs-edr-integration.html
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [CrowdStrike Falcon EDR integration, TISC Security Tools Integrations, TISC Integrations, Integrate, Threat Intelligence Security Center, Security Operations]
---

# Configure CrowdStrike EDR integration

Before you can use the CrowdStrike Falcon EDR integration, you must download it from the ServiceNow Store Store and add the appropriate Client ID and Client Secret.

## Before you begin

Role required: sn\_sec\_tisc.admin

**Important:**

-   Threat Intelligence Security Center application must be installed and activated.
-   Obtain the API Client ID and API Client Secret from CrowdStrike Falcon console.
-   In the CrowdStrike Falcon portal API Scopes, enable the **IOC Management: read and write access**.

## Procedure

1.  In your instance, access **Threat Intelligence Security Center**.

2.  [Download the integration from the ServiceNow Store](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/download-app-first-time.md).

3.  Select **Integrations** &gt; **Security Tools** &gt; **EDR**.

4.  Select **Configure New Security Tool** to configure CrowdStrike Falcon EDR integration.

5.  Select **CrowdStrike Falcon EDR**.

6.  On the Configure new security tool form, fill in the fields.

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

Integration type.

</td></tr><tr><td>

Integration Category

</td><td>

Integration category.

</td></tr><tr><td colspan="2">

**Integration Configuration**

</td></tr><tr><td>

Base URL

</td><td>

CrowdStrike API base URL. The default value is [https://api.crowdstrike.com](https://api.crowdstrike.com). For more information, see [https://falcon.crowdstrike.com/documentation/page/a2a7fc0e/crowdstrike-oauth2-based-apis\#k9578c40](https://falcon.crowdstrike.com/documentation/page/a2a7fc0e/crowdstrike-oauth2-based-apis#k9578c40)

</td></tr><tr><td>

Client ID

</td><td>

Client ID from CrowdStrike. For more information, see [https://falcon.crowdstrike.com/documentation/page/a2a7fc0e/crowdstrike-oauth2-based-apis](https://falcon.crowdstrike.com/documentation/page/a2a7fc0e/crowdstrike-oauth2-based-apis).

</td></tr><tr><td>

Client Secret

</td><td>

Client secret key from CrowdStrike. For more information, see [https://falcon.crowdstrike.com/documentation/page/a2a7fc0e/crowdstrike-oauth2-based-apis](https://falcon.crowdstrike.com/documentation/page/a2a7fc0e/crowdstrike-oauth2-based-apis).

</td></tr><tr><td>

Expiration period in days for any type of observables

</td><td>

Expiry period in days applied to observables sent to CrowdStrike EDR.**Note:** This option is a fall back expiration period when the expiration time is not set for any specific observable type.

</td></tr><tr><td>

IP Observable Expiration Time

</td><td>

Expiry period in days applied to IP observables sent to CrowdStrike EDR.

</td></tr><tr><td>

Domain Observable Expiration Time

</td><td>

Expiry period in days applied to domain observables sent to CrowdStrike EDR.

</td></tr><tr><td>

Hash Observable Expiration Time

</td><td>

Expiry period in days applied to Hash observables sent to CrowdStrike EDR.

</td></tr></tbody>
</table>7.  Select **Save**.

    The integration details are validated, and by default the CrowdStrike EDR integration's status is turned off.

8.  Select **Enable** to enable the CrowdStrike EDR integration.

    **Note:** Multiple configurations are allowed for CrowdStrike Falcon EDR integration.


**Parent Topic:**[CrowdStrike Falcon EDR integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/threat-intelligence-security-center/crowdstrike-edr-integration.md)

**Related topics**  


[Send observables to EDR](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/threat-intelligence-security-center/send-to-edr.md)

