---
title: Set up Microsoft Azure Active Directory
description: Set up Microsoft Azure Active Directory \(AD\).
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Microsoft Dynamics 365 Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up Microsoft Azure Active Directory

Set up Microsoft Azure Active Directory \(AD\).

## Before you begin

Role required: Global administrator and Dynamics 365 administrator in Microsoft admin center.

## Procedure

1.  Open Microsoft Azure App registration page and log in using an admin account.

2.  Select **+ New registration**.

    Register an application page appears.

3.  In the **Name** field, enter the name of the application that you want to register.

4.  Under Supported account types, select an account with the required organizational directory.

5.  Select **Register**.

6.  Open the application that you registered and navigate to the **Overview** section.

7.  Collect the Application \(client\) ID and Application \(tenant\) ID.

8.  Navigate to the Certificates and Secrets section.

9.  Create a client secret and collect the client secret key.

    You need the client secret key while configuring your ServiceNow instance.

10. Under API Permission, select **+ Add a permission** and then select **APIs my organization uses**.

11. Select Microsoft Graph and add the necessary permissions for both Delegated and Application types as required.

    -   `Organization.Read.All`
    -   `User.Read.All`
    -   `Offline_access`
12. Select Dynamics CRM and add the following permission.

    `user_impersonation`

    **Note:** These steps aren't applicable for user\_impersonation or Microsoft Dynamics CRM connection because the user\_impersonation scope is offered as a Delegated permission in Microsoft Dynamics CRM.

13. Under Grant consent, select **Grant admin consent**.

14. In the Authentication section, under the Redirect URI, enter the redirect URI of the ServiceNow instance.


