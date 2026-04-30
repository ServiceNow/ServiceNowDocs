---
title: Install and Configure
description: Install and configure Palo Alto Networks XSIAM integration for Security Operations application from the ServiceNow Store on your ServiceNow AI Platform instance.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-11-06"
reading_time_minutes: 1
breadcrumb: [Security Incident Response Integration with Cortex XSIAM by Palo Alto Networks, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Install and Configure

Install and configure Palo Alto Networks XSIAM integration for Security Operations application from the ServiceNow Store on your ServiceNow AI Platform® instance.

## Before you begin

Role required: sn\_si.admin, sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin because this role inherits the required permissions by default.

## Procedure

1.  Download **Security Incident Response Integration with Palo Alto Networks XSIAM** integration from the ServiceNow® Store and install it.

2.  Navigate to **All** &gt; **Security Operations** &gt; **Integrations** &gt; **Integration Configurations**.

3.  Search for **Security Incident Response Integration with Palo Alto Networks XSIAM** tile, and select **Configure**.

4.  On the form, fill in the fields.

<table id="table_evw_xjl_gxc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the Cortex XSIAM integration.

</td></tr><tr><td>

Authorization Key

</td><td>

Secret API key to authenticate XSIAM API requests.

 The Authorization Key should have Instance Administrator role.

</td></tr><tr><td>

Key ID

</td><td>

API key ID associated with the authorization key.

</td></tr><tr><td>

API URL

</td><td>

URL of the XSIAM tenant.

</td></tr></tbody>
</table>5.  Select **Submit**.

    The configured integration tile displays.


## What to do next

[Create an incident profile](pan-cortex-xsiam-profile.md)

