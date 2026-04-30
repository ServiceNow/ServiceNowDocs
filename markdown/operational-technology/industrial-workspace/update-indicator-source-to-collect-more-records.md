---
title: Review the indicator sources for a larger number of records
description: Review and update an indicator source to override the expected record count if you expect more than 1 million records to be collected from the indicator sources. This action helps to avoid system performance issues when collecting data for the Industrial Workspace.
locale: en-US
release: zurich
product: Industrial Workspace
classification: industrial-workspace
topic_type: task
last_updated: "2026-02-24"
reading_time_minutes: 1
breadcrumb: [Setting up the Operational Technology Vulnerability Response \(PA\) dashboard, Configure, Industrial Workspace, Operational Technology]
---

# Review the indicator sources for a larger number of records

Review and update an indicator source to override the expected record count if you expect more than 1 million records to be collected from the indicator sources. This action helps to avoid system performance issues when collecting data for the Industrial Workspace.

## Before you begin

Role required: admin or pa\_admin

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Indicators** &gt; **Automated Indicators**.

2.  Apply the filter **\[Application\] \[is\] \[Operational Technology Vulnerability Response\]**.

3.  Under the Indicator Source column, select the indicator source record that you want to edit.

4.  In the Records collection section, select the check box next to the **Override record collection** field.

5.  In the **Maximum number of fetched records** field, add a number greater than the default value of 1 million records.

    For example, **2 million**.

6.  Select **Update**.


**Parent Topic:**[Setting up the Operational Technology Vulnerability Response \(PA\) dashboard](../../operational-technology-management/concept/setting-up-the-otvr-pa-dashboard.md)

