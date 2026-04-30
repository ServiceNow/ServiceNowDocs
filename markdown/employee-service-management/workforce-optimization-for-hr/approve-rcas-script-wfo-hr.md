---
title: RCA approvals in Workforce Optimization for HR
description: After you install or upgrade to the latest Workforce Optimization for HR from ServiceNow Store, you might encounter Restricted Caller Access \(RCA\) approval messages.
locale: en-US
release: yokohama
product: Workforce Optimization for HR
classification: workforce-optimization-for-hr
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Activate Workforce Optimization for HR, Configuring Workforce Optimization for HR, Workforce Optimization for HR Overview, HR Service Delivery, Employee Service Management]
---

# RCA approvals in Workforce Optimization for HR

After you install or upgrade to the latest Workforce Optimization for HR from ServiceNow Store, you might encounter Restricted Caller Access \(RCA\) approval messages.

## Before you begin

Role required: sn\_hr\_wfo.admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Fix Scripts**.

2.  Right-click the header and choose **Import XML**.

3.  Click **Choose file** and select the XML file that you downloaded.

4.  Search and find the HR Agent WS bulk RCAs approval script record.

5.  Click **Run Script** to approve all the requested RCAs.

    **Note:** RCA fix script can approve the RCAs which exist at the time of execution. After running the RCA script \(if you install the Document Templates from ServiceNow Store, Human Resources Scoped App: Lifecycle Events, and Human Resources Scoped App: Employee Relations plugins\), re-run the RCA script to approve the new RCAs.


**Parent Topic:**[Activate Workforce Optimization for HR](../concept/activate-wfo-hr.md)

