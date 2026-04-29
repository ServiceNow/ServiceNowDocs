---
title: Submit an IoC Lookup request from the Security Incident Catalog
description: If the Security Incident Response plugin is activated, you can submit threat lookups for files, hash values, URLs, and IP addresses from the Security Incident Catalog. The requests are submitted and you can view the results in the My Requests module.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage lookups and scans, Managing security incidents and inbound requests, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Submit an IoC Lookup request from the Security Incident Catalog

If the Security Incident Response plugin is activated, you can submit threat lookups for files, hash values, URLs, and IP addresses from the Security Incident Catalog. The requests are submitted and you can view the results in the **My Requests** module.

## Before you begin

Role required: none

## About this task

Lookups are automatically performed for the default lookup type for each lookup source listed in the lookup record. The results of the lookup request are available in the **My Requests** module.

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Security Incident Catalog**.

2.  Click **IoC Lookup**.

3.  Click **Lookup files, hash values, URLs or IP addresses**.

4.  Enter one or more of the following:

<table id="table_vks_thr_ns"><thead><tr><th>

Item to lookup

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Files

</td><td>

Click the paperclip icon, then locate and attach the files you want to lookup. **Note:** By default, the **Lookup Type** for **File**is inactive. Files are converted and submitted as a hash value.

</td></tr><tr><td>

URLs

</td><td>

In the **URLs** field, enter the URLs you want to lookup, separated by commas. For example: www.abc.com,www.xyz.net.

</td></tr><tr><td>

IP addresses

</td><td>

In the **IP addresses** field, enter the IP addresses you want to lookup, separated by commas.

</td></tr><tr><td>

Hash values

</td><td>

In the **Hash values** field, enter the hash values you want to lookup, separated by commas.**Note:** When the **Lookup Type** for **File** is inactive, this value is the default action for both **File** and **Hash values**.

</td></tr></tbody>
</table>5.  When you have made your selections, click **Submit**.

6.  To view the status and/or results of the lookups, navigate to **Self-Service** &gt; **My Requests**.

7.  Click the SR number for the request.

    The work notes under **Activity** list the tasks performed during the lookup, including the creation of individual lookups for each file, hash value, URL, or IP address, and the lookup results.


