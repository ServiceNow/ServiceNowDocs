---
title: Submit a vulnerability scan request from a security incident
description: If your security incident has one or more configuration items \(servers, computers, and so on\), they can be scanned for vulnerabilities from the Security Incident Response form.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage lookups and scans, Managing security incidents and inbound requests, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Submit a vulnerability scan request from a security incident

If your security incident has one or more configuration items \(servers, computers, and so on\), they can be scanned for vulnerabilities from the Security Incident Response form.

## Before you begin

The Vulnerability Response plugin must be activated.

Role required: sn\_si.write

## Procedure

1.  [Create a security incident](../concept/si-manual-creation.md) and include at least one resource.

    You can also open an existing incident that has configuration items.

2.  When you have completed your entries on the form, select and hold \(or right-click\) the form header and select **Save**.

    After the record has been saved, a **Scan for Vulnerabilities** related link appears.

    **Note:** If the **Scan for Vulnerabilities** related list is not shown, you must navigate to **Vulnerability** &gt; **Scanners**, set up at least one scanner, and set its default to **true**.

3.  Select **Scan for Vulnerabilities**.

    **Note:**

    A message appears at the top of the security incident form, along with a link to the scan record.

    ![Scan request with link](../image/ScanRequest.png)

4.  You can Select the scan request number to view the scan record.

    The incident details show the results of the scan in the Security Scan Request record.


