---
title: Configure proxies when performing MID-less upgrade using a Content Delivery Network \(CDN\)
description: Create proxies for added security when upgrading MID-less agents via a Content Delivery Network \(CDN\). You add proxy servers to the sn\_agent\_proxy table on the ServiceNow instance.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-10-28"
reading_time_minutes: 1
breadcrumb: [ACC installation, ACC deployment - servers, Agent Client Collector, IT Operations Management]
---

# Configure proxies when performing MID-less upgrade using a Content Delivery Network \(CDN\)

Create proxies for added security when upgrading MID-less agents via a Content Delivery Network \(CDN\). You add proxy servers to the sn\_agent\_proxy table on the ServiceNow instance.

## Before you begin

Role required: agent\_client\_collector\_admin

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Package Download Proxies**.

2.  Select **New** to create a new proxy server.

3.  Fill in the fields on the page.

<table id="table_wjh_2ck_dhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A descriptive name to identify the proxy server.

</td></tr><tr><td>

URL

</td><td>

The URL of the proxy server that is accessed when the agent downloads the installer. Enter the URL in the following format: `some.example.com:8800`.

</td></tr><tr><td>

Domain

</td><td>

Select one of the following:-   **leaf**: Select if domain separation is active, and select the leaf domain for the proxy to be used in.
-   **global**: Select if domain separation is not active.


</td></tr><tr><td>

Order

</td><td>

A number indicating which proxy is used first when the agent downloads the installer from the CDN. Lower numbers are used first.

</td></tr><tr><td>

Active

</td><td>

Select for the URL to be invoked.Clear for the URL to be ignored.

</td></tr></tbody>
</table>    If no proxy server is specified, the default of **direct** is invoked, instructing the agent to download the installer directly from the CDN.


