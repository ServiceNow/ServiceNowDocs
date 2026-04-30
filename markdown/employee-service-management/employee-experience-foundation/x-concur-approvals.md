---
title: Manage approvals from SAP Concur
description: As an administrator, you can sync, view, track, and fulfill the requests from other business applications such as SAP Concur from a unified Employee Center Pro location.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Approvals hub integration with SAP Concur, Approval hub integrations, Approvals hub, Setup task management, Configure, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Manage approvals from SAP Concur

As an administrator, you can sync, view, track, and fulfill the requests from other business applications such as SAP Concur from a unified Employee Center Pro location.

## Before you begin

Role required: sp\_admin

## About this task

View expense reports, itemizations, and receipts of the SAP Concur account from your ServiceNow instance.

## Procedure

1.  Navigate to **All** &gt; **Employee Center** &gt; **Concur Configuration** \(sn\_ex\_cnc\_concur\_configuration\).

2.  Click **New** or update the existing configuration.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Base URL|Base URL of the instance. For example, assuming the base URL of `https://api.example.com/`, the `/reports` endpoint refers to `https://api.example.com/reports`.|
    |Report relative path|Relative path of the report `/goto/expense-report/{report_id}`.|
    |Active|Status of the web application. Only when a Concur configuration is active, the Concur Expense Reports table gets the report URL populated. The same URL is used by the **My task** page UI to redirect to Concur system.|
    |Domain|Domain of the configuration. This field is automatically filled per the current domain and is used for domain separation. Per domain, only one Concur configuration can be in active state.|

4.  Click **Save**.

    Configuration is complete.


## Result

Base URL and relative path help display the fetched reports and expenses metadata from SAP Concur. The base URL and relative path help the approver navigate to SAP Concur from the respective approval or report for more details.

**Parent Topic:**[Approvals hub integration with SAP Concur](../concept/x-concur-sa-integration.md)

