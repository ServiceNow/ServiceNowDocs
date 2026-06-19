---
title: Move an automation request to the In progress state
description: As you begin the development for the automation request, move it to the In progress state. This state notifies anyone using Automation Center that the work for the automation is in progress.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/automation-center/move-automationrequest-to-inprogress.html
release: zurich
product: Automation Center
classification: automation-center
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Working with automations, Use, Automation Center, Workflow Data Fabric]
---

# Move an automation request to the In progress state

As you begin the development for the automation request, move it to the **In progress** state. This state notifies anyone using Automation Center that the work for the automation is in progress.

## Before you begin

Create an automation request. For more information, see [Creating an automation request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/automation-center/create-automation-request.md).

Verify that the state of the automation request is **Planned**.

Role required: sn\_ac.automation\_technical\_user or sn\_ac.automation\_admin

## Procedure

1.  Navigate to **All** &gt; **Automation Center** &gt; **Automation Center Home**.

2.  Select the list icon \(\[Omitted image "autocenter-list-icon.png"\] Alt text: List icon.\).

3.  On the **Lists** tab, under **Build**, select **All Automation Requests**.

4.  Open the automation request that you want to move to the In-progress state.

5.  In the form header, select **Move to In progress**.


## What to do next

Update the **Automation** field in the automation request form. This field is visible only when the state of the automation request is **In progress**. For more information, see [Automation request form from Automation Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/automation-center/automation-request-autocenter-form.md).

**Parent Topic:**[Working with automations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/automation-center/automations.md)

