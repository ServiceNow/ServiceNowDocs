---
title: Manual client registration use case: GitHub
description: This use case illustrates manual client registration for GitHub. For this, the Client ID and Client secret must be generated for your OAuth application in GitHub account.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/mcp-mcr-gh-usecase.html
release: australia
topic_type: task
last_updated: "2026-08-03"
reading_time_minutes: 1
breadcrumb: [Manual client registration, Model Context Protocol connectors, Build integrations with connectors, Connect, Workflow Data Fabric]
---

# Manual client registration use case: GitHub

This use case illustrates manual client registration for GitHub. For this, the **Client ID** and **Client secret** must be generated for your OAuth application in GitHub account.

## Before you begin

Role required: admin

## Procedure

1.  Log in to [https://github.com/](https://github.com/).

2.  On the dashboard, select your profile icon.

    \[Omitted image "github-spoke-profile-icon.png"\] Alt text: GitHub profile icon.

3.  Select **Settings**.

4.  In the Settings page, on the left panel, select **Developer settings**.

5.  Click **OAuth Apps** and click **New OAuth app**.

6.  On the firm, fill these fields.

    |Field|Description|
    |-----|-----------|
    |Application name|Name to identify the application.|
    |Homepage URL|URL of your ServiceNow instance.|
    |Authorization callback URL|Callback URL of your ServiceNow instance in this format: `https://<ServiceNow-Instance-Name>.service-now.com/oauth_redirect.do`.|

7.  Click **Register Application**.

    \[Omitted image "github-register-app.png"\] Alt text: Register the application.

    The developer settings for the application are displayed.

8.  Click **Generate a new client secret**.

    Values of **Client ID** and **Client secret** are displayed.

    \[Omitted image "github-id-sec.png"\] Alt text: Values of Client ID and Client secret.

9.  Copy and record the values of **Client ID** and **Client secret** for later use.


## What to do next

Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Connect Hub** to manually register the client in your ServiceNow instance. During the client registration, provide the values of **Client ID** and **Client secret**. For instructions, see [Manual client registration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/mcp-mcr-a.md).

\[Omitted image "dcr-connect.jpg"\] Alt text:

