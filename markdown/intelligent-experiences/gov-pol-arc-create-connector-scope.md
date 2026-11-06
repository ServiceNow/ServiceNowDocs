---
title: Create a connector scope for an Arc policy
description: Limit what ServiceNow Arc can do through a connector, such as reading mail without sending it, by granting only the connector operations a team needs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/gov-pol-arc-create-connector-scope.html
release: australia
topic_type: task
last_updated: "2026-10-22"
reading_time_minutes: 2
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI, connector scope, oauth scope, microsoft 365 scopes, approval gate, arc policies]
breadcrumb: [Working with Arc policy rules, Managing Arc policies, Controlling AI asset usage, Govern AI assets, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Create a connector scope for an Arc policy

Limit what ServiceNow Arc can do through a connector, such as reading mail without sending it, by granting only the connector operations a team needs.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward and sn\_app\_arc.admin

## About this task

A connector scope names one operation, such as sending email, that Arc can perform through a connector. The scopes a policy grants apply on top of the user's own connection credential, so Arc can't use a permission the credential has unless the policy grants the matching scope. Users can turn off scopes you grant, but they can't turn on a scope you haven't granted.

The **Active** and **Approval gate** settings belong to this policy only. Other policies that use the same scope keep their own settings.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Govern** &gt; **Policies** &gt; **Arc policies**.

2.  Select the policy you want to update.

3.  Select **More**.

4.  Select **Connector scopes**.

5.  Select **Create connector scopes**.

    If the policy already has connector scopes, select **+ Add rule** instead.

6.  On the form, fill in the fields.

<table id="table_connector_scope_fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Scope Name**

</td><td>

Identifier Arc matches against the connector's permissions at run time. Enter it exactly as the connector defines it, for example, `Mail.Send` for the Microsoft 365 permission to send email.

</td></tr><tr><td>

**Scope Label**

</td><td>

Readable name that identifies the scope in lists, for example, Send Outlook emails.

</td></tr><tr><td>

**Connector**

</td><td>

Connector the scope applies to.

 -   **Browser**
-   **GitHub**
-   **Google Workspace**
-   **Microsoft 365**
-   **Microsoft Teams**
-   **ServiceNow**


</td></tr><tr><td>

**Description**

</td><td>

What the scope permits, for other administrators who review it later, for example, Allows the app to send emails on behalf of the user.

</td></tr><tr><td>

**Active**

</td><td>

Option to grant the scope to the users this policy covers. Cleared by default. Select it, or the scope doesn't take effect.

</td></tr><tr><td>

**Approval gate**

</td><td>

Option to require users to approve the scope before Arc uses it with the connector. Cleared by default. Select it for scopes that send, write, or change data on the user's behalf.

</td></tr></tbody>
</table>7.  Select **Create**.


## Result

The scope appears on the policy's **Connector scopes** tab with its **Active** and **Approval gate** settings, and applies to the users the policy covers at their next policy sync.

## Example: Let the agent send email only with approval

Your account managers want Arc to draft and send customer follow-ups from Outlook, but sending should wait for the account manager's approval. Create a connector scope with the following values:

-   **Scope Name**: `Mail.Send`
-   **Scope Label**: `Send Outlook emails`
-   **Connector**: **Microsoft 365**
-   **Description**: `Allows the agent to send email on the user's behalf, with approval.`
-   **Active**: Selected
-   **Approval gate**: Selected

The scope name must match the Microsoft 365 permission exactly. **Active** grants the scope, and **Approval gate** makes users approve the scope before the agent uses it to send. Without this scope, the agent can't send email for these users, even if their Microsoft 365 connection allows it.

