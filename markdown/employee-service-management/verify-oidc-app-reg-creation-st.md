---
title: Verify OIDC Application Registry creation for a self-configured app setup
description: Verify whether the OIDC Application Registry was created when Microsoft Teams Application Registry was created and mapped to the configuration during a self-configured app setup process.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Integrating Notify connector self-configured app with Microsoft Teams, Integration for Agent Experience, Setup for integrating self-configured apps, Setup the Servicenow instance, Microsoft Teams and Microsoft 365, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, Employee Service Management]
---

# Verify OIDC Application Registry creation for a self-configured app setup

Verify whether the OIDC Application Registry was created when Microsoft Teams Application Registry was created and mapped to the configuration during a self-configured app setup process.

## Before you begin

Role required: admin

## About this task

Mapping a Microsoft Teams Application Registry after creation automatic creates an OIDC Application Registry as a part of the self-configured app setup. If this automatic creation fails, issues occur in processing call backs that might cause meeting information not to be updated in real time.

For more information, see [Create a Microsoft Teams application registry entry to connect the created app to ServiceNow instance](create-app-registry-entry.md) and [Update the records in the Microsoft Teams Configuration page](map-app-reg-cred-alias-ms-teams-config.md).

## Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Filter the list by the Client ID created during the app creation in Microsoft Teams.

    Ensure that there is also an External OIDC Provider type Application Registry for the same Client ID along with the OAuth Provider type created. For the External OIDC Provider type Application Registry information, see [Update the records in the Microsoft Teams Configuration page](map-app-reg-cred-alias-ms-teams-config.md). For the Client ID information on the Microsoft Azure portal, see [Create an app in Microsoft Teams to enable making calls](create-app-ms-teams.md).

3.  If the Application Registry with External OIDC Provider type for the Client ID is missing, create it manually.

    1.  Select **New** on the Application Registries page.

    2.  Select **Configure an OIDC provider to verify ID tokens**.

    3.  In the **Name** field, enter your OAuth provider name and append `OIDC`.

        For example, if your OAuth Provider name is `MS Teams SC Config`, you would name your OIDC `MS Teams SC Config OIDC`.

    4.  Select **Client ID** same as the OAuth Provider value.

    5.  For the **Client Secret** value, select **invalid\_value**. \(This value is not relevant\).

    6.  For the **OAuth OIDC Provider Configuration** value, select **Notify Teams OIDC Config**.

    7.  For the **Redirect URL** valuesas **invalid\_value** \(This value is not relevant\).

    8.  Right-click the form header and select **Save**.

    By default, an OAuth Entity profile is created. Ensure the **Grant Type** is **Client Credentials**.

4.  Create an OAuth Entity scope.

    1.  Select **OAuth Entity Scopes** tab on the Application Registries page.

    2.  Double-click **Insert a new row** and enter `Notify MS Teams SC OIDC` appended with `Default Profile`.

        For example, if your OIDC Config name is `MS Teams SC Config OIDC`, then you can enter the name as `MS Teams SC Config OIDC Default Profile`.

    3.  Enter `https://api.botframework.com/.default` as the OAuth scope.

    4.  Right-click the form header and select **Save**.


## What to do next

[Configure Notify connector for Microsoft Teams](../concept/config-notify-ms-teams.md).

**Parent Topic:**[Integrating Notify connector self-configured app with Microsoft Teams](../concept/setup-notify-ms-teams-single-tenant.md)

