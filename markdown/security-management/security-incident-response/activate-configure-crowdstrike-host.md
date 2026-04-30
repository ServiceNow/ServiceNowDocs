---
title: Get started with the CrowdStrike Falcon Host integration
description: The Integration Configuration feature allows you to quickly activate and set up third-party security integrations, including the CrowdStrike Falcon Host integration. Before you can use the CrowdStrike Falcon Host integration, you must download it from the ServiceNow Store and then add a user name and password.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [CrowdStrike Falcon Host integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Get started with the CrowdStrike Falcon Host integration

The Integration Configuration feature allows you to quickly activate and set up third-party security integrations, including the CrowdStrike Falcon Host integration. Before you can use the CrowdStrike Falcon Host integration, you must download it from the ServiceNow Store and then add a user name and password.

## Before you begin

-   If you are upgrading CrowdStrike Falcon Host integration from a previous version, then you must delete the existing configuration and set up a new configuration. The new integration supports OAUTH2 authentication. This update requires you to enter the **API Client ID** and the **API Client Secret** to authenticate and complete the configuration.
-   In the CrowdStrike Falcon Host portal **API Scopes**, enable the **Read** and **Write** setting for **IOCs \(Indicators of Compromise\)**.

Role required: sn\_si\_admin

## Procedure

1.  [Download the integration from the ServiceNow Store](../../../security-incident-response/reference/download-app-first-time.md).

2.  When the installation is complete, navigate to **Security Operations** &gt; **Integrations** &gt; **Integration Configurations**.

    The available security integrations appear as a series of cards.

3.  In the CrowdStrike Falcon Host card, click **Configure**.

4.  On the form, fill in the fields to complete the configuration:

<table id="table_ifn_tlk_mnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Name**

</td><td>

Name of the integration, for example, `demo-1`.

</td></tr><tr><td>

**API Client ID**

</td><td>

The client ID that you obtain from the settings section of your account profile in CrowdStrike Falcon Host portal.

</td></tr><tr><td>

**API Client Secret**

</td><td>

The client secret key that you obtain from the settings section of your account profile in CrowdStrike Falcon Host portal.

</td></tr></tbody>
</table>5.  Click **Submit**.


## Result

After it is configured, the CrowdStrike Falcon Host integration can be selected for publishing observables to watchlists in Security Incident Response.

