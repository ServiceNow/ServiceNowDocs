---
title: Configure the Service Graph Connector for Microsoft Defender for IoT \(Azure\)
description: Use the guided setup for the Service Graph Connector for Microsoft Defender for IoT \(Azure\) to lead you through the integration steps.
locale: en-US
release: australia
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Service Graph Connector for Microsoft Defender for IoT \(Azure\), Integrate, Operational Technology Manager, Operational Technology]
---

# Configure the Service Graph Connector for Microsoft Defender for IoT \(Azure\)

Use the guided setup for the Service Graph Connector for Microsoft Defender for IoT \(Azure\) to lead you through the integration steps.

## Before you begin

Dependencies and requirements:

-   The [Integration Commons for CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/cmdb-integration-commons/integration-commons-for-cmdb.md) store app, which is automatically installed.
-   The [CMDB CI Class Models app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/cmdb-ci-class-models/cmdb-ci-class-models.md), which is automatically installed.
-   The ITOM Discovery License plugin \(com.snc.itom.discovery.license\). You must activate this plugin.
-   ITOM Licensing plugin \(com.snc.itom.license\). For more information, see [Request Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/t_ActivateTheDiscoveryPlugin.md).
-   The Datastream Action plugin \(com.glide.hub.action\_type.datastream\), which is automatically installed.
-   The Industrial Core plugin. You must activate this plugin.

    The Industrial Core plugin is required to access the class mappings table for the Service Graph Connector for Microsoft Defender for IoT \(Azure\). For more information about the Industrial Core plugin, see [Industrial Core plugin](../reference/industrial-core-plugin.md).


Role required: admin

**Note:** If you have an earlier version of the Service Graph Connector for Microsoft Defender for IoT \(Azure\), then don’t migrate data from the old connector. You must uninstall the previous version and run the new integration.

## Procedure

1.  Ensure that the application scope is set to the Service Graph Connector for Microsoft Defender for IoT \(Azure\) application by using the application picker.

    For more information, see [Application picker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/c_ApplicationPicker.md).

2.  Navigate to **All** &gt; **Service Graph for MSFT D4IoT \(Azure\)** &gt; **Guided Setup**.

3.  On the Getting started page, select **Get Started**.

4.  To access the Azure resources, complete the following:

    1.  Select the Access to Azure Resources task.

    2.  Once you complete the instructions in the description, select **Mark as Complete**.

5.  To set up the connections and credentials, complete the following:

    1.  In the Configure Connections and Credentials section, select the Setup Connections and Credentials task.

    2.  Select **Configure**.

    3.  Select the **SG-OT Azure Connection** record.

    4.  Select the Create New Connection &amp; Credential related link.

    5.  In the Create Connection and Credential window, fill in the following fields.

        |Field|Description|
        |-----|-----------|
        |Connection Name|Display name for the connection record|
        |Connection URL|Azure URL|
        |OAuth Client ID|Client ID \(application ID\) or Service Principal ID|
        |OAuth Client Secret|Client secret key associated with the Service Principal|
        |OAuth Token URL|URL to fetch Authorization token. Replace &lt;tenantid&gt; in the URL with the Tenant ID value.|

        **Note:** When a token generation is successful, a new window appears with a success message. When a token generation isn’t successful, a new window with the error message `OAuth flow failed` appears. Please check the details provided and try again by editing the record you created.

    6.  Select **Create and Get OAuth Token**.

6.  To test the connection, complete the following:

    1.  In the Setup Connections and Credentials section, select the Test/Validate Connection task.

    2.  Select the **Test Connection** UI action from the related links section on the data source record for sensors.

        After completing the connection test, view the results. You must perform the suggested troubleshooting steps until the test result returns **Success**.

7.  To configure the system properties, complete the following:

    1.  In the Configure System Properties section, select **Configure**.

    2.  Configure the following system properties.

<table id="table_bt3_df4_lzb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_msftd4iotazsgc.resource\_path

</td><td>

Set the resource path property.The default Resource Path for the ARG REST API version 2021-03-01 is`/providers/Microsoft.ResourceGraph/resources`.

</td></tr><tr><td>

sn\_msftd4iotazsgc.pagesize.sensor

</td><td>

Set the page size property for sensors.-   As Azure ARG REST API supports pagination, you can choose the number of records per page for each API.
-   The default is 1000 records per page.

**Note:** 1000 is also the maximum number of records per page.

</td></tr><tr><td>

sn\_msftd4iotazsgc.pagesize.device

</td><td>

Set the page size property for devices.-   As Azure ARG REST API supports pagination, you can choose the number of records per page for each API.
-   The default is 1000 records per page.

**Note:** 1000 is also the maximum number of records per page.

</td></tr><tr><td>

sn\_msftd4iotazsgc.get\_all\_devices

</td><td>

-   For devices, you can choose to fetch all records \(box checked\) or the delta \(box unchecked\).
-   The DELTA fetches all the records created or updated since the start time of the last successful import in the CMDB.
 **Note:** When you run the Devices Integration for the first time, all records are imported independent of this property.

</td></tr><tr><td>

sn\_msftd4iotazsgc.convert\_sensor\_names\_to\_lowercase

</td><td>

Set this property for devices import. -   This system property is used to convert the sensor names provided by Microsoft Azure into lowercase while importing devices.
-   This is required as Microsoft Azure expects data for the query in a lowercase format.


</td></tr><tr><td>

sn\_msftd4iotazsgc.filter.device\_sub\_types

</td><td>

Set this property for filtering the devices during device import by sub type. -   Comma-separated list of Microsoft Azure sub types to filter the devices.
-   For example: to import only PLCs and servers, provide the value from the DeviceSubType attribute from Microsoft Azure as `Server, PLC`.


</td></tr><tr><td>

sn\_msftd4iotazsgc.filter.device\_tags

</td><td>

Set this property for filtering the devices during device import by device tag. -   Comma-separated list of case sensitive tags that are needed to filter devices.
-   For example: to import devices with specific tags, provide a list of values from the DeviceTags attribute in Microsoft Azure.


</td></tr><tr><td>

sn\_msftd4iotazsgc.filter.custom\_query

</td><td>

Set this property to add more filters for device import apart from the Device SubType and Device Tags filter. -   Query to filter based on other attributes.
-   This allows filtering for other attributes. For more information, see [Azure Query Language](https://learn.microsoft.com/en-us/azure/governance/resource-graph/concepts/query-language).


</td></tr><tr><td>

sn\_msftd4iotazsgc.azure\_d4iot\_site\_map\_fields

</td><td>

An object of fields from the Microsoft Defender for IoT \(Azure\) Site Map. When a field is set to **True**, the Service Graph Connector for Microsoft Defender for IoT \(Azure\) passes the value of the Site Map field to the corresponding field on each CI discovered by the integration at the Azure site.If set to **False** or not populated on the Site Map record, the field isn't set on the imported CIs associated with the Azure site.

For consistency with the other integrations using the NIDS framework, check this system property. By default, only **location** and **equipment\_model\_entity** are set to **True**.

</td></tr><tr><td>

sn\_msftd4iotazsgc.devices\_fetch\_type

</td><td>

Indicates if devices are fetched per sensor, Active Scan devices, or both.

</td></tr><tr><td>

sn\_msftd4iotazsgc.active\_scan\_get\_all\_devices

</td><td>

Set this system property to import all Active Scan devices. If not checked, then only the Active Scan devices created or updated since the last successful import are imported. The default value is **No**.

</td></tr><tr><td>

sn\_msftd4iotazsgc.filter.active\_scan.device\_sub\_types

</td><td>

Comma-separated list of Azure subtypes to filter the Active Scan devices. For example, to only import PLCs and servers, provide the value from the Device SubType attribute as `Server, PLC` in Azure.

</td></tr><tr><td>

sn\_msftd4iotazsgc.filter.active\_scan.device\_tags

</td><td>

Comma-separated list of case sensitive tags needed to filter Active Scan devices. For example, to import Active Scan devices with specific tags, provide a list of values from the DeviceTags attribute from Azure.

</td></tr><tr><td>

sn\_msftd4iotazsgc.filter.active\_scan.custom\_query

</td><td>

Query to filter other attributes for Active Scan devices. For example, to allow filtering on other attributes.For more information about the Azure query language, see [Azure Query Language](https://learn.microsoft.com/en-us/azure/governance/resource-graph/concepts/query-language) for more information.

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

    2.  Select **SG-OT Microsoft Azure D4IoT Sensors Scheduled Import** to review or change the sensors import schedule as needed.

        1.  Select **Active** to activate the sensors import schedule.
        2.  By default, the sensors import schedule is configured to run daily at midnight. Change the schedule using the **Run** and **Time** fields.
        3.  Select the **Conditional** check box to make this schedule conditional.
        4.  Select **Execute Now** to start a manual import.
    3.  Select **SG-OT Microsoft Azure D4IoT Devices Scheduled Import** to review or change the devices import schedule as needed.

        1.  Select **Active** to activate the sensors import schedule.
        2.  By default, the sensors import schedule is configured to run daily at midnight. Change the schedule using the **Run** and **Time** fields.
        3.  Select the **Conditional** check box to make this schedule conditional.
        4.  Select **Execute Now** to start a manual import.
        **Note:** Devices are queried per sensor. The Service Graph Connector only queries for devices detected by a validated sensor. For more information, see step 9.

11. When configuration items \(CIs\) are created in the CMDB, asset records are created.

    The asset record contains the model category of the CI. For more information about the model categories for Operational Technology \(OT\), see [Model categories for Operational Technology](../reference/model-categories-for-ot.md). To view the model category for an OT device, complete the following:

    1.  Navigate to **All** &gt; **Operational Technology \(OT\)** &gt; **All OT Devices**.
    2.  Select an OT device to view its asset record in a new tab.
12. To troubleshoot the Service Graph Connector for Microsoft Defender for IoT \(Azure\), complete the following:

    1.  Select the \[OPTIONAL\] Troubleshooting the Service Graph Connector for Microsoft Defender for IoT \(Azure\) section.

    2.  In the Execute the validations scheduled job task, select **Configure**.

    3.  Select **Execute Now**.

        This job performs tasks to validate the configurations for SGC and the connection to Microsoft Azure. If configuration issues are found, the validation results report the problem and suggest troubleshooting steps. Wait for the scheduled job to finish.

    4.  Once the scheduled job is complete, Navigate back to the \[OPTIONAL\] Troubleshooting the Service Graph Connector for Microsoft Defender for IoT \(Azure\) section.

    5.  In the Review validation results task, select **Configure**.

        This step opens the execution logs and suggestions of the last troubleshooting run for you to view.

    6.  Address the suggestions as needed.

        **Note:** You can use the scheduled script at any point after the initial configuration of the Service Graph Connector Integration for Claroty CTD. To trigger validations, navigate to **All** &gt; **Service Graph for MSFT D4IoT \(Azure\)** &gt; **Troubleshooting** &gt; **Run Troubleshooting**. To view the validation results, navigate to **All** &gt; **Service Graph for MSFT D4IoT \(Azure\)** &gt; **Troubleshooting** &gt; **Results**.


## What to do next

You can now connect Microsoft Defender for IoT \(Azure\) with the ServiceNow Service Graph Connector for Microsoft Defender for IoT \(Azure\). For more information, see [Connecting your Microsoft Defender for IoT \(Azure\) subscription to the ServiceNow Service Graph Connector for Microsoft Defender for IoT \(Azure\) \(KB1587770\)](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1587770).

**Parent Topic:**[Service Graph Connector for Microsoft Defender for IoT \(Azure\)](../concept/integration-sgc-microsoft-defender-iot-azure.md)

