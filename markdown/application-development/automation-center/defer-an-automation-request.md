---
title: Defer an automation request
description: Defer an automation request from Automation Center if the priority of the request has changed and it is not urgent anymore.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/automation-center/defer-an-automation-request.html
release: australia
product: Automation Center
classification: automation-center
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Working with automations, Use, Automation Center, Discover, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# Defer an automation request

Defer an automation request from Automation Center if the priority of the request has changed and it is not urgent anymore.

## Before you begin

Create an automation request. For more information, see [Creating an automation request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/automation-center/create-automation-request.md).

Verify that the state of the automation request is either **New** or **In Progress**.

Role required: sn\_ac.automation\_technical\_user or sn\_ac.automation\_admin

## About this task

Deferring an automation request is one of the life-cycle stages of an automation request.

## Procedure

1.  2.  3.  On the **Lists** tab, under **Build**, select **All Automation Requests**.

4.  Open the automation request that you want to defer.

5.  In the form header, select **Defer**.

    **Warning:** After you move an automation request to the Defer state, you can't change or delete the entries on the Automation request form, associated automation tasks, and resources.


## What to do next

You can move the automation request to Planned state or reject the automation request. For more information, see [Move an automation request to the Planned state](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/automation-center/move-automation-request-to-planned.md) and [Reject an automation request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/automation-center/reject-automation-request.md).

**Parent Topic:**[Working with automations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/automation-center/automations.md)

