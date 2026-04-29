---
title: Submit a vulnerability scan request from the Security Incident Response catalog
description: You can submit vulnerability scans for CIs and IP addresses from the Security Incident Response catalog. The requests are submitted and you can view the results in the My Requests module.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Manage lookups and scans, Managing security incidents and inbound requests, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Submit a vulnerability scan request from the Security Incident Response catalog

You can submit vulnerability scans for CIs and IP addresses from the Security Incident Response catalog. The requests are submitted and you can view the results in the **My Requests** module.

## Before you begin

Role required: none

## About this task

Use this catalog item to trigger a vulnerability scan on one or more configuration items or IP addresses directly from the Security Incident Response catalog. The scan uses the vulnerability scanner configured in your instance \(for example, Qualys or Tenable\). Scan results appear in the **Activities** section of your service request. Scans typically complete within a few minutes, depending on the number of targets and scanner response time.

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Security Incident Catalog**.

2.  Select **Vulnerability scan**.

    ![Security incident catalog](../image/sec-inc-cat.png)

3.  Select **Scan Configuration Item and IP addresses**.

4.  Enter one or more of the following to be scanned.

    |Item to be scanned|Description|
    |------------------|-----------|
    |Configuration item|In the **Configuration Item to scan** field, select the CI to be scanned.|
    |IP addresses|In the **IP addresses to scan** field, enter the IP addresses, separated by commas.|

5.  When you have made your selections, click **Submit**.

    If an observable is found, an indicator is created, according to STIXX standards.

6.  To view the status and/or results of the scans, navigate to **Self-Service** &gt; **My Requests**.

7.  Select the SR number for the request.

    The work notes under **Activities** list the tasks performed during the scan, including the creation of individual scans for each CI or IP address, and the results of the scans.


## What to do next

After the scan completes, review the results in the work notes of your service request. If vulnerabilities are found, a security incident or vulnerability item may be automatically created based on your instance configuration.

