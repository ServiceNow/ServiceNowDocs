---
title: Executing scripts required for setting up AWS
description: You must execute scripts provided with the Service Graph Connector for AWS to set up the AWS environment for importing data.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [Service Graph Connector for AWS, Service Graph Connector for AWS scripts]
breadcrumb: [Configure the AWS environment, AWS, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Executing scripts required for setting up AWS

You must execute scripts provided with the Service Graph Connector for AWS to set up the AWS environment for importing data.

**Important:** Before executing an AWS script, ensure that you have completed the prerequisites. See [Prerequisites for executing scripts](sgc-cmdb-aws-scripts-prereq.md#).

The AWS scripts provided with the connector configure AWS resources to import the configuration items \(CIs\) data into the CMDB. To learn more, see [AWS resources used by the Service Graph Connector for AWS](sgc-cmdb-aws-concepts.md).

Based on the AWS environment requirements, the scripts provided with the Service Graph Connector for AWS are categorized as described in the following table.

<table id="table_w2k_kkm_4zb" class="nav-card"><tbody><tr><td>

[Basic scripts![](../../../reuse/icons/brand-icons/bus-optimize-manage.svg)Scripts for configuring the AWS environment to import data by using the connector.](sgc-cmdb-aws-script-op.md#section_vfh_wyf_4zb)

</td><td>

[Deep discovery scripts![](../../../reuse/icons/brand-icons/bus-discover.svg)Scripts for setting up deep discovery on Amazon Elastic Compute Cloud \(Amazon EC2\) instances.](sgc-cmdb-aws-script-op.md#section_ahc_jwf_4zb)

</td><td>

[Amazon EKS scripts![](../../../reuse/icons/brand-icons/bus-service-aware-cmdb.svg)Scripts for setting up Amazon Elastic Kubernetes Service \(EKS\) clusters.](sgc-cmdb-aws-script-op.md#section_osh_4zf_4zb)

</td></tr></tbody>
</table>## Basic scripts

Use the basic scripts to configure the AWS environment for importing data using the Service Graph Connector for AWS.

The following table describes the basic AWS scripts available with the connector, the input parameters entered when executing a script, the conditions to execute the scripts, and the script execution results.

<table id="table_jw4_yyf_4zb" class="custom-rows"><thead><tr><th class="filter">

Script

</th><th>

Input parameters

</th><th>

Execution condition

</th><th class="filter">

Result

</th></tr></thead><tbody><tr><td>

EnableAWSConfig.yml

</td><td>

None

</td><td>

Execute the script in all the AWS accounts and AWS regions by creating a CloudFormation StackSet in the management account.

 See [Create a stack set](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-getting-started-create.html) on the AWS documentation site.

</td><td>

Enables the AWS Config recorder.

</td></tr><tr><td>

CreateServiceNowUser.yml

</td><td>

-   **SNUserName**

Name of the ServiceNow IAM user that was created as part of the setup. See [Prerequisites for executing scripts](sgc-cmdb-aws-scripts-prereq.md#).

Default value: `NOWSGCUser`

-   **MbrActRoleName**

Name of the ServiceNow IAM role that was created as part of the setup. See [Prerequisites for executing scripts](sgc-cmdb-aws-scripts-prereq.md#).

Default value: `SnowOrganizationAccountAccessRole`


</td><td>

Execute the script by creating a stack either in the management account or in a designated member account.

 See [Creating a stack on the AWS CloudFormation console](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-console-create-stack.html) on the AWS documentation site.

</td><td>

Creates the ServiceNow IAM user.

</td></tr><tr><td>

CreateSnowOrganizationAccountAccessRoleInMemberAccount.yml

</td><td>

-   **ACNNBR**

Management account ID when the ServiceNow IAM user is in a management account

Or

Designated member account ID when the ServiceNow IAM user is in a designated member account.

-   **S3Bucket**

Amazon S3 bucket name to get the `SendCommand` output.

-   **ServiceNowUserName**

Name of the ServiceNow IAM user that was created as part of the setup. See [Prerequisites for executing scripts](sgc-cmdb-aws-scripts-prereq.md#).

Default value: `NOWSGCUser`


</td><td>

Execute the script in all the AWS accounts by creating a CloudFormation StackSet in the management account.

 See [Create a stack set](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-getting-started-create.html) on the AWS documentation site.

</td><td>

Enables read-only IAM policies, roles, and groups for the ServiceNow IAM user.

</td></tr><tr><td>

SnowDesignatedAccountAccessRoleInManagementAccount.yml

</td><td>

-   **MEMBERACTNBR**

Member account ID where the ServiceNow IAM user was created.


</td><td>

Execute the script by creating a stack in the management account.

 See [Creating a stack on the AWS CloudFormation console](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-console-create-stack.html) on the AWS documentation site.

 **Note:** Use the `SnowDesignatedAccountAccessRoleInManagementAccount.yml` script only when the ServiceNow IAM user was created in a member account.

</td><td>

Creates the ServiceNow IAM role in the management account.

</td></tr><tr><td>

AWS-SystemsManager-AutomationExecutionRole.yml

</td><td>

None

</td><td>

Execute the script in all the AWS accounts by creating a CloudFormation StackSet in the management account.

 See [Create a stack set](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-getting-started-create.html) on the AWS documentation site.

</td><td>

Provisions the execution role necessary to run automations in member accounts. A prerequisite for configuring Systems Manager Automation.

</td></tr><tr><td>

AWS-SystemsManager-AutomationAdministrationRole.yml

</td><td>

None

</td><td>

Execute the script by creating a stack in the management account.

 See [Creating a stack on the AWS CloudFormation console](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-console-create-stack.html) on the AWS documentation site.

</td><td>

Provisions the administrator role in the management account necessary to run cross-account automation across multiple accounts. A prerequisite for configuring Systems Manager Automation.

</td></tr></tbody>
</table>## Deep discovery scripts

Use the deep discovery scripts to set up deep discovery on Amazon EC2 instances.

**Note:** Execute the deep discovery scripts only when you want to perform deep discovery on EC2 instances.

The following table describes the deep discovery scripts, the input parameters entered when executing a script, the conditions to execute the scripts, and the script execution results.

<table id="table_fjg_vs4_jzb"><thead><tr><th>

Script

</th><th>

Input parameters

</th><th>

Execution condition

</th><th>

Result

</th></tr></thead><tbody><tr><td>

AmazonSSMForInstancesRoleSetup.yml

</td><td>

-   **S3Bucket**

S3 bucket name that collects the details from EC2 instances. See [Prerequisites for executing scripts](sgc-cmdb-aws-scripts-prereq.md#).


</td><td>

Execute the script in all the AWS accounts by creating a CloudFormation StackSet in the management account.

 See [Create a stack set](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-getting-started-create.html) on the AWS documentation site.

</td><td>

Creates the AmazonSSMForInstancesRole IAM instance profile role to be attached to the EC2 instances.

</td></tr><tr><td>

SG-AWS-RunShellScript-Setup.yml

</td><td>

None

</td><td>

Execute the script in all the AWS accounts and the AWS regions by creating a CloudFormation StackSet in the management account.

 AWS administrators must update SSM documents and verify that EC2 instances can execute relevant commands for proper integration.

 See [Create a stack set](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-getting-started-create.html) on the AWS documentation site.

</td><td>

Creates AWS Systems Manager \(SSM\) documents to fetch deep discovery data from a Linux EC2 instance.Retrieves version details for middleware applications, including Apache HTTP server, Nginx server, Apache Tomcat server, and MySQL instance.

</td></tr><tr><td>

SG-AWS-RunPowerShellScript-Setup.yml

</td><td>

None

</td><td>

Execute the script in all the AWS accounts and the AWS regions by creating a CloudFormation StackSet in the management account.

 See [Create a stack set](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-getting-started-create.html) on the AWS documentation site.

</td><td>

Creates AWS SSM documents to fetch deep discovery data from a Windows EC2 instance.

</td></tr></tbody>
</table>## Amazon EKS scripts

Use the Amazon EKS scripts to set up Amazon Elastic Kubernetes Service \(EKS\) clusters.

**Note:** Execute the Amazon EKS scripts only when the Amazon EKS service for Kubernetes clusters is required.

The following table describes the Amazon EKS scripts, the conditions to execute the scripts, and the script execution results.

<table id="table_psh_4zf_4zb"><thead><tr><th>

Script

</th><th>

Execution condition

</th><th>

Result

</th></tr></thead><tbody><tr><td>

SG-AWS-RunKubeCtlEKSNamesShellScript.yml

</td><td>

Execute the script in all the AWS accounts and the AWS regions where the EC2 Bastion hosts are located by creating a CloudFormation StackSet in the management account.

 See [Create a stack set](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-getting-started-create.html) on the AWS documentation site.

</td><td>

Creates an AWS SSM document to discover EKS clusters associated with EC2 Bastion hosts.

 **Note:** An AWS Cloud administrator can update the SSM document in their AWS setup.

</td></tr><tr><td>

SG-AWS-RunKubeCtlShellScript.yml

</td><td>

Execute the script in all the AWS accounts and the AWS regions where the EC2 Bastion hosts are located by creating a CloudFormation StackSet in the management account.

 See [Create a stack set](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-getting-started-create.html) on the AWS documentation site.

</td><td>

Creates an AWS SSM document to fetch CIs related to Kubernetes components, such as pods, services, and deployments, from EKS clusters.

 **Note:** An AWS Cloud administrator can update the SSM document in their AWS setup.

</td></tr></tbody>
</table>