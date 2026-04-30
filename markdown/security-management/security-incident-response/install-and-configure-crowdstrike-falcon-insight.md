---
title: Install and configure CrowdStrike Falcon Insight
description: Install and configure the CrowdStrike Falcon Insight for Security Operations application from the ServiceNow Store on your ServiceNow AI Platform instance.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [CrowdStrike Falcon Insight integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Install and configure CrowdStrike Falcon Insight

Install and configure the CrowdStrike Falcon Insight for Security Operations application from the ServiceNow Store on your ServiceNow AI Platform instance.

## Before you begin

Role required: admin

**Note:** You can associate a capability with only one profile. You can't associate a capability with multiple profiles. When you configure CrowdStrike servers, you can't reuse a CrowdStrike capability with multiple profiles that share the CrowdStrike server. Your profiles can have the same CrowdStrike capability, each profile should use its own CrowdStrike server.

## Procedure

1.  Download the CrowdStrike Falcon Insight for Security Operations integration from the ServiceNow Store and install it.

2.  Navigate to **Security Operations** &gt; **Integrations** &gt; **Integration Configurations**.

3.  Search for the CrowdStrike Falcon Insight for Security Operations integration tile, and click **Configure**.

4.  On the form, fill in the fields to complete the configuration:

<table id="table_evw_xjl_gxc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the integration, for example, `demo-1`.

</td></tr><tr><td>

CrowdStrike Falcon Insight API URL

</td><td>

Base URL that hosts the CrowdStrike API. Enter the URL with the HTTPS protocol. For example, https://api.crowdstrike.com.

</td></tr><tr><td>

Client ID

</td><td>

The client ID that you obtain from the settings section of your account profile in the CrowdStrike Falcon Insight portal.

</td></tr><tr><td>

Client Secret

</td><td>

The client secret key that you obtain from the settings section of your account profile in the CrowdStrike Falcon Insight portal.

</td></tr></tbody>
</table>    ![CrowdStrike Falcon Insight configuration tile.](../image/falcon-insight-configuration-tile.png)

5.  Click **Submit**.


## Result

After the integration is successfully validated and submitted, it’s saved on the Security Integrations page as a tile. You can view the CrowdStrike Falcon Insight module in the application navigator.

