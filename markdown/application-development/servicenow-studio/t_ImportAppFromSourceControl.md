---
title: Legacy - Import application or application-customization from source control
description: Import an application or application-customization from a source control repository to continue developing it on this instance.
locale: en-US
release: xanadu
product: ServiceNow Studio
classification: servicenow-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Legacy - Source Control integration, Legacy - ServiceNow Studio, Building pro-code applications, Developing your application, Building applications]
---

# Legacy - Import application or application-customization from source control

Import an application or application-customization from a source control repository to continue developing it on this instance.

## Before you begin

**Important:** Starting with the Xanadu release, the legacy version of ServiceNow Studio is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Try building and editing apps in the current version of ServiceNow Studio instead. For more information, see [Building applications with ServiceNow Studio](../../servicenow-studio/concept/servicenow-studio-landing.md).

-   Role required: admin or source\_control

    -   Restrict permissions on the access token to allow read and write access to the Git repository.
    -   The repository user credentials must grant read and write access.
    For more information, see [Link an application or application-customization to source control](t_LinkAnApplicationToSourceControl.md).

-   Verify that the non-production instance has network access to the Git repository.
-   Verify that the repository contains a valid application.
-   Ensure that users add the email address to their respective Users Table \(ServiceNow sys\_user\) record that they use in their commits to the Git repository.
-   Learn more about application-customizations [Managing application-customizations](manage-customizations-store-apps.md).

## About this task

The source control integration does not support importing an application on a production instance. Instead install applications on a production instance from the application repository, an update set, or the ServiceNow Store.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **Studio**.

    The system displays the Welcome to Studio page.

2.  Click **Open Studio** &gt; **Go**.

    The system opens Studio and the Switch Applications window.

3.  Click **Import from Source Control**.

    Studio displays the Import from Source Control fields.

    ![Switch Applications window showing Source Control fields](../image/ImportFromSourceControl.png)

4.  Enter the following field values.

<table id="table_skj_zxl_s5"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Network protocol

</td><td>

Https or ssh credential type that enables secure channel data exchange.

</td></tr><tr><td>

URL

</td><td>

The URL to the Git repository where the application files reside. **Note:** If the Git repo URL for SSH provided by your Git server does not work, check with your Git server owner or provider for the correct URL. There may be additional specifications such as scheme protocol prefixes, port numbers, and so on, required for your Git repo URL to function.

</td></tr><tr><td>

Credential

</td><td>

Select the credential for your Git repository. \(See [Getting started with Credentials](https://www.servicenow.com/docs/access?context=credentials-getting-started&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).\)**Note:** If you select the ssh network protocol, enter a valid credential of the SSH Private Key type. If you select the https protocol, enter a valid credential of the Basic Auth Credentials type.

</td></tr><tr><td>

Branch

</td><td>

The repository branch to work on within the application. **Note:**

The default branch is named after your instance. If you do not choose a name, the branch defaults to **master**.

</td></tr><tr><td>

MID Server Name

</td><td>

Select an existing MID Server to link to a Git repository stored behind your corporate firewall.**Note:** Use a separate MID Server to prevent conflicts with Discovery activities.

</td></tr><tr><td>

Default email

</td><td>

The committer email address is defined by the sys\_user record if available. But if a committer's sys\_user record email field is empty, the system generates an alternate email \(username@instancename.service-now.com\). You can also enter a default email address and change it later. To use that default email address in all cases, select the check box.

</td></tr></tbody>
</table>    **Note:** All application developers on the instance share the credential used to link a Git repository to an application.

5.  Click **Import**.

    The system compares the checksum in the `checksum.txt` file to current checksum. When the checksum values match, the integration skips validation and imports the application. When the checksum values do not match, the integration first validates and sanitizes the application files before importing them.

6.  Click **Select Application**.

    Studio displays the application as a new choice in the Switch Applications window.


## What to do next

-   Review the upgrade logs for any sanitization applied to application files during the import.
-   Select the imported application to edit it.

**Parent Topic:**[Legacy - Source Control integration](../concept/c_SourceControlIntegration.md)

**Related topics**  


[MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)

[Getting started with credentials](https://www.servicenow.com/docs/access?context=credentials-getting-started&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)

