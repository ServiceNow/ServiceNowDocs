---
title: Register a custom application in the Microsoft Azure portal
description: Provide authorization for the ServiceNow instance by registering a custom application with Azure Active Directory.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/digital-end-user-experience-dex/register-a-custom-application-ms-azure-portal.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-10-24"
reading_time_minutes: 1
breadcrumb: [Configuring DEX for Microsoft 365, Configure, Digital End-User Experience, IT Operations Management]
---

# Register a custom application in the Microsoft Azure portal

Provide authorization for the ServiceNow instance by registering a custom application with Azure Active Directory.

## Before you begin

Role required: Azure Active Directory admin

## Procedure

1.  Log in to the [Microsoft Azure portal](https://portal.azure.com/).

2.  Under **Azure services**, select **App registrations**.

    \[Omitted image "ms-teams-app-reg.png"\] Alt text: Register an app.

3.  Under **App Registrations**, select **New registration**.

    \[Omitted image "ms-teams-new-reg.png"\] Alt text: New app registration.

4.  Enter a name and select **Register**.

    \[Omitted image "ms-teams-regapp.png"\] Alt text: Registering an app.

    The application is registered and essential application details are displayed.

5.  Copy and record the value of **Application \(client\) ID** and **Directory \(tenant\) ID** for later use.

6.  Select **Certificates &amp; secrets**, and select **New client secret**.

7.  In the form, enter a **Description** and select **Add**.

    \[Omitted image "ms-teams-client-sec.png"\] Alt text: Add a client secret.

8.  Copy the **Value** of the client secret for later use.

    \[Omitted image "ms-teams-copy-sec.png"\] Alt text: Copy the client secret.

9.  Select **API permissions**.

10. Under **Configured permissions**, select **Add a permission**.

11. Under **Request API permissions**, select **Microsoft Graph**.

    \[Omitted image "ms-teams-api-perm.png"\] Alt text: Add permissions.

12. Select **Application permissions**.

13. Ensure that these permissions are provided to your custom app:

    -   User.Read.All
    -   CallRecords.Read.All
    For more information about the API permissions, see [Add permissions to access your web API](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-configure-app-access-web-apis#add-permissions-to-access-your-web-api) in [Microsoft Learn](https://learn.microsoft.com/en-us/).

14. Select **Add permissions**.

    \[Omitted image "Application\_permissions.png"\] Alt text: Microsoft Graph application permissions with the Add permissions button

15. Select **Grant admin consent**.

    \[Omitted image "Configured\_permissions.png"\] Alt text: Configured permissions with the Grant admin consent option

    The system prompts you to confirm your consent.

16. Select **Yes**.

    A confirmation message is displayed that admin consent is granted for the requested permissions.

    \[Omitted image "Granted\_permision.png"\] Alt text: Confirmation message that admin consent is granted for the requested permissions


