---
title: Configure Service Graph Connector for Google Console
description: Set up scheduled import jobs to pull in Chromebook device data from the Google Console into your CMDB.
locale: en-US
release: yokohama
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 9
breadcrumb: [Google Console, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure Service Graph Connector for Google Console

Set up scheduled import jobs to pull in Chromebook device data from the Google Console into your CMDB.

## Before you begin

To use this Service Graph Connector, you need a subscription to a Subscription Unit that is based in the IT Operations Management \(ITOM\) Visibility application or in the ITOM Discovery application. As defined in the section titled "Managed IT Resource Types" in [ServiceNow Subscription Unit Overview](https://www.servicenow.com/products/entitlements-packages.html) for your subscription, for managed IT resources that are created or modified in the CMDB by this Service Graph Connector, but that aren’t yet managed by [ITOM Visibility or ITOM Discovery](https://www.servicenow.com/docs/access?context=itom-license-module&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US), these resources will increase Subscription Unit consumption from that application. Review your current Subscription Unit consumption within ITOM Visibility or ITOM Discovery to ensure available capacity.

Dependencies and requirements:

-   The Integration Commons for CMDB store app, which is automatically installed. See [Integration Commons for CMDB](../concept/integration-commons-for-cmdb.md).
-   The CMDB CI class models store app, which is automatically installed. See [CMDB CI Class Models](../concept/cmdb-ci-class-models.md).
-   ITOM Licensing plugin \(com.snc.itom.license\). See [Request Discovery](https://www.servicenow.com/docs/access?context=t_ActivateTheDiscoveryPlugin&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US).

Role required: admin

## Procedure

1.  Verify that the application scope is set to the Service Graph Connector for Google Console application by using the application picker.

    For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

2.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **Google Console** &gt; **Setup**.

3.  On the Service Graph Connector for Google Console page, verify that the **Quick Start** option is selected and then select **Continue**.

4.  Configure the authentication credentials to send requests to the Google Console API.

    1.  In the Configure the Connection and Credentials section of the Service Graph Connector for Google Console page, select **Start**.

    2.  Set up the Google Console environment.

        1.  Select the Google Console Setup Instructions task.
        2.  Select the link to the [Service Graph connector for Google Console - Setup Instructions \[KB1516892\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB1516892) article in the Now Support Knowledge Base and follow the instructions to set up the Google Console environment.

            **Note:** Make a note of the destination keystore password. You need to specify this password while importing the Java Keystore \(JKS\) certificate into the Service Graph Connector for Google Console application.

        3.  Set the Google Console Setup Instructions task to complete by selecting the **Mark as complete** check box and then select **Continue**.
    3.  Create an X.509 certificate to associate the JKS certificate for the Google Console application with the Service Graph Connector for Google Console.

        1.  Select the Create X.509 certificate task.
        2.  In the X.509 Certificates list, select **New**.
        3.  On the form, fill in the fields.

            |Field|Description|
            |-----|-----------|
            |Name|Name of the X.509 certificate. For example, `SG-GoogleConsole-509Certificate`.|
            |Type|Certificate container. Select **Java Key Store**.|
            |Key store password|Password to access the JKS certificate as noted down in the [previous step](sgc-config-google-console-integ.md#keystorepwd).|

            **Note:** You can leave the value of other fields as-is.

        4.  Select the manage attachments icon \(![Manage Attachments icon.](../../../common/image/AttachmentIcon.png)\).
        5.  Select **Choose file** to browse and upload the keystore.p12 file for the JKS certificate you created in the [previous step](sgc-config-google-console-integ.md#keystorepwd).
        6.  Close the dialog box.
        7.  Select the **Validate Stores/Certificates** related link.
        8.  On successful validation, select **Update** to return to the guided setup page.
        9.  Set the Create X.509 certificate task to complete by selecting the **Mark as complete** check box and then select **Continue**.
    4.  Configure the connection.

        1.  Verify that the application scope is set to the Service Graph Connector for Google Console application by using the application picker.
        2.  Select the Configure the Connection task and then select **Click Here**.
        3.  On the Connections page that opens in another browser tab, select **Edit** for the **SG-GoogleConsole** connection that is available by default.
        4.  On the form, fill in the fields.

<table id="table_zhs_djn_21c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name to identify the connection record. For example, `SG-GoogleConsole`.Don’t modify the name for the default connection alias `SG-GoogleConsole`.

</td></tr><tr><td>

Service Account Email

</td><td>

Email address of the service account in Google Console.

</td></tr><tr><td>

Keystore Password

</td><td>

The password that you used when you created the JKS file in the [previous step](sgc-config-google-console-integ.md#keystorepwd).

</td></tr><tr><td>

Keystore

</td><td>

Select the name of the JKS file you created in the [previous step](sgc-config-google-console-integ.md#keystorepwd).

</td></tr></tbody>
</table>        5.  Select **Edit and Get OAuth Token**.
        6.  After the OAuth token is generated, return to the guided setup.
        7.  Set the Configure the Connection task to complete by selecting the **Mark as complete** check box and then select **Continue**.
    5.  Set up the configuration properties.

        1.  Select the Add configuration properties task.
        2.  In the Service Graph Connections section, review and modify the property details by selecting a property from the **Property** column in the Service Graph Connection Properties related list.

            You can configure the **Customer ID** property to pull Chromebook devices for the specified customer ID.

        3.  Select **Update** in the Service Graph Connection Properties section.
        4.  Set the Add connection properties task to complete by selecting the **Mark as complete** check box and then select **Continue**.
    6.  Test the Google Console API connection to import data from the Google Console application.

        1.  Select the Test Connection task.
        2.  Test the connection by selecting the **Test Connection** related link.

            Testing the connection might take a few moments. The page is refreshed to show the test results.

        3.  When the **Status** field is set to **Success**, select **Update**.

            If any of the tests have errors, follow the suggestions for remediation.

        4.  Set the Test Connection task to complete by selecting the **Mark as complete** check box and then select **Continue**.
5.  Integrate with multiple Google Console instances.

    1.  Follow the instructions in the [Service Graph connector for Google Console - Setup Instructions \[KB1516892\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB1516892) article in the Now Support Knowledge Base to set up the Google Console environment.

        **Note:** Make a note of the destination keystore password.

    2.  In the Add Multiple Instances section of the Service Graph Connector for Google Console page, select **Start**.

    3.  Create data sources for the new Google Console connection.

        1.  Ensure that you have edit permissions for the Datasource \[sys\_data\_source\] table.
        2.  Select the Update Data Source Access task.
        3.  To edit the record, select the **Global** application scope from the application picker.
        4.  In the Application Access related list of the Data Source form that opens in a new tab, select the **Can create**, **Can update**, and **Can delete** check boxes.
        5.  Select **Update**.
        6.  From the application picker, select the Service Graph Connector for Google Console application scope.
        7.  Set the Update Data Source Access task to complete by selecting the **Mark as complete** check box and then select **Continue**.
    4.  Create a scheduled import job for the new Google Console connection.

        1.  Ensure that you have edit permissions for the Scheduled data import \[scheduled\_import\_set\] table.
        2.  Select the Update Scheduled Data Import task.
        3.  To edit the record, select the **Global** application scope from the application picker.
        4.  In the Application Access related list of the Scheduled Data Import form, select the **Can create**, **Can update**, and **Can delete** check boxes.
        5.  Select **Update**.
        6.  From the application picker, select the Service Graph Connector for Google Console application scope.
        7.  Set the Update Scheduled Data Import task to complete by selecting the **Mark as complete** check box and then select **Continue**.
    5.  Create an X.509 certificate for the new Google Console instance by repeating the step [4.c](sgc-config-google-console-integ.md#x509cert), and then mark the Create X.509 certificate task to complete by selecting the **Mark as complete** check box and then select **Continue**.

    6.  Add another connection for the new Google Console instance.

        1.  Verify that the application scope is set to the Service Graph Connector for Google Console application by using the application picker.
        2.  Select the Add Another Connection task and then select **Click Here**.
        3.  On the Connections page that opens in another browser tab, select **Add Connection**.
        4.  On the form, fill in the fields.

            |Field|Description|
            |-----|-----------|
            |Connection Name|Name to identify the connection record.|
            |Service Account Email|Email address of the service account in Google Console.|
            |Keystore Password|The password that you used when you created the JKS file in the [previous step](sgc-config-google-console-integ.md#keystorepwd-multiple).|
            |Keystore|Select the name of the JKS file you created in the [previous step](sgc-config-google-console-integ.md#keystorepwd-multiple).|

        5.  Select **Create and Get OAuth Token**.
        6.  After the OAuth token is generated, return to the guided setup.
        7.  Set the Add Another Connection task to complete by selecting the **Mark as complete** check box and then select **Continue**.
    7.  Add the configuration properties for the new Google Console instance.

        1.  Select the Add configuration properties task.
        2.  Select the connection record you created in the [previous step](sgc-config-google-console-integ.md#connection-name).
        3.  In the Service Graph Connections section, review and modify the property details by selecting a property from the **Property** column in the Service Graph Connection Properties related list.

            You can configure the **Customer ID** property to pull Chromebook devices for the specified customer ID.

        4.  Select **Update** in the Service Graph Connection Properties section.
        5.  Set the Add connection properties task to complete by selecting the **Mark as complete** check box and then select **Continue**.
    8.  Test the Google Console API connection to import data from new Google Console instance.

        1.  Select the Test New Connections task.
        2.  Select the connection record you created in the [previous step](sgc-config-google-console-integ.md#connection-name).
        3.  Test the connection by selecting the **Test Connection** related link.

            Testing the connection might take a few moments. The page is refreshed to show the test results.

        4.  When the **Status** field is set to **Success**, select **Update**.

            If any of the tests have errors, follow the suggestions for remediation.

        5.  Set the Test New Connections task to complete by selecting the **Mark as complete** check box and then select **Continue**.
6.  Configure the scheduled job for the import of Google Console data.

    1.  In the Configure the scheduled jobs section of the Service Graph Connector for Google Console page, select **Start**.

    2.  Select the **SG-GoogleConsole-ChromeDevices** scheduled job.

        For a multiple instance setup, select the scheduled job created with the scheduled import in step [5.d](sgc-config-google-console-integ.md#scheduled-import-multi-instance) for the new connection.

    3.  On the Scheduled Data Import form, verify the field values.

        For more information, see [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US#table_r53_5hm_xp).

    4.  Select the **Active** check box to activate the scheduled job.

    5.  In the **Run** field, select **Periodically** to specify how often the job will run.

    6.  Select **Update**.

    7.  Set the Configure the scheduled jobs task to complete by selecting the **Mark as complete** check box and then select **Continue**.

7.  On the Service Graph Connector for Google Console page, select **Complete** to save your changes.

8.  In the Complete setup dialog box, select **Complete** to complete the setup.

9.  In the message box that appears, select **Done**.


