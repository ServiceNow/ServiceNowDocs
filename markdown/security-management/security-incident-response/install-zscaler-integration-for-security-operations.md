---
title: Install and configure Security Incident Response integration with Zscaler
description: Install and configure the Security Incident Response integration with Zscaler internet Access product from the ServiceNow Store to start using the integration on your ServiceNow AI Platform instance.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Security Incident Response integration with Zscaler, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Install and configure Security Incident Response integration with Zscaler

Install and configure the Security Incident Response integration with Zscaler internet Access product from the ServiceNow Store to start using the integration on your ServiceNow AI Platform instance.

## Before you begin

Role required: sn\_si.admin

## Procedure

1.  Download the Security Incident Response integration with Zscaler product from the ServiceNow Store and install it.

2.  Navigate to **Security Operations** &gt; **Integrations** &gt; **Integration Configurations**.

3.  Search for the Security Incident Response integration with Zscaler tile and select **Configure** &gt; **Create new configuration**.

4.  On the form, fill in the fields.

<table id="table_kyc_qbg_p4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Server Name

</td><td>

Zscaler server name. For example, ZSserver.

</td></tr><tr><td>

Active

</td><td>

Indicator that the profile is active.

</td></tr><tr><td>

Order

</td><td>

Flow priority. The value for this field indicates the order of the workflows when two or more profiles share triggering conditions.

 The flow with the lowest number has the highest priority.

To set the order of operation, enter a value. For example, 100, 200, 300, 400.The default is 100.

</td></tr><tr><td>

Zscaler API URL

</td><td>

Base URL that hosts the Zscaler API. For example, `[https://example.zscalerbeta.net](https://example.zscalerbeta.net)`

</td></tr><tr><td>

User Name

</td><td>

User name for the Zscaler Internet Access admin account.

</td></tr><tr><td>

Password

</td><td>

Password for the Zscaler Internet Access admin account.

</td></tr><tr><td>

API Key

</td><td>

API key that you obtained from the Zscaler Internet Access administration portal.**Note:** **The user must have sn\_si.admin role to setup the integration.**

</td></tr></tbody>
</table>    The following example shows the Zscaler configuration page.

    ![Zscaler integration configuration page.](../image/zscaler-configuration.png "ZScaler configuration page")

5.  Select **Validate and Update**.


## Result

After you validate and save this configuration, return to the Zscaler Configurations page.

