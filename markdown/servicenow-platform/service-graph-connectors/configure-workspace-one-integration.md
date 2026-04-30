---
title: Configure Service Graph Connector for VMware Workspace ONE UEM
description: Use the Service Graph Connector for VMware Workspace ONE UEM to pull mobile and computing devices data from VMware Workspace ONE Unified Endpoint Management \(UEM\) into your ServiceNow instance.
locale: en-US
release: xanadu
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2026-03-01"
reading_time_minutes: 11
breadcrumb: [VMware Workspace ONE UEM, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure Service Graph Connector for VMware Workspace ONE UEM

Use the Service Graph Connector for VMware Workspace ONE UEM to pull mobile and computing devices data from VMware Workspace ONE Unified Endpoint Management \(UEM\) into your ServiceNow instance.

## Before you begin

To use this Service Graph Connector, you need a subscription to a Subscription Unit that is based in the IT Operations Management \(ITOM\) Visibility application or in the ITOM Discovery application. As defined in the section titled "Managed IT Resource Types" in [ServiceNow Subscription Unit Overview](https://www.servicenow.com/products/entitlements-packages.html) for your subscription, for managed IT resources that are created or modified in the CMDB by this Service Graph Connector, but that aren’t yet managed by [ITOM Visibility or ITOM Discovery](https://www.servicenow.com/docs/access?context=itom-license-module&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US), these resources will increase Subscription Unit consumption from that application. Review your current Subscription Unit consumption within ITOM Visibility or ITOM Discovery to ensure available capacity.

Dependencies and requirements:

-   The [Integration Commons for CMDB](../concept/integration-commons-for-cmdb.md) store app, which is automatically installed.
-   The CMDB CI class models store app, which is automatically installed. See [CMDB CI Class Models](../concept/cmdb-ci-class-models.md).
-   The ITOM Discovery License plugin \(com.snc.itom.discovery.license\). You must activate this plugin.
-   ITOM Licensing plugin \(com.snc.itom.license\). For more information, see [Request Discovery](https://www.servicenow.com/docs/access?context=t_ActivateTheDiscoveryPlugin&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US).
-   The Datastream Action plugin \(com.glide.hub.action\_type.datastream\), which is automatically installed.

Role required: SGC-Admin \(sn\_cmdb\_int\_util.sgc\_admin\) or admin

**Note:** The admin user role is required to run background scripts and to provide access to global tables to the SGC-Admin user. For information about the user roles for Service Graph Connectors, see [Service Graph Connector user roles](../concept/cmdb-sgc-intro.md#section_ett_spp_4hc).

When using client credentials for authentication, obtain the OAuth credentials from your VMware Workspace ONE UEM administrator. Make a note of the following details:

-   Application \(client\) ID
-   Client Secret
-   Token URL

For information about how to get OAuth credentials, see the [VMware documentation site](https://docs.vmware.com/en/VMware-Workspace-ONE-UEM/services/UEM_ConsoleBasics/GUID-BF20C949-5065-4DCF-889D-1E0151016B5A.html).

## About this task

To configure the Service Graph Connector for VMware Workspace ONE UEM, you must configure either OAuth authentication credentials or basic authentication credentials.

## Procedure

1.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **Workspace ONE UEM** &gt; **Setup**.

2.  On the Getting started page, select **Get Started**.

3.  In the Configure the Connection and Credentials section of the Service Graph Connector for VMware Workspace ONE UEM page, select **Get Started**.

4.  Configure authentication credentials for the connection.

    You can configure either a basic authentication connection or an OAuth connection.

    1.  For the Set authentication type task, select **Configure**.

        -   To enable basic authentication, set the value of the **auth\_type** connection property to `basic`.
        -   To enable OAuth authentication, set the value of the **auth\_type** connection property to `oauth`.
    2.  Select **Update**, and navigate back to the guided setup page.

    3.  Set the Set authentication type task to complete by selecting **Mark as Complete**.

5.  Configure the credentials for authentication.

    -   Configure a basic authentication connection.
        1.  For the Configure the Basic Auth Credentials task, select **Configure**.
        2.  On the form, fill in the fields.

<table id="table_vbr_lk1_bgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the authentication.For example, `WorkspaceOneUEM Basic Auth Credentials`.

</td></tr><tr><td>

User name

</td><td>

Your VMware Workspace ONE UEM user name.

</td></tr><tr><td>

Password

</td><td>

Your VMware Workspace ONE UEM password.

</td></tr></tbody>
</table>        3.  Select **Update**, and navigate back to the guided setup page.
        4.  Set the Configure the Basic Auth Credentials task to complete by selecting **Mark as Complete**.
        5.  For the Configure API key task, select **Configure** to configure an API key for the basic authentication connection.
        6.  In the **API Key** field, enter your VMware Workspace ONE UEM API key or tenant code.
        7.  Select **Update**, and navigate back to the guided setup page.
        8.  Set the Configure API key task to complete by selecting **Mark as Complete**.
    -   Configure an OAuth connection.
        1.  For the Configure the OAuth Credentials task, select **Configure**.
        2.  On the form, fill in the fields.

<table id="table_bbq_srm_bgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the authentication.For example, `WorkspaceOneUEM OAuth Provider`.

</td></tr><tr><td>

Client ID

</td><td>

Application \(client\) ID of your VMware Workspace ONE UEM client application as noted in the [Before you begin](configure-workspace-one-integration.md#prereq_np3_cv3_kqb) section.

</td></tr><tr><td>

Client Secret

</td><td>

Client secret of your VMware Workspace ONE UEM client application as noted in the [Before you begin](configure-workspace-one-integration.md#prereq_np3_cv3_kqb) section.

</td></tr></tbody>
</table>        3.  Select **Update**, and navigate back to the guided setup page.
        4.  Set the Configure the OAuth Credentials task to complete by selecting **Mark as Complete**.
6.  Establish an HTTP connection to send requests to the VMware Workspace ONE UEM API.

    1.  For the Configure HTTP connection task, select **Configure**.

    2.  On the HTTP\(s\) Connection form, specify the host name of your VMware Workspace ONE UEM instance in the **Host** field.

        **Note:** The HTTP connection is pre-configured to use the authentication credentials that were configured in steps [4](configure-workspace-one-integration.md#step_vdc_nfh_cgc) and [5](configure-workspace-one-integration.md#step_n4j_nfh_cgc).

    3.  Select **Update**.

    4.  Set the Configure HTTP Connection task to complete by selecting **Mark as Complete**.

7.  Test the connection.

    1.  For the Test the Connection task, select **Configure**.

    2.  Select the **Test Connection** related link to start the testing process.

    3.  When the **Status** field is set to **Success**, navigate back to the guided setup page.

        If any of the tests have errors, follow the suggestions for remediation.

    4.  Set the Test the Connection task to complete by selecting **Mark as Complete**.

8.  Set up the scheduled import job.

    1.  For the Configure the scheduled job task, select **Configure**.

        The SG-Workspace ONE UEM Devices and Apps scheduled job is set to inactive by default.

    2.  Select the **SG-Workspace ONE UEM Devices and Apps** scheduled job.

    3.  On the Scheduled Data Import form, verify the field values for the scheduled job.

        For more information, see [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US#table_r53_5hm_xp).

    4.  Select the **Active** check box to activate the SG-Workspace ONE UEM Devices and Apps scheduled job.

    5.  In the **Run** field, select **Periodically** to specify how often the job should run.

    6.  Select **Update**.

        Alternatively, select **Execute Now** to execute the import schedule immediately.

    7.  Set the Configure the scheduled job task to complete by selecting **Mark as Complete**.

9.  Add multiple instances.

    **Note:** If you don't need to add multiple instances, you can skip this step.

    1.  In the Add multiple instances section of the Service Graph Connector for VMware Workspace ONE UEM page, select **Get Started**.

    2.  For the Update scheduled data import access task, select **Configure**.

    3.  Select the Scheduled data import \[scheduled\_import\_set\] table.

    4.  Select the **Global** application scope by using the application picker.

    5.  In the Application Access related list, select the **Can create**, **Can update**, and **Can delete** check boxes, if not already selected.

    6.  Select **Update**, and then navigate back to the guided setup.

    7.  Modify the application scope again to **Service Graph Connector for VMware Workspace ONE UEM** by using the application picker.

    8.  Set the Update scheduled data import access task to complete by selecting **Mark as Complete**.

    9.  For the Update Data Source Access task, select **Configure**.

    10. Select the Data Source \[sys\_data\_source\] table.

    11. Repeat steps [9.d](configure-workspace-one-integration.md#substep_v4t_kfd_1gc) to [9.g](configure-workspace-one-integration.md#substep_mzy_kfd_1gc).

    12. Set the Update Data Source Access task to complete by selecting **Mark as Complete**.

    13. Clear the cache for the new connection.

        1.  For the Clear cache for Data Source and Import Set tables task, select **Configure**.
        2.  Select the **Global** application scope by using the application picker.
        3.  In the **Run script** text box of the background script page, enter the following script:

            ```
            GlideTableManager.invalidateTable("sys_data_source");      
                  GlideCacheManager.flushTable("sys_data_source");
                  GlideTableManager.invalidateTable("scheduled_import_set");      
                  GlideCacheManager.flushTable("scheduled_import_set");
                  GlideTableManager.invalidateTable("sys_db_object");      
                  GlideCacheManager.flushTable("sys_db_object");
            ```

        4.  Select **Run Script** to run the background script.

            The script may take several minutes to execute.

        5.  After the script is executed, select **Close**.
        6.  Modify the application scope again to **Service Graph Connector for VMware Workspace ONE UEM** by using the application picker.
        7.  Set the Clear cache for Data Source and Import Set tables task to complete by selecting **Mark as complete**.
    14. Configure the connection for the VMware Workspace ONE UEM instance.

        You can configure either a basic authentication connection or an OAuth connection.

        -   Configure a basic authentication connection.
            1.  For the Add basic authentication connection task, select **Configure**.
            2.  To create a new connection, select **Add Connection**.
            3.  In the Connection Information section of the Create Connection window, fill in the fields.

<table id="table_kzt_k3d_1gc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection name

</td><td>

Name to identify the VMware Workspace ONE UEM connection record.

</td></tr><tr><td>

Connection URL

</td><td>

Connection URL of your VMware Workspace ONE UEM connection.Use the format `https://*host-name*/API` for the connection URL.

</td></tr></tbody>
</table>            4.  In the Credential Information section of the Create Connection window, fill in the fields.

                |Field|Description|
                |-----|-----------|
                |Username|VMware Workspace ONE UEM account user name that is used to authenticate the connection request.|
                |Password|Password that is used to authenticate the connection request.|

            5.  Select **Create Connection**.
            6.  Navigate back to the guided setup, and set the Add basic authentication connection task to complete by selecting **Mark as Complete**.
            7.  For the Configure API key task, select **Configure** to configure an API key for the basic authentication connection.
            8.  Select the **API Key** record that corresponds to the connection alias for the new basic authentication connection.
            9.  Set the API key, and then select **Update**.
            10. Navigate back to the guided setup, and set the Configure API key task to complete by selecting **Mark as Complete**.
        -   Configure an OAuth connection.
            1.  For the Add an OAuth connection task, select **Configure**.
            2.  To create a new connection, select **Add Connection**.
            3.  In the Connection Information section of the Create Connection window, fill in the fields.

<table id="table_bzk_l3d_1gc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name to identify the VMware Workspace ONE UEM connection record.

</td></tr><tr><td>

Connection URL

</td><td>

Connection URL of your VMware Workspace ONE UEM controller.Use the format `https://*host-name*/API` for the connection URL.

</td></tr></tbody>
</table>            4.  In the Credential Information section of the Create Connection window, fill in the fields.

                |Field|Description|
                |-----|-----------|
                |OAuth Client ID|Application \(client\) ID of your VMware Workspace ONE UEM client application as noted in the [Before you begin](configure-workspace-one-integration.md#prereq_np3_cv3_kqb) section.|
                |OAuth Client Secret|Client secret of your VMware Workspace ONE UEM client application as noted in the [Before you begin](configure-workspace-one-integration.md#prereq_np3_cv3_kqb) section.|

                For information about how to get OAuth credentials, see the [VMware documentation site](https://docs.vmware.com/en/VMware-Workspace-ONE-UEM/services/UEM_ConsoleBasics/GUID-BF20C949-5065-4DCF-889D-1E0151016B5A.html).

            5.  Select **Create and Get OAuth Token**.
            6.  Navigate back to the guided setup, and set the Add an OAuth connection task to complete by selecting **Mark as Complete**.
    15. Test the newly added connections.

        1.  For the Test connections task, select **Configure**.
        2.  From the **Name** column, select the new connection.
        3.  Select the **Test Connection** related link to start the testing process.
        4.  When the **Status** field is set to **Success**, return to the guided setup page.

            **Note:** If any of the tests have errors, follow the suggestions for remediation.

        5.  Set the Test connections task to complete by selecting **Mark as Complete**.
    16. Configure the scheduled job to import data from the VMware Workspace ONE UEM application.

        The SG-Workspace ONE UEM Devices and Apps scheduled job is set to inactive by default.

        1.  For the Configure import schedule task, select **Configure**.
        2.  Select the **SG-Workspace ONE UEM Devices and Apps** scheduled job.
        3.  On the Scheduled Data Import form, verify the field values for the scheduled job.

            For more information, see [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US#table_r53_5hm_xp).

        4.  Select the **Active** check box to activate the SG-Workspace ONE UEM Devices and Apps scheduled job.
        5.  In the **Run** field, select **Periodically** to specify how often the job should run.
        6.  Select **Update**.

            Alternatively, select **Execute Now** to execute the import schedule immediately.

10. Configure additional settings.

    1.  In the Configure additional settings \(optional\) section of the Service Graph Connector for VMware Workspace ONE UEM page, select **Get Started**.

    2.  For the Configure duplicate detection rules task, select **Configure**.

    3.  On the CMDB Duplicate Row Rule form, select **Active**.

    4.  Update the Value field to `true` to activate the duplicate detection rule during data import.

    5.  Select **OK**, and navigate back to the guided setup.

    6.  To remove fields from being evaluated, add the field names as a comma-separated list in the Ignore Fields column on the CMDB Duplicate Row Rules form.

        Use this option for fields that change with every import.

    7.  Set the Configure duplicate detection rules task to complete by selecting **Mark as Complete**.

    8.  For the Enable software import task, select **Configure**.

    9.  Select the connection record for which you want to enable the import of software data.

        The **turn\_off\_software\_import** connection property is set to `true` by default.

    10. Set the **turn\_off\_software\_import** connection property value to `false` to import software data.

    11. Set the Enable software import task to complete by selecting **Mark as Complete**.

    12. For the Import non-managed software task, select **Configure**.

    13. Select the connection record for which you want to import non-managed software data.

        By default, software records that have the **IsManaged** field set to `false` aren't imported.

    14. Set the **managed\_apps\_only** connection property value to `false` to import non-managed software data.

    15. Set the Import non-managed software task to complete by selecting **Mark as Complete**.

    16. For the Import apps based on software status value task, select **Configure**.

        By default, the connector imports applications that have the status value `2`, `3`, or `5`.

        |Status|Value|
        |------|-----|
        |Pending Install|1|
        |Installed|2|
        |Pending Removal|3|
        |Removed|4|
        |Unknown|5|

    17. Select the connection record for which you want to update the set of imported applications.

    18. Set the **import\_apps\_with\_status** connection property value to the required software status values \(as a comma-separated list\).

    19. Set the Import apps based on software status value task to complete by selecting **Mark as Complete**.


