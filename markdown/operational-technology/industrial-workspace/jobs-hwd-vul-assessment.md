---
title: Run scheduled jobs to perform Hardware Vulnerability Assessment
description: Execute scheduled jobs to perform hardware vulnerability assessment.
locale: en-US
release: australia
product: Industrial Workspace
classification: industrial-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up the Hardware Vulnerability Assessment of Operational Technology devices using guided setup, Configure, Industrial Workspace, Operational Technology]
---

# Run scheduled jobs to perform Hardware Vulnerability Assessment

Execute scheduled jobs to perform hardware vulnerability assessment.

## Before you begin

Role required: sn\_otvr.vul\_event\_manager and admin

## About this task

You must perform the following scheduled jobs to detect firmware vulnerabilities of any OT devices in the inventory:

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace Admin** &gt; **Guided Setup** &gt; **Operational Technology Vulnerability Response** &gt; **Hardware Vulnerability Assessment** &gt; **Scheduled Vulnerability Assessment Jobs** &gt; **Configure** &gt; **Scheduled Jobs**.

    **Important:**

    -   You must run **Hardware Assessment - Full** before you schedule the **Hardware Assessment - Delta** job. You can run the **Hardware Assessment - Full** on demand.
    -   You can schedule **Hardware Assessment - Delta** job to run daily, weekly, or according to your required frequency.
2.  Select **Hardware Assessment - Full** &gt; **Execute Now**.

    This job performs an assessment on all OT devices in the inventory to detect any firmware vulnerabilities regardless of prior assessments.

3.  Select **Hardware Assessment - Delta** &gt; **Active**.

    Select **Run** and choose a frequency from the list. The **Hardware Assessment - Delta** job runs according to the frequency that you select.

    This job performs incremental assessments, targeting only changes or updates since the last assessment run. It captures changes on firmware, normalized contents, and vulnerabilities since the last successful run of the hardware vulnerability assessment. This job makes sure that you can maintain continuous monitoring and timely updates.

4.  Select **Hardware Vulnerability Assessment - Mark Expired Assessments** &gt; **Active** to start this job.

    Select **Run** and choose a frequency from the list. The **Hardware Vulnerability Assessment - Mark Expired Assessments** job runs according to the frequency that you select.

    Hardware vulnerability assessments are based on the firmware data available for a device. If you update the firmware version of a device, the existing assessments based on the previous firmware version are no longer valid and are considered as expired assessments. You can delete expired assessments, which are older than a month. However, you must perform new vulnerability assessments for the devices with an updated firmware version.


**Parent Topic:**[Set up the Hardware Vulnerability Assessment of Operational Technology devices using guided setup](configure-hva-using-guided-setup.md)

**Related topics**  


[bundle-platadm.c_ScheduledJobs]

