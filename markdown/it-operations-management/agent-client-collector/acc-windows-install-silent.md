---
title: Install the Agent Client Collector on a Windows machine using silent installation
description: Install the Agent Client Collector on a Windows machine using silent installation when you want to deploy the agent at scale.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Agent Client Collector installation on a Windows machine, Configuring Agent Client Collector Framework, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Install the Agent Client Collector on a Windows machine using silent installation

Install the Agent Client Collector on a Windows machine using silent installation when you want to deploy the agent at scale.

## About this task

Silent installation automatically creates a local user called **servicenow** \(unless another existing user is invoked with the **LOCALUSERNAME** parameter, as described in the command parameters table in the following procedure\). The servicenow user password is randomly generated and is not stored in the system. A security event is created on the host machine which, if repeated, requires opening a support case. For details, see [KB1649116](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1649116) article in the Now Support Knowledge Base.

## Before you begin

Role required: agent\_client\_collector\_admin

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Deployment** &gt; **Agent Downloads**.

2.  From the Windows Download section, download the MSI installer by selecting the Download icon \(![Select the download icon to download the application.](../image/icon-download-blue.png)\).

    ![Page where you can download Agent Client Collector.](../image/console-download-acc-win-installer2.png)

3.  To run Silent installation to disable installation reports, run the command line appearing in the **Silent installation** section of the procedure, as follows:

    `msiexec /i <msi_file_path> /quiet /qn /norestart ACC_API_KEY=<key_value> ACC_MID=wss://<mid_ip>:<websocket_port>/ws/events ACC_ALLOW_LIST=False`

    To enable the allow list of specified checks when running silent installation, set the **ACC\_ALLOW\_LIST** parameter to **True**.

4.  To configure multiple MID Servers with Silent installation, run the command line appearing in the **Silent installation** section of the procedure with comma separated values, as follows:

    `msiexec /i <msi_file_path> /quiet /qn /norestart ACC_API_KEY=<key_value> ACC_MID="wss://<mid1_ip>:<websocket1_port>/ws/events,wss://<mid2_ip>:<websocket2_port>/ws/events"`

    Insert the following parameter values in the command:

<table id="table_al4_f4s_wlb"><thead><tr><th>

Parameter

</th><th>

Type

</th><th>

Value

</th></tr></thead><tbody><tr><td>

ACC\_API\_KEY

</td><td>

String

</td><td>

The API key used to access the MID Server websocket.

</td></tr><tr><td>

ACC\_MID

</td><td>

String

</td><td>

The URL of the MID Server websocket.

</td></tr><tr><td>

ACC\_ALLOW\_LIST

</td><td>

Boolean

</td><td>

Indicates whether the allow-list is enabled \(True\) or disabled \(False\).Default = True

</td></tr><tr><td>

START\_SERVICE

</td><td>

Boolean

</td><td>

Indicates whether the agent starts automatically upon installation \(true\) or must be started manually \(false\).Default = True

</td></tr><tr><td>

LOCALUSERNAME

</td><td>

String

</td><td>

Account running the Agent Client Collector as a Windows service. Possible values:-   SYSTEM
-   LOCALSERVICE
-   DOMAIN\\gMSA$
-   string \(local username\)
Default = `servicenow`

When using the SYSTEM, LOCALSERVICE, or DOMAIN\\gMSA$ accounts:

-   You do not have to configure a password.
-   You must run the relevant .msi command, as described in [Account commands for LocalService, LocalSystem, and gMSA during Windows installation](../reference/gmsa-and-local-account-commands.md).


</td></tr><tr><td>

LOCALUSERPASSWORD

</td><td>

String

</td><td>

Password used to access the agent.Default = &lt;randomly generated password&gt;

</td></tr><tr><td>

ISDOMAIN

</td><td>

Boolean

</td><td>

Assigns a domain user account to the Windows service. Possible values:-   0 - DOMAIN is ignored
-   1 - DOMAIN is used


</td></tr><tr><td>

DOMAIN

</td><td>

String

</td><td>

Indicates the user domain. Applies only to domain user accounts \(not gMSA\)

</td></tr><tr><td>

PASSWORD\_NEVER\_EXPIRES

</td><td>

Boolean

</td><td>

Indicates whether the user password expires \(false\) or never expires \(true\).Default = false

</td></tr></tbody>
</table>    The configured MID Server values are automatically added to the `acc.yml` file. The agent connects to the first available MID Server in the list.

    To configure a secondary MID server, enter the following syntax in the `backend-url` section of the `acc.yml` file, per the `.yml` standard: `- "wss://<MID IP>:<Web socket port>/ws/events"` \(with the quotation marks\).

    For the `<MID IP>` value, you can assign either the MID FQDN or CNAME. To enable high availability, use either the Auto MID Selection algorithm, or manage a virtual IP with a load balancer. For more information, see the [ITOM Agent Client Collector documentation material \[KB1122613\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1122613) article in the HI Knowledge Base.


-   **[Uninstall Agent Client Collector from a Windows system using a single-line command](acc-uninstall-windows-single-line.md)**  
Uninstall the Agent Client Collector from a Windows machine by running an efficient single-line command. If the script is not connected to the instance, you might have to uninstall Agent Client Collector manually.

**Parent Topic:**[Agent Client Collector installation on a Windows machine](../concept/acc-windows-install-concept.md)

