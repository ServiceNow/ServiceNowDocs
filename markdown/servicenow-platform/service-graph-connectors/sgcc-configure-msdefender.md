---
title: Configure Service Graph Connector for Microsoft Defender Endpoint using SGC Central
description: Set up scheduled import jobs to pull in Microsoft Defender for Endpoint data into your Configuration Management Database \(CMDB\).
locale: en-US
release: yokohama
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2026-03-06"
reading_time_minutes: 4
breadcrumb: [Microsoft Defender for Endpoint, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure Service Graph Connector for Microsoft Defender Endpoint using SGC Central

Set up scheduled import jobs to pull in Microsoft Defender for Endpoint data into your Configuration Management Database \(CMDB\).

## Before you begin

Complete the following tasks:

-   Install Service Graph Connector for Microsoft Defender Endpoint version 1.1.0 or later from the ServiceNow Store. For ServiceNow Store installation steps, see [Install a ServiceNow Store application](https://www.servicenow.com/docs/access?context=t_InstallApplications&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).
-   Verify that you have an active subscription to Microsoft Defender for Endpoint.
-   Verify that you have created an Azure application to get programmatic access to Microsoft Defender for Endpoint. See [Create an app to access Microsoft Defender for Endpoint without a user](https://learn.microsoft.com/en-us/defender-endpoint/api/exposed-apis-create-app-webapp?view=o365-worldwide) in the Microsoft 365 documentation.
-   Obtain the tenant ID, client ID, and client secret details for the Microsoft Defender for Endpoint administrator account.
-   Enable the Machine.Read.All and Machine.ReadWrite.All permissions in Microsoft Defender for Endpoint. See [Permissions](https://learn.microsoft.com/en-us/microsoft-365/security/defender-endpoint/api/get-machines?view=o365-worldwide#permissions) for the List machines API in the Microsoft 365 documentation.

Role required: The following table shows the roles required for each stage of the playbook.

|Stage|Role|
|-----|----|
|Prerequisites|admin|
|Setup|SGC-Admin \(sn\_cmdb\_int\_util.sgc\_admin\) or admin|

**Note:** The admin user role is required to run background scripts and to provide access to global tables to the SGC-Admin user. For information about the user roles for Service Graph Connectors, see [Service Graph Connector user roles](../../configuration-management/concept/cmdb-sgc-intro.md#section_ett_spp_4hc).

## About this task

The playbook experience for onboarding connectors is activated with SGC Central in the Service Graph Workspace or CMDB Workspace. To configure the SGC Central application, see [Configuring SGC Central](../concept/sgcc-configuring.md) and for more information on how to interact with a playbook, see [Interact with Playbook](https://www.servicenow.com/docs/access?context=playbook-ui&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

## Procedure

1.  Use one of the following methods to open SGC Central:

    -   Navigate to **Workspaces** &gt; **Service Graph Workspace**, and from the left navigation panel, select the Ingestion icon ![](../../configuration-management/image/icon-sgc-central.png) to open the SGC Central view.
    -   Navigate to **Workspaces** &gt; **CMDB Workspace** &gt; **SGC Central**.
2.  On the Overview page, select **Create connection**.

    **Tip:** Alternatively, you can select **Create connection** on the All connections page.

3.  On the Create connection window, select the Microsoft Defender connector type, and then select **Configure connection**.

    A default connection, SG Defender OAuth2.0 connection, for Microsoft Defender for Endpoint is available within the application. As the Service Graph Connector for Microsoft Defender Endpoint supports only a single instance, you can configure the default connection for the first time or resume editing it thereafter.

4.  Complete the initial prerequisites when setting up a connection for the first time using a connector.

    **Note:** This step is required only during the first-time setup. See [Perform initial setup tasks when creating a connection in SGC Central](sgcc-first-time-setup.md).

5.  Enter connection details and test the API connection for importing Microsoft Defender for Endpoint data.

    1.  In the **Setup** stage of the playbook, select the **Configure and test connection** activity.

    2.  On the form, fill in the fields.

<table id="table_ahn_xtg_rmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name to identify the Microsoft Defender for Endpoint connection record.**Note:** This field is automatically set to `SG Defender OAuth2.0 connection`. Leave the field value as is.

</td></tr><tr><td>

OAuth Client ID

</td><td>

Application \(client\) ID of your Microsoft Defender for Endpoint as described in the [Before you begin](sgcc-configure-msdefender.md#prereq_bbj_rbg_ndc) section.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Client Secret of your Microsoft Defender for Endpoint as described in the [Before you begin](sgcc-configure-msdefender.md#prereq_bbj_rbg_ndc) section.

</td></tr><tr><td>

OAuth token URL

</td><td>

Token URL of your Microsoft Defender for Endpoint.Enter the token URL in the following format:

```
https://login.microsoftonline.com/*&lt;tenantid&gt;*/oauth2/v2.0/token
```

Where *&lt;tenantid&gt;* is the tenant ID of your Microsoft Defender for Endpoint as described in the [Before you begin](sgcc-configure-msdefender.md#prereq_bbj_rbg_ndc) section.

</td></tr><tr><td>

Use MID Server

</td><td>

Option to use a MID Server.**Note:** Use of a MID Server is optional.

</td></tr><tr><td>

Mid Selection

</td><td>

Name of the MID Server used by the connector.This field appears only when the **Use MID Server** check box is selected.

</td></tr></tbody>
</table>    3.  Select **Update and test connection**.

    4.  Once the connection test is complete, select **Continue**.

6.  Configure the import schedule to import data at regular intervals.

    1.  In the **Setup** stage of the playbook, select the **Configure import schedule** activity.

    2.  Select **Configure import schedule**.

    3.  Expand the Parent scheduled data import within the Import schedules list to select the **SG-Defender Machines** import schedule.

    4.  In the Configure import schedule dialog box, select the **Active** check box, and then fill in the run schedule and time details.

        For more information, see [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US#table_r53_5hm_xp).

    5.  Select **Save**.

        Alternatively, select **Execute Now** to execute the import schedule immediately.

    6.  Select **Continue**.

7.  In the **Setup** stage of the playbook, select the **Confirm connection setup** activity to verify whether the connection was configured.


## What to do next

Select **View all connections** to review the connection details. The configured connection appears in the Installed connections list.

**Related topics**  


[Service Graph Connector for Microsoft Defender Endpoint](../../configuration-management/concept/sgc-cmdb-integration-msdefender.md)

[CMDB classes targeted in Service Graph Connector for Microsoft Defender Endpoint](../../configuration-management/reference/sgc-cmdb-msdefender-classes.md)

[Accessing the connection details of Service Graph Connector for Microsoft Defender Endpoint](../../configuration-management/concept/sgc-cmdb-msdefender-conn.md#)

