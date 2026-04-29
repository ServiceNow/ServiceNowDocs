---
title: Integrating source control with the ServiceNow IDE
description: Integrate with remote Git repositories to manage applications in source control with the ServiceNow IDE.
locale: en-US
release: australia
product: ServiceNow IDE \(Family Release\)
classification: servicenow-ide-family-release
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ServiceNow IDE, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Integrating source control with the ServiceNow IDE

Integrate with remote Git repositories to manage applications in source control with the ServiceNow IDE.

You can connect to a Git provider using basic or OAuth 2.0 authentication. Then, initialize a repository for an application in the ServiceNow IDE and push it to a remote repository or clone a remote repository that contains an application. After setting up authentication and connecting to a repository, you can use common Git commands to manage applications in source control.

Learn how to get started using source control in the ServiceNow IDE in the following topics.

## Instance requirements

If an instance includes modified configurations for saving attachments, the following requirements must be met to perform Git operations:

-   If the **glide.attachment.extensions** system property is configured, it must contain `txt,gitdata`.
-   If the **glide.security.attachment\_type.use\_blacklist** system property is set to true, the **glide.attachment.blacklisted.extensions** system property must not contain `txt,gitdata` and the **glide.attachment.blacklisted.types** system property must not contain `text/plain,application/octet-stream`.

If you want to use custom extensions for attachments, set the following properties to custom values: **sn\_glider.git.attachment.extension.text** and **sn\_glider.git.attachment.extension.binary**. For more information, see [ServiceNow IDE properties](../reference/servicenow-ide-properties.md).

-   **[Connect to a Git provider using basic authentication with the ServiceNow IDE](../task/connect-git-provider-basic-auth.md)**  
Connect to a Git domain using basic authentication credentials to manage applications in source control from the ServiceNow IDE.
-   **[Connect to a Git provider using OAuth 2.0 with the ServiceNow IDE](connect-git-provider-oauth-2.md#)**  
Set up an OAuth 2.0 application registry and credentials to connect to your Git provider from the ServiceNow IDE.
-   **[Configure a MID Server to use source control with the ServiceNow IDE](../task/configure-mid-server-source-control.md)**  
Configure a MID Server to use source control with the ServiceNow IDE if your Git provider is behind a firewall.
-   **[Initialize a Git repository with the ServiceNow IDE](../task/initialize-git-repository-servicenow-ide.md)**  
Initialize a local Git repository for an application and push it to a remote Git repository to manage an application in source control.
-   **[Using source control in the ServiceNow IDE](using-source-control-servicenow-ide.md)**  
Use Git commands and other source control features in the ServiceNow IDE to manage changes to an application across a development team.

**Parent Topic:**[ServiceNow IDE](servicenow-ide-landing.md)

