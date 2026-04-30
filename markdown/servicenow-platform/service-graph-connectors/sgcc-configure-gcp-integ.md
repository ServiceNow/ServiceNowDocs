---
title: Configure Service Graph Connector for GCP using SGC Central
description: Use the playbook available with the SGC Central application to set up the Service Graph Connector for GCP for pulling in GCP project data into the CMDB.
locale: en-US
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2026-03-06"
reading_time_minutes: 5
breadcrumb: [GCP, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure Service Graph Connector for GCP using SGC Central

Use the playbook available with the SGC Central application to set up the Service Graph Connector for GCP for pulling in GCP project data into the CMDB.

## Before you begin

Install Service Graph Connector for GCP version 1.8.0 or later from the ServiceNow Store. For ServiceNow Store installation steps, see [Install a ServiceNow Store application](https://www.servicenow.com/docs/access?context=t_InstallApplications&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## About this task

The playbook experience for onboarding connectors is activated with SGC Central in the Service Graph Workspace or CMDB Workspace. To configure the SGC Central application, see [Configuring SGC Central](../concept/sgcc-configuring.md) and for more information on how to interact with a playbook, see [Interact with Playbook](https://www.servicenow.com/docs/access?context=playbook-ui&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

## Procedure

1.  Use one of the following methods to open SGC Central:

    -   Navigate to **Workspaces** &gt; **Service Graph Workspace**, and from the left navigation panel, select the Ingestion icon to open the SGC Central view.
    -   Navigate to **Workspaces** &gt; **CMDB Workspace** &gt; **SGC Central**.
2.  On the Overview page, select **Create connection**.

    **Tip:** Alternatively, you can select **Create connection** on the All connections page.

3.  On the Create connection window, select the GCP connector type and then select **Create connection**.

4.  Complete the initial prerequisites when setting up a connection for the first time using a connector.

    **Note:** This step is required only during the first-time setup. See [Perform initial setup tasks when creating a connection in SGC Central](sgcc-first-time-setup.md).

5.  Complete the prerequisites for setting up the GCP environment.

    1.  Set up the GCP environment and create a Java KeyStore \(JKS\) certificate to encrypt the security certificates obtained from a GCP application.

        1.  In the **Prerequisites** stage of the playbook, select the **Review setup instructions** activity.
        2.  Select **Service Graph connector for GCP - Setup Instructions** link to view the setup instructions included in the [Service Graph connector for GCP - Setup Instructions \[KB1220598\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB1220598) article in the Now Support Knowledge Base.
        3.  Make a note of the destination keystore password. You need to specify this password while importing the JKS certificate into the Service Graph Connector for GCP application.
        4.  Select the **I have read the setup instructions** check box to confirm that you have set up the GCP environment according to the instructions.
        5.  Select **Continue**.
        6.  After completing the **Review setup instructions** activity, select **Continue**.
    2.  Create an X.509 certificate to associate the JKS certificate for the GCP application with the Service Graph Connector for GCP.

        **Note:** You can skip this step if you're reusing an existing certificate by selecting **Skip**.

        1.  In the **Prerequisites** stage of the playbook, select the **Create X.509 certificate** activity.
        2.  Select **New**.
        3.  On the form, fill in the fields.

            |Field|Description|
            |-----|-----------|
            |Name|Name of the X.509 certificate. For example, `SG-GCP-509Certificate-Org1`.|
            |Key store password|Password to access the JKS certificate as noted down in the step [5.a.iii](sgcc-configure-gcp-integ.md#keystorepwd).|
            |Short description|Description of the X.509 certificate.|

        4.  In the Attachments section, select **Add File** to browse and upload the keystore.p12 file for the JKS certificate you created in step [5.a](sgcc-configure-gcp-integ.md#jks).
        5.  Select the **I have read the setup instructions** check box after you have completed the setup.
        6.  After completing the **Create X.509 certificate** activity, select **Continue**.
6.  Download the scripts that are required to enable deep discovery for the Service Graph Connector for GCP.

    1.  In the **Prerequisites** stage of the playbook, select the **Download GCP deep discovery scripts** activity.

    2.  Download the deep discovery scripts for Linux and Windows VMs.

        For more information about deep discovery for the Service Graph Connector for GCP, see the [Service Graph Connector for GCP - Deep Discovery Setup Instructions \[KB2213095\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2213095) article in the Now Support Knowledge Base.

    3.  After completing the **Download GCP deep discovery scripts** activity, select **Continue**.

7.  Enter connection details and test the API connection for importing GCP data.

    1.  In the **Setup** stage of the playbook, select the **Create and test connection** activity.

    2.  On the form, fill in the fields.

<table id="table_ahn_xtg_rmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name to identify the GCP connection record.

</td></tr><tr><td>

Service Account Email

</td><td>

ServiceNow service account associated with the GCP application.

</td></tr><tr><td>

Keystore

</td><td>

Name of the X.509 certificate that you created in step [5.b](sgcc-configure-gcp-integ.md#x509cert).

</td></tr><tr><td>

Keystore Password

</td><td>

Password to access the JKS certificate as noted down in the step [5.a.iii](sgcc-configure-gcp-integ.md#keystorepwd).

</td></tr><tr><td>

Organization Id

</td><td>

ID of the organization associated with the GCP application.

</td></tr><tr><td>

Discovery Scope

</td><td>

Discovery scope of the GCP application. The available options are:-   **Organization**

Select **Organization** when the ServiceNow service account has access to data within the GCP organization.

-   **Projects**

Select **Projects** when the ServiceNow service account has access to data within GCP projects only.

</td></tr></tbody>
</table>    3.  Select **Update and test connection**.

    4.  Once the connection test is complete, select **Continue**.

8.  Configure the deep discovery connection properties.

    1.  In the **Setup** stage of the playbook, select the **Configure connection properties** activity.

        If deep discovery is already configured on the connection, the values are pre-populated on the Deep Discovery properties form. For more information about the deep discovery connection properties for GCP, see [Deep discovery connection properties](../../configuration-management/concept/sgc-gcp-deep-discovery.md#section_xwn_4c3_cgc).

    2.  Review the pre-populated fields on the Deep Discovery properties form.

    3.  After completing the **Configure connection properties** activity, select **Continue**.

9.  Configure the import schedule to import data at regular intervals.

    1.  In the **Setup** stage of the playbook, select the **Configure import schedule** activity.

    2.  Select **Configure import schedule**.

    3.  Expand the Parent scheduled data import within the Import schedules list to select the **SG-GCP Organization** import schedule.

    4.  In the Configure import schedule dialog box, select the **Active** check box, and then fill in the run schedule and time details.

        For more information, see [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US#table_r53_5hm_xp).

    5.  Select **Save**.

        Alternatively, select **Execute Now** to execute the import schedule immediately.

    6.  Select **Continue**.

10. In the **Setup** stage of the playbook, select the **Confirm connection creation** activity to verify whether the connection was configured.


## What to do next

Select **View all connections** to review the connection details. The configured connection appears in the Installed connections list.

**Related topics**  


[Service Graph Connector for GCP](../../configuration-management/concept/sgc-cmdb-integration-gcp.md)

[Deep discovery for Service Graph Connector for GCP](../../configuration-management/concept/sgc-gcp-deep-discovery.md)

