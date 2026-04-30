---
title: Legacy - Link an application or application-customization to source control
description: Linking an application or application-customization to source control allows application developers to manage changes from a Git repository.
locale: en-US
release: xanadu
product: ServiceNow Studio
classification: servicenow-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Legacy - Source Control integration, Legacy - ServiceNow Studio, Building pro-code applications, Developing your application, Building applications]
---

# Legacy - Link an application or application-customization to source control

Linking an application or application-customization to source control allows application developers to manage changes from a Git repository.

## Before you begin

**Important:** Starting with the Xanadu release, the legacy version of ServiceNow Studio is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Try building and editing apps in the current version of ServiceNow Studio instead. For more information, see [Building applications with ServiceNow Studio](../../servicenow-studio/concept/servicenow-studio-landing.md).

-   Role required: admin
-   Learn more about [Managing application-customizations](manage-customizations-store-apps.md).
-   Create a dedicated Git repository for the application. For increased security, enable multi-factor authentication for the Git repository.
-   Generate an access token that the source control integration can use instead of a password and multi-factor authentication passkey. Search for personal access token on [GitHub](https://help.github.com) or [GitLab](https://docs.gitlab.com).
-   Restrict permissions on the access token to allow read and write access to the Git repository.
-   Verify that the non-production instance has network access to the Git repository.
-   Ensure that users add the email address to their respective Users Table \(ServiceNow sys\_user\) records that they use in their commits to the Git repository.
-   Learn more: [Legacy - Migrate completed update set history to Source Control](../concept/migrate-update-set-history.md)

## About this task

The source control integration does not support linking to an application or customization on a production instance. Instead, install applications on a production instance from the application repository, an update set, or the ServiceNow Store.

## Procedure

1.  Open the application you want to link to source control in Studio.

2.  Navigate to **Source Control** &gt; **Link to Source Control**.

    Studio displays the Link to Source Control dialog box.![Link to Source Control dialog box](../image/mid-server-ssh-box.png)

3.  Enter the connection details for the Git repository.

<table id="table_s3x_2fl_p5"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Network protocol

</td><td>

HTTPS or SSH credential type that enables secure channel data exchange.

</td></tr><tr><td>

URL

</td><td>

The URL to the Git repository where you want to save application files. For SSH protocol, use command to generate private key `ssh-keygen -t rsa -m PEM -b 4096 -C “email@address”`.**Note:** If the Git repo URL for SSH provided by your Git server does not work, check with your Git server owner or provider for the correct URL. There may be additional specifications such as scheme protocol prefixes, port numbers, and so on, required for your Git repo URL to function.

</td></tr><tr><td>

Credential

</td><td>

The credential to be used with the selected protocol. See [Getting started with Credentials](https://www.servicenow.com/docs/access?context=credentials-getting-started&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US) to learn more about creating credentials.**Note:** If you select the SSH network protocol, enter a valid credential of the SSH private key type. If you select the https protocol, enter a valid credential of the Basic Auth credentials type.

</td></tr><tr><td>

Branch

</td><td>

The repository branch to work on within the application.

</td></tr><tr><td>

MID Server Name

</td><td>

The name of the existing MID Server to link through.**Note:** Use a separate MID Server to prevent conflicts with Discovery activities.

Be sure that the MID server user can create files to the sys\_attachment table and that the table can accept files of the “bundle” type.

 Linking or [importing](t_ImportAppFromSourceControl.md) an application through a MID Server enables access to repositories behind a firewall. See the [Using MID Server with source control](../concept/tips-source-control-midserver.md) and [MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) topics to learn more

</td></tr><tr><td>

Default email

</td><td>

The committer email address is defined by the sys\_user record if available. But if a committer's sys\_user record email field is empty, the system generates an alternate email \(username@instancename.service-now.com\). You can also enter a default email address and change it later. To use that default email address in all cases, select the check box.

</td></tr><tr><td>

Commit Comment

</td><td>

An optional description of the repository or application.

</td></tr></tbody>
</table>    **Note:** All application developers on the instance share a single set of repository credentials.

4.  Click **Submit**.

    The system validates the connection and user credentials and displays a success message.

    All application developers on the instance can use the linked Git repository to manage changes.


-   **[Legacy - Using MID Server with source control](../concept/tips-source-control-midserver.md)**  
The ServiceNow® MID Server enables communication and the movement of data between a ServiceNow instance and external applications, data sources, and services.

**Parent Topic:**[Legacy - Source Control integration](../concept/c_SourceControlIntegration.md)

**Related topics**  


[Getting started with credentials](https://www.servicenow.com/docs/access?context=credentials-getting-started&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)

