---
title: Configure property for Hardware Vulnerability Assessment to create VIT automatically
description: Configure this property to automatically create vulnerable items \(VIT\) based on the hardware vulnerability assessment.
locale: en-US
release: xanadu
product: Industrial Workspace
classification: industrial-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Setting up Hardware Vulnerability Assessment of OT devices using guided setup, Configure, Industrial Workspace, Operational Technology]
---

# Configure property for Hardware Vulnerability Assessment to create VIT automatically

Configure this property to automatically create vulnerable items \(VIT\) based on the hardware vulnerability assessment.

## Before you begin

Role required: sn\_vul.manage\_exposure\_assessment

## About this task

Configuring this property determines if new vulnerable item records are created automatically for fully matched hardware vulnerability assessments. Alternatively, you can also manually create VITs.

## Procedure

1.  Navigate to **Configure Vulnerability Assessment Properties** &gt; **Configure** &gt; **Vulnerability Response Properties** &gt; **Vulnerability Assessment**.

2.  Select **Yes**.

    The default value is **Yes**.

    When set to **Yes**, new vulnerable item records will be created automatically for fully matched hardware vulnerability assessments. You can set the value to **No** if you want to create VITs manually.

3.  Select **Save**.


**Parent Topic:**[Setting up Hardware Vulnerability Assessment of OT devices using guided setup](configure-hva-using-guided-setup.md)

