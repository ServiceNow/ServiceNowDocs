---
title: Create BI report paths for Oracle HCM Cloud spoke
description: Create BI reports paths to specify the folder paths where the reports are saved.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Oracle HCM Cloud Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Create BI report paths for Oracle HCM Cloud spoke

Create BI reports paths to specify the folder paths where the reports are saved.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Oracle HCM Cloud** &gt; **BI Report Paths**.

2.  Click **New**.

3.  On the form, fill in the fields:

    |Field|Description|
    |-----|-----------|
    |Report Name|Name of the BI report.|
    |Action Name|Name of the action.|
    |Folder Path|Folder path of Oracle HCM Cloud.|

    |Report Name|Action Name|Folder Path|
    |-----------|-----------|-----------|
    |Holiday Calendar Report.xdo|Look up Holiday Calendar|/Custom/Human Capital Management/|
    |Legislativedatagroup Report.xdo|Get Legislative Group ID|/Custom/Human Capital Management/|
    |USOnlinePayslip.xdo|Look up Payroll|/Human Capital Management/Payroll/Payment Distribution/US/|
    |Element Screen Entry Values.xdo|Look up Payroll Elements|/Custom/Human Capital Management/|
    |Individual Compensation Report.xdo|Look up Individual Compensation|/Custom/Human Capital Management/|

    **Note:** Report Name and Folder Path may vary based on the Oracle HCM Cloud instance.


