---
title: Tibco BusinessWorks and EMS discovery
description: Discovery can find Tibco ActiveMatrix BusinessWorks and Enterprise Message Service \(EMS\). Service Mapping can discover application services containing Tibco BusinessWorks, Enterprise Message Service \(EMS\), and their components.Map an application service containing Tibco BusinessWorks and Enterprise Message Service \(EMS\) and verify that Service Mapping discovered all Tibco components correctly.
locale: en-US
release: yokohama
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Map a single application service using classic Service Mapping, Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Tibco BusinessWorks and EMS discovery

Discovery can find Tibco ActiveMatrix BusinessWorks and Enterprise Message Service \(EMS\). Service Mapping can discover application services containing Tibco BusinessWorks, Enterprise Message Service \(EMS\), and their components.

## Data collected by Discovery for Tibco ActiveMatrix BusinessWorks

The following data is collected in the ActiveMatrix Business Works `[cmdb_ci_appl_tibco_matrix]` table.

|Table and field|Description|
|---------------|-----------|
|ActiveMatrix Business Works \[cmdb\_ci\_appl\_tibco\_matrix\]|
|Name \[name\]|The attributes of ActiveMatrix BusinessWorks configuration item.|
|Version \[version\]|
|TCP port\(s\) \[tcp\_port\]|
|Class \[sys\_class\_name\]|
|Fully qualified domain name \[fqdn\]|
|IP Address \[ip\_address\]|
|Configuration directory \[config\_directory\]|
|Configuration file \[config\_file\]|
|Installation directory \[install\_directory\]|
|Project \[project\]|

## Data collected by Discovery for Tibco Enterprise Message Service

By default, Discovery uses the **Enterprise Message Service** pattern to discover Tibco Enterprise Message Service.

For a list of privileged commands that you need for Discovery and Service Mapping, see [Service Mapping commands requiring a privileged user](../reference/r_CommandsnCredentials.md). This list includes commands that require elevated rights to discover and map Unix-based hosts in your organization.

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

|Table and field|Field Name|
|---------------|----------|
|Tibco Enterprise Message Services \[cmdb\_ci\_appl\_tibco\_message\]|
|Name \[name\]|Attributes of the Tibco Enterprise Message Services configuration item.|
|Version \[version\]|
|Class \[sys\_class\_name\]|
|Fully qualified domain name \[fqdn\]|
|IP Address \[ip\_address\]|
|Installation directory \[install\_directory\]|
|TCP port\(s\) \[tcp\_port\]|
|Configuration directory \[config\_directory\]|
|Configuration file \[config\_file\]|
|Installation directory \[install\_directory\]|

## Data collected by Service Mapping

Service Mapping can discover application services that contain Tibco ActiveMatrix BusinessWorks \(including BusinessWorks Process\), Tibco Enterprise Message Service \(EMS\), Tibco Enterprise Message Service \(EMS\) Queue.

**Parent Topic:**[Map a single application service using classic Service Mapping](../task/t_DefineNewBusinessService.md)

## Map application services containing Tibco BusinessWorks and EMS

Map an application service containing Tibco BusinessWorks and Enterprise Message Service \(EMS\) and verify that Service Mapping discovered all Tibco components correctly.

### Before you begin

-   \(If hosted on Unix\) Configure [applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) for the Tibco EMS.
-   \(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).
-   \(If hosted on a Unix server\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).
-   \(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

Role required: service\_mapping\_admin

### Procedure

1.  Create a service instance.

    1.  Navigate to **All** &gt; **Service Mapping** &gt; **Service Instances**.

    2.  Click **New**.

        The **Discoverable by Service Mapping** option is selected by default.

    3.  In the **Name** field, enter a descriptive name for the service instance.

2.  Define the entry point for this application service:

    1.  Select the **Other application** tile.

        The **Discoverable by Service Mapping** option is selected by default.

    2.  From the Select Entry Point Type list, select `HTTP(s) Endpoint, TCP Endpoint, Tibco BW Endpoint`.

    3.  Define the entry point as follows:

        -   The URL to the process that correlates to the Tibco BusinessWorks Project, for example, `http://10.xx.xx.xx:6710/GetMemberActivitiy/Processes/ServiceGetMemberActivitiy.service`.
        -   \(Optional\) The hostname on which the BusinessWorks Project runs as a service.
    4.  Click **Add**.

    5.  Click **Save**.

3.  Click **Additional Info** on the left and clear the **Traffic based discovery** check box.

4.  Click **Update**.

5.  Verify that the mapping result is satisfactory:

    1.  Click **View Map** and wait until the mapping is complete.

        It may take a few minutes.

    2.  Review the application service map and make sure that the service layout is as in the following examples.

        ![Check the result of mapping an application service containing Tibco components.](../image/TIBCO-components.png)

    In addition, verify that the BusinessWorks CIs are inclusions each of which contain a BusinesWorks process. Also, verify that the EMS CIs are inclusions containing EMS Queues.

    ![Check inclusions for Tibco applications.](../image/TIBCO-components-inclusions.png)


If the mapping result is not as you expected, perform basic troubleshooting.

<table id="table_kjv_sdy_32b"><thead><tr><th>

Symptom

</th><th>

Cause

</th><th>

Solution

</th></tr></thead><tbody><tr><td>

\(Only for deployments hosting BusinessWorks on a Unix server\) The service instance map shows the BusinessWorks CI without an inclusion of the BusinessWorks process.The discovery log shows the error message stating that the user does not have sufficient credentials.

</td><td>

Service Mapping failed to run the `TibcoFilesParser.ksh` command.

</td><td>

Make sure that you provided a user with elevated rights as described in [Service Mapping commands not requiring a privileged user](../reference/r_NonSudoCommands.md).

</td></tr><tr><td>

Service Mapping failed to discover the outgoing connections of EMS to the EMS process.

</td><td>

Service Mapping failed to run the `tibemsadmin` command.

</td><td>

Make sure that you provided a user with elevated rights as described in [Service Mapping commands not requiring a privileged user](../reference/r_NonSudoCommands.md).

</td></tr></tbody>
</table>