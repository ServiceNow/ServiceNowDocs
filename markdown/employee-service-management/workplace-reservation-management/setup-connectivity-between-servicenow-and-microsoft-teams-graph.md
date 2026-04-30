---
title: Setup OAuth connectivity between ServiceNow and Microsoft Teams Graph
description: Register your Microsoft Teams Graph with ServiceNow instance for OAuth authorization to get recordings after a virtual meeting.
locale: en-US
release: xanadu
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Connect Workplace Reservation Management with Microsoft Teams, Configure Workplace Reservation Management portal, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Setup OAuth connectivity between ServiceNow and Microsoft Teams Graph

Register your Microsoft Teams Graph with ServiceNow® instance for OAuth authorization to get recordings after a virtual meeting.

## Before you begin

Authenticate Microsoft Teams Graph with Microsoft Azure. Follow the similar procedure explained in [Authenticate Microsoft Teams with Microsoft Azure](authenticate-microsoft-teams-with-micrsoft-azure.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Select **Microsoft Teams Graph**.

3.  On the form, edit the following fields:

    |Filed|Description|
    |-----|-----------|
    |Client ID|Client ID created during the app creation. You can copy it from **Application overview** in the Microsoft Azure portal.|
    |Client Secret|The password you generated when creating the app in Microsoft Azure.|
    |Authorization URL|OAuth authorization code endpoint. Enter `https://login.microsoftonline.com/<tenant_id>/oauth2/v2.0/authorize`.|
    |Token URL|OAuth server token endpoint. Enter `https://login.microsoftonline.com/<tenant_id>/oauth2/v2.0/token >`.|
    |Redirect URL|OAuth callback endpoint. The URL is automatically filled as `https://<instance-name>.service-now.com/oauth_redirect.do`.|

4.  Right-click in the form header and click **Save**.

    A system-generated OAuth entity profile is created and displayed in the OAuth Entity Profiles related list. For example, `Microsoft Teams Graph default_profile`.

5.  Save the changes.


## Result

The OAuth registration is added for Microsoft Teams Graph.

**Parent Topic:**[Connect Workplace Reservation Management with Microsoft Teams](connect-rsv-mgmt-with-teams.md)

**Previous topic:**[Setup OAuth connectivity with Microsoft Teams Connections spoke for virtual meeting](setup-connectivity-between-servicenow-and-microsoft-teams-connection-spoke.md)

**Next topic:**[Create credential for Microsoft Teams Communication](create-credentials-for-microsoft-teams-connection.md)

