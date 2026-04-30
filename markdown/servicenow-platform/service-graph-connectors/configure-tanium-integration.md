---
title: Configure Service Graph Connector for Tanium using the guided setup
description: Set up scheduled import jobs to pull in data from Tanium into your Configuration Management Database \(CMDB\).
locale: en-US
release: xanadu
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2025-12-09"
reading_time_minutes: 10
breadcrumb: [Tanium, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure Service Graph Connector for Tanium using the guided setup

Set up scheduled import jobs to pull in data from Tanium into your Configuration Management Database \(CMDB\).

## Before you begin

**Important:** Unless there are configuration issues, use SGC Central to configure the connection. The guided setup method for configuration is being deprecated.

To use this Service Graph Connector, you need a subscription to a Subscription Unit that is based in the IT Operations Management \(ITOM\) Visibility application or in the ITOM Discovery application. As defined in the section titled "Managed IT Resource Types" in [ServiceNow Subscription Unit Overview](https://www.servicenow.com/products/entitlements-packages.html) for your subscription, for managed IT resources that are created or modified in the CMDB by this Service Graph Connector, but that aren’t yet managed by [ITOM Visibility or ITOM Discovery](https://www.servicenow.com/docs/access?context=itom-license-module&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US), these resources will increase Subscription Unit consumption from that application. Review your current Subscription Unit consumption within ITOM Visibility or ITOM Discovery to ensure available capacity.

Dependencies and requirements:

-   The [Integration Commons for CMDB](../concept/integration-commons-for-cmdb.md) store app, which is automatically installed.
-   The CMDB CI class models store app, which is automatically installed. See [CMDB CI Class Models](../concept/cmdb-ci-class-models.md).
-   The Datastream Action plugin \(com.glide.hub.action\_type.datastream\), which is automatically installed.

**Note:** If you have an earlier version of the Service Graph Connector for Tanium, then do not migrate data from the old connector. You must uninstall the previous version and run the new integration.

Role required: admin

## About this task

For more information on the Service Graph Connector for Tanium setup, see [How do I configure the Tanium Service Graph Connector?](https://www.servicenow.com/community/cmdb-articles/tanium-service-graph-connector/ta-p/2754467) article on the ServiceNow Community site.

## Procedure

1.  Ensure that the application scope is set to the Service Graph Connector for Tanium application by using the application picker.

    For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

2.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **Tanium** &gt; **Setup**.

3.  On the Getting started page, select **Get Started**.

4.  Configure the authentication credentials and HTTP connection.

    1.  On the Service Graph Connector for Tanium page, in the Configure the Connection and Credentials section, select **Set authentication type**.

    2.  For the Set authentication type task, select **Configure**.

    3.  Specify the system property details for the authentication type.

        1.  In the **Value** field, enable either token-based authentication or basic authentication.

            -   To enable the basic authorization, enter `basic`.
            -   To enable the token-based authorization, enter `token`.
            **Note:** Tanium Platform 7.6.2 supports only token-based authorization for an on-premise setup. To use Tanium Platform 7.6.2 or later versions, enable the token-based authorization type and enter the details for the token-based authorization in the next step.

        2.  Select **Update**.
        3.  Set the Set authentication type task to complete by selecting **Mark as Complete**.
    4.  Configure the connection based on the authentication type.

        1.  For the basic authorization type:
            1.  For the Configure the Basic auth Credentials task, select **Configure**.

                **Note:** The Configure the Basic auth Credentials task appears only when you have specified `basic` as the value in the step [4.c.i](configure-tanium-integration.md#step-value).

            2.  Select **Edit** for Basic authentication within the sn\_tanium\_integ scope.
            3.  In the Connection Information section of the Edit Connection window, fill in the fields.

<table id="table_d3y_j5s_bdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection name

</td><td>

Name to identify the Tanium connection record.`Token-based authentication` is the default credential alias name and is read-only.

</td></tr><tr><td>

Host name

</td><td>

Base URL or IP address of the Tanium server.**Note:** This field is automatically set to the URL to connect to the application. Leave the field value as is.

</td></tr></tbody>
</table>            4.  \(Optional\) If a MID Server is required for the Tanium server connection, select the **Use MID Server** check box. Then, select the MID Server-related fields accordingly.
            5.  In the Credential Information section, enter the Tanium account user name in the **Username** field and the password in the **Password** field.
            6.  Select **Edit connection**.
            7.  Return to the guided setup page.
            8.  Set the Configure the Basic auth Credentials task to complete by selecting **Mark as Complete**.
        2.  For the token-based authorization type:
            1.  For the Configure the Token auth Credentials task, select **Configure**.

                **Note:** The Configure the Token auth Credentials task appears only when you have specified `token` as the value in the step [4.c.i](configure-tanium-integration.md#step-value).

            2.  Select **Edit** for Token-based authentication within the sn\_tanium\_integ scope.
            3.  In the Connection Information section of the Edit Connection window, fill in the fields.

<table id="table_uwz_zjg_3cc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection name

</td><td>

Name to identify the Tanium connection record.`Token-based authentication` is the default credential alias name and is read-only.

</td></tr><tr><td>

Host name

</td><td>

Tanium base URL or IP address. **Note:** This field is automatically set to the URL to connect to the application. Leave the field value as is.

</td></tr></tbody>
</table>            4.  \(Optional\) If a MID Server is required for the Tanium server connection, select the **Use MID Server** check box. Then, select the MID Server-related fields accordingly.
            5.  In the Credential Information section of the Edit Connection window, enter the authentication token for the Tanium API in the **Token** field to grants access to Tanium data.
            6.  Select **Edit connection**.
            7.  Return to the guided setup page.
            8.  Set the Configure the Token auth Credentials task to complete by selecting **Mark as Complete**.
    5.  Test the connection.

        1.  For the Test connection task, select **Configure**.
        2.  Select the **Test Connection** related link to start the testing process.
        3.  When the **Status** field is set to **Success**, return to the guided setup page.

            **Note:** If any of the tests have errors, follow the suggestions for remediation.

        4.  Set the Test the connection task to complete by selecting **Mark as Complete**.
    6.  Create a custom view.

        **Note:** The integration depends on a custom view from Tanium.

        1.  Configure the view on your Tanium instance.
            1.  On your Tanium instance, navigate to **Modules** &gt; **Asset**.
            2.  Select **Views**.
            3.  If you have not done so already, create the ServiceNow \(reserved\) view by selecting **Create View** &gt; **Create ServiceNow view**.

                **Note:** By default, the ServiceNow \(reserved\) view is non-editable.

            4.  Create a copy of the view to edit it.
            5.  Edit the copy.
                1.  Add all fields from the **SIU Product Usage** bucket.
                2.  Add **Asset** to the **Last Seen** field.
                3.  Add **Network Adapter** to the **Model** field.
            6.  Save the view.
        2.  Select the view on your ServiceNow instance.
            1.  In the guided setup, for the Configure the View task, select **Configure**.
            2.  In the ServiceNow instance, select the view you created in step [4.f.i](configure-tanium-integration.md#config-view).
            3.  Select **Set View**.
            4.  Set the Configure the View task to complete by selecting **Mark as Complete**.
    7.  In the ADM setup instruction section, ignore the instructions as application dependency mapping is not supported currently.

5.  Configure the Tanium scheduled jobs.

    1.  For the Configure the Scheduled Import task, select **Configure**.

    2.  Select the scheduled job that you want to activate.

    3.  On the Scheduled Data Import form, verify the field values for a scheduled job and select the **Active** check box to activate the scheduled job.

        **Note:** When using a token-based authentication, the user you specify in the **Run as** field for a scheduled job must have the connection\_admin role.

        For more information, see [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US#table_r53_5hm_xp).

    4.  Select **Update**.

    5.  Repeat the steps [5.b](configure-tanium-integration.md#select-job) to [5.d](configure-tanium-integration.md#exe-job) for each scheduled job for data import.

    6.  Set the Configure the Scheduled Import task to complete by selecting **Mark as Complete**.

6.  Add multiple instances.

    **Note:** If you don't need to add multiple instances, you can skip this step.

    1.  On the Service Graph Connector for Tanium page, in the Add Multiple Icons section, select the **Update Data Source Access** task.

    2.  On the next page, in the Update Data Source Access section, select **Configure**.

    3.  Select the Data Source \[sys\_data\_source\] table.

    4.  Select the **Global** application scope by using the application picker.

    5.  In the Application Access related list, select the **Can create**, **Can update**, and **Can delete** check boxes, if not already selected.

    6.  Select **Update** to close the tab and return to the guided setup.

    7.  Modify the application scope again to **Service Graph Connector for Tanium** by using the application picker.

    8.  Set the Update Data Source Access task to complete by selecting **Mark as Complete**.

    9.  Repeat the steps [6.d](configure-tanium-integration.md#global) to [6.g](configure-tanium-integration.md#app) for the Update Scheduled data import access task with the Scheduled data import \[scheduled\_data\_set\] table and set the task to complete by selecting **Mark as Complete**.

    1.  Clear the cache for the new connection.

        1.  For the Clear Cache for Datasource and Import set task, select **Configure**.
        2.  In the **Run script** text box of the background script page, enter the following script:

            ```
            GlideTableManager.invalidateTable("sys_data_source");
                  GlideCacheManager.flushTable("sys_data_source");
            
                  GlideTableManager.invalidateTable("scheduled_import_set");
                  GlideCacheManager.flushTable("scheduled_import_set");
            
                  GlideTableManager.invalidateTable("sys_db_object");
                  GlideCacheManager.flushTable("sys_db_object");
            ```

        3.  Select **Run Script** to run the background script in the **global** scope.

            The script may take several minutes to execute.

        4.  After the script is executed, select **Close**.
        5.  From the application picker, select the **Service Graph Connector for Tanium** application.
        6.  Set the Clear Cache for Datasource and Import set task to complete by selecting **Mark as complete**.
    2.  Add a basic authorization connection to another Tanium instance.

        **Note:** Tanium Platform 7.6.2 supports only token-based authorization for an on-premise setup. To use Tanium Platform 7.6.2 or later versions, use the token-based authorization.

        1.  For the Add Another Basic Auth Connection task, select **Configure**.
        2.  To create a new connection, select **Add Connection**.
        3.  Enter the connection details on the Create Connection form.
        4.  Select **Create Connection**.
        5.  Navigate back to the guided setup and set the Add Another Basic Auth Connection task to complete by selecting **Mark as Complete**.
    3.  Add a token-based authorization connection to another Tanium instance.

        1.  For the Add Another Token Auth Connection task, select **Configure**.
        2.  To create a new connection, select **Add Connection**.
        3.  Enter the connection details on the Create Connection form.
        4.  Select **Create Connection**.
        5.  Navigate back to the guided setup and set the Add Another Token Auth Connection task to complete by selecting **Mark as Complete**.
    4.  Set configuration properties for newly added connections.

        1.  For the Set configuration properties task, select **Configure**.
        2.  From the **Name** column, select the new connection.
        3.  In the Service Graph Connection Properties related list, review and modify the following properties.

            |Field|Value|
            |-----|-----|
            |max\_retry\_count|Determines the number of retry attempts triggered for a Tanium Asset REST action in case of failure.|
            |pagination\_record\_count|Specifies the page size for each API call made during a Tanium Application Data REST action.|
            |rest\_action\_limit|Specifies the page size for each API call made during a Tanium Asset REST action.|
            |view\_id|Specifies the identifier used to fetch hardware and software data from a specific Tanium view. To modify the view identifier, access the SG Tanium Connection \[sn\_tanium\_integ\_connection\] table.|

        4.  Return to the guided setup page.
        5.  Set the Set configuration properties task to complete by selecting **Mark as Complete**.
    5.  Test the newly added connections.

        1.  For the Test connections task, select **Configure**.
        2.  From the **Name** column, select the new connection.
        3.  Select the **Test Connection** related link to start the testing process.
        4.  When the **Status** field is set to **Success**, return to the guided setup page.

            **Note:** If any of the tests have errors, follow the suggestions for remediation.

        5.  Set the Test connections task to complete by selecting **Mark as Complete**.
    6.  Set the Tanium view for the connection.

        1.  For the Set view task, select **Configure**.
        2.  In the **Connection and Credentials Alias** field, search for and select the alias created earlier in the Add Another Basic Auth Connection or Add Another Token Auth Connection task.
        3.  In the **View** field, search for and select the corresponding Tanium view associated with the connection.
        4.  Select **Set View**.
        5.  Set the Set view task to complete by selecting **Mark as Complete**.
    7.  Skip the ADM setup for multi instance task as ADM is not supported currently.

    8.  Configure the Tanium scheduled job.

        1.  For the Configure the Scheduled Imports task, select **Configure**.
        2.  Select the scheduled data import that you want to activate.
        3.  On the Scheduled Data Import form, verify the field values for the scheduled job and select the **Active** check box.

            **Note:** When using a token-based authentication, the user you specify in the **Run as** field for a scheduled job must have the connection\_admin role.

            For more information, see [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US#table_r53_5hm_xp).

        4.  Select **Update**.
        5.  Repeat steps [6.h.ii](configure-tanium-integration.md#select-job-2) to [6.h.iv](configure-tanium-integration.md#exe-job-2) for each scheduled job for data import.
        6.  Set the Configure the Scheduled Imports task to complete by selecting **Mark as Complete**.
7.  Use the advanced settings to manage excluding the serial number population on the IBM AIX and Oracle Solaris operating system \(OS\) platforms.

    1.  In the Advanced section of the guided setup, for the Advanced Settings task, select **Configure**.

    2.  To exclude the serial number population, enter `false` in the **Exclude the serial number population** field.

    3.  Select **Save**.

    4.  Close the window and set the Advanced Settings task to complete by selecting **Mark as Complete**.


