---
title: Set up a Microsoft Entra ID
description: This section describes how a Discovery Console for OT user can set up an Microsoft Entra ID integration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/users-entra-id-setup.html
release: australia
topic_type: task
last_updated: "2026-04-07"
reading_time_minutes: 2
breadcrumb: [Users page, Use the Console pages, Discovery Console for Operational Technology \(OT\), Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Set up a Microsoft Entra ID

This section describes how a Discovery Console for OT user can set up an **Microsoft Entra ID** integration.

## Before you begin

Role required: admin

## About this task

The **Microsoft Entra ID** integration enables users to log in to the Discovery Console for OT using their organization’s **Microsoft Entra ID** cloud identity access management \(IAM\) credentials. This removes the need for managing separate usernames and passwords within the application.

This feature relies on configuring an application in **Microsoft Entra ID** and providing the required details in the Console settings.

**Note:** This feature requires the Discovery Console for OT to have internet access.

This integration allows seamless and secure authentication using **Microsoft Entra ID**, improving user experience and aligning with enterprise identity management practices.

To enable an **Entra ID** log in, an administrator must complete the following steps.

**Note:** Check with Microsoft for the latest documentation before you begin this procedure.

## Procedure

1.  Register an application in Entra ID.

2.  In the Azure application:

    1.  Navigate to **Entra ID &gt; App** registrations.

    2.  Create a new application; for example "Console app".

    3.  Configure a Redirect URI pointing to the Console URL; for example, https://&lt;console-url&gt;.

3.  Collect required values.

    From the Entra ID application, locate the following information.

    -   Domain: Organization’s primary domain, for example, company.onmicrosoft.com.
    -   Tenant ID: Found in the Entra ID **Overview**.
    -   Client ID: Application \(client\) ID from App registration.
    -   Client Secret: Generated under **Certificates &amp; secrets**.
    -   Object ID: Application object ID.
4.  Configure Console settings.

5.  In the Discovery Console for OT:

    1.  Navigate to **Console &gt; Users**.

    2.  Next to the **Actions** button, select **Settings**.

        \[Omitted image "image.entra-id-top-settings-5"\] Alt text: Settings

    3.  Enter all required values.

        -   Domain
        -   Tenant ID
        -   Client ID
        -   Client Secret
        -   Object ID
        \[Omitted image "image.entraId-setting"\] Alt text: Entra ID Settings

    4.  Select **Save**.

6.  Enable the log in option.

    -   In the Entra settings, toggle **Show Microsoft Log in button**.
    -   This enables the SSO log in for end users.
    \[Omitted image "image.console-microsoft-log-in-smaller"\] Alt text: Microsoft sign in


## Result

Once configured, user can log in by doing:

1.  Open the Console log in page.
2.  Select the **Sign in with Microsoft** button.
3.  Authenticate using the organization's Microsoft account.
4.  After successfully authenticating, the user is redirected to the Console and is logged in.

**Note:** Important considerations:

-   The Client secret must be kept secure and renewed before expiration.
-   The redirect URI in Entra must exactly match the Console URL.
-   Incorrect Tenant ID or Client ID results in authentication failures.
-   Admin consent may be required when configuring permissions in Entra.

