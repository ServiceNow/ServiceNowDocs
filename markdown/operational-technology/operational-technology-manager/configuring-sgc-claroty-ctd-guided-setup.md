---
title: Configure the Service Graph Connector Integration for Claroty CTD
description: Use the guided setup for Service Graph Connector Integration for Claroty CTD to lead you through the integration steps.
locale: en-US
release: xanadu
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2025-04-18"
reading_time_minutes: 14
breadcrumb: [Service Graph Connector Integration for Claroty CTD, Integrate, Operational Technology Manager, Operational Technology]
---

# Configure the Service Graph Connector Integration for Claroty CTD

Use the guided setup for Service Graph Connector Integration for Claroty CTD to lead you through the integration steps.

## Before you begin

Dependencies and requirements:

-   The [Integration Commons for CMDB](https://www.servicenow.com/docs/access?context=integration-commons-for-cmdb&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) store app, which is automatically installed.
-   The [CMDB CI Class Models](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US), which is automatically installed.
-   The ITOM Discovery License plugin \(com.snc.itom.discovery.license\). You must activate this plugin.
-   ITOM Licensing plugin \(com.snc.itom.license\). For more information, see [Request Discovery](https://www.servicenow.com/docs/access?context=t_ActivateTheDiscoveryPlugin&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US).
-   The Datastream Action plugin \(com.glide.hub.action\_type.datastream\), which is automatically installed.
-   Review that **View** access is enabled in Claroty CTD for the following user permissions to collect data from Claroty CTD to ServiceNow:
    -   Visibility
    -   Investigation
-   The Industrial Core plugin. You must activate this plugin.

    The Industrial Core plugin is required to access the class mappings table for the Service Graph Connector Integration for Claroty CTD.


Role required: admin

**Note:** If you have an earlier version of the Service Graph Connector Integration for Claroty CTD, then don’t migrate data from the old connector. You must uninstall the previous version and run the new integration.

## Procedure

1.  Ensure that the application is set to Service Graph Connector Integration for Claroty CTD by using the application picker.

    For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

2.  Navigate to **All** &gt; **Service Graph Connector Claroty CTD** &gt; **Guided Setup**.

3.  On the Getting started page, select **Get Started**.

4.  To configure a MID Server, complete the following:

    1.  In the Setup Connections and Credentials section, select the Configure MID server task.

    2.  Select **Mark as complete** once you complete the MID Server configuration.

5.  To set up the connections records, complete the following:

    1.  In the Setup Connections and Credentials section, select the Configure Connections task.

    2.  Select **Configure**.

    3.  Open the Claroty CTD API record in the Connections table.

    4.  In the **Connection URL** field, enter the name of the URL for your Claroty CTD Enterprise Management Console \(EMC\).

        For example, [https://192.168.1.100](https://192.168.1.100).

    5.  If you're using a MID Server, select the **Use MID Server** check box in the record.

        **Note:** If you're not using a MID Server, go to step 5g.

    6.  From the Advanced MID Server Configuration related list, select a MID Server and a MID Selection.

    7.  Select **Update**.

    8.  Repeat steps 5a to 5h to update the **Claroty CTD EMC Base Auth** record.

6.  To set up the credentials records, complete the following:

    1.  In the Setup Connections and Credentials section, select the Configure Credentials task.

    2.  Select **Configure**.

    3.  Open the Claroty CTD EMC Base Auth record in the Credentials table.

    4.  In the **User name** field, enter the user name that you used to log in to the Claroty CTD EMC.

    5.  In the **Password** field, enter the password that you used to log in to the Claroty CTD EMC.

    6.  Select **Update**.

7.  To test the connection, complete the following:

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

Set to **false**.If you need to add this system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

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

        For more information, see [MID Server certificate check policies](https://www.servicenow.com/docs/access?context=mid-security-checks&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

8.  To set the system properties that configure the API resource paths, pagination sizes, and API key expiration times,complete the following:

    1.  In the Configure System Properties section, select **Configure**.

    2.  Configure the system properties in the following table:

<table id="table_r1w_vcf_3yb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_clarotyctdsgc.resourcepath.site

</td><td>

Property to set the resource path for the sites:

 **Note:** The resource path for the sites is provided by default for the Claroty CTD Enterprise Management Console \(EMC\) V4.4.3 API version for the CTD sites and devices.

 If you want to use a different API version, you can override the paths.

</td></tr><tr><td>

sn\_clarotyctdsgc.resourcepath.device

</td><td>

Property to set the resource path for the devices:

 **Note:** The resource path for the devices is provided by default for the CTD EMC V4.4.3 API version for the CTD sites and devices.

 If you want to use a different API version, you can override the paths.

</td></tr><tr><td>

sn\_clarotyctdsgc.pagesize.device

</td><td>

Property to set the number of device records to fetch in a paginated REST call to the Claroty CTD EMC. The default value is 500 records per page.

 **Note:** 500 is the maximum number of devices per page.

</td></tr><tr><td>

sn\_clarotyctdsgc.resourcepath.baseline

</td><td>

Property to set the resource path for the baselines:

 **Note:** The resource path for the baselines is provided by default for the CTD EMC V4.4.3 API version for the CTD sites and devices.

 If you want to use a different API version, you can override the paths.

</td></tr><tr><td>

sn\_clarotyctdsgc.pagesize.baseline

</td><td>

Property to set the number of baseline records to fetch in a paginated REST call to the Claroty CTD EMC. The default value is 500 records per page.

</td></tr><tr><td>

sn\_clarotyctdsgc.get\_all\_baselines

</td><td>

Property to fetch all records for baselines or only the new records since the start time of the last successful import.

 **Note:** When you import baselines for the first time, all records are imported regardless of the setting for this property.

</td></tr><tr><td>

sn\_clarotyctdsgc.resourcepath.entity

</td><td>

Property to set the resource path for the entities:

 **Note:** The resource path for the entities is provided by default for the CTD EMC V4.4.3 API version for the CTD sites and devices. If you want to use a different API version, you can override the paths.

</td></tr><tr><td>

sn\_clarotyctdsgc.resourcepath.program

</td><td>

Property to set the resource path for the installed programs:

 **Note:** The resource path for the installed programs is provided by default for the CTD EMC V4.4.3 API version for the CTD sites and devices.

 If you want to use a different API version, you can override the paths.

</td></tr><tr><td>

sn\_clarotyctdsgc.pagesize.entity

</td><td>

Property to set the number of entity records to fetch in a paginated REST call to the Claroty CTD EMC. The default value is 500 records per page.

</td></tr><tr><td>

sn\_clarotyctdsgc.pagesize.program

</td><td>

Property to set the number of program records to fetch in a paginated REST call to the Claroty CTD EMC. The default value is 500 records per page.

</td></tr><tr><td>

sn\_clarotyctdsgc.api\_token\_life\_in\_minutes

</td><td>

Property to set the number of minutes that the API is considered active. After the time expires, the Service Graph Connector fetches a new API key during the next import. The default value is 0 and a new token is fetched for each REST call.

 **Note:** You can change the value to keep the same token for a maximum of 24 hours and reduce the number of REST calls.

</td></tr><tr><td>

sn\_clarotyctdsgc.classify\_based\_on\_os

</td><td>

Property to provide a list of classes that support the classification by OS as part of the Service Graph Connector Integration for Claroty CTD. When the flag is set to **True**, the classification by OS is supported. When it is set to **False**, the Service Graph Connector no longer classifies by OS. For example:

```
{ "cmdb_ci_ip_switch":true, 
"cmdb_ci_nids":false }
```

</td></tr><tr><td>

sn\_clarotyctdsgc.filter.asset\_type\_code

</td><td>

Property to provide a list of codes for device types separated by the delimiter \($\).For more information about Claroty types and codes, see [CMDB classes targeted](../reference/sgc-claroty-ctd-classes.md). For example, to only import PLC and HMI device types, enter the Claroty type code as `0$1`.

</td></tr><tr><td>

sn\_clarotyctdsgc.filter.asset\_purdue\_level

</td><td>

Property to provide a list of Purdue Levels separated by the delimiter \($\). For example, to only filter devices with Purdue Levels 1 and 2, To only filter Devices with Purdue Level 1 &amp; 2, set the value as `1.0$2.0`.

</td></tr></tbody>
</table>    3.  Select **Save**.

9.  To import CTD sites, complete the following:

    1.  In the Configure CTD Sites section, select the Import CTD Sites task.

    2.  Select **Configure**.

    3.  Select the **Execute Now** button.

10. To configure Network Intrusion Detection Systems \(NIDS\), complete the following:

    1.  In the Configure CTD Sites section, select the Configure NIDS task.

    2.  Select **Mark as Complete** once you setup the NIDS used to get devices from Claroty CTD.

11. To configure the import schedules to run the sites, devices, baselines, and installed programs, complete the following:

    **Note:** Empty rack slots associated with a PLC are no longer imported into the Configuration Management Database \(CMDB\).

    1.  In the Configure Import Schedules section, select the Configure Sites Import Schedule task.

    2.  Select **Configure**.

    3.  In the Scheduled Data Imports table, select **SG-OT CTD Sites Scheduled Import**.

        -   By default, the sites import schedule is configured to run every day at midnight.
        -   You must import and validate the CTD sites before you import the devices.
    4.  Complete the following actions as needed to review or change the import schedule as needed:

<table id="table_if3_lwk_3yb"><thead><tr><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enter a conditional script

</td><td>

Enter a conditional script that determines whether a scheduled import should run by selecting **Conditional**.

</td></tr><tr><td>

Change the default import schedule

</td><td>

Change the default import schedule by setting the **Run** field as necessary.

</td></tr><tr><td>

Reference a user in the Users table

</td><td>

Reference a user in the Users table by selecting a user in the **Runs as** field.

 **Note:** By default, this field is set to System Administrator. The selected user must be assigned the admin role for the import to be successful. If left empty, the import schedule uses the roles of the logged-in user.

</td></tr><tr><td>

Run an import

</td><td>

Run an import by selecting Execute Now. You can import either all records or only new records since the start time of the last successful import, based on the system properties configured. For more information, see [Configure guided setup](configuring-sgc-claroty-ctd-guided-setup.md).

</td></tr><tr><td>

Activate the import

</td><td>

Activate the import by selecting the **Active** check box.

</td></tr><tr><td>

Save any schedule changes

</td><td>

Save any schedule changes by selecting **Update**.

</td></tr></tbody>
</table>    5.  In the Configure Import Schedules section, select the Configure Devices Import Schedule task.

    6.  Select **Configure**.

    7.  In the Scheduled Data Imports table, select **SG-OT CTD Devices Scheduled Import** to review or change the import schedule for your devices.

        -   By default, the devices import schedule is configured to run every day at midnight.
        -   Devices are queried by the CTD site. The Service Graph Connector only queries for devices that are detected by validated CTD sites.
    8.  Complete the following actions as needed to review or change the import schedule as needed:

<table id="table_vzc_3zk_3yb"><thead><tr><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enter a conditional script

</td><td>

Enter a conditional script that determines whether a scheduled import should run by selecting **Conditional**.

</td></tr><tr><td>

Change the default import schedule

</td><td>

Change the default import schedule by setting the **Run** field as necessary.

</td></tr><tr><td>

Reference a user in the Users table

</td><td>

Reference a user in the Users table by selecting a user in the **Runs as** field.

 **Note:** By default, this field is set to System Administrator. The selected user must be assigned the admin role for the import to be successful. If left empty, the import schedule uses the roles of the logged-in user.

</td></tr><tr><td>

Run an import

</td><td>

Run an import by selecting Execute Now. You can import either all records or only new records since the start time of the last successful import, based on the system properties configured. For more information, see [Configure guided setup](configuring-sgc-claroty-ctd-guided-setup.md).

</td></tr><tr><td>

Activate the import

</td><td>

Activate the import by selecting the **Active** check box.

</td></tr><tr><td>

Save any schedule changes

</td><td>

Save any schedule changes by selecting **Update**.

</td></tr></tbody>
</table>    9.  In the Configure Import Schedules section, select the Configure Baselines Import Schedule task.

    10. Select **Configure**.

    11. In the Scheduled Data Imports table, select **SG-OT CTD Baselines Scheduled Import** to review or change the import schedule for the baselines.

        By default, the baselines import schedule is configured to run after the parent OT Control System runs.

    12. Complete the following actions as needed to review or change the import schedule as needed.

<table id="table_qs5_21l_3yb"><thead><tr><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enter a conditional script

</td><td>

Enter a conditional script that determines whether a scheduled import should run by selecting **Conditional**.

</td></tr><tr><td>

Change the default import schedule

</td><td>

Change the default import schedule by setting the **Run** field as necessary.

</td></tr><tr><td>

Reference a user in the Users table

</td><td>

Reference a user in the Users table by selecting a user in the **Runs as** field.

 **Note:** By default, this field is set to System Administrator. The selected user must be assigned the admin role for the import to be successful. If left empty, the import schedule uses the roles of the logged-in user.

</td></tr><tr><td>

Run an import

</td><td>

Run an import by selecting Execute Now. You can import either all records or only new records since the start time of the last successful import, based on the system properties configured. For more information, see [Configure guided setup](configuring-sgc-claroty-ctd-guided-setup.md).

</td></tr><tr><td>

Activate the import

</td><td>

Activate the import by selecting the **Active** check box.

</td></tr><tr><td>

Save any schedule changes

</td><td>

Save any schedule changes by selecting **Update**.

</td></tr></tbody>
</table>    13. In the Configure Import Schedules section, select the Configure Sites Installed Programs Import Schedule task.

    14. Select **Configure**.

    15. In the Scheduled Data Imports table, select **SG-OT CTD Installed Programs Scheduled Import** to review or change the schedule for the installed programs import.

        By default, the installed programs import schedule is configured to run every day at midnight.

    16. Complete the following actions as needed to review or change the import schedule as needed.

<table id="table_dbf_t1l_3yb"><thead><tr><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enter a conditional script

</td><td>

Change the default import schedule by setting the **Run** field as necessary.

</td></tr><tr><td>

Change the default import schedule

</td><td>

Change the default import schedule by setting the **Run** field as necessary.

</td></tr><tr><td>

Reference a user in the Users table

</td><td>

Reference a user in the Users table by selecting a user in the **Runs as** field.

 **Note:** By default, this field is set to System Administrator. The selected user must be assigned the admin role for the import to be successful. If left empty, the import schedule uses the roles of the logged-in user.

</td></tr><tr><td>

Run an import

</td><td>

Run an import by selecting Execute Now. You can import either all records or only new records since the start time of the last successful import, based on the system properties configured. For more information, see step 7c.

</td></tr><tr><td>

Activate the import

</td><td>

Activate the import by selecting the **Active** check box.

</td></tr><tr><td>

Save any schedule changes

</td><td>

Save any schedule changes by selecting **Update**.

</td></tr></tbody>
</table>12. When configuration items \(CIs\) are created in the CMDB, asset records are created.

    The asset record contains the model category of the CI. For more information about the model categories for Operational Technology \(OT\), see [Model categories for Operational Technology](../reference/model-categories-for-ot.md). To view the model category for an OT device, complete the following:

    1.  Navigate to **All** &gt; **Operational Technology \(OT\)** &gt; **All OT Devices**.
    2.  Select the OT device that you want to view the asset record for.
    3.  Next to the **Asset** field, select the **Preview this record** \(![Preview this record icon](../image/preview-record-icon.png)\) icon.
    4.  Select **Open Record**.
13. To troubleshoot the Service Graph Connector Integration for Claroty CTD, complete the following:

    1.  Select the \[OPTIONAL\] Troubleshooting the Service Graph Connector for Claroty CTD section.

    2.  In the Execute the validations scheduled job task, select **Configure**.

    3.  Select **Execute Now**.

        This job performs tasks to validate the configurations for SGC and the connection to Claroty CTD. If configuration issues are found, the validation results report the problem and suggest troubleshooting steps. Wait for the scheduled job to finish.

    4.  Once the scheduled job is complete, navigate back to the \[OPTIONAL\] Troubleshooting the Service Graph Connector for Claroty CTD section.

    5.  In the Review validation results task, select **Configure**.

        This step opens the execution logs and suggestions of the last troubleshooting run for you to view.

    6.  Address the suggestions as needed.

        **Note:** You can use the scheduled script at any point after the initial configuration of the Service Graph Connector Integration for Claroty CTD. To trigger validations, navigate to **All** &gt; **Service Graph Connector for Claroty CTD** &gt; **Troubleshooting** &gt; **Run Troubleshooting**. To view the validation results, navigate to **All** &gt; **Service Graph Connector for Claroty CTD** &gt; **Troubleshooting** &gt; **Results**.

        For additional information about troubleshooting issues while using the Service Graph Connector Integration for Claroty CTD, see [Troubleshooting scenarios for the Service Graph Connector Integration for Claroty CTD \(KB1502041\)](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1502041).


**Parent Topic:**[Service Graph Connector Integration for Claroty CTD](../concept/sgc-cmdb-integration-claroty-ctd.md)

