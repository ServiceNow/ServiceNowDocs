---
title: Install and configure Microsoft Defender for EDR Integration
description: Install and configure the Microsoft Defender for EDR integration from the ServiceNow Store.
locale: en-US
release: xanadu
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2025-04-13"
reading_time_minutes: 2
breadcrumb: [Microsoft Defender for EDR Integration, TISC Security Tools integrations, TISC Integrations, Integrating Threat Intelligence Security Center, Threat Intelligence Security Center, Security Operations]
---

# Install and configure Microsoft Defender for EDR Integration

Install and configure the Microsoft Defender for EDR integration from the ServiceNow Store.

## Before you begin

Role required: sn\_sec\_tisc.admin

-   Threat Intelligence Security Center application must be installed and activated from ServiceNow store.
-   Obtain the API Tenant ID, Client ID, and Client Secret from Microsoft Defender for EDR console.

## Procedure

1.  Download the Microsoft Defender for EDR integration from the ServiceNow Store and install it.

2.  Using your instance, access **Threat Intelligence Security Center**.

3.  [Download the integration from the ServiceNow Store](../../security-incident-response/reference/download-app-first-time.md).

4.  Select **Integrations** &gt; **Security Tools** &gt; **EDR**.

5.  Click **Configure new source tool integration**.

6.  Select **Microsoft Defender for EDR** option.

7.  Click **Select**.

8.  On the form, fill in the following fields.

<table id="table_iqf_n4p_tzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the new security tool integration configuration. For example, Microsoft Defender for EDR integration.

</td></tr><tr><td>

Integration Category

</td><td>

Option that displays the integration category.

</td></tr><tr><td>

Vendor Name

</td><td>

Name of the vendor. The details of the selected vendor is populated by default.

</td></tr><tr><td>

Integration Type

</td><td>

Option that displays the integration type.

</td></tr><tr><td>

Description

</td><td>

Enter the description for the new security tool integration configuration.

</td></tr><tr><td colspan="2">

**Integration Configuration**

</td></tr><tr><td>

Base URL

</td><td>

The base URL is the Microsoft Defender for EDR API base URL. The default value is [https://api.securitycenter.microsoft.com/](https://api.securitycenter.microsoft.com/).

</td></tr><tr><td>

Tenant ID

</td><td>

The tenant ID that you obtained from Microsoft Defender.

</td></tr><tr><td>

Client ID

</td><td>

The client ID that you obtained from Microsoft Defender.

</td></tr><tr><td>

Client Secret

</td><td>

The client secret key that you obtained from Microsoft Defender.

</td></tr><tr><td>

Prefilled title\(used during submission\)

</td><td>

The prefilled title defines the parameters required for submitting indicators to Microsoft Defender.These details are displayed by default, so you don’t need to re-enter them each time you configure the integration.

</td></tr><tr><td>

Prefilled description\(used during submission\)

</td><td>

The prefilled description outlines the required parameters for submitting indicators to Microsoft Defender.These details are displayed by default, so you don’t need to re-enter them each time you configure the integration.

</td></tr><tr><td>

Expiration period in days for any type of observables

</td><td>

The expiry period in days that are applied for any type of observable\(s\) when they are sent to Microsoft Defender EDR.**Note:** This option is a fall back expiration period when the expiration time is not set for any specific observable type.

</td></tr><tr><td>

Expiration period in days for IP type of observables

</td><td>

The expiry period in days that are applied for the IP type of observable when they are sent to Microsoft Defender EDR.

</td></tr><tr><td>

Expiration period in days for Domain type of observables

</td><td>

The expiry period in days that are applied for the domain type of observable when they are sent to Microsoft Defender EDR.

</td></tr><tr><td>

Expiration period in days for Hash type of observables

</td><td>

The expiry period in days that are applied for the Hash type of observable when they are sent to Microsoft Defender EDR.

</td></tr></tbody>
</table>9.  Click **Save** after complete adding the necessary configuration information.

10. Click **Enable** to enable the configuration, after you save the new Microsoft Defender EDR integration.

    A confirmation message is displayed that the enrichment integration is enabled successfully.


## Result

After the integration is configured, You can select the required any type of observable that supports Microsoft Defender EDR from Threat Intel Library.

**Parent Topic:**[Microsoft Defender for EDR Integration](../concept/tisc-ms-defender-integration.md)

