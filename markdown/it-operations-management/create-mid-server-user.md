---
title: Create a MID Server user
description: Create a user account with the mid\_server role so MID Servers can authenticate and communicate with the ServiceNow instance.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-28"
reading_time_minutes: 1
keywords: [ITOM, user roles, Now Assist]
breadcrumb: [ITOM Configuration Console for Discovery, Now Assist for Setup \(ITOM Visibility\), Now Assist for Setup \(ITOM\), IT Operations Management]
---

# Create a MID Server user

Create a user account with the mid\_server role so MID Servers can authenticate and communicate with the ServiceNow instance.

## Before you begin

Verify the following:

-   You have installed the ITOM Visibility plugin. For more information, see [Install ITOM Visibility using Now Assist for Setup](install-nowassist-setup-itom-visibility.md).
-   You have installed the Now Assist for IT Operations Management plugin. For more information, see [Install Now Assist for IT Operations Management](install-now-assist-itom.md).
-   You're on the Configure IT Operations Management page of the Configuration Console. For more information, see [Access the ITOM Configuration Console](access-itom-config-console-disco.md).

Role required: admin

## About this task

MID Servers require a MID Server user account to authenticate with the instance. Assigning the mid\_server role allows the MID Server to connect and pass validation checks. ServiceNow monitors MID Server user settings to help prevent validation failures. You can use a dedicated user per MID Server or share a user across multiple MID Servers.

**Note:** Using the same logged‑in user across multiple MID Servers can generate issue records when more than one MID Server is **Up**. Configure a unique logged‑in user per MID Server. See [\(KB1552863\) MID Server Unique Logged In User](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1552863) for more information and remediation steps.

## Procedure

1.  Navigate to **Configuration Summary** &gt; **Discovery** &gt; **Platform foundations**.

2.  Expand **Platform foundations**.

3.  Select **MID server user**.

4.  Select **Create user**.

    The Create MID server user page displays.

5.  Complete the following fields.

<table id="table_izp_lsv_bjc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User ID

</td><td>

Enter a user name for the MID Server user. This name is specified in the **mid.instance.username** parameter of the configuration file that the MID Server installer creates. For details, see [MID Server parameters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-parameters.md).

 **Note:** Avoid using the same MID Server logged in user across multiple MID Servers.

</td></tr><tr><td>

Password

</td><td>

Enter a password for the MID Server user. This password is specified in the **mid.instance.password** parameter of the configuration file that the MID Server installer creates.

</td></tr></tbody>
</table>6.  Select **Create user**.

    You're returned to the MID server user page.

7.  To complete the setup, select **Mark as configured**.


**Related topics**  


[Create the MID Server user and grant the role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/t_SetupMIDServerRole.md)

