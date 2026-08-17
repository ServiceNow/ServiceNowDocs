---
title: Fluent source control in ServiceNow Studio
description: Integrate with remote Git repositories to manage Fluent applications in source control ServiceNow Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/fluent-source-control-sn-studio.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: concept
last_updated: "2026-07-23"
reading_time_minutes: 1
breadcrumb: [Source control integration, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Fluent source control in ServiceNow Studio

Integrate with remote Git repositories to manage Fluent applications in source control ServiceNow Studio.

You can connect to a Git provider using basic or OAuth 2.0 authentication. Then, initialize a repository for an application in the ServiceNow Studio and push it to a remote repository or clone a remote repository that contains an application. After setting up authentication and connecting to a repository, you can use common Git commands to manage applications in source control.

## Instance requirements

If an instance includes modified configurations for saving attachments, the following requirements must be met to perform Git operations:

-   If the `glide.attachment.extensions` system property is configured, it must contain `txt,gitdata`.
-   If the `glide.security.attachment_type.use_blacklist` system property is set to true:
    -   The `glide.attachment.blacklisted.extensions` system property must not contain `txt,gitdata` and
    -   The `glide.attachment.blacklisted.types` system property must not contain `text/plain,application/octet-stream`.

If you want to use custom extensions for attachments, set the `sn_glider.git.attachment.extension.text` and `sn_glider.git.attachment.extension.binary` properties to custom values. For more information, see [ServiceNow Studio properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/servicenow-studio-properties.md).

-   **[Connect to a Git provider using basic authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/fluent-sc-connect-to-git-provider-basic-auth.md)**  
Connect to a Git domain or repository using basic authentication credentials to manage applications in Fluent source control from ServiceNow Studio.
-   **[Connect to a Git provider using OAuth 2.0](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/fluent-sc-connect-to-git-provider-oauth-2-0.md)**  
Set up an OAuth 2.0 application registry and credentials to connect to your Git provider from ServiceNow Studio.
-   **[Configure a MID Server to use source control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/fluent-sc-configure-mid-server-to-use-sc.md)**  
Configure a MID Server to use source control with ServiceNow Studio if your Git provider is behind a firewall.
-   **[Clone a Git repository from ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/fluent-sc-clone-git-repository.md)**  
Clone a remote Git repository to collaborate on applications in Fluent source control in ServiceNow Studio.
-   **[Initialize a Git repository](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/fluent-sc-initialize-git-repo.md)**  
Initialize a local Git repository for an application in ServiceNow Studio and push it to a remote Git repository to manage an application in source control.
-   **[Using Fluent source control in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/fluent-sc-using-fluent-source-control.md)**  
Use Git commands and other source control features in ServiceNow Studio to manage changes to an application across a development team.

**Parent Topic:**[Source control integration in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/source-control-integration.md)

