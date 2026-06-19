---
title: Edit a Git repository configuration in ServiceNow Studio
description: Edit a Git repository configuration in ServiceNow Studio to update the network protocol, credentials, or other connection details.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/sns-sc-edit-git-repo-configuration.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2026-05-07"
reading_time_minutes: 1
breadcrumb: [Source control integration, Configure, ServiceNow Studio, Developing your application, Building applications]
---

# Edit a Git repository configuration in ServiceNow Studio

Edit a Git repository configuration in ServiceNow Studio to update the network protocol, credentials, or other connection details.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  In the file navigator, select the application you want to open.

3.  Select **App details** to open the app in the canvas.

4.  Select **Source control** &gt; **Edit repository configuration**.

    \[Omitted image "source-control-edit-repo-purple.png"\] Alt text: Edit Repository Configuration menu item

5.  Update the fields you want to change.

<table id="table_iyl_tsc_yxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Network protocol

</td><td>

Protocol for source control: **HTTPS** or **SSH**.

</td></tr><tr><td>

URL

</td><td>

The URL of the Git repository.

</td></tr><tr><td>

Branch

</td><td>

The current branch for the repository.

</td></tr><tr><td>

Connect with a MID Server

</td><td>

Whether or not to use a MID Server connection, which enables access to repositories behind a firewall.**Note:** If you have no MID Server name, select a new one from the drop-down list. If you select a new MID Server, apply the change in the **Source control** menu before performing any further source control operations to avoid errors.

</td></tr><tr><td>

Default email

</td><td>

The committer email address, taken from the sys\_user record when available. If a committer's sys\_user record email field is empty, the system generates an alternate email address \(username@instancename.service-now.com\). Enter a default email address to use when no sys\_user email is available. To use the default email address in all cases, select **Always use this email for commits from all developers**.

</td></tr><tr><td>

Credential

</td><td>

The saved credentials to use for the source control connection. All application developers on the instance share a single set of credentials per repository. For more information about working with credentials, see .

</td></tr></tbody>
</table>    \[Omitted image "aes-app-properties-repo-purple.png"\] Alt text: View and edit application repository configurations.

6.  Select **Save**.

    The repository configuration is updated and the new settings apply to all future source control operations for this application.


**Parent Topic:**[Source control integration in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/source-control-integration.md)

