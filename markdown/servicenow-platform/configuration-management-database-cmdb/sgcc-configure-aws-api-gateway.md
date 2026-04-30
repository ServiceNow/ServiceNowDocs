---
title: Configure API Service Graph Connector for AWS API Gateway using SGC Central
description: Set up scheduled import jobs to pull in AWS API Gateway data into your CMDB.
locale: en-US
release: xanadu
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [AWS API Gateway, API Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure API Service Graph Connector for AWS API Gateway using SGC Central

Set up scheduled import jobs to pull in AWS API Gateway data into your CMDB.

## Before you begin

Install API Service Graph Connector for AWS API Gateway version 1.0.0 or later from the ServiceNow Store. For ServiceNow Store installation steps, see [Install a ServiceNow Store application](https://www.servicenow.com/docs/access?context=t_InstallApplications&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

The authentication mechanism used by the connector is AWS Signature Type \(HMAC Authentication Technique\) with AWS Security Token Service \(STS\) token. For information about permissions, see the [API Service Graph Connector for AWS API Gateway - Setup Instructions \[KB1962734\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB1962734) article in the Now Support Knowledge Base.

Role required: The following table shows the roles required for each stage of the playbook.

|Stage|Role|
|-----|----|
|Prerequisites|admin|
|Setup|SGC-Admin \(sn\_cmdb\_int\_util.sgc\_admin\) or admin|

**Note:** The admin user role is required to run background scripts and to provide access to global tables to the SGC-Admin user. For information about the user roles for Service Graph Connectors, see [Service Graph Connector user roles](../../configuration-management/concept/cmdb-sgc-intro.md#section_ett_spp_4hc).

## About this task

The playbook experience for onboarding connectors is activated with SGC Central in the Service Graph Workspace or CMDB Workspace. To configure the SGC Central application, see [Configuring SGC Central](../concept/sgcc-configuring.md) and for more information on how to interact with a playbook, see [Interact with Playbook](https://www.servicenow.com/docs/access?context=playbook-ui&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

**Note:** Alternatively, you can configure a default connection already available from the installed or draft connections in SGC Central. Go to **All** &gt; **Service Graph Connectors**, then select **Setup** for the connector from the menu. To learn about installed and draft connections, see [Managing connections added for Service Graph Connectors in SGC Central](../concept/sgcc-managing-connection.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **CMDB Workspace**.

2.  In the CMDB Workspace, select **SGC Central**.

3.  On the Overview page, select **Create connection**.

    **Tip:** Alternatively, you can select **Create connection** on the All connections page.

4.  On the Create connection window, select the AWS API Gateway connector type, and then select **Create connection**.

5.  Complete the initial prerequisites when setting up a connection for the first time using a connector.

    **Note:** This step is required only during the first-time setup. See [Perform initial setup tasks when creating a connection in SGC Central](sgcc-first-time-setup.md).

6.  Enter connection details and test the API connection for importing AWS API Gateway data.

    1.  In the **Setup** stage of the playbook, select the **Create and test connection** activity.

    2.  On the form, fill in the fields.

<table id="table_l2g_zn4_nyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AWS API Gateway Connection Name

</td><td>

Name to identify the AWS API Gateway connection record.For example, `SG-AWS-API-Gateway connection`.

</td></tr><tr><td>

Access Key

</td><td>

Access key ID of the IAM user that has permissions to interact with the AWS resources.

</td></tr><tr><td>

Secret Key

</td><td>

Secret access key that corresponds to the Access key ID required for authenticating the connection securely.

</td></tr></tbody>
</table>    3.  Select **Create and test connection**.

    4.  Once the connection test is complete, select **Continue**.

7.  Copy configuration properties from an existing AWS connection.

    **Note:** The Copy configuration properties activity is displayed only when an AWS connection is already set up on your instance.

    1.  In the **Setup** stage of the playbook, select the **Copy configuration properties** activity.

    2.  In the **AWS Connection** field, select the connection.

        The values of the following properties are copied from the selected AWS connection:

        -   Standalone account ID
        -   Management account ID
        -   Gov cloud
        -   STS assume role
        -   AWS regions
        -   Config aggregator name
        -   Config aggregator account
        -   Config aggregator region
    3.  Select **Continue**.

    4.  Once the connection test is complete, select **Continue**.

8.  Set the configuration properties for the connection.

    1.  In the **Setup** stage of the playbook, select the **Set configuration properties** activity.

    2.  Fill in the property details.

        **Note:** If you select to copy the configuration properties from an existing AWS connection, the properties listed in the step [7.b](sgcc-configure-aws-api-gateway.md#exist-props) are copied from the existing connection automatically.

        |Property|Description|
|Management account ID or standalone account ID|
        |--------|-----------|
        |----------------------------------------------|
        |Management account ID|Management account ID associated with the AWS API Gateway account.|
        |Standalone account ID|ID of a member account associated with the AWS API Gateway account.|
        |STS assume role name and AWS regions|
        |STS assume role name|STS Assume Role name of the AWS account that is used for querying the STS Assume Role API to obtain the API credentials.|
        |AWS regions|List of comma-separated regions where the AWS API Gateway resides.|
        |Config aggregator setup|
        |Config aggregator account ID|AWS account ID where the aggregator resource type in the AWS Config service has been configured.|
        |Config aggregator name|Name of the aggregator resource type in the AWS Config service.|
        |Config aggregator region|Region where the aggregator resource type resides.|
        |API usage data|
        |Collect Usage Data|Option to enable usage data collection to retrieve API usage data over a specified duration.|
        |Collection period in days|Duration in days for collecting API usage data.|
        |Gov cloud setup|
        |Is gov cloud|Option to indicate that the connection setup is for the AWS GovCloud.|

    3.  Select **Continue**.

9.  Configure the import schedule to import data at regular intervals.

    1.  In the **Setup** stage of the playbook, select the **Configure import schedule** activity.

    2.  Expand the Parent scheduled data import within the Import schedules list to select the **Managed API Rest** import schedule associated with your connection.

        **Note:** The connection name is prefixed to the schedule name.

    3.  In the Configure import schedule dialog box, select the **Active** check box, and then fill in the run schedule and time details.

        For more information, see [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US#table_r53_5hm_xp).

    4.  Select **Save**.

        Alternatively, select **Execute Now** to execute the import schedule immediately.

    5.  Select **Continue**.

10. In the **Setup** stage of the playbook, select the **Confirm connection creation** activity to verify whether the connection was configured.


## What to do next

Select **View all connections** to review the connection details. The configured connection appears in the Installed connections list.

You can then manage connections from the SGC Central view of the CMDB Workspace. For more information, see [Managing connections added for Service Graph Connectors in SGC Central](../concept/sgcc-managing-connection.md).

**Related topics**  


[API Service Graph Connector for AWS API Gateway](../../configuration-management/concept/api-sgc-aws-gateway.md)

[Target tables for storing API Service Graph Connector for AWS API Gateway data](../../configuration-management/reference/api-sgc-aws-gateway-tables.md)

