---
title: Update the records in the Microsoft Teams Configuration page
description: Update the created records in Microsoft Teams to make seamless calls.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/employee-experience-foundation/map-app-reg-cred-alias-ms-teams-config.html
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrating Notify connector self-configured app with Microsoft Teams, Integration for Agent Experience, Setup for integrating self-configured apps, Setup the Servicenow instance, Integrating ServiceNow with Microsoft Teams and Microsoft 365, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Update the records in the Microsoft Teams Configuration page

Update the created records in Microsoft Teams to make seamless calls.

## Before you begin

Role required: Microsoft Teams admin

## Procedure

1.  Navigate to **All** &gt; **Notify** &gt; **Microsoft Teams** &gt; **Configuration**.

2.  On the Microsoft Teams Configuration form, fill in the fields.

    -   Credential Alias: Provide `sn_msteams_com_spk.MSTeamsCommunicationsSpoke` in the field.
    -   Application registry: Select the Application Registry record created in the section [Create a Microsoft Teams application registry entry to connect the created app to ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/create-app-registry-entry.md).
    -   Tenant ID: Enter the tenant ID created during the app creation in Microsoft Teams. For the tenant ID information on the Microsoft Azure portal, see [Create an app in Microsoft Teams to enable making calls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/create-app-ms-teams.md).
    -   Requester: Select the Credential alias record created in the section [Create a Connection &amp; Credentials alias for Microsoft Teams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/create-connection-credential-aliases.md).
    -   Service user Azure ID: Enter the objectId of the service user created in [Create a Service user to make calls from Microsoft Teams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/provide-app-access-policy-nc-st.md).
    -   Enable create online meeting: Ensure this option is selected.
3.  Right-click the form header and select **Save**.


## Result

OIDC Application Registry is created.

**Parent Topic:**[Integrating Notify connector self-configured app with Microsoft Teams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/setup-notify-ms-teams-single-tenant.md)

