---
title: Create an application registry entry in your ServiceNow instance
description: Register the application with the instance to participate in OAuth authorization.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integrate Meeting Extensions self-configured app with Microsoft Teams, Integration for Agent Experience, Setup for integrating self-configured apps, Setup the Servicenow instance, MS Teams and Microsoft 365, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Create an application registry entry in your ServiceNow instance

Register the application with the instance to participate in OAuth authorization.

## Before you begin

Role required: oauth\_admin

## Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Select **New**.

3.  For the **What kind of OAuth application** field, select **Configure an OIDC provider to verify ID tokens**.

4.  On the form, fill in the fields.

    -   Name: Enter a name to uniquely identify the record; for example, Microsoft Teams.
    -   Client ID: Enter the client ID value in the format `api://<instance-name>.service-now.com/<client-id>` from the section [Create an app in Microsoft Teams to enable making calls](../../notify2/task/create-app-ms-teams.md).
    -   Client Secret: Enter any random value as client secret and make a note of it.
    -   Add an OAuth OIDC Provider Configuration record.
        1.  Select **OAuth OIDC Provider Configuration** lookup to create a new record and select **New**.
        2.  On the OIDC Provider Configuration New record form, fill in the fields.

<table id="table_tbr_bwl_gcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

OIDC Provider

</td><td>

Name to uniquely identify the record.

 For example, Microsoft Teams meeting extensions.

</td></tr><tr><td>

OIDC Metadata URL

</td><td>

Enter value in the following format:

 `https://login.microsoftonline.com/{tenant_id_from_azure}/v2.0/.well-known/openid-configuration`

 To copy tenant ID, see [Create an app in Microsoft Teams to enable making calls](../../notify2/task/create-app-ms-teams.md).

</td></tr><tr><td>

User claim

</td><td>

Enter any preferred user-name.

</td></tr></tbody>
</table>        3.  Right-click on the OIDC Provider Configuration New record form header and select **Save**.
        4.  Select **Submit**.
    -   Add an OAuth Entity Scope record.
        1.  Select **OAuth Entity Scopes** related list.
        2.  Add a record with the values `Default` in **Name** and `.default` in **OAuthscope**.
5.  Select **Save** on the OAuth OIDC Entity form.

6.  Generate a new OAuth token.

    1.  Navigate to **Notify** &gt; **Microsoft Teams** &gt; **Configuration**.

    2.  Open the record associated with the **Requester** by selecting **Preview this record** icon and then select **Open Record**.

    3.  Select the **Get OAuth Token** related link to refresh the token.

    4.  Select **Update** on the OAuth 2.0 Credentials form.

    5.  Select **Update** on the Microsoft Teams configuration form.


## What to do next

After completing Meeting Extensions integration with Microsoft Teams, see the section [Meeting Extensions for Microsoft Teams](../concept/meeting-extensibility-ms-teams.md).

**Parent Topic:**[Integrate Meeting Extensions self-configured app with Microsoft Teams](../concept/setup-meeting-extensibility-single-tenant.md)

