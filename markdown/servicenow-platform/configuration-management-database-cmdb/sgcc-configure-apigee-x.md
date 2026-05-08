---
title: Configure API Service Graph Connector for Apigee X using SGC Central
description: Set up scheduled import jobs to pull in Apigee X data into your CMDB.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Apigee X, API Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure API Service Graph Connector for Apigee X using SGC Central

Set up scheduled import jobs to pull in Apigee X data into your CMDB.

## Before you begin

Install API Service Graph Connector for Apigee X version 1.0.0 or later from the ServiceNow Store. For ServiceNow Store installation steps, see Install a ServiceNow Store application.

Role required: The following table shows the roles required for each stage of the playbook.

|Stage|Role|
|-----|----|
|Prerequisites|admin|
|Setup|SGC-Admin \(sn\_cmdb\_int\_util.sgc\_admin\) or admin|

**Note:** The admin user role is required to run background scripts and to provide access to global tables to the SGC-Admin user. For information about the user roles for Service Graph Connectors, see [Service Graph Connector user roles](../../configuration-management/concept/cmdb-sgc-intro.md#section_ett_spp_4hc).

## About this task

The playbook experience for onboarding connectors is activated with SGC Central in the CMDB Workspace. To configure the SGC Central application, see [Configuring SGC Central](../concept/sgcc-configuring.md) and for more information on how to interact with a playbook, see Interact with Playbook.

**Note:** Alternatively, you can configure a default connection already available from the installed or draft connections in SGC Central. Go to **All** &gt; **Service Graph Connectors**, then select **Setup** for the connector from the menu. To learn about installed and draft connections, see [Managing connections added for Service Graph Connectors in SGC Central](../concept/sgcc-managing-connection.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **CMDB Workspace**.

2.  In the CMDB Workspace, select **SGC Central**.

3.  On the Overview page, select **Create connection**.

    **Tip:** Alternatively, you can select **Create connection** on the All connections page.

4.  On the Create connection window, select the Apigee X connector type, and then select **Create connection**.

5.  Complete the initial prerequisites when setting up a connection for the first time using a connector.

    **Note:** This step is required only during the first-time setup. See [Perform initial setup tasks when creating a connection in SGC Central](sgcc-first-time-setup.md).

6.  Complete the prerequisites for setting up the Apigee X environment.

    1.  Set up the Apigee X environment and create a Java KeyStore \(JKS\) certificate to encrypt the security certificates obtained from an Apigee X application.

        1.  In the **Prerequisites** stage of the playbook, select the **Review setup instructions** activity.
        2.  Review and complete the setup instructions on the [API Service Graph connector for Apigee X - Setup Instructions \[KBB0010364\]](https://support.servicenow.com/kb_view.do?sysparm_article=KBB0010364) article in the Now Support Knowledge Base.

            You must create a service account, assign roles, bind roles to the service account, enable APIs, create a P12 file, and register it in your ServiceNow instance.

            Make a note of the destination keystore password. You need to specify this password while importing the JKS certificate into the API Service Graph Connector for Apigee X application.

        3.  Select the **I have read the setup instructions** check box to confirm that you have set up the Apigee X environment according to the instructions.
        4.  Select **Continue**.
    2.  Create an X.509 certificate to associate the Java KeyStore \(JKS\) certificate for the Apigee X application with the connector.

        **Note:** You can skip this step if you're reusing a previously created certificate.

        1.  In the **Prerequisites** stage of the playbook, select the **Create X.509 certificate** activity.
        2.  On the form, fill in the fields.

            |Field|Description|
            |-----|-----------|
            |Name|Name of the X.509 certificate. For example, `ApigeeX-509Certificate`.|
            |Key store password|Password to access the JKS certificate as noted down in the [previous step](sgcc-configure-apigee-x.md#keystorepwd).|
            |Short description|Description of the X.509 certificate.|

        3.  In the Attachments section, select **Add File**.
        4.  Browse and select the P12 file for the JKS certificate you created in the [previous step](sgcc-configure-apigee-x.md#create-p12).
        5.  On the Upload a file dialog box, select **Upload**.
        6.  Select **Continue**.
7.  Enter connection details and test the API connection for importing Apigee X data.

    1.  In the **Setup** stage of the playbook, select the **Create and test connection** activity.

    2.  On the form, fill in the fields.

        |Field|Description|
        |:----|:----------|
        |Connection name|Name to identify the Apigee X connection record.|
        |Service account email|Email address associated with the ServiceNow service account used for authentication with Apigee X as noted in the [previous step](sgcc-configure-apigee-x.md#create-p12).|
        |X.509 certificate|Name of the X.509 certificate as noted in the [previous step](sgcc-configure-apigee-x.md#create-p12).|
        |Keystore password|Password associated with the keystore as noted in the [previous step](sgcc-configure-apigee-x.md#keystorepwd).|

    3.  Select **Create and test connection**.

    4.  Once the connection test is complete, select **Continue**.

8.  Set the configuration properties for the connection.

    1.  In the **Setup** stage of the playbook, select the **Set configuration properties** activity.

    2.  Enter the properties.

<table id="table_nn3_31v_3cc"><thead><tr><th>

Property

</th><th>

Description

</th></tr><tr><th class="sub-head" colspan="2">

Apigee identification

</th></tr></thead><tbody><tr><td>

Apigee organization name/GCP project id

</td><td>

Apigee X organization names or GCP project IDs from which data should be fetched. If left blank, data is retrieved from all permitted Apigee X organizations.For multiple values, separate them with commas.

</td></tr><tr><td class="sub-head" colspan="2">

Data retrieval configuration

</td></tr><tr><td>

Include environments

</td><td>

Apigee X environments to include in the connection.For multiple environments, separate them with commas. Only API proxies in the environments listed in the **Include environments** property are imported.

If you leave this field empty, the data sources within the connector import API proxies from all environments.

</td></tr><tr><td>

Collection period \(in days\)

</td><td>

Duration in days for collecting API usage data.

</td></tr><tr><td>

Collect usage data

</td><td>

Option to enable usage data collection to retrieve API usage data over a specified duration.

</td></tr><tr><td>

Expand HTTP method types

</td><td>

HTTP methods including `GET`, `POST`, `PUT`, `PATCH`, `DELETE`, `OPTIONS`, `HEAD`, `CONNECT`, and `TRACE`, to consider for routes.For multiple methods, separate them with commas.If left blank, results in a single API Frontend being created with the `ALL` method, indicating support for all standard HTTP methods.

</td></tr><tr><td class="sub-head" colspan="2">

GCP identification

</td></tr><tr><td>

GCP Organization id

</td><td>

GCP organization ID for retrieving data from GCP Organization, GCP Folder, and GCP Project data sources.

</td></tr></tbody>
</table>    3.  Select **Continue**.

9.  Configure the import schedule to import data at regular intervals.

    1.  In the **Setup** stage of the playbook, select the **Configure import schedule** activity.

    2.  Expand the Parent scheduled data import within the Import schedules list to select the **Apigee Organization** import schedule associated with your connection.

        **Note:** The connection name is prefixed to the schedule name.

    3.  In the Configure import schedule dialog box, select the **Active** check box, and then fill in the run schedule and time details.

        For more information, see Schedule a data import.

    4.  Select **Save**.

        Alternatively, select **Execute Now** to execute the import schedule immediately.

    5.  Select **Continue**.

10. In the **Setup** stage of the playbook, select the **Confirm connection creation** activity to verify whether the connection was created.


## What to do next

Select **View all connections** to review the connection details. The configured connection appears in the Installed connections list.

You can then manage connections from the SGC Central view of the CMDB Workspace. For more information, see [Managing connections added for Service Graph Connectors in SGC Central](../concept/sgcc-managing-connection.md).

**Related topics**  


[API Service Graph Connector for Apigee X](../../configuration-management/concept/api-sgc-apigee-x.md)

[Target tables for storing API Service Graph Connector for Apigee X data](../../configuration-management/reference/api-sgc-apigee-x-tables.md)

