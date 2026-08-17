---
title: Connect to a Git provider using basic authentication
description: Connect to a Git domain or repository using basic authentication credentials to manage applications in Fluent source control from ServiceNow Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/fluent-sc-connect-to-git-provider-basic-auth.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2026-07-24"
reading_time_minutes: 1
keywords: [ServiceNow studio, source control, fluent, pro-code development]
breadcrumb: [Fluent source control in ServiceNow Studio, Source control integration, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Connect to a Git provider using basic authentication

Connect to a Git domain or repository using basic authentication credentials to manage applications in Fluent source control from ServiceNow Studio.

## Before you begin

-   From your Git provider, generate a personal access token to use for basic authentication to the Git domain. You must provide your Git user name and personal access token when configuring your credentials for ServiceNow Studio.
-   Create a dedicated Git repository for an application in a Git provider such as GitHub, GitLab, Bitbucket, or Azure Repos.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  Use one of the following keyboard shortcuts to open the command palette:

    -   Windows: Ctrl-Shift-P
    -   Mac: Cmd-Shift-P
3.  Enter `Git: Set IDE Git credentials` and press Enter.

4.  From the New Git credential form, select **Basic auth**.

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Git repository URL|HTTPS URL of a Git repository associated with your Git credentials.|
    |Git username|Git username.|
    |Personal access token|Personal access token that you generate from your Git provider.|
    |Use this credential for all repositories|Option to use the credentials for all repositories in the Git domain associated with the Git repository URL.|

6.  Select **Submit**.


## Result

Your Git credentials are associated with your user on the instance and used for all repositories in the domain from the Git repository URL. If you add different credentials for a repository in the same domain, the new credentials are used and the previous credentials are set to inactive.

## What to do next

After initializing or cloning a repository, you can begin using Fluent source control. For more information, see [Using Fluent source control in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/fluent-sc-using-fluent-source-control.md).

To manage existing Git credentials, use the `Git: Manage Git credentials` command from the command palette.

**Parent Topic:**[Fluent source control in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/fluent-source-control-sn-studio.md)

