---
title: Set up Microsoft Azure Active Directory
description: Set up Microsoft Azure Active Directory \(AD\).
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Microsoft Dynamics 365 Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Set up Microsoft Azure Active Directory

Set up Microsoft Azure Active Directory \(AD\).

## Before you begin

Role required: Global administrator and Dynamics 365 administrator in Microsoft admin center.

## Procedure

1.  Open Microsoft Azure App registration page and log in using an admin account.

2.  Click **+ New registration**.

    Register an application page appears.

3.  In the **Name** field, enter the name of the application that you want to register.

4.  Under Supported account types, select an account with the required organizational directory.

5.  Click **Register**.

6.  Open the application that you registered and go to **Overview** section.

7.  Collect the Application \(client\) ID and Application \(tenant\) ID.

8.  Go to Certificates and Secrets section.

9.  Create a new client secret.

10. Collect the client secret key.

    You will need the client secret key while configuring your ServiceNow instance.

11. Under API Permission, click **+ Add a permission** and select APIs my organization uses.

12. Select Microsoft Graph and add the following Application Permissions.

    -   `Organization.Read.All`
    -   `User.Read.All`
    -   `Offline_access`
13. Select Dynamics CRM and add the following Application Permissions.

    `user_impersonation`

14. Under Grant consent, click **Grant admin consent**.

15. In the Authentication section, under the Redirect URI, enter the redirect URI of the ServiceNow instance.


