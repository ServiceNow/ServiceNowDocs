---
title: Configure Service Graph Connector for AWS using SGC Central
description: Use the playbook available with the SGC Central application to set up the Service Graph Connector for AWS for pulling in AWS data into the CMDB
locale: en-US
release: yokohama
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2026-03-02"
reading_time_minutes: 11
breadcrumb: [AWS, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure Service Graph Connector for AWS using SGC Central

Use the playbook available with the SGC Central application to set up the Service Graph Connector for AWS for pulling in AWS data into the CMDB

## Before you begin

-   Install Service Graph Connector for AWS version 2.7.0 or later from the ServiceNow Store. For ServiceNow Store installation steps, see [Install a ServiceNow Store application](https://www.servicenow.com/docs/access?context=t_InstallApplications&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).
-   Verify that you’ve completed the prerequisites for setting up AWS. See [Configure the AWS environment](../../configuration-management/task/sgc-cmdb-aws-task-overview.md).

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

3.  On the Create connection window, select the AWS connector type and then select **Create connection**.

4.  Complete the initial prerequisites when setting up a connection for the first time using a connector.

    **Note:** This step is required only during the first-time setup. See [Perform initial setup tasks when creating a connection in SGC Central](sgcc-first-time-setup.md).

5.  Complete the prerequisites for setting up the AWS environment.

    1.  Configure the basic setup in the AWS environment required for importing data using the connector.

        1.  In the **Prerequisites** stage of the playbook, select the **Download basic scripts** activity.
        2.  Execute the scripts to configure the AWS environment.

            For more information on executing scripts, see [Basic scripts](../../configuration-management/concept/sgc-cmdb-aws-script-op.md#section_vfh_wyf_4zb).

        3.  Select the **I have read the instructions and executed the script accordingly** check box to confirm that you have executed the scripts.
        4.  Select **Continue**.
    2.  Set up deep discovery on Amazon Elastic Compute Cloud \(Amazon EC2\) instances.

        **Note:** Complete this step only to perform deep discovery on EC2 instances. Else, select **Skip**.

        1.  In the **Prerequisites** stage of the playbook, select the **Download deep discovery scripts** activity.
        2.  Execute the scripts to configure Amazon EC2 instances for deep discovery.

            For more information on executing scripts, see [Deep discovery scripts](../../configuration-management/concept/sgc-cmdb-aws-script-op.md#section_ahc_jwf_4zb).

        3.  Select **Continue**.
    3.  Set up Amazon Elastic Kubernetes Service \(EKS\) clusters.

        **Note:** Complete this step only when the Amazon EKS service for Kubernetes clusters is required. Else, select **Skip**.

        1.  In the **Prerequisites** stage of the playbook, select the **Download Amazon EKS scripts** activity.
        2.  Execute the scripts to set up Amazon EKS clusters.

            For more information on executing scripts, see [Amazon EKS scripts](../../configuration-management/concept/sgc-cmdb-aws-script-op.md#section_osh_4zf_4zb).

        3.  Select **Continue**.
6.  Complete the setup for configuring the connector for importing data.

    1.  Create and test connection.

        1.  In the **Setup** stage of the playbook, select the **Create and test connection** activity.
        2.  On the form, fill in the fields.

<table id="table_iw5_j5k_wbc"><thead><tr><th>

Field

</th><th>

 

</th></tr></thead><tbody><tr><td>

Connection name

</td><td>

Name to identify the AWS connection record.For example, `SG_AWS_CredentialAlias_Org`.

</td></tr><tr><td>

Access Key ID

</td><td>

Access key ID of the IAM user that has permissions to interact with the AWS resources.

</td></tr><tr><td>

Secret Access Key

</td><td>

Secret access key that corresponds to the Access key ID required for authenticating the connection securely.

</td></tr><tr><td>

Use MID Server

</td><td>

Option to use a MID Server.**Note:** Use of a MID Server is optional.

</td></tr><tr><td>

Mid Selection

</td><td>

Name of the MID Server used by the connector.This field appears only when the **Use MID Server** check box is selected.

</td></tr></tbody>
</table>        3.  Select **Create and test connection**.
        4.  Once the connection test is complete, select **Continue**.
    2.  Set configuration properties for the connection to access the AWS resources.

        1.  In the **Setup** stage of the playbook, select the **Set configuration properties** activity.
        2.  In the Organization details section, fill in the organization details including the account identifier, name and description of the AWS organization.
        3.  In the S3 account details section, fill in the details.

            |Field|Description|
            |-----|-----------|
            |S3 account ID|Numeric identifier of the AWS account that hosts the Amazon Simple Storage Service \(Amazon S3\) bucket.|
            |S3 bucket name|Name of the Amazon S3 bucket that collects the details from Amazon EC2 instances.|
            |S3 region|Region where the Amazon S3 bucket resides.|

        4.  In the **AWS regions** field of the AWS regions and STS assume role name section, enter the AWS regions to collect the CI data.

            By default, the Service Graph Connector for AWS runs through all the AWS regions to collect the CI data.

            You can enter AWS specific regions to speed up the CI data import process. For example, `us-east1, us-east-2`.

            If you update the **AWS regions** field value later, clear the value of the **Last run datetime** field in all the data sources related to the Service Graph Connector for AWS to import a new set of data.

        5.  In the **STS assume role name** field of the AWS regions and STS assume role name section, enter the AWS Identity and Access Management \(IAM\) role name.

            The AWS IAM role name is obtained by the ServiceNow user by calling the AssumeRole API offered by the AWS Security Token Service \(STS\). The AssumeRole API returns a set of temporary security credentials for the ServiceNow user to access the AWS resources.

            **Note:** Enter the IAM role name but don’t prefix `arn` in the name. If you leave this field is empty, the value of this field is automatically set to **SnowOrganizationAccountAccessRole**, which is the default IAM role name for the ServiceNow user.

        6.  In the SSM SendCommand document details section, enter the name of the document that defines the actions run by the AWS Systems Manager \(SSM\) on a Linux-based Amazon EC2 instance or a Windows-based Amazon EC2 instance in their respective fields.
        7.  In the **Management account ID** field of the Management account ID and standalone account ID section, enter the management account ID in the AWS organization.

            Enter a value for this field when the ServiceNow user was created in an AWS member account.

            The account calls the ListAccounts API associated with the AWS organization to collect CI information from all the accounts. For more information, see [ListAccounts](https://docs.aws.amazon.com/organizations/latest/APIReference/API_ListAccounts.html) on the AWS documentation site.

        8.  In the **Standalone account ID** field of the Management account ID and standalone account ID section, enter the ID of a member account in the AWS organization.

            **Note:** When specifying a standalone account, the AWS organization-related data such as the organization name, organization units, organization ID, and service accounts are not imported. To import the full data later, clear any value mentioned in the **Standalone account ID** field. See the [Service Graph Connector for AWS - Standalone Setup \[KB1642159\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1642159) article in the Now Support Knowledge Base.

        9.  In the AWS config aggregator details section, enter the AWS account details for the aggregator resource type.

<table id="table_ztj_2cm_wbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Config aggregator account

</td><td>

AWS account where the aggregator resource type in the AWS Config service has been configured.Enter a value in this field when you’re using an AWS Config aggregator.

</td></tr><tr><td>

Config aggregator name

</td><td>

Name of the aggregator resource type. This field is available only when you enter a value in the **Config aggregator account** field.

</td></tr><tr><td>

Config aggregator region

</td><td>

Region where the aggregator resource type resides. This field is available only when you enter a value in the **Config aggregator account** field.

</td></tr></tbody>
</table>        10. In the AWS key rotation setup section, enter the key rotation process details.

            |Field|Description|
            |-----|-----------|
            |AWS rotate keys|Option to enable the key rotation process.|
            |AWS key rotation date|Key rotation date. Set the value to the required key rotation date for the first run. For subsequent runs, this field is automatically set to the rotation date. This field is available only when you select the **AWS Rotate Keys** check box.|
            |AWS key rotation period \(in days\)|Key rotation period in days. This field is available only when you select the **AWS rotate keys** check box.|
            |AWS key rotation status|Status message of a key rotation displaying whether the rotation was a success or a failure. This field is automatically set to display the key rotation status message. This field is available only when you select the **AWS rotate keys** check box. If the rotation status is a failure, an email notification is triggered, if configured.|
            |Email accounts for receiving error notifications|Comma-separated list of the email addresses of recipients who receive notifications about the AWS key rotation errors.|
            |Email account groups for receiving error notifications|Comma-separated list of the ServiceNow groups who receive notifications about the AWS key rotation errors.|

        11. Select the **Is gov cloud** check box in the Gov cloud setup section to indicate that the connection setup is for the AWS GovCloud.
        12. In the SSM EKS SendCommand document details section, enter the AWS SSM document details.

            |Field|Description|
            |-----|-----------|
            |EKS cluster names document|Name of the AWS SSM document to discover EKS clusters associated with EC2 Bastion hosts.|
            |EKS shell script document|Name of the AWS SSM document to fetch CIs related to Kubernetes components, such as pods, services, and deployments, from EKS clusters.|

        13. Select **Save properties**.
        14. Select **Continue**.
    3.  Configure the required EC2 resources for Amazon Elastic Kubernetes Service \(EKS\) to import EKS cluster data.

        **Note:** Complete this step only when EC2 resources are needed. Else, select **Skip** for the **Configure EKS EC2 resources** activity.

        An EKS EC2 resource is a bastion host that has network access to EKS clusters. The EKS clusters aren't directly accessible to the connector. Therefore, you must provide the EKS EC2 resource details. For importing EKS cluster data, the connector uses the SSM Send Command on EKS EC2 resources to run kubectl commands remotely.

        **Note:** Ensure that you’ve configured your AWS environment for the EKS integration. For more information, see the [Service Graph Connector for AWS - Amazon EKS Integration \[KB1437138\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB1437138) article in the Now Support Knowledge Base.

        1.  In the **Setup** stage of the playbook, select the **Configure EKS EC2 resources** activity.
        2.  On the Configure EKS EC2 resources page, select **New**.
        3.  On the Configure EKS EC2 resources window that appears, fill in the fields.

            |Field|Description|
            |-----|-----------|
            |EKS EC2 Resource Id|Identifier of the EKS EC2 resource.|
            |EC2 Region|AWS region where the EKS EC2 resource is located.|
            |EC2 Account|User name assigned to the EKS EC2 resource account.|
            |Connection Alias|Connection alias associated with the AWS environment setup and configured in step [6.a.ii](sgcc-configure-aws-integ.md#aws-cred-0).|
            |Connection|Connection name associated with the AWS environment setup and configured in step [6.a.ii](sgcc-configure-aws-integ.md#aws-cred-0).|
            |Active|Option to activate the EKS EC2 resource.|

        4.  Select **Save**.
        5.  Repeat steps from [6.c.ii](sgcc-configure-aws-integ.md#eks-ec2-add) to [6.c.iv](sgcc-configure-aws-integ.md#eks-ec2-save) to add more EKS EC2 resources.
        6.  Select **Continue**.
    4.  Run the AWS diagnostic tool before running a scheduled import job to identify any issues in the AWS environment setup.

        1.  In the **Setup** stage of the playbook, select the **Run diagnostic tests** activity.
        2.  On the Run diagnostic test page, select an option to exclude the corresponding test results from the diagnostic summary.
            -   **Skip SSM setup tests**

                Excludes the software inventory data from the summary results by not calling the GetInventory API. Select this option when you’ve opted out or not set up the configuration for SSM.

            -   **Skip SSM Deep Discovery tests**

                Excludes the deep discovery data from the summary results. Select this option when you’ve opted out or not set up the configuration for SSM deep discovery.

            -   **Skip EKS setup tests**

                Excludes the EKS data from the summary results by not running the kubectl commands.

                **Note:** This check box appears only when you’ve configured EC2 resources in the **Configure EKS EC2 resources** activity.

        3.  Select **Run diagnostic test** and wait for the test to complete.
        4.  Review the diagnostic summary, the API access results, and the IAM permission validation logs.
        5.  When the test results are successful, select **Continue**.
    5.  Configure the import schedule to import data at regular intervals.

        1.  In the **Setup** stage of the playbook, select the **Configure import schedule** activity.
        2.  Expand the Parent scheduled data import within the Import schedules list to select the **SG-AWS-Organization** import schedule.
        3.  In the Configure import schedule dialog box, select the **Active** check box, and then fill in the run schedule and time details.

            For more information, see [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US#table_r53_5hm_xp).

        4.  Select **Save**.

            Alternatively, select **Execute Now** to execute the import schedule immediately.

        5.  Select **Continue**.
    6.  In the **Setup** stage of the playbook, select the **Confirm connection setup** activity to verify whether the connection was created.


## What to do next

Select **View all connections** to review the connection details. The configured connection appears in the Installed connections list.

**Related topics**  


[Service Graph Connector for AWS](../../configuration-management/concept/cmdb-integration-aws-sg.md)

[CMDB classes targeted in Service Graph Connector for AWS](../../configuration-management/reference/cmdb-aws-classes.md)

[Supported AWS resource types](../../configuration-management/reference/cmdb-sgc-aws-resource-types.md)

[Accessing the connection details of Service Graph Connector for AWS](../../configuration-management/concept/sgc-cmdb-aws-conn.md#)

[Additional features within the Service Graph Connector for AWS](../../configuration-management/concept/sgc-cmdb-aws-add-features.md)

