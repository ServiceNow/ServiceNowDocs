---
title: Link an app to source control in ServiceNow Studio
description: Linking an application or application-customization to source control allows application developers to manage changes in ServiceNow Studio from a Git repository.
locale: en-US
release: australia
product: ServiceNow Studio
classification: servicenow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Source control integration, Configure, ServiceNow Studio, Developing your application, Building applications]
---

# Link an app to source control in ServiceNow Studio

Linking an application or application-customization to source control allows application developers to manage changes in ServiceNow Studio from a Git repository.

## Before you begin

-   Learn more about [Manage customizations to applications](../../applications/task/manage-customizations-store-apps.md).
-   Create a dedicated Git repository for the application. For increased security, enable multi-factor authentication for the Git repository.
-   Generate an access token that the source control integration can use instead of a password and multi-factor authentication passkey while creating a Credential record. Search for personal access token on [GitHub](https://help.github.com) or [GitLab](https://docs.gitlab.com).
-   Restrict permissions on the access token to allow read and write access to the Git repository.
-   Verify that the non-production instance has network access to the Git repository.
-   Ensure that users add the email address to their respective Users table \[sys\_user\] records that they use in their commits to the Git repository.
-   Role required: admin

## About this task

The source control integration does not support linking to an application or customization on a production instance. Instead, install applications on a production instance from the application repository, an update set, or ServiceNow Studio.

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  In the file navigator, select the application you want to open.

3.  Select **App details** to open the app in the canvas.

4.  Select **Source control** &gt; **Link to source control**.

    ![Link to source control dialog box](../../app-engine-studio/image/source-control-link-to-sc-purple.png)

5.  Enter the connection details for the Git repository.

<table id="table_s3x_2fl_p5"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Network protocol

</td><td>

Https or SSH credential type that enables secure channel data exchange.

</td></tr><tr><td>

URL

</td><td>

The URL to the Git repository where you want to save application files. For SSH protocol, use command to generate private key `ssh-keygen -t rsa -m PEM -b 4096 -C “email@address”`.**Note:** If the Git repository URL for SSH provided by your Git server does not work, check with your Git server owner or provider for the correct URL. There may be additional specifications such as scheme protocol prefixes, port numbers, and so on, required for your Git repository URL to function.

</td></tr><tr><td>

Branch

</td><td>

The repository branch to work on within the application.**Note:** This branch is used for commits. The default branch is set to "main" if it is not already set in the remote repository. If there is no default branch on the remote git repository, the instance creates a new default branch with the name "main". This is configured using the `glide.source_control.git_default_branch` system property.

</td></tr><tr><td>

MID Server Name

</td><td>

The name of the existing MID Server to link through.**Note:** Use a separate MID Server to prevent conflicts with Discovery activities.

Be sure that the MID Server user can create files to the \[sys\_attachment\] table, and that the table can accept files of the “bundle” type.

Linking or an application through a MID Server enables access to repositories behind a firewall. See [MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) for more information.

</td></tr><tr><td>

Default email

</td><td>

The committer email address is defined by the sys\_user record if available. But if a committer's sys\_user record email field is empty, the ServiceNow AI Platform generates an alternate email \(username@instancename.service-now.com\). You can also enter a default email address and change it later. To use that default email address in all cases, select the check box.

</td></tr><tr><td>

Credential

</td><td>

The credential to be used with the selected protocol. See [Get started with credentials](https://www.servicenow.com/docs/access?context=credentials-getting-started&version=australia&pubname=australia-platform-security&ft:locale=en-US) to learn more about creating credentials.**Note:** If you select the SSH network protocol, enter a valid credential of the SSH private key type. If you select the https protocol, enter a valid credential of the Basic Auth credentials type.

</td></tr><tr><td>

Commit Comment

</td><td>

An optional description of the repository or application.

</td></tr></tbody>
</table>    **Note:** All application developers on the instance share a single set of repository credentials.

6.  Select **Link to source control**.

    The ServiceNow AI Platform validates the connection and user credentials and displays a success message.

    All application developers on the instance can use the linked Git repository to manage changes.


**Parent Topic:**[Source control integration in ServiceNow Studio](../concept/source-control-integration.md)

**Related topics**  


[MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

[Getting started with credentials](https://www.servicenow.com/docs/access?context=credentials-getting-started&version=australia&pubname=australia-platform-security&ft:locale=en-US)

