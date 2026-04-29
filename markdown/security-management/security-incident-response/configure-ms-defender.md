---
title: Install and Configure
description: Install and Configure Microsoft Defender integration from the ServiceNow Store to control how incidents are retrieved, processed, and converted into security incidents within SIR.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Microsoft Defender integration for Security Operations, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Install and Configure

Install and Configure Microsoft Defender integration from the ServiceNow® Store to control how incidents are retrieved, processed, and converted into security incidents within SIR.

## Before you begin

Role required: sn\_si.admin, sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin because this role inherits the required permissions by default.

## Procedure

1.  Download **Microsoft Defender** integration from the ServiceNow® Store and install it.

2.  Navigate to **All** &gt; **Security Operations** &gt; **Integrations** &gt; **Integration Configurations**.

3.  Search for **Microsoft Defender-Incident Ingestion Configuration** tile, and select **Configure**.

4.  On the form, fill in the fields.

<table id="table_evw_xjl_gxc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the Microsoft Defender integration.

</td></tr><tr><td>

Cloud Environment

</td><td>

Isolated instance of Microsoft Defender cloud services configured to meet specific requirements such as data residency, security, compliance, and regulatory standards.Options include: GLOBAL, US-GOV-GCC-HIGH, US-GOV-DOD, CHINA

</td></tr><tr><td>

Tenant ID

</td><td>

Microsoft Defender Tenant ID. Instance from which all the incidents in the Microsoft portal are retrieved.

</td></tr><tr><td>

Client ID

</td><td>

Client ID of the application registered in the Microsoft portal.Roles required in Defender include:

-   SecurityIncident.Read.All
-   SecurityIncident.ReadWrite


</td></tr><tr><td>

Client Secret

</td><td>

Client secret of your registered application in the Microsoft portal.

</td></tr></tbody>
</table>5.  Select **Submit**.

    The configured integration tile displays.


## What to do next

[Create an incident profile](ms-defender-profile.md)

