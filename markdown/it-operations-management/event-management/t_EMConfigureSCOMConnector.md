---
title: Configure the SCOM connector instance
description: Configure the Microsoft System Center Operations Manager \(SCOM\) connector to receive alerts and Metric Intelligence raw data from the SCOM server. SCOM event collection and metric collection are handled by two separate connector definitions: SCOM \(for alerts and bi-directional exchange\) and SCOM Metrics \(for Metric Intelligence raw data\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/event-management/t\_EMConfigureSCOMConnector.html
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 10
breadcrumb: [Configure alert collection from SCOM, Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure the SCOM connector instance

Configure the Microsoft System Center Operations Manager \(SCOM\) connector to receive alerts and Metric Intelligence raw data from the SCOM server. SCOM event collection and metric collection are handled by two separate connector definitions: SCOM \(for alerts and bi-directional exchange\) and SCOM Metrics \(for Metric Intelligence raw data\).

## Before you begin

Common prerequisites \(both connectors\):

-   The MID Server is running on Windows.
-   The MID Server resides in the same domain as the SCOM server.
-   The MID Server uses the same time zone as the SCOM server.

Additional prerequisites for SCOM event collection:

-   The MID Server is running with a user that has local admin permissions to enable the MID Server to run PowerShell.
-   The MID Server user has read access to the SCOM API.
-   The MID Server has .NET framework version 3.5 \(for SCOM 2007/2012\) or .NET 4.6 or higher \(for SCOM 2016/2019/2022/2025\).
-   If Bi-directional is selected, ensure that PowerShell version 3.0 is installed on Windows and the MID Server is running with a user that has local admin permissions.

Additional prerequisites for SCOM metric collection:

The MID Server that retrieves metrics is configured with the Metric Intelligence extension and the extension is in Started mode. See Manually configure the Metric Intelligence extension.If "Database login with Windows authentication" is selected, the MID Server service must run with a user having read access to the SCOM database \(OperationsManagerDW\). To configure this: In the local services, right-click the MID Server service and select Properties. In the Log On tab, ensure that "This account" is selected with the details of the Windows domain user that has read access to the SCOM database.

If "Database login with Windows authentication" is NOT selected, you need a Windows credential in the credential store that has read access to the OperationsManagerDW database.

Upgrading from a previous release: If you are upgrading from a release where a single SCOM connector handled both events and metrics, the upgrade automatically disables metric collection on the old SCOM connector and deprecates the old metric-related parameters and event rules. Your existing SCOM connector continues to handle event collection as before — no action needed for events. To resume metric collection after the upgrade, create a new SCOM Metrics connector instance.

Role required: evt\_mgmt\_admin

## About this task

There are two connector definitions for SCOM. The SCOM \(Events\) connector collects alerts using PowerShell and native .NET SCOM client executables. It requires DLL files from the SCOM server to be uploaded to the MID Server. It also supports bi-directional alert exchange. The SCOM Metrics connector collects Metric Intelligence raw data using JavaScript running JDBC directly against the OperationsManagerDW database. It does not require any DLL files and does not collect events or support bi-directional exchange.

You can also use this setup for the SCOM managed instance on Azure.

This connector has the **logPayloadForDebug** log parameter enabled, which logs event and metric payloads from the source system. Once debugging is complete, set this parameter to **false** to prevent overloading the system.

Supported versions:

-   2007 – version 6.1.7221.0
-   2012 – version 7.1.10226.0
-   2016 – version 7.2.117190 and 7.3.13261.0
-   2019 – version 10.19.10050.0
-   2022 – version 10.22.10118.0

## Procedure

1.  Configure the SCOM \(Events\) connector instance.

    Follow these steps to collect SCOM alerts and optionally enable bi-directional alert exchange. This connector uses PowerShell and native .NET SCOM client executables.

    1.  On the SCOM server, download the following files to a local computer.

<table id="table_gmh_wv4_qjc"><thead><tr><th>

Version

</th><th>

SCOM path and library names

</th></tr></thead><tbody><tr><td>

SCOM 2012R2 or SCOM 2012

</td><td>

`%ProgramFiles%\Microsoft System Center 2012 R2 or 2012\Operations Manager\Server\SDK Binaries` -   `Microsoft.EnterpriseManagement.Core.dll`
-   `Microsoft.EnterpriseManagement.OperationsManager.Common.dll`
-   `Microsoft.EnterpriseManagement.Runtime.dll`


</td></tr><tr><td>

SCOM 2007

</td><td>

`%ProgramFiles%\System Center Operations Manager 2007\SDK Binaries` -   `Microsoft.EnterpriseManagement.OperationsManager.Common.dll`
-   `Microsoft.EnterpriseManagement.OperationsManager.dll`
**Note:** Don't append 2007 to the `Microsoft.EnterpriseManagement.OperationsManager.Common.dll` file.

</td></tr><tr><td>

SCOM 2016

</td><td>

`%ProgramFiles%\Microsoft System Center 2016\Operations Manager\Server\SDK Binaries` -   `Microsoft.EnterpriseManagement.Core.dll`
-   `Microsoft.EnterpriseManagement.OperationsManager.dll`
-   `Microsoft.EnterpriseManagement.Runtime.dll`
**Note:** The MID Server must be installed with .NET 4.6 or higher.

</td></tr><tr><td>

SCOM 2019

</td><td>

`%ProgramFiles%\Microsoft System Center 2019\Operations Manager\Server\SDK Binaries` -   `Microsoft.EnterpriseManagement.Core.dll`
-   `Microsoft.EnterpriseManagement.OperationsManager.dll`
-   `Microsoft.EnterpriseManagement.Runtime.dll`
**Note:** The MID Server must be installed with .NET 4.6 or higher.

</td></tr><tr><td>

SCOM 2022

</td><td>

-   `Microsoft.EnterpriseManagement.Core.dll`
-   `Microsoft.EnterpriseManagement.OperationsManager.dll`
-   `Microsoft.EnterpriseManagement.Runtime.dll`
 **Note:** The MID Server must be installed with .NET 4.6 or higher.

</td></tr><tr><td>

SCOM 2025

</td><td>

-   `Microsoft.EnterpriseManagement.Core.dll`
-   `Microsoft.EnterpriseManagement.OperationsManager.dll`
-   `Microsoft.EnterpriseManagement.OperationsManager.Common.dll`
-   `Microsoft.EnterpriseManagement.Runtime.dll`
 **Note:** The MID Server must be installed with .NET 4.6 or higher.

</td></tr></tbody>
</table>        **Note:** A connection cannot be made to SCOM 2012/SCOM 2016/SCOM 2019/SCOM 2022 and SCOM 2007 from the same MID Server. To work with both SCOM 2012/SCOM 2016/SCOM 2019/SCOM 2022 \(any of them\) and SCOM 2007 in your instance, do the following before uploading files to your instance:

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

        For details on the connector instance fields displayed on the page, see [SCOM connector instance form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/scom-connector-instance-form.md).

    7.  Select and hold \(or right-click\) the form header and select **Save**.

        The connector instance values are added to the form and the parameters that are relevant to the connector appear.

    8.  In the Connector Instance Values section, you can edit the values of the mandatory SCOM parameters.
        1.  **login\_with\_windows\_authentication** Default value: **false**.

            Set to **true** to enable SCOM event collection and the bi-directional exchange of event values to work with Windows authentication. When invoking this value, ensure that you do the following on the MID Server:

            1.  Navigate to the list of local services, select and hold \(or right-click\) the MID Server service, and select **Properties**.
            2.  In the **Log On** tab, ensure that **This account** is selected with the details of the user in the Windows domain with read access to the SCOM database.
        2.  **scom\_date\_format**: Default format: M/d/yyyy/ h:mm:ss a

            If you receive an event whose date is in a different format, modify this value to match the format of the incoming event. If you do not, the event does not process correctly.

            For example, if an event arrives on June 27, 2019 at 11:25 AM with a listed date of **2019/06/27/ 11:25:00 a**, modify the **scom\_date\_format** value to **yyyy/M/d/ h:mm:ss a** to match the format of the received event.

            In **scom\_date\_format**, `a` represents AM, and `p` represents PM.

        3.  **scom\_initial\_sync\_in\_days**: Default value: 7.
        4.  **scom\_version**: It is mandatory to specify the SCOM version.

            Select from 2025, 2022, 2019, 2016, 2012, or 2007.

        5.  **stop\_isMonitorAlert\_bidirectional**: Boolean.

            Set to **true** to stop only SCOM monitoring alerts bi-directionally. Stopping SCOM monitoring alerts can prevent false alarms on the SCOM console when attempting to update the alerts. When set to **false**, SCOM monitoring alerts continue running bi-directionally for all types of SCOM alerts. Default value = false.

        6.  **scom\_alert\_bulk\_size**: Default value: 500. Number of alerts fetched per SCOM collection cycle.
        7.  **debug\_enabled**: Default value: false. Set to true to enable debug logging on the MID Server.
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
    13. After a successful test, select the **Active** check box and then select **Update**.
    If bi-directional is configured, the bi-directional exchange of values to-and-from the external event source is enabled. These scenarios describe the default bi-directional functionality for SCOM connectors:

    -   When an alert is resolved in SCOM, it is auto-closed in ServiceNow. However, it is updated irrespective of the bi-directional feature because during each collection cycle, all alert changes are updated.
    -   When an alert is manually closed in ServiceNow, it is auto-closed in SCOM. If the alert state is changed to **Reopen**, SCOM is also updated.
    -   When an incident is created and associated to an alert in ServiceNow, SCOM receives the incident number as a ticket ID. However, the state of the incident is not available on SCOM. Therefore when the incident is resolved in ServiceNow, SCOM is not updated as the incident number remains the same. When the alert is associated with a new incident, the new incident number is updated in SCOM.
2.  Configure the SCOM Metrics connector instance.

    Follow these steps to collect Metric Intelligence raw data from SCOM. This connector connects directly to the SCOM OperationsManagerDW database using JDBC. It does not require SCOM DLL files on the MID Server. Note: This connector collects metrics only. It does not collect events or support bi-directional exchange. To collect SCOM alerts, configure the SCOM \(Events\) connector.

    1.  Navigate to **Event Management** &gt; **Integrations** &gt; **Connector Instances**.
    2.  Click **New** and create a new connector instance.
    3.  In the **Connector definition** field, select **SCOM Metrics**.
    4.  Fill in the following fields:

        | | |
        |---|---|
        |Metrics database host|The IP address or hostname of the server hosting the OperationsManagerDW database.|
        |Connect using a named instance|Select this if the SQL Server uses a named instance instead of a port number.|
        |Metrics database port|The port used by the database. Default is 1433. This field is hidden if "Connect using a named instance" is selected.|
        |Metrics database named instance|The SQL Server named instance name. This field is visible only when "Connect using a named instance" is selected.|
        |Database login with Windows authentication|Select this to use the MID Server service account's Windows credentials for database access. When selected, the database credential field is hidden.|
        |Database credential|Visible only when Windows authentication is NOT selected. Select a Windows credential from the credential store that has read access to the OperationsManagerDW database. This field is mandatory when Windows authentication is disabled.|
        |Metrics collection schedule \(seconds\)|Frequency in seconds to repeat metric collection. Default is 10.|

    5.  Right-click the form header and select **Save**.
    6.  In the Connector Instance Values section, configure the following parameters:

        |Field|Description|
        |-----|-----------|
        |scom\_db\_name|The name of the SCOM data warehouse database. Default is OperationsManagerDW. Change this only if your database has been renamed.|
        |metric\_chunk\_size|Default value is 50000. Maximum number of metric records fetched per batch.|
        |debug\_enabled|Default is false. Set to true to enable debug logging on the MID Server.|
        |log\_payload|Default is false. Set to true to log raw metric payloads for debugging. Set back to false after debugging is complete to avoid overloading the system.|

    7.  Right-click the form header and select **Save**.
    8.  Select **Test connector** to verify the database connection.

        The test runs a simple query against the OperationsManagerDW database to confirm connectivity.

    9.  After a successful test, select the **Active** check box and select **Update**.

**Parent Topic:**[Configure alert collection from SCOM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/t_EMConfigureSCOMConnectorInstance.md)

