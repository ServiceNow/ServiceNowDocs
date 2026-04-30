---
title: Run scheduled jobs to perform Hardware Vulnerability Assessment
description: Execute scheduled jobs to perform hardware vulnerability assessment.
locale: en-US
release: xanadu
product: Industrial Workspace
classification: industrial-workspace
topic_type: task
last_updated: "2025-01-10"
reading_time_minutes: 2
breadcrumb: [Setting up Hardware Vulnerability Assessment of OT devices using guided setup, Configure, Industrial Workspace, Operational Technology]
---

# Run scheduled jobs to perform Hardware Vulnerability Assessment

Execute scheduled jobs to perform hardware vulnerability assessment.

## Before you begin

Role required: sn\_otvr.vul\_event\_manager

Hardware Vulnerability Assessment is based on the vulnerability assessment feature in Vulnerability Response. Before scheduling the jobs for HVA, navigate to **All** &gt; **Vulnerability Response** &gt; **Administration** &gt; **Integrations** and run the following NVD integrations:

<table id="table_sbn_qlp_dt"><thead><tr><th>

Integration

</th><th>

Description

</th></tr></thead><tbody><tr><td>

NIST National Vulnerability Database Integration - API \(CVE only\)

</td><td>

Retrieves only NIST NVD vulnerability data \(CVE\). By default, this integration is automatically set to run daily.

</td></tr><tr><td>

NIST National Vulnerability Database Integration-API \(CPE only\)

</td><td>

Retrieves CPE data from NIST NVD. This integration is inactive by default. Activate this integration to capture CPE data that includes a formal name format, a method for checking names against a system, and a description format for binding text and tests to a name. This information is stored in Vulnerable Software.

This integration is set to run daily and is inactive by default. For more information, see [Activate the NIST National Vulnerability Database–API \(CPE only\)](https://www.servicenow.com/docs/access?context=install-nvd&version=xanadu&pubname=xanadu-security-management&section=activate-nist-nvd-cpe-only-integration&ft:locale=en-US).

</td></tr><tr><td>

NIST National Vulnerability Database Integration-API \(Unmapped CPE\)

</td><td>

Retrieves CPE data associated with fetched CVE from NIST NVD. This integration is inactive by default.Activate this integration to capture CPE data that includes a formal name format, a method for checking names against a system, and a description format for binding text and tests to a name. This information is stored in an NVD vulnerability entry record related list. This integration is set to run On Demand and is inactive by default. For more information, see [Activate the NIST National Vulnerability Database–API \(Unmapped CPE\)](https://www.servicenow.com/docs/access?context=install-nvd&version=xanadu&pubname=xanadu-security-management&section=activate-nist-nvd-unmapped-cpe&ft:locale=en-US).

</td></tr></tbody>
</table>For more information, see:

-   [Understanding the NVD integrations](https://www.servicenow.com/docs/access?context=nvd-vuln-integration&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US).
-   [Install the Vulnerability Response Integration with the NIST National Vulnerability Database](https://www.servicenow.com/docs/access?context=install-nvd&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)

## About this task

You must perform the following scheduled jobs to detect firmware vulnerabilities of any OT devices in the inventory:

## Procedure

1.  Navigate to **Scheduled Vulnerability Assessment Jobs** &gt; **Configure** &gt; **Scheduled Jobs**.

    **Important:**

    -   You must run **Hardware Assessment - Full** before you schedule the **Hardware Assessment - Delta** job. You can run the **Hardware Assessment - Full job** on demand.
    -   You can schedule **Hardware Assessment - Delta** job to run daily, weekly, or according to your required frequency.
2.  Select **Hardware Assessment - Full** &gt; **Execute Now**.

    This job performs an assessment on all OT devices in the inventory to detect any firmware vulnerabilities regardless of prior assessments.

3.  Select **Hardware Assessment - Delta** &gt; **Active**.

    Select **Run** and choose a frequency from the list. The **Hardware Assessment - Delta** job runs according to the frequency that you select.

    This job performs incremental assessments, targeting only changes or updates since the last assessment run. It captures changes on firmwares, normalized contents, and vulnerabilities since the last successful run of the hardware vulnerability assessment. This job makes sure you can maintain continuous monitoring and timely updates.


**Parent Topic:**[Setting up Hardware Vulnerability Assessment of OT devices using guided setup](configure-hva-using-guided-setup.md)

**Related topics**  


[Scheduled jobs](https://www.servicenow.com/docs/access?context=c_ScheduledJobs&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)

