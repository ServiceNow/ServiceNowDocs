---
title: Respond to approval requests in Arc
description: Before Arc takes a sensitive action, such as changing a record or deleting a file, it pauses and asks for your permission. Responding to these requests keeps you in control of what the agent does on your behalf.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/respond-approval-requests.html
release: australia
topic_type: task
last_updated: "2026-09-27"
reading_time_minutes: 1
keywords: [approval requests, approval card, Always Allow]
breadcrumb: [Use, ServiceNow Arc, Extend, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# Respond to approval requests in Arc

Before Arc takes a sensitive action, such as changing a record or deleting a file, it pauses and asks for your permission. Responding to these requests keeps you in control of what the agent does on your behalf.

## Before you begin

Role required: sn\_app\_arc.user

## About this task

When Arc needs permission, an approval card appears in the chat and processing pauses until you respond.

## Procedure

1.  Open the chat that shows the approval card.

2.  Review the action on the card.

    The card title names what this one action does. The description says what's at stake, such as what the action changes, deletes, or sends, who it affects, and whether it can be undone.

3.  Select how Arc should proceed.

<table id="table-approval-options"><thead><tr><th>

Permission options

</th><th>

Result

</th></tr></thead><tbody><tr><td>

Allow

</td><td>

Arc takes this action and allows it for the rest of the current task. Arc asks again in a later task.

</td></tr><tr><td>

**Always Allow**

</td><td>

Arc takes this action now and doesn't ask again. The action is added to your standing approvals. **Note:** Select **Always Allow** only for actions you would approve every time. You can revoke a standing approval at any time in **Settings** &gt; **Approvals**.

</td></tr><tr><td>

Deny

</td><td>

Arc doesn't take the action. **Note:** If an action looks unexpected or outside what you asked for, deny it and stop the task.

</td></tr></tbody>
</table>    For a Microsoft 365 capability set to **Ask me first**, the card offers only **Allow** and **Deny**, and Arc asks again every time it uses that capability.

4.  If you have set up TOTP authorization, enter the six-digit code from your authenticator app.

    For more information, see [Set up TOTP authorization for sensitive actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/setup-totp-security.md).


**Parent Topic:**[Using ServiceNow Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/servicenow-cowork-using.md)

