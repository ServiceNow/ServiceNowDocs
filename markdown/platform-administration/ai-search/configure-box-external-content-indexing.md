---
title: Configure Box for external content indexing
description: Create and authorize an OAuth 2.0 application in the Box developer console to allow the Box external content connector to access your Box source system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-search/configure-box-external-content-indexing.html
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Box external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Configure Box for external content indexing

Create and authorize an OAuth 2.0 application in the Box developer console to allow the Box external content connector to access your Box source system.

## Before you begin

You need administrator access to the Box developer console and the Box Admin UI portal.

You must have created a private/public key pair for the Box external content connector and extracted the public key certificate in PEM-encoded \(Base64 ASCII\) X.509 format. For details on creating the public/private key pair and extracting the public key certificate, see [Create a public/private key pair for the Box external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/create-key-pair-box-external-content-connector.md).

Role required: none

## About this task

The Box external content connector retrieves documents and user permissions from your Box source system using the Box API.

To allow the connector to access your Box source system via the Box API, you must configure and authorize an OAuth 2.0 application in the Box developer console. Your connector administrator can use settings copied from the OAuth 2.0 application and its API key to configure the Box external connector for proper connection to your source system.

## Procedure

1.  In the Box developer console, create a new OAuth 2.0 application for the Box external content connector.

    1.  Navigate to [https://app.box.com/developers/console](https://app.box.com/developers/console) and log in with administrator credentials.

    2.  Select **Create Platform App**, then select **Custom App**.

        \[Omitted image "box-create-platform-app.png"\] Alt text: My Platform Apps screen in Box developer console.

    3.  In the Create a Custom App window, enter a name for your app and specify its purpose, then select **Next**.

        \[Omitted image "box-create-custom-app-1.png"\] Alt text: Create a Custom App screen 1 of 2 in Box developer console.

    4.  In the Create a Custom App windows, select **Server Authentication \(with JWT\)**, then select **Create App**.

        \[Omitted image "box-create-custom-app-2.png"\] Alt text: Create a Custom App screen 2 of 2 in Box developer console.

        The **Configuration** screen for your new OAuth 2.0 application appears.

2.  Configure your new OAuth 2.0 application with required settings and generate a public/private keypair for it.

    1.  In the App Access Level section, select the **App + Enterprise Access** option.

        \[Omitted image "box-configuration-app-access-level.png"\] Alt text: App Access Level configuration settings in Box developer console.

    2.  In the Application Scopes section, under the **Content Actions** heading, select the **Read all files and folders stored in Box** and **Write all files and folders stored in Box** options if they're not already selected.

        \[Omitted image "box-configuration-application-scopes.png"\] Alt text: Application Scopes configuration settings in Box developer console.

    3.  In the Advanced Features section, select the **Make API calls using the as-is header** and **Generate user access tokens** options.

        \[Omitted image "box-configuration-advanced-features.png"\] Alt text: Advanced Features configuration settings in Box developer console.

    4.  In the Add and Manage Public Keys section, select **Add a Public Key**.

        \[Omitted image "box-configuration-add-manage-public-keys.png"\] Alt text: Add and Manage Public Keys configuration settings in Box developer console.

        The Add a new Public Key dialog box appears.

    5.  In the Add a new Public Key dialog box, paste the PEM-encoded public key text, including the `-----BEGIN PUBLIC KEY-----` and `-----END PUBLIC KEY-----` markers, into the **Public Key** field, then select **Verify and Save**.

        \[Omitted image "box-configuration-add-new-public-key.png"\] Alt text: Add a new Public Key dialog box in Box developer console.

    6.  Copy the public key ID string that Box displays for the new public key and store it in a secure location.

        \[Omitted image "box-configuration-copy-public-key-id.png"\] Alt text: ID shown for new public key in Box developer console.

        **Important:** Your connector administrator needs this public key ID string when configuring the Box external content connector.

    7.  In the App Settings section, select **Download as JSON**, then save the downloaded JSON-format settings file in a secure location.

        \[Omitted image "box-configuration-download-json-file.png"\] Alt text: App Settings section in Box developer console.

        **Important:** Your connector administrator needs this JSON-format settings file when configuring the Box external content connector.

    8.  Select **Save Changes**.

        A message appears, reporting that the OAuth 2.0 app's configuration has been successfully updated.

3.  Submit an authorization request for your new OAuth 2.0 application.

    1.  Navigate to the **Authorization** screen for your new OAuth 2.0 application.

    2.  Select **Review and Submit**.

        \[Omitted image "box-authorization-review-submit.png"\] Alt text: Review and Submit option in Box developer console authorization settings.

    3.  On the Review App Authorization Submission screen, enter a description for your OAuth 2.0 application, then select **Submit**.

        \[Omitted image "box-review-app-authorization-submission.png"\] Alt text: Review App Authorization Submission screen in Box developer console.

        The app's Authorization Status shows **Pending Authorization**.

4.  In the Box Admin UI portal, authorize your new OAuth 2.0 application.

    1.  Navigate to [https://app.box.com/master](https://app.box.com/master) and log in with administrator credentials.

    2.  Select the **Integrations** menu icon \[Omitted image "box-integrations-icon.png"\] Alt text:, then navigate to the **Platform Apps Manager** tab.

    3.  Select **Server Authentication Apps** and find the entry for your new OAuth 2.0 application.

    4.  Open the app entry's context menu by selecting its overflow icon \[Omitted image "box-admin-ui-overflow-icon.png"\] Alt text:, then select **Authorize App**.

        \[Omitted image "box-platform-apps-manager-authorize-app.png"\] Alt text: Platform Apps Manager screen in Box Admin UI portal.

    5.  On the Authorize App screen, select **Authorize**.

        \[Omitted image "box-authorize-app.png"\] Alt text: Authorize App screen in Box Admin UI portal.

        The app's Authorization Status changes to **Authorized**.


## What to do next

Provide the following items to your connector administrator:

-   The email address for the Box administrator account that you used to configure the OAuth 2.0 application.
-   The public key ID string that you copied in step [2.f](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/configure-box-external-content-indexing.md).
-   The JSON-format settings file that you downloaded in step [2.g](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/configure-box-external-content-indexing.md).

Your connector administrator needs these items to configure a Box external content connector to retrieve user boxes and security principals from your Box source system.

For details on creating and configuring a Box Cloud external content connector, see [Create a Box external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/create-ext-cont-connector-box.md).

**Parent Topic:**[Box external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/box-external-content-connector.md)

