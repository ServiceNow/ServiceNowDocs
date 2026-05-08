---
title: Configure Service Graph Connector for AWS using the guided setup
description: Set up the AWS environment and scheduled jobs to pull in AWS data into the CMDB.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 16
breadcrumb: [AWS, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure Service Graph Connector for AWSusing the guided setup

Set up the AWS environment and scheduled jobs to pull in AWS data into the CMDB.

## Before you begin

**Important:** Unless there are configuration issues, use the SGC Central view in the Service Graph Workspace or CMDB Workspace to configure the connection for the connector, as the guided setup method is planned for deprecation.

To use this Service Graph Connector, you need a subscription to a Subscription Unit that is based in the IT Operations Management \(ITOM\) Visibility application or in the ITOM Discovery application. As defined in the section titled "Managed IT Resource Types" in [ServiceNow Subscription Unit Overview](https://www.servicenow.com/products/entitlements-packages.html) for your subscription, for managed IT resources that are created or modified in the CMDB by this Service Graph Connector, but that aren’t yet managed by ITOM Visibility or ITOM Discovery, these resources will increase Subscription Unit consumption from that application. Review your current Subscription Unit consumption within ITOM Visibility or ITOM Discovery to ensure available capacity.

Dependencies and requirements:

-   The [Integration Commons for CMDB](../concept/integration-commons-for-cmdb.md) store app, which is automatically installed.
-   The CMDB CI class models store app, which is automatically installed. See [CMDB CI Class Models app](../concept/cmdb-ci-class-models.md).
-   Discovery Core plugin \(com.snc.discovery.core\), which is automatically installed by Discovery.
-   The ITOM Discovery License plugin \(com.snc.itom.discovery.license\). You must activate this plugin.
-   ITOM Licensing plugin \(com.snc.itom.license\). For more information, see Request Discovery.

Ensure that you’ve completed the prerequisites for setting up AWS. See [Configure the AWS environment](sgc-cmdb-aws-task-overview.md).

**Note:** When upgrading from an earlier version, ensure that you’ve updated the SSM documents and IAM permissions in your AWS instance.

-   For updating SSM documents, run the `SG-AWS-RunShellScript-Setup.yml`, `SG-AWS-RunPowerShellScript-Setup.yml`, and `SG-AWS-RunKubeCtlShellScript.yml` scripts.
-   For updating the IAM permissions assigned to the SnowOrganizationAccountAccessRole role, run the `CreateSnowOrganizationAccountAccessRoleInMemberAccount.yml` script.

Role required: SGC-Admin \(sn\_cmdb\_int\_util.sgc\_admin\) or admin

**Note:** The admin user role is required to run background scripts and to provide access to global tables to the SGC-Admin user. For information about the user roles for Service Graph Connectors, see [Service Graph Connector user roles](../concept/cmdb-sgc-intro.md#section_ett_spp_4hc).

## About this task

For more information on the **Service Graph Connector for AWS** setup instructions, see the following articles:

-   [Service Graph Connector for AWS - Setup Instructions \[KB1220597\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB1220597) article on the Now Support Knowledge Base.
-   [Service Graph Connector for AWS - Introduction](https://www.servicenow.com/community/cmdb-articles/service-graph-connector-for-aws-introduction/ta-p/2300757) on the ServiceNow Community site.
-   [SGC-AWS - Release 2.0 Features](https://www.servicenow.com/community/cmdb-articles/sgc-aws-release-2-0-features/ta-p/2511663) on the ServiceNow Community site.

If you upgrade the connector, complete the following tasks before the upgrade process:

-   If there are any customizations, delete the records associated with the Service Graph Connector for AWS from the Customer Updates \[sys\_update\_xml\] table. See Customer Updates table.
-   Upgrade any dependencies.

After you've installed the latest version of the Service Graph Connector for AWS:

-   Perform a full import of data from your AWS instance. Verify that the **Use last run datetime** field value is cleared for all the AWS data sources in the Data Source \[sys\_data\_source\] table.
-   Download and rerun the AWS scripts. See [Configure the AWS environment](sgc-cmdb-aws-task-overview.md).

## Procedure

1.  Ensure that you’ve selected the **Service Graph Connector for AWS** application scope by using the application picker.

    For more information, see Application picker.

2.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **AWS** &gt; **Setup**.

3.  [Configure the AWS environment](sgc-cmdb-aws-task-overview.md).

    **Note:** For the Download the scripts task, select **Configure** to download the scripts.

    After you’ve downloaded the scripts and configured the AWS environment, set the Download the scripts and AWS Setup Instructions tasks to complete.

4.  Configure the authentication credentials to authenticate requests sent to the AWS APIs.

    1.  Configure your AWS credentials.

        1.  For the Configure the connection section of the Service Graph Connector for AWS page, select **Get Started**.
        2.  For the Configure the credentials task, select **Configure**.
        3.  In the **Name** field, enter a name for the authentication.

            `SG-AWS-Credentials-Org` is the default credential alias name. You can add multiple AWS instances. However, don’t modify the default connection alias.

        4.  Enter the access key ID and the secret access key in the **Access Key ID** and **Secret Access Key** fields respectively.

            The AWS access keys are long-term credentials for the IAM user and include two parts: an access key ID and a secret access key. You must use both the access key ID and the secret access key together to authenticate requests.

        5.  Return to the Configure the connection task page by selecting the back icon \(&lt;\).
        6.  Set the Configure the credentials task to complete by selecting **Mark as Complete**.
    2.  Test the AWS API connection to import data from the AWS application.

        1.  For the Test the connection task in the Configure the connection section, select **Configure**.
        2.  Select the **Test Connection** related link.
        3.  When the **Status** field is set to **Success**, select the back icon \(&lt;\) to return to the guided setup.
        4.  Set the Test the connection task to complete by selecting **Mark as Complete**.
    3.  Update the required configuration properties for an AWS instance.

        1.  For the Update configuration properties for instance task, select **Configure**.
        2.  On the SG-AWS Configuration Properties form that opens in a new tab, review, and modify the fields.

<table id="table_rxc_xrt_zzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Connection Details

</td></tr><tr><td>

Connection Alias

</td><td>

Name to identify the AWS connection record. For example, `SG_AWS_CredentialAlias_Org`. You can add multiple AWS instances. However, don’t modify the name for the default connection alias `SG_AWS_CredentialAlias_Org`.

</td></tr><tr><td class="sub-head" colspan="2">

Organization Details

</td></tr><tr><td>

Organization Account

</td><td>

Numeric account identifier of the AWS organization.

</td></tr><tr><td>

Organization Name

</td><td>

Name of the AWS organization.

</td></tr><tr><td>

Organization Description

</td><td>

Description of the AWS organization.

</td></tr><tr><td class="sub-head" colspan="2">

AWS Regions

</td></tr><tr><td>

Regions

</td><td>

AWS regions to collect the CI data.By default, the Service Graph Connector for AWS runs through all the AWS regions to collect the CI data.

You can enter AWS specific regions to speed up the CI data import process. For example, `us-east1, us-east-2`.

If this field is left empty, the Service Graph Connector for AWS pulls the resources from all the AWS regions.

However, for the AWS GovCloud regions, don’t leave the **Regions** field empty. The supported AWS GovCloud regions are `us-gov-east-1` and `us-gov-west-1`.

If you update the **Regions** field value later, clear the value of the **Last run datetime** field in all the data sources related to the Service Graph Connector for AWS to import a new set of data.

</td></tr><tr><td class="sub-head" colspan="2">

STS Assume Role Name

</td></tr><tr><td>

STS Role

</td><td>

AWS Identity and Access Management \(IAM\) role name that is obtained by the ServiceNow user by calling the AssumeRole API offered by the AWS Security Token Service \(STS\). The AssumeRole API returns a set of temporary security credentials for the ServiceNow user to access the AWS resources.**Note:** Enter the IAM role name but don’t prefix `arn` in the name. If you leave this field is empty, the value of this field is automatically set to **SnowOrganizationAccountAccessRole**, which is the default IAM role name for the ServiceNow user.

</td></tr><tr><td class="sub-head" colspan="2">

S3 Account Details

</td></tr><tr><td>

S3 Account Id

</td><td>

Numeric identifier of the AWS account that hosts the Amazon Simple Storage Service \(Amazon S3\) bucket.

</td></tr><tr><td>

S3 Bucket Name

</td><td>

Name of the Amazon S3 bucket that collects the details from Amazon EC2 instances.

</td></tr><tr><td>

S3 Region

</td><td>

Region where the Amazon S3 bucket resides.

</td></tr><tr><td class="sub-head" colspan="2">

SSM SendCommand Document Details

</td></tr><tr><td>

SSM Send Command Linux Name

</td><td>

Name of the document that defines the actions run by the AWS Systems Manager \(SSM\) on a Linux-based Amazon EC2 instance.

</td></tr><tr><td>

SSM Send Command Windows Name

</td><td>

Name of the document that defines the actions run by the AWS SSM on a Windows-based Amazon EC2 instance.

</td></tr><tr><td class="sub-head" colspan="2">

Management Account ID

</td></tr><tr><td>

Management Account ID

</td><td>

Management account in the AWS organization. The account calls the ListAccounts API associated with the AWS organization to collect CI information from all the accounts. For more information, see [ListAccounts](https://docs.aws.amazon.com/organizations/latest/APIReference/API_ListAccounts.html) on the AWS documentation site.Enter a value for this field when the ServiceNow user was created in an AWS member account.

</td></tr><tr><td class="sub-head" colspan="2">

Standalone Account ID Details

</td></tr><tr><td>

Standalone Account ID

</td><td>

ID of a member account in the AWS organization.**Note:** When specifying a standalone account, AWS organization-related data such as the organization name, organization units, organization ID, and service accounts are not imported. If you want to import the full data later, clear any value mentioned in the **Standalone Account ID** field. See the [Service Graph Connector for AWS - Standalone Setup \[KB1642159\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1642159) article in the Now Support Knowledge Base.

</td></tr><tr><td class="sub-head" colspan="2">

AWS Config Aggregator Details

</td></tr><tr><td>

Config Aggregator Account

</td><td>

AWS account where the aggregator resource type in the AWS Config service has been configured.Enter a value in this field when you’re using an AWS Config aggregator.

</td></tr><tr><td>

Config Aggregator Name

</td><td>

Name of the aggregator resource type. This field is available only when you enter a value in the **Config Aggregator Account** field.

</td></tr><tr><td>

Config Aggregator Region

</td><td>

Region where the aggregator resource type resides. This field is available only when you enter a value in the **Config Aggregator Account** field.

</td></tr><tr><td class="sub-head" colspan="2">

AWS Key Rotation Setup

</td></tr><tr><td>

AWS Rotate Keys

</td><td>

Option to enable the key rotation process.

</td></tr><tr><td>

AWS Key Rotation Date

</td><td>

Key rotation date. Set the value to the required key rotation date for the first run. For subsequent runs, this field is automatically set to the rotation date. This field is available only when you select the **AWS Rotate Keys** check box.

</td></tr><tr><td>

AWS Key Rotation Period \(in Days\)

</td><td>

Key rotation period in days. This field is available only when you select the **AWS Rotate Keys** check box.

</td></tr><tr><td>

AWS Key Rotation Status

</td><td>

Status message of a key rotation displaying whether the rotation was a success or a failure. This field is automatically set to display the key rotation status message. This field is available only when you select the **AWS Rotate Keys** check box. If the rotation status is a failure, an email notification is triggered, if configured.

</td></tr><tr><td>

Email accounts for receiving error notifications

</td><td>

Comma-separated list of the email addresses of recipients who receive notifications about the AWS key rotation errors.

</td></tr><tr><td>

Email account groups for receiving error notifications

</td><td>

Comma-separated list of the ServiceNow groups who receive notifications about the AWS key rotation errors.

</td></tr><tr><td class="sub-head" colspan="2">

Gov Cloud Setup

</td></tr><tr><td>

Is Gov Cloud

</td><td>

Option to indicate that the connection setup is for the AWS GovCloud.

</td></tr><tr><td class="sub-head" colspan="2">

SSM EKS SendCommand Document Details

</td></tr><tr><td>

EKS Cluster Names Document

</td><td>

Name of the AWS SSM document to discover EKS clusters associated with EC2 Bastion hosts.

</td></tr><tr><td>

EKS Shell Script Document

</td><td>

Name of the AWS SSM document to fetch CIs related to Kubernetes components, such as pods, services, and deployments, from EKS clusters.

</td></tr></tbody>
</table>        3.  Select **Save** and then **Close** to close the tab and return to the guided setup tab.
        4.  Set the Update configuration properties for instance task to complete by selecting **Mark as Complete**.
5.  Configure the required EC2 resources for Amazon Elastic Kubernetes Service \(EKS\) to import EKS cluster data.

    An EKS EC2 resource is a bastion host that has network access to EKS clusters. The EKS clusters aren't directly accessible to the connector. Therefore, you must provide the EKS EC2 resource details. For importing EKS cluster data, the connector uses the SSM Send Command on EKS EC2 resources to run kubectl commands remotely.

    **Note:** Ensure that you’ve configured your AWS environment for the EKS integration. For more information, see the [Service Graph Connector for AWS - Amazon EKS Integration \[KB1437138\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB1437138) article in the Now Support Knowledge Base.

    1.  For the Configure the EKS Resource Details section of the Service Graph Connector for AWS page, select **Get Started**.

    2.  For the Enter the EKS EC2 Resource Details task, select **Configure**.

    3.  On the form that opens in a new tab, fill in the fields.

<table id="table_dlp_xnv_1yb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

EKS EC2 Resource Id

</td><td>

Identifier of the EKS EC2 resource.

</td></tr><tr><td>

EC2 Account

</td><td>

User name assigned to the EKS EC2 resource account.

</td></tr><tr><td>

EC2 Region

</td><td>

AWS region where the EKS EC2 resource is located.

</td></tr><tr><td>

Active

</td><td>

Option to activate the EKS EC2 resource.**Note:** Set to false, if you are not using the EKS EC2 resource resource.

</td></tr><tr><td>

Connection

</td><td>

Connection alias associated with the AWS environment setup and configured in step [4.a](configure-aws-integration.md#aws-cred-0).

</td></tr></tbody>
</table>    4.  Select **Submit** to return to the guided setup.

    5.  Repeat steps from [5.b](configure-aws-integration.md#ec2) to [5.d](configure-aws-integration.md#ec2-end) to add multiple EKS EC2 resources.

        All the EKS EC2 resources are added to the SG-AWS-EKS-Master \[sn\_aws\_integ\_sg\_aws\_eks\_master\] table.

    6.  Set the Enter the EKS EC2 Resource Details task to complete by selecting **Mark as Complete**.

6.  Run the AWS diagnostic tool before running a scheduled import job to identify any issues in the AWS environment setup.

    1.  For the Service Graph AWS Diagnostic Tool section of the Service Graph Connector for AWS page, select **Get Started**.

    2.  For the AWS Setup Diagnostic Tool task, select **Configure**.

    3.  Select the organization ID from the text field.

    4.  Select **Run Diagnostic Test**.

        **Tip:** Select one of the following options to exclude the corresponding test results from the diagnostic summary:

        -   **Skip SSM setup tests**

            Excludes the software inventory data from the summary results by not calling the GetInventory API. Select this option when you’ve opted out or not set up the configuration for SSM.

        -   **Skip SSM Deep Discovery tests**

            Excludes the deep discovery data from the summary results. Select this option when you’ve opted out or not set up the configuration for SSM deep discovery.

        -   **Skip EKS setup tests**

            Excludes the EKS data from the summary results by not running the kubectl commands. Select this option when you’ve opted out or not set up the EKS integration.

    5.  View only EKS cluster test results by selecting **View EKS Test Details**.

    6.  Preview any previous diagnostic tool results by selecting **Load DT Results**, selecting a diagnostic ID, and then selecting **Load Results**.

    7.  When you finish reviewing the diagnostic summary results, select the back button of your browser to return to the guided setup.

    8.  Set the AWS Setup Diagnostic Tool task to complete by selecting **Mark as Complete**.

7.  Configure the scheduled jobs to import data from the AWS application.

    1.  In the Configure the scheduled import jobs section of the Service Graph Connector for AWS page, select **Get started**.

    2.  For the Configure the scheduled job task, select **Configure**.

    3.  Select the scheduled job that you want to activate.

    4.  On the Scheduled Data Import form, verify the field values for the scheduled job.

        For more information, see Schedule a data import.

    5.  Select **Update**.

    6.  Repeat the steps [7.c](configure-aws-integration.md#select-job) to [7.e](configure-aws-integration.md#exe-job) for each scheduled job for data import.

    7.  Select the back icon \(&lt;\) to return to the guided setup page.

    8.  Set the Configure the scheduled job task to complete by selecting **Mark as Complete** in the guided setup.

8.  Add multiple AWS instances.

    1.  In the Add Multiple Instances section of the Service Graph Connector for AWS page, select **Get Started**.

    2.  Ensure that you have edit permissions for the Datasource \[sys\_data\_source\] table to create data sources for the new instance.

        1.  Select the **Global** application scope by using the application picker.
        2.  For the Update Data Source Access task, select **Configure**.
        3.  In the Application Access related list, select the **Can create**, **Can update**, and **Can delete** check boxes, if not already selected.
        4.  Select **Update** to close the tab and return to the guided setup.
        5.  Modify the application scope again to **Service Graph Connector for AWS** by using the application picker.
        6.  Set the Update Data Source Access task to complete by selecting **Mark as Complete**.
    3.  Update access for scheduled import jobs.

        1.  Select the **Global** application scope by using the application picker.
        2.  For the Update Scheduled Data Import Access task, select **Configure**.
        3.  In the Application Access related list, select the **Can create**, **Can update**, and **Can delete** check boxes, if not already selected.
        4.  Select **Update** to close the tab and return to the guided setup tab.
        5.  Set the Update Scheduled Data Import Access task to complete by selecting **Mark as Complete**.
        6.  Modify the application scope again to **Service Graph Connector for AWS** by using the application picker.
    4.  Clear the cache of the Data Source \[sys\_data\_source\] and Scheduled Data Imports \[scheduled\_import\_set\] tables to enable creating a data source for the new connection in the Service Graph Connector for AWS.

        1.  For the Clear Cache for Data Source and Scheduled Data Imports tables task, select **Configure**.
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
        5.  Set the Clear Cache for Data Source and Scheduled Data Imports tables task to complete by selecting **Mark as Complete**.
        6.  Modify the application scope again to **Service Graph Connector for AWS** by using the application picker.
    5.  Create a credential alias for the new AWS connection in the Service Graph Connector for AWS.

        1.  For the Create new Connection &amp; Credentials Alias Record task, select **Configure**.
        2.  On the Connection &amp; Credential Aliases form that opens in a new tab, fill in the connection details.
        3.  Select **Submit** and close the tab and return to the guided setup tab.
        4.  Set the Create new Connection &amp; Credentials Alias Record task to complete by selecting **Mark as Complete**.
    6.  Create credentials for the new AWS credential alias.

        1.  For the Create new Connection &amp; Credentials Alias Record task, select **Configure**.
        2.  On the Connections page of the Workflow Studio, select **Add Connection**.
        3.  In the Create Connection window, fill in the connection name, access key, and secret key details.
        4.  Select **Create Connection**.
        5.  Close the Workflow Studio and return to the guided setup tab.
        6.  Set the Create new Connection &amp; Credentials Alias Record task to complete by selecting **Mark as Complete**.
    7.  Update properties for the new instance for the Service Graph Connector for AWS by selecting **Configure** for the Configure AWS environment for the new Instance task.

        For more information, follow the step [4.c](configure-aws-integration.md#aws-prop) discussed earlier for configuring the properties of the AWS connection available by default.

        When you're done updating the properties, set the Configure AWS environment for the new Instance task to complete by selecting **Mark as Complete**.

    8.  Enter the EKS EC2 Resource details by selecting **Configure** for the Update EKS Resource Details task.

        For more information, follow the step [5](configure-aws-integration.md#step-eks) discussed earlier for configuring the EKS EC2 Resource details for the AWS connection available by default.

        When you're done updating the properties, set the Update EKS Resource Details task to complete by selecting **Mark as Complete**.

    9.  Configure the scheduled imports for the new AWS instance.

        1.  For the Configure the Scheduled Imports task, select **Configure**.
        2.  In the Scheduled Data Imports list that opens in a new tab, select the organization of the AWS instance that you want to configure.
        3.  Select the scheduled data import that you want to activate.
        4.  On the Scheduled Data Import form, modify the field values for the scheduled job.
        5.  Select **Update**.
        6.  Repeat the steps [8.i.iii](configure-aws-integration.md#new-import-1) to [8.i.v](configure-aws-integration.md#new-import-2) for each scheduled job for data import.
        7.  Close the tab for the Scheduled Data Imports list and return to the guided setup tab.
        8.  Set the Configure the Scheduled Imports task to complete by selecting **Mark as Complete** in the guided setup.

**Related topics**  


[Handling import failures for large AWS resources](../concept/sgc-cmdb-aws-large-data-vol.md)

[Handling memory utilization errors for Service Graph Connector for AWS](../concept/sgc-cmdb-aws-memory.md)

