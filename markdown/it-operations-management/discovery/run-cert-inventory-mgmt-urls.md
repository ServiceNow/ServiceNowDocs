---
title: Run Certificate Discovery via individual URL scans
description: To initiate certificate discovery through URL scans, you must manually include individual URLs and configure a new certificate Discovery schedule.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Visibility to TLS certificates, Configuring Certificate Inventory and Management, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Run Certificate Discovery via individual URL scans

To initiate certificate discovery through URL scans, you must manually include individual URLs and configure a new certificate Discovery schedule.

## Before you begin

Role required: discovery\_admin or admin

## About this task

Only the certificates that are available on the server during URL scans can be discovered. To confirm the available certificates, use the following command:

`openssl s_client -showcerts -connect <URL>:<PORT> </dev/null`

## Procedure

1.  Navigate to **All** &gt; **Certificate Management** &gt; **Certificate Discovery Source URLS**.

2.  To add individual URLs to the table, select **New**.

    Ensure accurate results by entering URLs in the following format: scheme://host:port. The port is optional, and defaults are used if not provided. For example: https://www.servicenow.com or https://servicenow.com:443, ldaps://myldap.com or ldaps://myldap.com:636.

3.  Create a Discovery schedule with the following fields.

    For more information on setting up your Discovery schedules, see [Schedule a horizontal discovery](t_CreateADiscoverySchedule.md#).

    1.  Select **Discovery**: **Certificates**.

    2.  Select **Certificate Discovery Type**: **URL Certificate Discovery**.

        Keep the batch size as is, unless there is a specific recommendation to change it.

4.  To add or delete other URLs, from the **Certificate URLs** tab, select **Edit**.

5.  Select **Submit**.

6.  Select the checkbox to include URLs from the HTTP\(s\) Endpoint \[cmdb\_ci\_endpoint\_http\] table in the discovery process.


## Result

When your Discovery schedule runs, it automatically scans for any certificates on the specified URLs and fetches all URLs from the cmdb\_ci\_endpoint\_http table. It then creates a mapping between the URL and the schedule in the **sn\_disco\_certmgmt\_cert\_url\_sched\_m2m**.

With Service Mapping enabled, by default, it creates a relationship between the HTTP endpoint and application when it creates an entry in cmdb\_ci\_endpoint\_http. For example, the Amazon application is automatically connected to amazon.com.

The relationship is: cmdb\_ci\_endpoint\_http\[parent\] --&gt; \[Implement End Point To::Implement End Point From\] --&gt; cmdb\_ci\_appl\[child\].

If the above relationship exists, the URL certificate discovery creates an additional relationship between the certificate and application. This relationship is: cmdb\_ci\_appl\[parent\] --&gt; \[Uses::Used by\] --&gt; cmdb\_ci\_certificate\[child\].

**Note:** URL discovery schedules do not generate server configuration items \(CIs\).

