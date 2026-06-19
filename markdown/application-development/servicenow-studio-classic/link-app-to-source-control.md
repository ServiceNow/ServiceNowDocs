---
title: Link an app to source control in ServiceNow Studio
description: Link an application or application customization to a Git repository in ServiceNow Studio so application developers can manage changes directly from the platform.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/link-app-to-source-control.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2026-05-07"
reading_time_minutes: 3
breadcrumb: [Source control integration, Configure, ServiceNow Studio, Developing your application, Building applications]
---

# Link an app to source control in ServiceNow Studio

Link an application or application customization to a Git repository in ServiceNow Studio so application developers can manage changes directly from the platform.

## Before you begin

-   Review [Manage customizations to applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/application-repository-self-hosted/manage-customizations-store-apps.md) before linking a customization.
-   Create a dedicated Git repository for the application. For increased security, enable multi-factor authentication for the Git repository.
-   Generate an access token for the source control integration to use instead of a password and multi-factor authentication passkey when creating a Credential record. Search for personal access token on [GitHub](https://help.github.com) or [GitLab](https://docs.gitlab.com).
-   Restrict permissions on the access token to allow read and write access to the Git repository.
-   Verify that the non-production instance has network access to the Git repository.
-   Ensure that each user adds the email address they use in their Git commits to their Users table \[sys\_user\] record.
-   Role required: admin

## About this task

Source control integration does not support linking to an application or customization on a production instance. To install applications on a production instance, use the application repository, an update set, or ServiceNow Studio.

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  In the file navigator, select the application you want to open.

3.  Select **App details** to open the app in the canvas.

4.  Select **Source control** &gt; **Link to source control**.

    \[Omitted image "source-control-link-to-sc-purple.png"\] Alt text: Link to source control dialog box

5.  Enter the connection details for the Git repository.

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

The URL of the Git repository where you want to save application files. For SSH protocol, use the following command to generate a private key: `ssh-keygen -t rsa -m PEM -b 4096 -C "email@address"`.**Note:** If the SSH URL provided by your Git server does not work, contact your Git server owner or provider for the correct URL. Additional specifications such as scheme protocol prefixes and port numbers may be required.

</td></tr><tr><td>

Branch

</td><td>

The repository branch to use for commits. The default branch is set to "main" if it is not already set in the remote repository. If there is no default branch in the remote Git repository, the instance creates a new default branch named "main". Configure this using the `glide.source_control.git_default_branch` system property.

</td></tr><tr><td>

MID Server Name

</td><td>

The name of the existing MID Server to link through. Use a separate MID Server to prevent conflicts with Discovery activities.Verify that the MID Server user can create files in the \[sys\_attachment\] table and that the table accepts files of the "bundle" type.

Connecting through a MID Server enables access to repositories behind a firewall. For more information, see .

</td></tr><tr><td>

Default email

</td><td>

The committer email address is taken from the sys\_user record when available. If a committer's sys\_user record email field is empty, the ServiceNow AI Platform generates an alternate email address \(username@instancename.service-now.com\). Enter a default email address to use when no sys\_user email is available.To use the default email address in all cases, select the check box.

</td></tr><tr><td>

Credential

</td><td>

The credential to use with the selected protocol. For more information about creating credentials, see .**Note:** For SSH protocol, enter a valid credential of the SSH private key type. For HTTPS protocol, enter a valid credential of the Basic Auth credentials type.

</td></tr><tr><td>

Commit Comment

</td><td>

An optional description of the repository or application.

</td></tr></tbody>
</table>    **Note:** All application developers on the instance share a single set of repository credentials.

6.  Select **Link to source control**.

    The ServiceNow AI Platform validates the connection and user credentials and displays a success message. All application developers on the instance can now use the linked Git repository to manage changes.


**Parent Topic:**[Source control integration in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/source-control-integration.md)

**Related topics**  


[bundle-platcap.mid-server-landing]

[bundle-psec.credentials-getting-started]

