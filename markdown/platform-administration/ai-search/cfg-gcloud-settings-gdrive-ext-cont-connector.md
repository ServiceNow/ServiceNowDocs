---
title: Configure Google Drive for external content indexing
description: Enable the Google Drive and Admin SDK APIs and create a Google Cloud service account to allow the Google Drive external content connector to crawl shared drives and security principals in your Google Drive source system.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-06-25"
reading_time_minutes: 4
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configuring source systems for external content indexing, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure Google Drive for external content indexing

Enable the Google Drive and Admin SDK APIs and create a Google Cloud service account to allow the Google Drive external content connector to crawl shared drives and security principals in your Google Drive source system.

## Before you begin

You need super administrator credentials for your organization's Google Cloud and Google Admin consoles. To learn about super administrator accounts, see the [Prebuilt administrator roles](https://support.google.com/a/answer/2405986) and [Super administrator account best practices](https://cloud.google.com/resource-manager/docs/super-admin-best-practices) Google resources.

Role required: none

## About this task

The Google Drive external content connector retrieves content from your Google Drive source system using APIs and a service account configured in the Google Cloud console. The connector also relies on domain-wide delegation for the service account, which is configured in the Google Admin console.

Your search administrator can use settings copied from the Google Cloud console to configure the Google Drive external content connector for proper connection to your Google Drive source system.

## Procedure

1.  Enable the Google Drive and Admin SDK APIs for your selected project.

    1.  Log in to the Google Cloud console at [https://console.cloud.google.com/](https://console.cloud.google.com/).

    2.  If necessary, select the displayed project name to open the **Select a project** dialog box, then select the appropriate project for your organization's Google Drive content.

        The console displays the selected project's name.

    3.  Locate and select the **APIs &amp; Services** menu item.

        If this menu item is not visible on the Google Cloud page, enter `APIs & Services` in the search field and select the **APIs &amp; Services** search result.

    4.  On the APIs &amp; Services page, select **Enable APIs and Services**.

    5.  Locate and select the **Google Drive API** tile, then select **Enable**.

        The API appears in the Enabled APIs &amp; services listing for your project.

    6.  Repeat steps [1.c](cfg-gcloud-settings-gdrive-ext-cont-connector.md#enable-api-first-substep) through [1.e](cfg-gcloud-settings-gdrive-ext-cont-connector.md#enable-api-last-substep), but this time locate, select, and enable the **Admin SDK API**.

2.  Create a new Google Cloud service account for your selected project.

    1.  In the Google Cloud console, locate and select the **IAM &amp; Admin** &gt; **Service Accounts** menu item.

        If this menu item is not visible on the Google Cloud page, enter `Service Accounts` in the search field and select the **Service Accounts** search result.

    2.  On the Service accounts page, select **Create Service Account**.

    3.  Enter a display name, an account ID, and a description for the service account, then select **Create and Continue**.

    4.  Select **Done**.

        The service account appears in the Service Accounts listing for your project.

3.  Add a private key to your new Google Cloud service account.

    1.  In the Google Cloud console, on the Service Accounts page, select the email address for the service account.

    2.  In the service account editor, select the **Keys** section header.

    3.  Select **Add key**, then select **Create new key**.

    4.  In the Create private key dialog box, select the JSON key type, then select **Create**.

    5.  When prompted, download the JSON-format private key file to a secure location.

        **Important:** Your AI Search administrator needs the JSON-format private key file to configure a Google Drive external content connector.

    6.  Select **Close**.

4.  Activate domain-wide delegation in Google Admin for your new Google Cloud service account.

    1.  In the Google Cloud console, on the Service Accounts page, copy and record the OAuth 2 Client ID value for your new service account.

    2.  Log in to the Google Admin console at [https://admin.google.com/](https://admin.google.com/).

    3.  Navigate to **Security** &gt; **Access and data control** &gt; **API controls**.

    4.  Select **Manage domain wide delegation**.

    5.  In the API clients list, select **Add new**.

    6.  In the **Client ID** field, enter the service account's OAuth 2 Client ID that you copied in step [4.a](cfg-gcloud-settings-gdrive-ext-cont-connector.md#copy-oauth-2-client-id-substep).

    7.  In the **OAuth scopes** field, enter `https://www.googleapis.com/auth/drive.readonly, https://www.googleapis.com/auth/admin.directory.user.readonly, https://www.googleapis.com/auth/admin.directory.group.readonly`.

        This field's value is a single comma-separated string, not multiple strings.

    8.  Select **Authorize**.


## What to do next

Provide the following items to your AI Search administrator:

-   Your Google Workspace domain name, in the format `example.com`. You can find your domain name by navigating to the [https://admin.google.com/ac/domains/manage](https://admin.google.com/ac/domains/manage) Google administration page.
-   The email address for a user account that has permission to access your Google Workspace domain’s user directory. The Google Drive external content connector uses this account to enumerate users and groups of the domain.

    **Note:** This should be an email address from your organization's domain, not a service account email address from the `iam.gserviceaccount.com` domain.

-   The JSON private key file for the Google Cloud service account that you downloaded in step [3.e](cfg-gcloud-settings-gdrive-ext-cont-connector.md#download-json-private-key-substep).

Your AI Search administrator needs these items to configure a Google Drive external content connector to retrieve searchable content and security principals from your Google Drive instance.

For details on creating and configuring a Google Drive external content connector, see [Create a Google Drive external content connector](create-ext-cont-connector-gdrive.md).

**Parent Topic:**[Configuring source systems for external content indexing](../concept/cfg-src-sys-ext-content-indexing.md)

