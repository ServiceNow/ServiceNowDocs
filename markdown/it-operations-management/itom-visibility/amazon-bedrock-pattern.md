---
title: Amazon Bedrock pattern-based discovery
description: AI Agent Topology Mapping discovers Amazon Bedrock AI services and agents during horizontal discovery.
locale: en-US
release: zurich
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 10
keywords: [Amazon Bedrock, AI Agent Topology Mapping, AWS Bedrock, AI discovery]
breadcrumb: [Reference, AI Agent Topology Mapping, ITOM Visibility, IT Operations Management]
---

# Amazon Bedrock pattern-based discovery

AI Agent Topology Mapping discovers Amazon Bedrock AI services and agents during horizontal discovery.

## Request new or enhanced Patterns on the ServiceNow® Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/06a71b1367e4130051c9027e2685ef1e/1.6.0?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%26q%3DPatterns&sl=sh) to view all the available updates and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Amazon Bedrock data model

The following diagram illustrates the tables and relationships that the AI Agent Topology Mapping application creates when discovering Amazon Bedrock resources.

![Amazon Bedrock data model](../images/amazon-bedrock-data-model.png "Tables and relationships populated during Amazon Bedrock discovery")

**Note:** The **Deployed as::Deployment of** relationship between the AI Function \[cmdb\_ci\_function\_ai\] and AI System Digital Asset \[alm\_ai\_system\_digital\_asset\] tables is stored in the Asset-CI Relationship \[cmdb\_rel\_asset\_ci\] table and isn't represented in the Dependency View map.

## Discovery requirements

-   **Verify that the applications are up to date**

    Discovering these resources may require updating to the latest version of the following applications from the ServiceNow Store:

    -   AI Agent Topology Mapping
    -   Discovery and Service Mapping Patterns
    -   Visibility Content
    -   CMDB CI Class Models
-   **Update the method used for pointed discovery for the AWS CloudFormation Template \(CFT\) stack**

    If you use Cloud Provisioning and Governance, you must update the **getOperationGR\(type\)** method. This update enables the pointed discovery to list the resources correctly for the AWS CFT stack after provisioning. For further information about the steps required to update this method, see the Knowledge Base article [KB0858437](https://support.servicenow.com/nav_to.do?uri=kb_knowledge.do?sys_id=54ecb719db1f1cd0fb115583ca961917).

-   **Activate the cloud-related CI relationships**

    To include discovered components into service instances, enable CI relationships used in tag-based discovery by Service Mapping. These CI relationships are available from the 1.0.68 release on the ServiceNow Store. For operational steps, see [Tag-based discovery configuration](../../service-mapping/concept/tag_discovery_configuration.md).

-   **Set up service accounts on the AWS Management Console**

    An AWS Organization is a collection of AWS accounts under a single account. In AWS Organizations, parent accounts are called management accounts. The sub-accounts that belong to a management account are called member accounts.

    The advantages of using management accounts in Discovery are:

    -   **Easy population of member accounts**

        After you configure the management account and supply the necessary credentials, you can test the connection to the account. If the test succeeds, Discovery returns a list of the member accounts in that management account. From this list, you can choose one or more member to include in the Discovery of the management account.

    -   **\(Optional\) Discover member resources using dynamically acquired credentials**

        When you run Discovery on your cloud resources, you don’t need separate credentials for each member account. The Cloud Discovery process handles credentials automatically by acquiring a temporary credential for each member via an AWS API. You can elect to use the default configuration or customize the MID Server to assume other roles for additional controls and security.

    For more information, see [Setting up AWS service accounts](../../it-operations-management/concept/setup-aws-service-accounts.md).

-   **Use IAM user policy on the AWS Management Console**

    To use the IAM user policy instead of credentials during discovery, configure the MID Server for AWS IAM roles. For more information, see [configure the MID Server for AWS IAM roles](../../it-operations-management/task/config-mid-iam-roles.md).

    To create the IAM user policy for provisioning AWS resources, see [Control AWS access and permissions using policies](../../it-operations-management/task/aws-create-user-policy-cloud-mgt.md). Ensure that the IAM user policy covers the following AWS resources:

    ```
    {
        "Version": "2012-10-17",
        "Statement": [
            {
                "Action": [
            "elasticloadbalancing:DescribeLoadBalancerPolicyTypes",
            "elasticloadbalancing:DescribeLoadBalancers",
            "elasticloadbalancing:DescribeLoadBalancerPolicies",
            "elasticloadbalancing:DescribeInstanceHealth",
            "elasticloadbalancing:DescribeTags",
            "elasticloadbalancing:DescribeLoadBalancerAttributes",
            "account:ListRegions",
            "elasticloadbalancing:Describe*",
            "ec2:Describe*",
            "ec2:DescribeNetworkInterfaceAttribute",
            "ec2:DescribeInstanceStatus",
            "ec2:DescribeCustomerGateways",
            "ec2:DescribeSecurityGroups",
            "ec2:DescribeHosts",
            "ec2:DescribeImages",
            "ec2:DescribeVpcs",
            "ec2:DescribeAccountAttributes",
            "ec2:DescribeInstanceAttribute",
            "ec2:DescribeInstanceCreditSpecifications",
           
                ],
                "Effect": "Allow",
                "Resource": "*"
            }
        ]
    }
    
    ```

-   **Configure access to the AWS resources**

    To discover a single account, create an IAM account in the AWS Management Console, and ensure that it has the "ReadOnlyAccess" policy applied. To discover several member or child accounts, configure the credentials as described in [Access setup for AWS service accounts](../../it-operations-management/concept/access-aws-accounts.md).

-   **Configure the Discovery schedule to support GovCloud**

    Discovering AWS GovCloud \(US\) accounts requires using a datacenter URL when setting up an AWS service account. For more information, see [Create AWS service accounts](../../it-operations-management/task/create-aws-service-accounts.md).

-   **Configure a discovery schedule**

    [Create an AWS Discovery schedule in Discovery Admin Workspace](../../discovery/task/create-AWS-schedule-DAW.md).

-   **\(Optional\) Discover datacenters only for new members**

    Starting with Zurich Patch 2, you can discover datacenters only for new members added since the last discovery. For more information, see [Discover datacenters only for new cloud accounts](../../service-mapping/task/discover-datacenter-only-new-account.md).

-   **Optimize discovery by including only datacenters with resources**

    Starting with Discovery and Service Mapping Patterns version 1.29.0, you can optimize discovery by limiting it to only AWS datacenters with resources.

    -   Verify your service account has the following role permissions to access Config API:
        -   `config:GetDiscoveredResourceCounts`
        -   `config:DescribeConfigurationRecorderStatus`
    -   Verify AWS Config recorder is enabled and configured to record the all resource types.

        For instructions on configuring AWS Config recorder, go to the [AWS Documentation](https://docs.aws.amazon.com/) and search for the "Recording resources in the AWS Config console" article.

    -   Enable discovery of only datacenters with resources by setting the **mid.cloud.discovery.sonar.discover\_all\_aws\_datacenters** MID Server property to **false**. For more information, see [Limit AWS discovery to datacenters with resources](../../service-mapping/task/limit-aws-discovery-active-datacenter.md).
    For more information, see the **AWS resources discovery by datacenters** section in [AWS discovery using patterns](../../discovery/reference/data-discovered-aws-patterns.md).

-   **\(Optional\) Populate Service Account and Logical Datacenter fields in cloud CIs**

    Starting with Discovery and Service Mapping Patterns version 1.30.2, you can improve query performance by populating Service Account and Logical Datacenter fields directly in cloud CIs. For more information, see [Improved query performance with direct field population in CI tables](../../service-mapping/concept/query-service-account-ldc-fields.md).


## Verify the REST API Permissions

Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

## Data collection

The Amazon AWS - Bedrock Agents pattern collects AI System Digital Assets, AI Prompt Digital Assets, and Key Value information. You can view this information in the **Related Links** section of the CI record by navigating to **All** &gt; **Configuration** &gt; **AWS** &gt; **AWS Bedrock Agents** and selecting the relevant record.

AI Agent Topology Mapping application populates data in both CMDB and non-CMDB tables.

## Data stored in non-CMDB tables

The AI Agent Topology Mapping application populates data in non-CMDB tables when running the Amazon AWS - Bedrock Agents pattern.

If you have the AI Control Tower application, you can view the information in the AI Control Tower Workspace.

|Field|Description|
|-----|-----------|
|Display name \[display\_name\]|Display name of the Bedrock agent.|
|External record reference \[external\_ref\_id\]|Amazon Resource Name \(ARN\) of the Bedrock agent.|
|Model \[model\]|References the AI System Component Product Model \[cmdb\_ai\_system\_component\_product\_model\] table.|
|Asset type \[model\_category\]|Asset type of the agent. Value is set to **Agentic AI**.|
|State \[install\_status\]|State of the agent. Value is set to **Deployed**.|
|AI prompts \[ai\_prompts\]|References the AI Prompt Digital Asset \[alm\_ai\_prompt\_digital\_asset\] table.|
|AI models \[ai\_models\]|References the AI Model Digital Asset \[alm\_ai\_model\_digital\_asset\] table.|
|Configuration Item \[ci\]|References the AI Function \[cmdb\_ci\_function\_ai\] table.|

<table id="table_cmdb_ai_system_component"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the Bedrock agent.

</td></tr><tr><td>

Short description \[short\_description\]

</td><td>

Description of the Bedrock agent.

</td></tr><tr><td>

Status \[status\]

</td><td>

Operational status of the agent as returned by Bedrock. For example: PREPARED.

</td></tr><tr><td>

Version \[version\]

</td><td>

Version of the Bedrock agent.

</td></tr><tr><td>

Manufacturer \[manufacturer\]

</td><td>

Manufacturer of the agent model. Value is set to **AWS**.

</td></tr><tr><td>

Model categories \[cmdb\_model\_category\]

</td><td>

Model category. Value is set to **Agentic AI**.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Prompt information \[prompt\_info\]|Instruction text defined for the Bedrock agent.|
|Model \[model\]|References the AI Prompt Product Model \[cmdb\_ai\_prompt\_product\_model\] table.|
|Asset type \[model\_category\]|Asset type of the prompt. Value is set to **AI prompt**.|
|Configuration Item \[ci\]|References the AI Function \[cmdb\_ci\_function\_ai\] table.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the Bedrock agent, used to identify the associated prompt model.|
|Manufacturer \[manufacturer\]|Manufacturer of the prompt model. Value is set to **AWS**.|

|Field|Description|
|-----|-----------|
|Display name \[display\_name\]|Name of the foundation model.|
|External record reference \[external\_ref\_id\]|ARN of the foundation model.|
|Model \[model\]|References the AI Model Product Model \[cmdb\_ai\_model\_product\_model\] table.|
|Asset type \[model\_category\]|Asset type of the model. Value is set to **AI model**.|
|Vendor \[vendor\]|Provider of the foundation model.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the foundation model.|
|Model number \[model\_number\]|Model ID assigned by Amazon Bedrock.|
|Manufacturer \[manufacturer\]|Provider of the foundation model.|
|Model categories \[cmdb\_model\_category\]|Model category. Value is set to **AI model**.|

## Data stored in CMDB tables

AI Agent Topology Mapping populates the data in the CMDB when running the Amazon AWS - Bedrock Agents pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the Bedrock agent.|
|Object ID \[object\_id\]|ARN of the Bedrock agent.|
|Description \[short\_description\]|Description of the Bedrock agent.|
|Model number \[model\_number\]|Agent ID assigned by Amazon Bedrock.|
|Operational status \[operational\_status\]|Operational status of the resource. Default value is set to Operational.|
|Install Status \[install\_status\]|Install status of the resource. Default value is set to Installed.|
|Product instance identifier \[product\_instance\_id\]|Version of the Bedrock agent.|
|Comments \[comments\]|Resource type identifier. Value is set to **AWS::Bedrock::Agent**.|
|Manufacturer \[manufacturer\]|Manufacturer of the resource. Value is set to **AWS**.|

## Dependency Views map

On the Dependency Views map, you can view discovered Amazon Bedrock resources and the relationships between them.

![Amazon Bedrock AI Function CI and connection on a Dependency Views map](../images/amazon-bedrock-ai-function-dependency-view.png "AI Function dependency view")

## CI relationships

The Amazon AWS - Bedrock Agents pattern creates the following relationships to support Amazon Bedrock discovery.

|CI/Table|Relationship|CI/Table|
|--------|------------|--------|
|AI Function \[cmdb\_ci\_function\_ai\]|Deployed as::Deployment of|AI System Digital Asset \[alm\_ai\_system\_digital\_asset\]|
|AI Function \[cmdb\_ci\_function\_ai\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|AI System Digital Asset \[alm\_ai\_system\_digital\_asset\]|References|AI System Component Product Model \[cmdb\_ai\_system\_component\_product\_model\]|
|AI System Digital Asset \[alm\_ai\_system\_digital\_asset\]|References|AI Prompt Digital Asset \[alm\_ai\_prompt\_digital\_asset\]|
|AI System Digital Asset \[alm\_ai\_system\_digital\_asset\]|References|AI Model Digital Asset \[alm\_ai\_model\_digital\_asset\]|
|AI System Digital Asset \[alm\_ai\_system\_digital\_asset\]|References|AI Function \[cmdb\_ci\_function\_ai\]|
|AI Prompt Digital Asset \[alm\_ai\_prompt\_digital\_asset\]|References|AI Prompt Product Model \[cmdb\_ai\_prompt\_product\_model\]|
|AI Prompt Digital Asset \[alm\_ai\_prompt\_digital\_asset\]|References|AI Function \[cmdb\_ci\_function\_ai\]|
|AI Model Digital Asset \[alm\_ai\_model\_digital\_asset\]|References|AI Model Product Model \[cmdb\_ai\_model\_product\_model\]|
|Key Value \[cmdb\_key\_value\]|References|AI Function \[cmdb\_ci\_function\_ai\]|

## AWS tag discovery

The Amazon AWS - Bedrock Agents pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the AI Function \[cmdb\_ci\_function\_ai\] table.|

**Parent Topic:**[AI Agent Topology Mapping reference](ai-agent-topology-mapping-reference.md)

**Related topics**  


[AWS discovery using patterns](../../discovery/reference/data-discovered-aws-patterns.md)

