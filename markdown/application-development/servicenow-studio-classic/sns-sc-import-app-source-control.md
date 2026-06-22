---
title: Import an app from source control in ServiceNow Studio
description: Import an application from a Git repository into ServiceNow Studio to create a local copy of the app on your non-production instance. The repository must contain a valid ServiceNow application, and your credentials must have read access.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/sns-sc-import-app-source-control.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Source control in ServiceNow Studio, Applications in ServiceNow Studio, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Import an app from source control in ServiceNow Studio

Import an application from a Git repository into ServiceNow Studio to create a local copy of the app on your non-production instance. The repository must contain a valid ServiceNow application, and your credentials must have read access.

## Before you begin

-   Verify that the non-production instance has network access to the Git repository.
-   Verify that the repository contains a valid application.
-   Ensure that each user adds the email address they use in their Git commits to their Users table \[sys\_user\] record.
-   Review [Manage customizations to applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/application-repository-self-hosted/manage-customizations-store-apps.md) before importing a customization.
-   Role required: admin

## About this task

Source control integration does not support importing an application on a production instance. To install applications on a production instance, use the application repository, an update set, or ServiceNow Studio.

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  Select the **Create** dropdown list on the home page, then select **Import app**.

    \[Omitted image "sn-studio-create-import.png"\] Alt text: Select Import app from the Create dropdown list on the home page.

    \[Omitted image "sn-studio-import-app-sc.png"\] Alt text: Import an app from source control.

3.  Enter the connection details for the Git repository.

<table id="table_skj_zxl_s5"><thead><tr><th>

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

The URL of the Git repository where the application files reside.**Note:** If the SSH URL provided by your Git server does not work, contact your Git server owner or provider for the correct URL. Additional specifications such as scheme protocol prefixes and port numbers may be required.

</td></tr><tr><td>

Branch

</td><td>

The repository branch to use for the import.**Note:** The default branch is named after your instance. If you do not enter a name, the branch defaults to **master**.

</td></tr><tr><td>

Connect with a MID Server

</td><td>

Select whether to use an existing MID Server to connect to a Git repository behind a corporate firewall.**Note:** Use a separate MID Server to prevent conflicts with Discovery activities.

For more information, see [MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-landing.md).

</td></tr><tr><td>

Default email

</td><td>

The committer email address, taken from the sys\_user record when available. If a committer's sys\_user record email field is empty, the system generates an alternate email address \(username@instancename.service-now.com\). Enter a default email address to use when no sys\_user email is available. To use the default email address in all cases, select **Always use this email for commits from all developers**.

</td></tr><tr><td>

Credential

</td><td>

The credential to use for your Git repository. For more information, see [Getting started with Credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/credentials-getting-started.md).**Note:** For SSH protocol, enter a valid credential of the **SSH Private Key** type. For HTTPS protocol, enter a valid credential of the **Basic Auth Credentials** type.

</td></tr></tbody>
</table>    **Note:** All application developers on the instance share the credentials used to link a Git repository to an application.

4.  Select **Import app**.

    The system compares the checksum in the `checksum.txt` file to the current checksum. When the checksum values match, the integration skips validation and imports the application. When the checksum values do not match, the integration validates and sanitizes the application files before importing them.

5.  Select **Select Application**.

    ServiceNow Studio displays the imported application as a new option in the Switch Applications dialog.


## What to do next

-   Review the upgrade logs for any sanitization applied to application files during the import.
-   Select the imported application to open and edit it.

**Parent Topic:**[Source control in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/source-control-in-servicenow-studio.md)

