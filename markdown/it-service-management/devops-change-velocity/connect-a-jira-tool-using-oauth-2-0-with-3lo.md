---
title: Connect a Jira tool using OAuth 2.0 with 3LO
description: Authenticate a Jira tool connection using OAuth 2.0 with three-legged OAuth \(3LO\) to enable secure, delegated access to your Jira account.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/devops-change-velocity/connect-a-jira-tool-using-oauth-2-0-with-3lo.html
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2026-05-15"
reading_time_minutes: 2
breadcrumb: [Onboard Jira using Workspace, Jira, Integrate, DevOps Change Velocity, IT Service Management]
---

# Connect a Jira tool using OAuth 2.0 with 3LO

Authenticate a Jira tool connection using OAuth 2.0 with three-legged OAuth \(3LO\) to enable secure, delegated access to your Jira account.

## Before you begin

Role required: sn\_devops.admin, credential\_admin, &amp; sn\_jira\_spoke.jira\_admin.

## About this task

When DevOps Change Velocity is installed, the following records are created automatically.

-   The ServiceNow 3LO integration app is created. Authorize your Jira account through this app.
-   An OAuth application registry record called **DevOps Jira Cloud OAuth Application** is created and pre-populated with the Client ID, Client Secret, and other required fields.
-   An OAuth Entity Profile called **DevOps Jira Cloud OAuth Profile** is created with default set to true. This profile links to the pre-configured OAuth application registry \(DevOps Jira Cloud OAuth Application\).
-   An OAuth Entity Scope called **DevOps Jira Cloud OAuth Scope** containing the required scopes is created. This scope links to the pre-configured OAuth entity profile \(DevOps Jira Cloud OAuth Profile\) and the application registry record \(DevOps Jira Cloud OAuth Application\).

To authenticate your Jira tool using OAuth 2.0 with 3LO, you must:

-   Create an OAuth 2.0 Credential record. Each credential must be linked to a unique OAuth entity profile. The default profile can only be used for one credential.
-   If you are setting up a second or subsequent Jira connection in the same DevOps instance, the default OAuth entity profile is already in use. You must create a new entity profile before creating the credential.

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Select **New**.

    The system displays this message: `What type of Credentials would you like to create?`

3.  Select **OAuth 2.0 Credentials**.

4.  On the form, fill these values.

<table id="oauth-notify-webex"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify the record.

</td></tr><tr><td>

Active

</td><td>

Activates the credential record for use.

</td></tr><tr><td>

OAuth Entity Profile

</td><td>

-   First connection: Select the pre-configured default entity profile called **DevOps Jira Cloud OAuth Profile**.
-   Additional connections: Select a new entity profile. For information on creating new entity profiles, see step 10.


</td></tr><tr><td>

Applies to

</td><td>

Scope of the credential — all MID Servers in your network, or one or more **Specific MID servers**. Specify the MID Servers that should use this credential in the **MID servers** field.

</td></tr><tr><td>

Order

</td><td>

Order to apply this credential. For example, `100`.

</td></tr></tbody>
</table>5.  Open the context menu on the form header and select **Submit**.

6.  Select the **Get OAuth Token** related link.

    Atlassian opens for authorization.

7.  Sign in to your Atlassian account if prompted.

8.  Review the requested Jira scopes and select **Accept**.

    The access token is saved and refreshed automatically.

9.  Confirm the tokens in the OAuth credential list table.

    Both an access token and a refresh token should appear, linked to the entity profile. The **Type** column is hidden by default. To view it, select the gear icon in the upper-right corner of the table and add the **Type** column to the list.

10. Create an additional OAuth entity profile for a second Jira connection.

    1.  Enter a descriptive name, for example: Jira Account Profile.

    2.  Set **isDefault** to false.

        Only one default profile is allowed per OAuth application registry.

    3.  In the **OAuth provider** field, select **DevOps Jira Cloud OAuth Application**.

    4.  Save the record.

    5.  In the OAuth Entity Scope related list, add the pre-configured **DevOps Jira Cloud OAuth Scope** scope.

        The same scope record can be shared across all entity profiles.

    6.  Save the record.


**Parent Topic:**[Onboard Jira to DevOps Change Velocity — Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/devops-change-velocity/create-jira-tool-dev-ops.md)

