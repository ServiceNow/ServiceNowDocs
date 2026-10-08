---
title: Respond to approval requests in Cowork
description: Before Cowork takes a sensitive action, such as changing a record or deleting a file, it pauses and asks for your permission. Responding to these requests keeps you in control of what the agent does on your behalf.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/respond-approval-requests.html
release: zurich
topic_type: task
last_updated: "2026-09-27"
reading_time_minutes: 1
keywords: [approval requests, approval card, Allow always]
breadcrumb: [Use, ServiceNow Cowork, Enable AI experiences]
---

# Respond to approval requests in Cowork

Before Cowork takes a sensitive action, such as changing a record or deleting a file, it pauses and asks for your permission. Responding to these requests keeps you in control of what the agent does on your behalf.

## Before you begin

Role required: sn\_app\_cowork.user

## About this task

When Cowork needs permission, an approval card appears in the chat and processing pauses until you respond.

## Procedure

1.  Open the chat that shows the approval card.

2.  Review the action on the card.

3.  Select how Cowork should proceed.

<table id="table-approval-options"><thead><tr><th>

Permission options

</th><th>

Result

</th></tr></thead><tbody><tr><td>

Allow

</td><td>

Coworktakes this action now and asks again next time.

</td></tr><tr><td>

**Allow always**

</td><td>

Cowork takes this action now and doesn't ask again. The action is added to your standing approvals. This action is saved **Note:** Select **Allow always** only for actions you would approve every time. You can revoke a standing approval at any time in **Settings** &gt; **Approvals**.

</td></tr><tr><td>

Deny

</td><td>

Cowork doesn't take the action. **Note:** If an action looks unexpected or outside what you asked for, deny it and stop the task.

</td></tr></tbody>
</table>4.  If you have set up TOTP authorization, enter the six-digit code from your authenticator app.


**Parent Topic:**[Using ServiceNow Cowork](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/servicenow-cowork-using.md)

