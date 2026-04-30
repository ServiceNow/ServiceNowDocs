---
title: Import an app from source control in ServiceNow Studio
description: Importing an application from source control results in a new application being created in your ServiceNow instance based on the remote repository you specify. The account credentials you supply must have read access to the remote repository, and the remote repository you specify must contain a valid ServiceNow application.
locale: en-US
release: zurich
product: ServiceNow Studio
classification: servicenow-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Source control in ServiceNow Studio, Working with applications, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Import an app from source control in ServiceNow Studio

Importing an application from source control results in a new application being created in your ServiceNow instance based on the remote repository you specify. The account credentials you supply must have read access to the remote repository, and the remote repository you specify must contain a valid ServiceNow application.

## Before you begin

-   Verify that the non-production instance has network access to the Git repository.
-   Verify that the repository contains a valid application.
-   Ensure that users add the email address to their respective Users table \[sys\_user\] record that they use in their commits to the Git repository.
-   Learn more about application-customizations [Manage customizations to applications](../../applications/task/manage-customizations-store-apps.md).
-   Role required: admin

## About this task

The source control integration does not support importing an application on a production instance. Instead, install applications on a production instance from the application repository, an update set, or ServiceNow Studio.

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  Select the **Create** dropdown list on the home page, and select **Import app**.

    ![Select the Import app option from the Create dropdown list on the home page.](../image/sn-studio-create-import.png)

    ![Import an app from source control.](../image/sn-studio-import-app-sc.png)

3.  On the form, fill in the fields.

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

Branch

</td><td>

The repository branch to work on within the application. **Note:** The default branch is named after your instance. If you do not choose a name, the branch defaults to **master**.

</td></tr><tr><td>

Connect with a MID Server

</td><td>

Option to opt in and select an existing MID Server to link to a Git repository stored behind your corporate firewall.**Note:** Use a separate MID Server to prevent conflicts with Discovery activities.

See [MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) for more information.

</td></tr><tr><td>

Default email

</td><td>

The committer email address is defined by the sys\_user record if available. But if a committer's sys\_user record email field is empty, the system generates an alternate email \(username@instancename.service-now.com\). You can also enter a default email address and change it later. To use that default email address in all cases, select the **Always use this email for commits from all developers** check box.

</td></tr><tr><td>

Credential

</td><td>

Select the credential for your Git repository. For more information, see [Getting started with Credentials](https://www.servicenow.com/docs/access?context=credentials-getting-started&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).**Note:** If you select the ssh network protocol, enter a valid credential of the **SSH Private Key** type. If you select the https protocol, enter a valid credential of the **Basic Auth Credentials** type.

</td></tr></tbody>
</table>    **Note:** All application developers on the instance share the credential used to link a Git repository to an application.

4.  Select **Import app**.

    The system compares the checksum in the `checksum.txt` file to current checksum. When the checksum values match, the integration skips validation and imports the application. When the checksum values do not match, the integration first validates and sanitizes the application files before importing them.

5.  Select **Select Application**.


## Result

ServiceNow Studio displays the application as a new choice in the Switch Applications modal.

## What to do next

-   Review the upgrade logs for any sanitization applied to application files during the import.
-   Select the imported application to edit it.

**Parent Topic:**[Source control in ServiceNow Studio](../concept/source-control-in-servicenow-studio.md)

