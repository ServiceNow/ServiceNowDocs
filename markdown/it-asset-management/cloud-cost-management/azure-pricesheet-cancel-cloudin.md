---
title: Cancel an Azure Price sheet download job in Cloud Cost Management
description: An Azure Price sheet download job downloads price sheet data from Azure. You can cancel any Price sheet download job individually.
locale: en-US
release: zurich
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Schedule and manage the Cloud Cost Management jobs that download Microsoft Azure price sheets, Configure Cloud Cost Management for Microsoft Azure, Configure, Cloud Cost Management, IT Asset Management]
---

# Cancel an Azure Price sheet download job in Cloud Cost Management

An Azure Price sheet download job downloads price sheet data from Azure. You can cancel any Price sheet download job individually.

## Before you begin

For each provider, run Discovery on each service account.

Make sure to have the proper credentials and service account setup.

Role required: insights\_admin \[sn\_clin\_core.insights\_admin\].

## About this task

Cloud Cost Management downloads price sheet data from each provider one region at a time. If you cancel a running price sheet download job, the current region finishes downloading and the system cancels download for the remaining regions. If you delete a scheduled job execution, then all regions are marked as canceled.

## Procedure

1.  Navigate to **Cloud Cost Management Workspace** &gt; **Operations** &gt; **Administration** &gt; **Price sheet download jobs**.

2.  Select either a currently running or scheduled job that you want to cancel.

3.  On the Price Sheet Download job page, select **Cancel execution**.


