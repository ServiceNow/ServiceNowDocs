---
title: Update the records in the Microsoft Teams Configuration page
description: Update the created records in Microsoft Teams to make seamless calls.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2023-03-08"
reading_time_minutes: 1
breadcrumb: [Integrating Notify connector self-configured app with Microsoft Teams, Integration for Agent Experience, Setup for integrating self-configured apps, Setup the Servicenow instance, Microsoft Teams and Microsoft 365, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, Employee Service Management]
---

# Update the records in the Microsoft Teams Configuration page

Update the created records in Microsoft Teams to make seamless calls.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Notify** &gt; **Microsoft Teams** &gt; **Configuration**.

2.  On the Microsoft Teams Configuration form, fill in the fields.

    -   Credential Alias: Provide `sn_msteams_com_spk.MSTeamsCommunicationsSpoke` in the field.
    -   Application registry: Select the Application Registry record created in the section [Create a Microsoft Teams application registry entry to connect the created app to ServiceNow instance](create-app-registry-entry.md).
    -   Tenant ID: Enter the tenant ID created during the app creation in Microsoft Teams. For the tenant ID information on the Microsoft Azure portal, see [Create an app in Microsoft Teams to enable making calls](create-app-ms-teams.md).
    -   Requester: Select the Credential alias record created in the section [Create a Connection &amp; Credentials alias for Microsoft Teams](create-connection-credential-aliases.md).
    -   Service user Azure ID: Enter the objectId of the service user created in [Create a Service user to make calls from Microsoft Teams](provide-app-access-policy-nc-st.md).
    -   Enable create online meeting: Ensure this option is selected.
3.  Right-click the form header and select **Save**.


## Result

OIDC Application Registry is created.

**Parent Topic:**[Integrating Notify connector self-configured app with Microsoft Teams](../concept/setup-notify-ms-teams-single-tenant.md)

