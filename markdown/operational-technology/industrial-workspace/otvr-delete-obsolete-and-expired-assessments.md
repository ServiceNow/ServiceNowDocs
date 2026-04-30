---
title: Delete obsolete and expired hardware vulnerability assessments
description: Set up automatic deletion of obsolete or expired assessment records.
locale: en-US
release: yokohama
product: Industrial Workspace
classification: industrial-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Set up the Hardware Vulnerability Assessment of Operational Technology devices using guided setup, Configure, Industrial Workspace, Operational Technology]
---

# Delete obsolete and expired hardware vulnerability assessments

Set up automatic deletion of obsolete or expired assessment records.

## Before you begin

Role required: admin

## About this task

Configure the age of obsolete or expired assessments to be cleaned.

-   Obsolete assessments: Invalid assessments, which have been ignored or the associated vulnerable items \(VITs\) that are closed for more than two years.
-   Expired assessments: If you update the firmware version of a device, the existing assessments based on the previous firmware version become invalid and are considered as expired assessments. You can delete expired assessments, which are older than a month. However, you must perform new vulnerability assessments for the devices with an updated firmware version.

## Procedure

1.  Navigate to **All** &gt; **System Data Management** &gt; **Data Management Policies**.

2.  Search for and select the **sn\_vul\_analyst\_firmware\_vulnerability\_assessment** policy.

3.  Select the **Active** check box and configure clean-up rules according to your requirement.

    Configure the age in clean-up rules 1, 2, and 3, after which the obsolete and expired assessments are deleted:

    -   Rule 1: Delete the firmware vulnerabilities assessment whose associated Vulnerability Item \(VIT\) was closed more than two years ago, based on the last update date of the associated VIT
    -   Rule 2: Delete the firmware vulnerabilities assessments that have been ignored for a period exceeding two years, based on the creation date.
    -   Rule 3: Delete firmware assessments that have been expired over 30 days, based on the last update date.
4.  Select **Update**.


**Parent Topic:**[Set up the Hardware Vulnerability Assessment of Operational Technology devices using guided setup](configure-hva-using-guided-setup.md)

