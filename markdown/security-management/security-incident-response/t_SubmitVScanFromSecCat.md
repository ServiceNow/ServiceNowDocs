---
title: Submit a vulnerability scan request from the Security Incident Response catalog
description: You can submit vulnerability scans for CIs and IP addresses from the Security Incident Response catalog. The requests are submitted and you can view the results in the My Requests module.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-05-01"
reading_time_minutes: 1
breadcrumb: [Manage lookups and scans, Managing security incidents and inbound requests, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Submit a vulnerability scan request from the Security Incident Response catalog

You can submit vulnerability scans for CIs and IP addresses from the Security Incident Response catalog. The requests are submitted and you can view the results in the **My Requests** module.

## Before you begin

Role required: none

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Security Incident Catalog**.

2.  Click **Vulnerability scan**.

3.  Click **Scan Configuration Item and IP addresses**.

4.  Enter one or more of the following to be scanned.

    |Item to be scanned|Description|
    |------------------|-----------|
    |Configuration item|In the **Configuration Item to scan** field, select the CI to be scanned.|
    |IP addresses|In the **IP addresses to scan** field, enter the IP addresses, separated by commas.|

5.  When you have made your selections, click **Submit**.

    If an observable is found, an indicator is created, according to STIXX standards.

6.  To view the status and/or results of the scans, navigate to **Self-Service** &gt; **My Requests**.

7.  Click the SR number for the request.

    The work notes under **Activities** list the tasks performed during the scan, including the creation of individual scans for each CI or IP address, and the results of the scans.


