---
title: Install and configure CrowdStrike Next-Gen SIEM integration
description: Install and configure the CrowdStrike Next-Gen SIEM integration for Security Operations application from the ServiceNow Store on your ServiceNow AI Platform instance.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-06-05"
reading_time_minutes: 1
breadcrumb: [CrowdStrike Next-Gen SIEM integration for Security Operations, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Install and configure CrowdStrike Next-Gen SIEM integration

Install and configure the CrowdStrike Next-Gen SIEM integration for Security Operations application from the ServiceNow Store on your ServiceNow AI Platform instance.

## Before you begin

Role required: sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin because this role inherits the required permissions by default.

## Procedure

1.  Download the CrowdStrike Next-Gen SIEM integration from the ServiceNow Store and install it.

    For more information, see [Download an application from the ServiceNow Store for the first time](../../../security-incident-response/reference/download-app-first-time.md)

2.  Navigate to **Security Operations** &gt; **Integrations** &gt; **Integration Configurations**.

3.  Search for the CrowdStrike Next-Gen SIEM integration tile, and select **Configure**.

4.  On the form, fill in the fields.

<table id="table_evw_xjl_gxc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the CrowdStrike Next-Gen SIEM integration.

</td></tr><tr><td>

Client ID

</td><td>

The client ID that you obtain from the settings section of your account profile in the CrowdStrike portal.

</td></tr><tr><td>

Client Secret

</td><td>

The client secret key that you obtain from the settings section of your account profile in the CrowdStrike portal.

</td></tr><tr><td>

Region

</td><td>

Data center to pull data from. Specify the Region: US-1, US-2, EU-1, US-GOV-1, US-GOV-2By default, the field is set to US-1

</td></tr></tbody>
</table>5.  Select **Submit**.

    The configured integration tile displays.


## What to do next

[Create a detection profile for CrowdStrike Next-Gen SIEM](create-a-profile-cs-ng-siem.md)

