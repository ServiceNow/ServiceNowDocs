---
title: Edit a Git repository configuration
description: You can edit a Git repository's integration with App Engine Studio \(AES\) to change the network protocol selection, credentials or other field entries.
locale: en-US
release: australia
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrate with Git source control, Configure AES, Configure, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Edit a Git repository configuration

You can edit a Git repository's integration with App Engine Studio \(AES\) to change the network protocol selection, credentials or other field entries.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **App Engine Studio**.

2.  From the My Apps page, open your application.

3.  Select **Source control** &gt; **Edit repository configuration**.

    ![Edit Repository Configuration menu item](../image/source-control-edit-repo-purple.png)

4.  On the form, fill in the fields.

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

Connect with a MID server

</td><td>

Whether or not to use a MID server connection, which enables access to repositories behind a firewall.**Note:** If you have no MID server name, you can select a new one from the drop-down list. If you choose a new MID server, in the **Source control** menu before making any further source control operations to avoid errors.

</td></tr><tr><td>

Default email

</td><td>

Email address for the committer, which is defined by the sys\_user record, if available.If a committer's sys\_user record email field is empty, the system generates an alternate email \(username@instancename.service-now.com\). You can also enter a default email address and change it later by selecting the **Always use this email for commits from all developers** check box.

</td></tr><tr><td>

Credential

</td><td>

Saved credentials to use for the source control connection. All application developers on the instance share a single set of credentials per repository. For information on working with credentials, see [Get started with credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/credentials-getting-started.md).

</td></tr></tbody>
</table>    ![View and edit application repository configurations](../image/aes-app-properties-repo-purple.png)

5.  Select **Save**.


**Parent Topic:**[AES integration with a Git source control repository](../concept/aes-source-control-integration.md)

