---
title: Configure link unfurling using the Hostname allow list table
description: Use the Hostname allow list \[sys\_cs\_hostname\_allow\_list\] table to identify the list of hosts and domains that can be unfurled.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using link unfurling, Exploring other Virtual Agent features, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Configure link unfurling using the Hostname allow list table

Use the Hostname allow list \[sys\_cs\_hostname\_allow\_list\] table to identify the list of hosts and domains that can be unfurled.

## Before you begin

For security reasons, only the hosts and domains in the Hostname allow list table can be unfurled.

The Hostname allow list table includes the following hosts and domains by default:

-   Instance URL/hostname: &lt;*instance*&gt;.service-now.com or &lt;*customURL*&gt;.com
-   Instance root domain: \*service-now.com or \*.&lt;*yourdomain*&gt;.com
-   servicenow.com
-   \*.youtu.be
-   \*.youtube.com

Role required: admin

## Procedure

1.  Navigate to **All**, and then enter `sys_cs_hostname_allow.list` in the filter.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_std_m3v_ypb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Select this option to enable the host or domain that can be unfurled.

</td></tr><tr><td>

Hostname

</td><td>

Name of the host or domain that can be unfurled. You can use an asterisk \(\*\) to specify a wildcard in the host or domain name.For example, enter `*.domain.com`.

</td></tr><tr><td>

Domain

</td><td>

Domain group. The default is global.

</td></tr></tbody>
</table>4.  Click **Submit**.


**Parent Topic:**[Using link unfurling in Virtual Agent](../concept/va-link-unfurling.md)

