---
title: Configure flows for Legal Conflict of Interest
description: Review the flows installed with the Legal Conflict of Interest application and configure them to align with your business needs.
locale: en-US
release: australia
product: Legal Conflict of Interest
classification: legal-conflict-of-interest
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Legal Conflict of Interest, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Configure flows for Legal Conflict of Interest

Review the flows installed with the Legal Conflict of Interest application and configure them to align with your business needs.

## Before you begin

Ensure that the Legal Conflict of Interest application scope is selected.

Role required: sn\_lg\_coi.coi\_admin and admin

## About this task

Legal Conflict of Interest uses the following flows:

-   COI Approval flow: Triggers multi-level approvals when an employee submits a conflict of interest request
-   Scheduled Flow to Deactivate COI: Triggers to validate and deactivate any existing conflict of interest disclosure record that has the end date before the current date. The flow triggers at a scheduled time.

The flows are built using ServiceNow Workflow Studio, so make sure you’re familiar with the [Flow Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/flow-designer.md) basics.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Find the **COI Approval flow** and click the name of the flow to open.

3.  Modify the trigger to set the conditions for the flow to trigger, and actions to add or update the approval levels.

    For information on how to create or modify flows, see [Create a flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/create-flow.md).

4.  Click **Save**.

5.  Test the flow by clicking **Test**.

    For more information, see [Test a flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/flow-test.md).

6.  If not already active, click **Activate** to enable the flow.


**Parent Topic:**[Configure Legal Conflict of Interest](../concept/legal-coi-administration.md)

