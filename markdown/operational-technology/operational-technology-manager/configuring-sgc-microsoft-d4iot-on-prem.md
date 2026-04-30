---
title: Configure the Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\)
description: Use the Guided Setup for the Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\) to lead you through the integration steps.
locale: en-US
release: zurich
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\), Integrate, Operational Technology Manager, Operational Technology]
---

# Configure the Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\)

Use the Guided Setup for the Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\) to lead you through the integration steps.

## Before you begin

Dependencies and requirements:

-   The [Integration Commons for CMDB](https://www.servicenow.com/docs/access?context=integration-commons-for-cmdb&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) store app, which is automatically installed.
-   The [CMDB CI Class Models](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US), which is automatically installed.
-   The ITOM Discovery License plugin \(com.snc.itom.discovery.license\). You must activate this plugin.
-   ITOM Licensing plugin \(com.snc.itom.license\). For more information, see [Request Discovery](https://www.servicenow.com/docs/access?context=t_ActivateTheDiscoveryPlugin&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US).
-   The Datastream Action plugin \(com.glide.hub.action\_type.datastream\), which is automatically installed.

Role required: admin

**Note:** If you have an earlier version of the Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\), then don’t migrate data from the old connector. You must uninstall the previous version and run the new integration.

## Procedure

1.  Ensure that the application scope is set to the Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\) application by using the application picker.

    For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

2.  Navigate to **All** &gt; **Service Graph Connector Microsoft D4IoT** &gt; **Guided Setup**.

3.  On the Getting started page, select **Get Started**.

4.  To configure a MID Server, complete the following:

    1.  In the Setup Connections and Credentials section, select the Configure MID server task.

    2.  Select **Mark as complete** once you complete the MID Server configuration linked in the description.

5.  To update the Connection and Credentials Alias record, complete the following:

    1.  In the Setup Connections and Credentials section, select the Connections and Credentials task.

    2.  Select **Configure**.

    3.  Open the default record **Microsoft D4IoT Base API**.

    4.  From the Connections related list, select **New** to create a new HTTP\(s\) Connection record.

    5.  In the **Connection URL** field, enter the name for the URL of your Microsoft Defender for IoT Central Manager.

        For example, `https://192.168.1.100`.

    6.  If you are using a MID Server, select all of the following:

        -   **Use MID Server** box
        -   **MID Server** from the Advanced MID Server Configuration related list
        -   **MID Selection** from the list
    7.  In the **Credential** field, select the search icon to open the Credentials records list.

    8.  Select **New** to create a new record.

    9.  Select the **API Key Credentials** type.

    10. In the **API Key** field, enter a name and the API Key provided by your Microsoft Defender for IoT management console.

    11. Select **Submit** to create the credential record.

        To create an API Key in the Microsoft Defender for IoT management console, refer to Microsoft product documentation: [https://docs.microsoft.com/en-us/azure/defender-for-iot/organizations/references-work-with-defender-for-iot-apis](https://docs.microsoft.com/en-us/azure/defender-for-iot/organizations/references-work-with-defender-for-iot-apis).

    12. On the Connection form, select **Submit** to finish creating the Connection record.

6.  To test the connection, complete the following:

    1.  In the Setup Connections and Credentials section, select the Test/Validate Connection task.

    2.  Select the **Test Connection** UI action from the related links section on the data source record for sensors.

        After completing the connection test, view the results. You must perform the suggested troubleshooting steps until the test result returns **Success**.

    3.  Check that the connection manager has a valid certificate.

        A valid certificate must be installed for a production environment. For a non-production or proof of concept \(POC\) instance, you can configure the system properties to enable the integration to work when the connection manager doesn’t have a valid certificate. The following table lists the system properties that you can configure for a non-production environment.

<table id="table_scq_mjj_kyb"><thead><tr><th>

Property

</th><th>

Value

</th></tr></thead><tbody><tr><td>

com.glide.communications.httpclient.verify\_hostname

</td><td>

Set to **false**.

</td></tr><tr><td>

com.glide.communications.httpclient.verify\_revoked\_certificate

</td><td>

Set to **false**.If you need to add this system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

</td></tr><tr><td>

com.glide.communications.trustmanager\_trust\_all

</td><td>

Set to **true**.

</td></tr></tbody>
</table>    4.  Check the MID security policy.

        In the intranet record, verify that the columns in the following table show the specified values.

        |Column|Value|
        |------|-----|
        |Certificate chain check|**false**|
        |Hostname check|**false**|
        |Revocation check|**false**|

        For more information, see [MID Server certificate check policies](https://www.servicenow.com/docs/access?context=mid-security-checks&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

        The connection shows that it is set correctly when the progress window shows the Completion code **Success**, and the number of records processed shows as the same number of sensors in the connection manager.

7.  To configure the system properties, complete the following:

    1.  In the Configure System Properties section, select **Configure**.

    2.  Configure the following system properties.

<table id="table_bt3_df4_lzb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_msftd4iotsgc.resourcepath.sensor

</td><td>

Set the sensors resource path. -   The sensors resource path is provided by default for the V3 API version.
-   If you want to use a different API version, you can override the path.


</td></tr><tr><td>

sn\_msftd4iotsgc.resourcepath.device

</td><td>

-   The devices resource path is provided by default for the V3 API version.
-   If you want to use a different API version, you can override the path.


</td></tr><tr><td>

sn\_msftd4iotsgc.resourcepath.connection

</td><td>

-   The connections resource path is provided by default for the V3 API version.
-   If you want to use a different API version, you can override the path.


</td></tr><tr><td>

sn\_msftd4iotsgc.pagesize.device

</td><td>

Enter the number of records to display per page for each Devices and Connections API. Default value: 50 records per page

</td></tr><tr><td>

sn\_msftd4iotsgc.pagesize.connection

</td><td>

-   If you want to use a different Connection Alias than the Microsoft D4IoT Base API configured while setting up the connections and credentials records, you can enter the sys\_id of your custom Connection Alias record in this property field.
-   The default value of this property is empty. If this property field is left blank, the Microsoft D4IoT Base API Connection Alias is used by default.


</td></tr><tr><td>

sn\_msftd4iotsgc.get\_all\_devices

</td><td>

Select whether to fetch all records for devices, or only new records since the start time of the last successful import.**Note:** When you import devices for the first time, all records are imported regardless of the setting for this property.

</td></tr><tr><td>

sn\_msftd4iotsgc.get\_all\_connections

</td><td>

Select whether to fetch all records for connections, or only new records since the start time of the last successful import in the CMDB.**Note:** When you import connections for the first time, all records are imported regardless of the setting for this property.

</td></tr><tr><td>

sn\_msftd4iotsgc.ot.vr.integration.id

</td><td>

If you are using the Operational Technology Vulnerability Response application with the Service Graph for Microsoft Defender for IoT integration, provide the sys ID of the OT VR import record.**Note:** If the Operational Technology Vulnerability Response plugin is installed and this property field is left blank, the **Microsoft D4IoT Devices CVE Integration \(Delta Import\)** executes if Active is set to **true** on the record.

</td></tr></tbody>
</table>    3.  Select **Save**.

8.  To import sensors, complete the following:

    1.  In the Configure Sensors \(NIDS\) section, select the Import Sensors task.

    2.  Select **Configure**.

    3.  Select **Active** to activate the Scheduled Data Import job.

9.  To configure the NIDS, complete the following:

    1.  In the Configure Sensors \(NIDS\) section, select the Import Sensors task.

    2.  Select **Mark as complete** once you complete the NIDS configuration linked in the description.

10. To configure import schedules, complete the following:

    1.  In the Configure Import Schedules section, select **Configure**.

    2.  Select **SG-OT Microsoft D4IoT Sensors Scheduled Import** to review or change the sensors import schedule as needed.

        -   By default, the sensors import schedule is configured to run daily at midnight.
        -   Import sensors before importing devices or connections.
    3.  Select **Active** to activate the sensors import schedule.

    4.  Select **SG-OT Microsoft D4IoT Devices Scheduled Import** to review or change the devices import schedule as needed.

        -   By default, the devices import schedule is configured to run daily at midnight.
        -   Devices are queried by sensor. The Service Graph Connector queries for devices detected by validated sensors. For information about configuring Network Intrusion Detection System \(NIDS\) appliances, see [Validate the NIDS](validate-nids.md).
    5.  Select **Active** to activate the devices import schedule.

    6.  Select **SG-OT Microsoft D4IoT Connections Scheduled Import** to review or change the connections import schedule as needed.

        -   By default, the connections import schedule is configured to run after the devices import runs \(**After Parent Runs**\).
        -   Connections are only imported if both devices \(Source &amp; Destination in Microsoft API, or Parent &amp; Child in the CMDB\) are already in the CMDB.
        -   Import devices before importing connections.

**Parent Topic:**[Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\)](../concept/integration-sgc-microsoft-defender-iot-on-prem.md)

