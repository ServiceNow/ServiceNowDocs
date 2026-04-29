---
title: Configure the SCOM connector instance
description: Configure the Microsoft System Center Operations Manager \(SCOM\) connector instance to receive alerts and Metric Intelligence raw data from the SCOM server.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Configure alert collection from SCOM, Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure the SCOM connector instance

Configure the Microsoft System Center Operations Manager \(SCOM\) connector instance to receive alerts and Metric Intelligence raw data from the SCOM server.

## Before you begin

To activate **Metric Collection**, ensure that the MID Server that retrieves metrics is configured with the Metric Intelligence extension and that the extension is in **Started** mode. See [Manually configure the Metric Intelligence extension](configure-itoa-metric-extension.md).

Windows authentication is used by the connector to access the SCOM database \(OperationsManagerDW\). Therefore, if **Metric Collection** is selected and the **Database login with Windows authentication** option is also selected, ensure that the MID Server service runs with a user having read access to the SCOM database. Ensure that the correct credentials are used:

1.  In the local services, select and hold \(or right-click\) the MID Server service and select **Properties**.
2.  In the **Log On** tab, ensure that **This account** is selected. Include the details of the Windows domain user that has read access to the SCOM database.

Before starting the procedure to configure the connector, ensure that:

-   The MID Server is running with a user that has local admin permissions to enable the MID Server to run PowerShell.
-   The MID Server user has read access to the SCOM API.
-   The MID Server resides in the same domain as the SCOM server.
-   The MID Server uses the same time zone as the SCOM server.
-   The MID Server is running on Windows.
-   The MID Server has .NET framework version 3.5.

If **Bi-directional** is selected, ensure that:

-   PowerShell version 3.0 is installed on Windows.
-   The MID Server is running with a user that has local admin permissions to enable running PowerShell.

To upgrade an existing SCOM connector:

1.  On the Connector Instance - SCOM connector page \(**All** &gt; **Event Management** &gt; **Integrations** &gt; **Connector Instances**\), clear the **Collect Metrics** check box.
2.  Install the **em-connectors** plugin from the store.

Role required: evt\_mgmt\_admin

## About this task

To receive SCOM alerts, you can obtain the redistributable SCOM files from your SCOM application. Add the files to the MID Server, and then configure a SCOM connector instance to collect the alerts and Metric Intelligence raw data.

The collection of Metric Intelligence is performed using JavaScript running JDBC in place of PowerShell.

You can also use this setup for the SCOM managed instance on Azure.

This connector has the **logPayloadForDebug** log parameter enabled, which logs event and metric payloads from the source system. Once debugging is complete, set this parameter to **false** to prevent overloading the system.

Supported versions:

-   2007 – version 6.1.7221.0
-   2012 – version 7.1.10226.0
-   2016 – version 7.2.117190 and 7.3.13261.0
-   2019 – version 10.19.10050.0
-   2022 – version 10.22.10118.0
-   2025 - version 10.25.10132.0

## Procedure

1.  On the SCOM server, download the following files to a local computer.

<table id="choicetable_rnt_dzq_dt"><thead><tr><th align="left" id="d385659e305">

Version

</th><th align="left" id="d385659e308">

SCOM path and library names

</th></tr></thead><tbody><tr><td id="d385659e314">

**SCOM 2012R2 or SCOM 2012**

</td><td>

`%ProgramFiles%\Microsoft System Center 2012 R2 or 2012\Operations Manager\Server\SDK Binaries` -   `Microsoft.EnterpriseManagement.Core.dll`
-   `Microsoft.EnterpriseManagement.OperationsManager.Common.dll`
-   `Microsoft.EnterpriseManagement.Runtime.dll`


</td></tr><tr><td id="d385659e342">

**SCOM 2007**

</td><td>

`%ProgramFiles%\System Center Operations Manager 2007\SDK Binaries` -   `Microsoft.EnterpriseManagement.OperationsManager.Common.dll`
-   `Microsoft.EnterpriseManagement.OperationsManager.dll`
 **Note:** Do not append 2007 to the `Microsoft.EnterpriseManagement.OperationsManager.Common.dll` file.

</td></tr><tr><td id="d385659e371">

**SCOM 2016**

</td><td>

`%ProgramFiles%\Microsoft System Center 2016\Operations Manager\Server\SDK Binaries` -   `Microsoft.EnterpriseManagement.Core.dll`
-   `Microsoft.EnterpriseManagement.OperationsManager.dll`
-   `Microsoft.EnterpriseManagement.Runtime.dll`
 **Note:** The MID Server must be installed with .NET 4.6 or higher.

</td></tr><tr><td id="d385659e405">

**SCOM 2019**

</td><td>

`%ProgramFiles%\Microsoft System Center 2019\Operations Manager\Server\SDK Binaries` -   `Microsoft.EnterpriseManagement.Core.dll`
-   `Microsoft.EnterpriseManagement.OperationsManager.dll`
-   `Microsoft.EnterpriseManagement.Runtime.dll`
 **Note:** The MID Server must be installed with .NET 4.6 or higher.

</td></tr><tr><td id="d385659e440">

**SCOM 2022**

</td><td>

-   `Microsoft.EnterpriseManagement.Core.dll`
-   `Microsoft.EnterpriseManagement.OperationsManager.dll`
-   `Microsoft.EnterpriseManagement.Runtime.dll`
 **Note:** The MID Server must be installed with .NET 4.6 or higher.

</td></tr><tr><td id="d385659e471">

**SCOM 2025**

</td><td>

-   `Microsoft.EnterpriseManagement.Core.dll`
-   `Microsoft.EnterpriseManagement.OperationsManager.dll`
-   `Microsoft.EnterpriseManagement.OperationsManager.Common.dll`
-   `Microsoft.EnterpriseManagement.Runtime.dll`
 **Note:** The MID Server must be installed with .NET 4.6 or higher.

</td></tr></tbody>
</table>    **Note:** A connection cannot be made to SCOM 2012/SCOM 2016/SCOM 2019/SCOM 2022 and SCOM 2007 from the same MID Server. To work with both SCOM 2012/SCOM 2016/SCOM 2019/SCOM 2022 \(any of them\) and SCOM 2007 in your instance, do the following before uploading files to your instance:

    1.  Append .2012 to the end of the `Microsoft.EnterpriseManagement.OperationsManager.dll` file, so it becomes: `Microsoft.EnterpriseManagement.OperationsManager.dll.2012`. Do this for 2012/2016/2019/2022.
    2.  Append .2007 to the end of the `Microsoft.EnterpriseManagement.OperationsManager.dll` file found in the 2007 path.
    Using these modified file names enables the relevant MID Server to load the applicable DLL when both SCOM versions are deployed. Do not append 2007 to the `Microsoft.EnterpriseManagement.OperationsManager.Common.dll` file \(for SCOM 2007\).

    At any given time, you can define connectors of either SCOM 2007, SCOM 2012/2016, or SCOM2019. Since SCOM 2012 and SCOM 2016 use the same library files, they are able to work at the same time. Although, SCOM 2019 uses the different SCOM DLL files so you cannot configure SCOM 2012, 2016, and 2019 all together. Each SCOM connector can use the database of another connector, for metric support.

2.  Navigate to **MID Server** &gt; **JAR Files**.

3.  Select **New** and add a separate record for the SCOM version for each of the DLL files that you downloaded from the SCOM server.

    1.  In the **Name** field, specify the SCOM version and an identifier to make the name unique, for example `2012 1`.

        If you are using SCOM 2016, specify 2012 as the version.

    2.  Select the paper clip icon in the form header and then attach one of the appropriate DLL files that you downloaded.

    3.  Select **Submit**.

4.  Repeat step 3, creating a separate record for each of the remaining DLL files.

    Ensure that you have a unique identifier after the SCOM version for each file that you attach, for example `2012 2`.

5.  Navigate to **Event Management** &gt; **Integrations** &gt; **Connector Instances**.

6.  Click **New** and create a new connector instance.

    For details on the connector instance fields displayed on the page, see [SCOM connector instance form](../reference/scom-connector-instance-form.md).

7.  Select and hold \(or right-click\) the form header and select **Save**.

    The connector instance values are added to the form and the parameters that are relevant to the connector appear.

8.  In the Connector Instance Values section, you can edit the values of the mandatory SCOM parameters.

    1.  **login\_with\_windows\_authentication** Default value: **false**.

        Set to **true** to enable SCOM event collection and the bi-directional exchange of event values to work with Windows authentication.

        When invoking this value, ensure that you do the following on the MID Server:

        1.  Navigate to the list of local services, select and hold \(or right-click\) the MID Server service, and select **Properties**.
        2.  In the **Log On** tab, ensure that **This account** is selected with the details of the user in the Windows domain with read access to the SCOM database.
    2.  **metric\_chunk\_size**: Default value: 50000.

    3.  **scom\_date\_format**: Default format: M/d/yyyy/ h:mm:ss a

        If you receive an event whose date is in a different format, modify this value to match the format of the incoming event. If you do not, the event does not process correctly.

        For example, if an event arrives on June 27, 2019 at 11:25 AM with a listed date of **2019/06/27/ 11:25:00 a**, modify the **scom\_date\_format** value to **yyyy/M/d/ h:mm:ss a** to match the format of the received event.

        In **scom\_date\_format**, `a` represents AM, and `p` represents PM.

    4.  **scom\_initial\_sync\_in\_days**: Default value: 7.

    5.  **scom\_version**: It is mandatory to specify the SCOM version.

        Select from 2022, 2019, 2016, 2012, or 2007.

    6.  **stop\_isMonitorAlert\_bidirectional**: Boolean.

        Set to **true** to stop only SCOM monitoring alerts bi-directionally. Stopping SCOM monitoring alerts can prevent false alarms on the SCOM console when attempting to update the alerts. When set to **false**, SCOM monitoring alerts continue running bi-directionally for all types of SCOM alerts.

        Default value = false.

9.  Select and hold \(or right-click\) the form header and select **Save**.

10. Restart the MID Server service to copy the files.

11. Select **Test connector** to verify the connection between the MID Server and the connector.

    If the test fails, correct the problem by following the instructions issued by the error and then run another test.

    **Note:** Use a network tool, such as ping, to verify credential correctness and network connectivity from the MID Server to SCOM.

12. After a successful test, select the **Active** check box and then select **Update**.

    **Note:**

    The default binding rules that contain SCOM as the external source, that applies to IT alerts and Metric Intelligence raw data, are the following SCOM Management Packs:

    -   All OS Management Packs
    -   MS SQL Server
    -   IIS

## Example

If bi-directional is configured, the bi-directional exchange of values to-and-from the external event source is enabled.

These scenarios describe the default bi-directional functionality for SCOM connectors:

-   When an alert is resolved in SCOM, it is auto-closed in ServiceNow. However, it is updated irrespective of the bi-directional feature because during each collection cycle, all alert changes are updated.
-   When an alert is manually closed in ServiceNow, it is auto-closed in SCOM. If the alert state is changed to **Reopen**, SCOM is also updated.
-   When an incident is created and associated to an alert in ServiceNow, SCOM receives the incident number as a ticket ID. However, the state of the incident is not available on SCOM. Therefore when the incident is resolved in ServiceNow, SCOM is not updated as the incident number remains the same. When the alert is associated with a new incident, the new incident number is updated in SCOM.

**Parent Topic:**[Configure alert collection from SCOM](t_EMConfigureSCOMConnectorInstance.md)

