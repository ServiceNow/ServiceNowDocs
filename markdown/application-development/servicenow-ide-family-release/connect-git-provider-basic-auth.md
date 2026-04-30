---
title: Connect to a Git provider using basic authentication with the ServiceNow IDE
description: Connect to a Git domain using basic authentication credentials to manage applications in source control from the ServiceNow IDE.
locale: en-US
release: zurich
product: ServiceNow IDE \(Family Release\)
classification: servicenow-ide-family-release
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Integrate source control, ServiceNow IDE, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Connect to a Git provider using basic authentication with the ServiceNow IDE

Connect to a Git domain using basic authentication credentials to manage applications in source control from the ServiceNow IDE.

## Before you begin

-   From your Git provider, generate a personal access token to use for basic authentication to the Git domain . You must provide your Git user name and personal access token when configuring your credentials for the ServiceNow IDE.
-   Create a dedicated Git repository for an application in a Git provider such as GitHub, GitLab, Bitbucket, or Azure Repos.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **App Development** &gt; **ServiceNow IDE**.

2.  Use one of the following keyboard shortcuts to open the command palette:

    -   Windows: Ctrl-Shift-P
    -   Mac: Cmd-Shift-P
3.  Enter `Git: Set IDE Git credentials` and press Enter.

4.  From the New Git credential form, select **Basic auth**.

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Git repository URL|The HTTPS URL of a Git repository associated with your Git credentials.|
    |Git username|Your Git user name.|
    |Personal access token|A personal access token that you generate from your Git provider.|

6.  Select **Submit**.


## Result

Your Git credentials are associated with your user on the instance and used for all repositories in the domain from the Git repository URL. If you add different credentials for a repository in the same domain, the new credentials are used and the previous credentials are set to inactive.

## What to do next

After initializing or cloning a repository, you can begin using source control. For more information, see [Using source control in the ServiceNow IDE](../concept/using-source-control-servicenow-ide.md).

To manage existing Git credentials, use the `Git: Manage Git credentials` command from the command palette.

**Parent Topic:**[Integrating source control with the ServiceNow IDE](../concept/integrating-source-control-servicenow-ide.md)

**Related topics**  


[Connect to a Git provider using OAuth 2.0 with the ServiceNow IDE](../concept/connect-git-provider-oauth-2.md#)

[Configure a MID Server to use source control with the ServiceNow IDE](configure-mid-server-source-control.md)

[Initialize a Git repository with the ServiceNow IDE](initialize-git-repository-servicenow-ide.md)

[Using source control in the ServiceNow IDE](../concept/using-source-control-servicenow-ide.md)

