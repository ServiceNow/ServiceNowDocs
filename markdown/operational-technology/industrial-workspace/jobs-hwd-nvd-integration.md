---
title: Run NVD Integrations for Hardware Vulnerability Assessment
description: Install and run National Vulnerability Database \(NVD\) integrations to perform hardware vulnerability assessment.
locale: en-US
release: australia
product: Industrial Workspace
classification: industrial-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up the Hardware Vulnerability Assessment of Operational Technology devices using guided setup, Configure, Industrial Workspace, Operational Technology]
---

# Run NVD Integrations for Hardware Vulnerability Assessment

Install and run National Vulnerability Database \(NVD\) integrations to perform hardware vulnerability assessment.

## Before you begin

Role required: sn\_otvr.vul\_event\_manager and admin

## About this task

Hardware Vulnerability Assessment is based on the vulnerability assessment feature in Vulnerability Response. You must HVA run the NVD integrations to access the Common Vulnerabilities and Exposures \(CVEs\) data in the NVD database.

To understand what are the different NVD integrations and how do the integrations work, see:

-   [Understanding the NVD integrations](https://www.servicenow.com/docs/access?context=nvd-vuln-integration&version=australia&pubname=australia-security-management&ft:locale=en-US)
-   [Install the Vulnerability Response Integration with the NIST National Vulnerability Database](https://www.servicenow.com/docs/access?context=install-nvd&version=australia&pubname=australia-security-management&ft:locale=en-US)

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace Admin** &gt; **Guided Setup** &gt; **Operational Technology Vulnerability Response** &gt; **Hardware Vulnerability Assessment** &gt; **Configure Install and Run NVD Integration** &gt; **Configure**.

    Alternatively, you can navigate to **All** &gt; **Vulnerability Response** &gt; **Administration** &gt; **Integrations**

2.  Install and execute the following NVD Integrations:

    -   **NIST National Vulnerability Database Integration-API \(CVE only\)**
    -   **NIST National Vulnerability Database Integration-API \(CPE only\)**
    -   **NIST National Vulnerability Database Integration-API \(Unmapped CPE\)**

**Parent Topic:**[Set up the Hardware Vulnerability Assessment of Operational Technology devices using guided setup](configure-hva-using-guided-setup.md)

