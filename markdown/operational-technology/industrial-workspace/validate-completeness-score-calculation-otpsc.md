---
title: Validate the completeness score calculation
description: Validate that the CMDB Health Dashboard - Completeness Score Calculation is activated to run if you want to include the OT Device Data Completeness \(%\) indicator in the Operational Technology \(OT\) Progress Scorecard.
locale: en-US
release: australia
product: Industrial Workspace
classification: industrial-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up the Operational Technology Progress Scorecard, Configure, Industrial Workspace, Operational Technology]
---

# Validate the completeness score calculation

Validate that the **CMDB Health Dashboard - Completeness Score Calculation** is activated to run if you want to include the **OT Device Data Completeness \(%\)** indicator in the Operational Technology \(OT\) Progress Scorecard.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace Admin** &gt; **Guided Setup**.

2.  In the **Industrial Workspace** section, select **OT Progress Scorecard**.

3.  In the **Validate Completeness Score Calculation** task, select **Configure**.

4.  In the **CMDB Health Dashboard - Completeness Score Calculation** Scheduled Script Execution record, validate the following items:

    1.  Validate that the **Active** check box is checked.
    2.  To ensure accurate scores are collected for end of the month reporting, validate that **Run** field is configured
5.  Select **Update**.

    For more details on how completeness is calculated, see the **Completeness** section of [CMDB Health KPIs and metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/r_CMDBHealthMetrics.md).


**Parent Topic:**[Setting up the Operational Technology Progress Scorecard](../concept/setting-up-the-ot-progress-scorecard.md)

