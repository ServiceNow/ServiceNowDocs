---
title: Setup OAuth connectivity with Microsoft Teams Connections spoke for virtual meeting
description: Register your Microsoft Teams Communications spoke with ServiceNow instance for OAuth authorization.
locale: en-US
release: australia
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Connect Workplace Reservation Management with Microsoft Teams, Configure Workplace Reservation Management portal, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Setup OAuth connectivity with Microsoft Teams Connections spoke for virtual meeting

Register your Microsoft Teams Communications spoke with ServiceNow instance for OAuth authorization.

## Before you begin

Ensure the following:

-   [Authenticate Microsoft Teams with Microsoft Azure](authenticate-microsoft-teams-with-micrsoft-azure.md)
-   Change the application scope to Microsoft Teams Communication spoke.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Click **New**.

3.  Click **Connect to a third-party OAuth provider**.

4.  On the form, fill in the fields:

    |Field|Description|
    |-----|-----------|
    |Name|Unique name to identify the record, for example, Microsoft Teams Communications.|
    |Client ID|Client ID created during the app creation. You can copy it from **Application overview** in the Microsoft Azure portal.|
    |Client Secret|The password you generated when creating the app in Microsoft Azure.|
    |Default Grant Type|Grant type used to establish the token. Select **Client Credentials**.|
    |Authorization URL|OAuth authorization code endpoint. Enter `https://login.microsoftonline.com/<tenant_id>/oauth2/v2.0/authorize`.|
    |Token URL|OAuth server token endpoint. Enter `https://login.microsoftonline.com/<tenant_id>/oauth2/v2.0/token >`.|
    |Redirect URL|OAuth callback endpoint. The URL is automatically filled as `https://<instance-name>.service-now.com/oauth_redirect.do`.|

5.  Right-click in the form header and click **Save**.

    A system-generated OAuth entity profile is created and displayed in the OAuth Entity Profiles related list. For example, `Microsoft Teams Communication default_profile`.

6.  Update the OAuth entity profile.

    1.  Select the default OAuth entity profile.

    2.  On the form, in the OAuth Entity Profile Scopes related list, double-click **Insert a new row...**.

    3.  In the OAuth Entity Scope field, click the Search icon ![search icon](../../workplace-case-mgmt/image/search-icon.png).

    4.  In the OAuth Entity Scope window that opens, click **New**.

    5.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Enter a descriptive name, for example, MS Teams Communications.|
        |OAuth provider|Provider associated with this scope, for example, MS Sync.|
        |OAuth scope|The scope that you are granted by the provider. Enter `.default`.|

    6.  Click **Submit**.

7.  Save the changes.


## Result

The OAuth registration is added for Microsoft Teams Communications spoke.

**Parent Topic:**[Connect Workplace Reservation Management with Microsoft Teams](connect-rsv-mgmt-with-teams.md)

**Previous topic:**[Authenticate Microsoft Teams with Microsoft Azure](authenticate-microsoft-teams-with-micrsoft-azure.md)

**Next topic:**[Setup OAuth connectivity between ServiceNow and Microsoft Teams Graph](setup-connectivity-between-servicenow-and-microsoft-teams-graph.md)

