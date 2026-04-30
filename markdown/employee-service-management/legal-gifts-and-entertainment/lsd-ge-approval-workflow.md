---
title: Configure approval workflow for Gifts and Entertainment Compliance
description: Review the flows installed with the Gifts and Entertainment Compliance application and configure them to align to your company's policy.
locale: en-US
release: zurich
product: Legal Gifts and Entertainment
classification: legal-gifts-and-entertainment
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Gifts and Entertainment Compliance, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Configure approval workflow for Gifts and Entertainment Compliance

Review the flows installed with the Gifts and Entertainment Compliance application and configure them to align to your company's policy.

## Before you begin

Ensure that the Gifts and Entertainment Compliance application scope is selected.

Role required: sn\_lg\_gifts.gifts\_config

## About this task

Gifts and Entertainment Compliance uses the Gifts Approval flow to trigger multi-level approvals when an employee submits a gifts and entertainment disclosure request

The flows are built using ServiceNow Workflow Studio, so make sure you’re familiar with the [Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=zurich&pubname=zurich-application-development&ft:locale=en-US) basics.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Find the **Gifts Approval** and click the name of the flow to open.

3.  Modify the trigger to set the conditions for the flow to trigger, and actions to add or update the approval levels.

    For information on how to create or modify flows, see [Create a flow](https://www.servicenow.com/docs/access?context=create-flow&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

4.  Click **Save**.

5.  Test the flow by clicking **Test**.

    For more information, see [Test a flow](https://www.servicenow.com/docs/access?context=flow-test&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

6.  If not already active, click **Activate** to enable the flow.


**Parent Topic:**[Configure Gifts and Entertainment Compliance](../concept/lsd-ge-administration.md)

