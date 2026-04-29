---
title: Configure Workday for external content indexing
description: Create and authorize an OAuth 2.0 API client in your Workday tenant to allow the Workday external content connector to access your Workday source system.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Workday external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure Workday for external content indexing

Create and authorize an OAuth 2.0 API client in your Workday tenant to allow the Workday external content connector to access your Workday source system.

## Before you begin

You need administrator privileges for your organization's Workday tenant. You need modify access for these domains in the System functional area:

-   Set Up: Tenant Setup - Security
-   Security Administration

A Workday admin must have already completed the preliminary tasks shown in the following table.

|Preliminary task|Description|
|----------------|-----------|
|[Configure Workday security settings](configure-workday-security-settings.md)|Required task.|
|[Configure access to help articles in Workday](configure-public-help-articles-workday.md)|Optional task. Only required if you want the connector to retrieve searchable content and metadata from help articles accessible by all users in your Workday organization.|
|[Configure a payslip report in Workday](configure-payslip-report-workday.md)|Optional task. Only required if you want the connector to retrieve searchable content and metadata from payroll data.|
|[Configure a Learning assignment custom report in Workday](configure-learning-assignment-report-workday.md) and [Get Workday task code for Find Learning Assignments](get-workday-task-code-learning-assignments.md)|Optional tasks. Only required if you want the connector to retrieve searchable content and metadata from Learning assignment data.|
|[Get Workday task code for My Team's Birthday](get-workday-task-code-birthday.md) and [Get Workday task code for My Team Anniversaries](get-workday-task-code-anniversaries.md)|Optional tasks. Only required if you want the connector to retrieve searchable content and metadata from Manager hub data.|

Role required: none

## About this task

The Workday external content connector retrieves public help articles, benefits, learning assignments, Manager Insights Hub data, payroll information, PTO information, and vacation policies from your Workday source system using the Workday REST API.

To allow the connector to access your Workday source system via the Workday REST API, you must configure and authorize an OAuth 2.0 API client in your Workday tenant. Your connector admin can use settings copied from this OAuth 2.0 API client and your Workday tenant to configure the Workday external connector for proper connection to your source system.

## Procedure

1.  Log in to your Workday tenant and record its base connection URL and tenant name.

    1.  Navigate to your Workday tenant and log in with developer credentials.

    2.  Copy the base connection URL and the tenant name for your Workday tenant and record them in a secure location.

        Your tenant's base connection URL is the HTTPS protocol prefix and the hostname from the Workday URL that you see after logging in. Your tenant's name is the first path element that follows the hostname in the Workday URL. As an example, if logging in takes you to `https://wd-2-impl-services1.workday.com/example/d/home.htmld`, your base connection URL is `https://wd-2-impl-services1.workday.com` and your tenant name is `example`.

        **Important:** Your external content connector admin needs the base connection URL and tenant name when configuring the Workday external content connector.

2.  Enable OAuth 2.0 clients in your Workday tenant.

    1.  In the Workday search bar, search for the **Edit Tenant Setup - Security** task and select it.

    2.  On the Edit Tenant Setup - Security form, in the OAuth 2.0 Settings section, select the **OAuth 2.0 Clients Enabled** option, then select **OK**.

    3.  Select **Done**.

3.  Create a new OAuth 2.0 API client for the Workday external content connector.

    1.  In the Workday search bar, search for the **Register API Client** task and select it.

    2.  On the Register API Client form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Client Name|Unique name for this API client. As an example, you might enter `Workday external content connector`.|
        |Client Grant Type|Select **Authorization Code Grant**.|
        |Access Token Type|Select **Bearer**.|
        |Redirection URI|Enter `https://<instance-name>.service-now.com/oauth_redirect.do`, replacing `<instance-name>` with your ServiceNow AI Platform® instance name.|
        |Non-Expiring Refresh Tokens|Select this option.|
        |Grant Administrative Consent|Select this option.|
        |Scope \(Functional Areas\)|In the drop-down list, select **Custom Objects**, then select all of the listed scopes.|
        |Include Workday Owned Scope|Select this option.|

    3.  Select **OK**.

    Your new OAuth 2.0 API client is registered.

4.  Find the client ID and client secret for your new OAuth 2.0 API client.

    1.  Copy the client ID for your new OAuth 2.0 API client and store it in a secure location.

        **Important:** Your external content connector admin needs this client ID when configuring the Workday external content connector.

    2.  Copy the client secret for your new OAuth 2.0 API client and store it in a secure location.

        **Important:** Your external content connector admin needs this client secret when configuring the Workday external content connector.

    3.  Copy the token endpoint URL for your new OAuth 2.0 API client and store it in a secure location.

        **Important:** Your external content connector admin needs this token endpoint URL when configuring the Workday external content connector.

    4.  Copy the authorization endpoint URL for your new OAuth 2.0 API client and store it in a secure location.

        **Important:** Your external content connector admin needs this authorization endpoint URL when configuring the Workday external content connector.


## What to do next

Provide the following items to your connector admin:

-   The base connection URL for your Workday tenant that you copied in step [1.b](configure-workday-external-content-indexing.md#copy-connection-url-tenant-name-step).
-   The tenant name that you copied in step [1.b](configure-workday-external-content-indexing.md#copy-connection-url-tenant-name-step).
-   The client ID that you copied in step [4.a](configure-workday-external-content-indexing.md#copy-client-id-step).
-   The client secret that you copied in step [4.b](configure-workday-external-content-indexing.md#copy-client-secret-step).
-   The token endpoint URL that you copied in step [4.c](configure-workday-external-content-indexing.md#copy-token-url-step).
-   The authorization endpoint URL that you copied in step [4.d](configure-workday-external-content-indexing.md#copy-auth-url-step).

Your connector admin needs these items to configure a Workday external content connector to retrieve Workday content from your Workday source system.

For details on creating and configuring a Workday external content connector, see [Create a Workday external content connector](create-ext-cont-connector-workday.md).

**Parent Topic:**[Workday external content connector](../concept/workday-external-content-connector.md)

