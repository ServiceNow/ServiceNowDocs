---
title: Edit a Git repository configuration in ServiceNow Studio
description: You can edit a Git repository's integration with ServiceNow Studio to change the network protocol selection, credentials, or other field entries.
locale: en-US
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Source control integration, Configure, ServiceNow Studio, Developing your application, Building applications]
---

# Edit a Git repository configuration in ServiceNow Studio

You can edit a Git repository's integration with ServiceNow Studio to change the network protocol selection, credentials, or other field entries.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  In the file navigator, select the application you want to open.

3.  Select **App details** to open the app in the canvas.

4.  Select **Source control** &gt; **Edit repository configuration**.

    ![Edit Repository Configuration menu item](../../app-engine-studio/image/source-control-edit-repo-purple.png)

5.  On the form, fill in the fields.

<table id="table_iyl_tsc_yxb"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Network protocol

</td><td>

Protocol for source control, either **https** or **ssh**.

</td></tr><tr><td>

URL

</td><td>

URL address of your repository.

</td></tr><tr><td>

Branch

</td><td>

Current branch for the repository.

</td></tr><tr><td>

Connect with a MID Server

</td><td>

Whether or not to use a MID Server connection, which enables access to repositories behind a firewall.**Note:** If you have no MID Server name, you can select a new one from the drop-down list. If you choose a new MID Server, in the **Source control** menu before making any further source control operations to avoid errors.

</td></tr><tr><td>

Default email

</td><td>

Email address for the committer, which is defined by the sys\_user record, if available.If a committer's sys\_user record email field is empty, the system generates an alternate email \(username@instancename.service-now.com\). You can also enter a default email address and change it later by selecting the **Always use this email for commits from all developers** check box.

</td></tr><tr><td>

Credential

</td><td>

Saved credentials to use for the source control connection. All application developers on the instance share a single set of credentials per repository. For information on working with credentials, see [Get started with credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/credentials-getting-started.md).

</td></tr></tbody>
</table>    ![View and edit application repository configurations](../../app-engine-studio/image/aes-app-properties-repo-purple.png)

6.  Select **Save**.


**Parent Topic:**[Source control integration in ServiceNow Studio](../concept/source-control-integration.md)

