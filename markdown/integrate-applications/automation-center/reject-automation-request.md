---
title: Reject an automation request
description: Reject an automation request from Automation Center if it's a duplicate of an existing automation or if it doesn’t meet the required criteria.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/automation-center/reject-automation-request.html
release: australia
product: Automation Center
classification: automation-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Working with automations, Use, Automation Center, Workflow Data Fabric]
---

# Reject an automation request

Reject an automation request from Automation Center if it's a duplicate of an existing automation or if it doesn’t meet the required criteria.

## Before you begin

Create an automation request. For more information, see [Creating an automation request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/automation-center/create-automation-request.md).

After you reject an automation request, the life cycle of the automation request ends.

Role required: sn\_ac.automation\_technical\_user or sn\_ac.automation\_admin

## About this task

Rejecting an automation request is one of the life-cycle stages of an automation request.

## Procedure

1.  Navigate to **All** &gt; **Automation Center** &gt; **Automation Center Home**.

2.  Select the list icon \(\[Omitted image "autocenter-list-icon.png"\] Alt text: List icon.\).

3.  On the **Lists** tab, under **Build**, select **All Automation Requests**.

4.  Open the automation request that you want to reject.

5.  In the form header, select **Reject**.

    **Warning:** After you move an automation request to the Rejected state, you can't change or delete the entries on the Automation request form, associated automation tasks, and resources.


## Result

The Rejected state is the end state of a request. There are no operations possible after that state.

**Parent Topic:**[Working with automations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/automation-center/automations.md)

