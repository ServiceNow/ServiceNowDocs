---
title: Install the Agent Client Collector on a Windows machine manually
description: Install the Agent Client Collector on a Windows machine manually when you want to test the agent on a single system.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-08-17"
reading_time_minutes: 5
breadcrumb: [Agent Client Collector installation on a Windows machine, Configuring Agent Client Collector Framework, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Install the Agent Client Collector on a Windows machine manually

Install the Agent Client Collector on a Windows machine manually when you want to test the agent on a single system.

## Before you begin

1.  Ensure that you’ve configured the Agent Client Collector web server. For details, see [Configure the websocket server on the MID Server](acc-configure-web-server.md).
2.  Verify your server's OS and version.
3.  When using Microsoft Internet Explorer, do the following to prepare the Agent Client Collector installation file:
    1.  Navigate to **Server Manager** &gt; **Local Server**.
    2.  Turn off **IE Enhanced Security Configuration**.
    3.  Download the installation file.
    4.  Change the extension of the installation file from `.man` to `.msi`

For troubleshooting, see [KB2200094](https://support.servicenow.com/kb?id=kb_article_view;sysparm_article=KB2200094) article in the HI Knowledge Base.

Role required: agent\_client\_collector\_admin

## Procedure

1.  Navigate to **Agent Client Collector** &gt; **Agent Downloads**.

2.  To perform installation using the wizard:

    1.  Download the .msi file that is accessible from the link on the UI.

        The Installation Wizard opens.

    2.  Select **Next** until you reach the **MID Web Server Connection Settings** page.

        ![MID Connection Settings page](../image/ACC-MID-Connection-Settings-Updated.png)

    3.  Enter the relevant parameters in the dialog box fields:

        |Field name|Description|
        |----------|-----------|
        |MID Web Server Name/IP|IP address of the MID Web server.|
        |MID Web Server Port|Port number of the MID Web server. Use a number between 1024-49151.|
        |MID Web Server API Key|API key to access the MID Web server.|

    4.  Select **Next**.

        The **Create Local User Account** page appears.

        ![Create Local User Account page](../image/ACC-Create-Local-User-Account.png)

    5.  Select the relevant option in the dialog box.

<table id="table_hdl_d1z_hkb"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Use default user \(servicenow\)

</td><td>

Default user with which to run the Agent Client Collector on a Windows machine.Selecting this option creates a local user called **servicenow** as part of the installation.

The servicenow user password is randomly generated and is not stored in the system. A security event is created on the host machine which, if repeated, requires opening a support case. For details, see [KB1649116](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1649116) article in the HI Knowledge Base.

</td></tr><tr><td>

Select existing user

</td><td>

When selecting this option, configure the following subfields:-   **User Name**: User name to log in to the Windows environment.
-   **Password**: Password of the selected user.
The user can be one of the following:

-   Local user \(created by the virtual machine owner; provides added resiliency\).
-   Domain user \(created by IT personnel\).
-   Group Managed Service Account \(gMSA\): Enter the name of the group managed service account in the **User Name** field and leave the **Password** field empty.
-   Local Service Account: Enter **LOCALSERVICE** in the **User Name** field and leave the **Password** field empty.
-   Local System Account: Enter **SYSTEM** in the **User Name** field and leave the **Password** field empty.

Due to Windows UAC restrictions, running the agent as a local SYSTEM account is necessary to perform an upgrade via **msiexec**.

</td></tr></tbody>
</table>        **Note:** Using a Local System account creates the local group **ServiceNow Users**, and adds the created user to the group. The ServiceNow Users group has access to Agent Client Collector directories and has the following privileges:

        -   **Performance Monitor**: Comes with the base system; enables viewing all performance counters in the system.
        -   **Log on as a service**: Enables starting network services and services that run continuously, even when no one is logged onto the console.
        -   **Debug programs**: Enables debugging processes and reading process details for users outside the ServiceNow user group.
    6.  Select **Create User**.

        The system creates a Windows user with the specified credentials, and the Agent Client Collector Configuration page appears.

    7.  To enable the **Allow-List** containing the checks enabled to run after setup, select the **Enable executing command allow list** check box on the resulting page.

        ![Allow list check box](../image/ACC-Allow-List-Windows.png)

    8.  Select **Next** to open the installation page.

        When installation completes, click **Next** to complete and exit the wizard.

        After a successful installation, the service starts automatically and generates the following:

        -   User: Default = servicenow \(an existing user can also be configured to manage the service\). The servicenow user belongs to the local user group **ServiceNow Users**.
        -   Service: AgentClientCollector
        -   File location:
            -   Default for installation = `C:\Program Files\ServiceNow\agent-client-collector`
            -   Default for service files = `C:\ProgramData\ServiceNow\agent-client-collector`, which holds the `cache`, `config`, and `log` folders.
3.  To run Silent installation to disable installation reports, run the command line appearing in the **Silent installation** section of the procedure, as follows:

    `msiexec /i <msi_file_path> /quiet /qn /norestart ACC_API_KEY=<key_value> ACC_MID=wss://<mid_ip>:<websocket_port>/ws/events ACC_ALLOW_LIST=False`

    To enable the allow list of specified checks when running Silent installation, set the **ACC\_ALLOW\_LIST** parameter to **True**.

4.  To configure multiple MID Servers with Silent installation, run the command line appearing in the **Silent installation** section of the procedure with comma-separated values, as follows:

    `msiexec /i <msi_file_path> /quiet /qn /norestart ACC_API_KEY=<key_value> ACC_MID="wss://<mid1_ip>:<websocket1_port>/ws/events,wss://<mid2_ip>:<websocket2_port>/ws/events"`

    Insert the following parameter values in the command:

<table id="table_al4_f4s_wlb"><thead><tr><th>

Parameter

</th><th>

Value

</th></tr></thead><tbody><tr><td>

ACC\_API\_KEY

</td><td>

The API key used to access the MID Server websocket.

</td></tr><tr><td>

ACC\_MID

</td><td>

The URL of the MID Server websocket.

</td></tr><tr><td>

DENY\_LOCAL\_LOGON

</td><td>

When set to **True**, prevents any user other than the default servicenow user from logging onto the service.Default value: False

</td></tr><tr><td>

PASSWORD\_NEVER\_EXPIRES

</td><td>

When set to **True**, the password for the default servicenow user never expires.Default value: False

</td></tr><tr><td>

START\_SERVICE

</td><td>

When set to **True**, the Agent Client Collector service automatically starts after installation.Default value: True

</td></tr><tr><td>

LOCALUSERNAME

</td><td>

Account running the Agent Client Collector as a Windows service. Possible values:-   SYSTEM
-   LOCALSERVICE
-   DOMAIN\\gMSA$
-   string \(local username\)
Default = `servicenow`

When using the SYSTEM, LOCALSERVICE, or DOMAIN\\gMSA$ accounts, you do not have to configure a password.

</td></tr><tr><td>

LOCALPASSWORD

</td><td>

Password for the user specified in the LOCALUSERNAME parameter.

</td></tr></tbody>
</table>    The configured MID Server values are automatically added to the `acc.yml` file. The agent connects to the first available MID Server in the list.

    To configure a secondary MID server, enter the following syntax in the `backend-url` section of the `acc.yml` file, per the `.yml` standard: `- "wss://<MID IP>:<Web socket port>/ws/events"` \(with the quotation marks\).


-   **[Upgrade the Agent Client Collector manually on a Windows system](acc-install-upgrade-windows.md)**  
Perform a manual upgrade of your existing Agent Client Collector version on a system running a Windows OS.
-   **[Uninstall the Agent Client Collector manually from a Windows machine](acc-uninstall.md)**  
Uninstall the Agent Client Collector from a Windows machine manually instead of using the single-line procedure. Use the manual procedure if the command script is unavailable due to the specific agent not being connected to the instance.

**Parent Topic:**[Agent Client Collector installation on a Windows machine](../concept/acc-windows-install-concept.md)

