---
title: AWS discovery using patterns
description: Discovery and Service Mapping Patterns uses patterns to discover components of the Amazon AWS Cloud deployment during horizontal discovery. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 37
keywords: [Amazon, AWS, Cloud, Patterns, Discovery]
breadcrumb: [Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS discovery using patterns

Discovery and Service Mapping Patterns uses patterns to discover components of the Amazon AWS Cloud deployment during horizontal discovery. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Verify that the applications are up to date:**
    -   Discovery and Service Mapping Patterns
    -   CMDB CI Class Models
    -   Visibility Content
-   **Update the method used for pointed discovery for the AWS CloudFormation Template \(CFT\) stack**

    If you use Cloud Provisioning and Governance, you must update the **getOperationGR\(type\)** method. This update enables the pointed discovery to list the resources correctly for the AWS CFT stack after provisioning. For further information about the steps required to update this method, see the Knowledge Base article [KB0858437](https://support.servicenow.com/nav_to.do?uri=kb_knowledge.do?sys_id=54ecb719db1f1cd0fb115583ca961917).

-   **Activate the cloud-related CI relationships**

    To include discovered components into service instances, enable CI relationships used in tag-based discovery by Service Mapping. These CI relationships are available from the 1.0.68 release on the ServiceNow Store. For operational steps, see [Tag-based discovery configuration](../../service-mapping/concept/tag_discovery_configuration.md).

-   **Set up service accounts on the AWS Management Console**

    An AWS Organization is a collection of AWS accounts under a single account. In AWS Organizations, parent accounts are called management accounts. The sub-accounts that belong to a management account are called member accounts.

    **Note:** Cloud Discovery for AWS Organizations isn’t fully supported in a [GovCloud](https://docs.aws.amazon.com/govcloud-us/latest/UserGuide/whatis.html) isolated region.

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

-   **Configure a discovery schedule**

    [Create an AWS Discovery schedule in Discovery Admin Workspace](../task/create-AWS-schedule-DAW.md).

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
    For more information, see the **AWS resources discovery by datacenters** section.

-   **\(Optional\) Populate Service Account and Logical Datacenter fields in cloud CIs**

    Starting with Discovery and Service Mapping Patterns version 1.30.2, you can improve query performance by populating Service Account and Logical Datacenter fields directly in cloud CIs. For more information, see [Improved query performance with direct field population in CI tables](../../service-mapping/concept/query-service-account-ldc-fields.md).


## Verify the REST API Permissions

Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

**Note:** You can test the AWS REST APIs using Postman API platform. For more information, see the [How to test AWS REST API using POSTMAN \[KB0782183\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0782183) article in the Now Support Knowledge Base.

## Support for AWS services in the China region

The latest version of Discovery and Service Mapping Patterns supports discovering AWS services in the China region. You can discover these services on the ServiceNow AI Platform, starting from Xanadu Patch 3 and Washington DC Patch 9 instances.

Discovering AWS services in the China region requires using a datacenter URL when setting up an AWS service account. For example: `https://organizations.cn-northwest-1.amazonaws.com.cn`.

-   To learn more about AWS master account and sub-account support in the China region, see [KB1704526](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1704526).
-   To identify AWS patterns supported in the China region, refer to the Cloud Discovery patterns spreadsheet. The **AWS China Region Support** column has a Yes value for supported patterns.

## AWS resources discovery by datacenters

Starting with version 1.29.0, Discovery and Service Mapping Patterns introduces a new AWS datacenter discovery model. The previous model discovered all datacenters, regardless of whether they contained relevant resources. The new model improves the AWS discovery performance by focusing on only datacenters that contain resources.

AWS has multiple datacenters around the world, but resources like load balancers and virtual machines are typically deployed in only some of them. The **Amazon AWS Datacenter Discovery** pattern runs before all other AWS patterns to identify datacenters with resources related to your service account \("active"\) and those without \("passive"\). A datacenter can also be classified as "empty" due to API call errors, AWS Config service not being enabled, or permission issues. You can check the discovery log for the exact cause of the error. For more information, see [Logs for horizontal discovery](r_DiscoveryLog.md#).

After identifying "active", "passive", or "empty" datacenters, the discovery schedule continues to execute all AWS patterns only for "active" or "empty" datacenters, to discover your AWS cloud resources. "Passive" datacenters are ignored during the schedule. The **Refresh Datacenters** flow continues to display all regions, not just active ones. You don’t need to create another schedule when a resource is added or a datacenter switches from passive to active.

You might notice differences in the AWS discovery log, in discovery time and in the CMDB, depending on the service account and MID Server property settings.

Datacenters that have already been discovered before upgrading to Discovery and Service Mapping Patterns version 1.29.0 remain in the **Amazon AWS Datacenters** table. The **mid.cloud.discovery.sonar.discover\_all\_aws\_datacenters** MID Server property is set to **true** by default, which discovers all datacenters. To limit discovery to the "active" or "empty" datacenters, set this property to **false**. For information on setting up active datacenter discovery, see the **\(optional\) Optimize discovery by including only datacenters with resources** prerequisite.

|MID Server property setting|Flow|Discovered/displayed datacenters|
|---------------------------|----|--------------------------------|
|False|New schedule|All datacenters except passive|
|False|Refresh Datacenters|All datacenters|
|True \(default\)|New schedule|All datacenters|
|True \(default\)|Refresh Datacenters|All datacenters|

![Comparing MID Server property settings and discovered datacenters in schedule and refresh datacenter flows](../../service-mapping/image/aws-datacenter-model-flow.png "AWS datacenter model flow by mid.cloud.discovery.sonar.discover_all_aws_datacenters MID Server property setting")

## Data collected by Discovery during horizontal discovery

-   **Resources discovered using the Amazon AWS - ACL \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|Name of the network access control list \(ACL\).|
    |Object ID \[object\_id\]|Unique identifier, allocated by Amazon AWS Cloud for this resource.|

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|Name of the endpoint.|
    |Object ID \[object\_id\]|Unique identifier, allocated by Amazon AWS Cloud for this resource.|

-   **Resources discovered using the Amazon AWS - Application and Network LB \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|Name of the load balancer.|
    |Fully Qualified Domain Name \[fqdn\]|IP address of the fully qualified domain name of the load balancer.|
    |Object ID \[object\_id\]|The Amazon Resource Name \(ARN\) of the load balancer.|
    |DNS Name \[dns\_name\]|The public DNS name of the load balancer.|
    |Canonical Hosted Zone Name \[canonical\_hosted\_zone\_name\]|The name of the Amazon Route 53 hosted zone associated with the load balancer.|
    |Canonical Hosted Zone ID \[canonical\_hosted\_zone\_id\]|The ID of the Amazon Route 53 hosted zone associated with the load balancer.|
    |State \[state\]|The state of the load balancer.|
    |Short Description \[short\_description\]|A concatenation of the series of attributes for the load balancers like LB ARN, VPC ID, Type, and Zone.|
    |Comments \[comments\]|Identifier for internal usage \(deletion strategy\).|

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|Name of the Domain Name System \(DNS\).|
    |Object ID \[object\_id\]|Name of the DNS.|
    |IP Address \[ip\_address\]|IP address of the DNS.|
    |Comments \[comments\]|Identifier for internal usage \(deletion strategy\).|

-   **Resources discovered using the Amazon AWS - Availability Zone \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|Name of the Availability Zone.|
    |Object ID \[object\_id\]|Unique identifier, allocated by Amazon AWS Cloud for this resource.|
    |State \[state\]|The state of the Availability Zone. The possible values are: available, information, impaired, and unavailable.|

-   **Resources discovered using the Amazon AWS - Classic LB \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The name of the load balancer.|
    |Fully Qualified Domain Name \[fqdn\]|The DNS name of the load balancer.|
    |Object ID \[object\_id\]|Unique identifier, allocated by Amazon AWS Cloud for this resource.|
    |DNS Name \[dns\_name\]|The DNS name of the load balancer.|
    |Canonical Hosted Zone Name \[canonical\_hosted\_zone\_name\]|The DNS name of the load balancer.|
    |Canonical Hosted Zone ID \[canonical\_hosted\_zone\_id\]|The ID of the Amazon Route 53 hosted zone for the load balancer.|

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|IP address of the Load Balancer.|
    |Object ID \[object\_id\]|IP address of the Load Balancer.|
    |IP Address \[ip\_address\]|IP address of the Load Balancer.|
    |Comments \[comments\]|Comments related to the Configuration Item \(CI\).|

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|Name of the Domain Name System \(DNS\).|
    |IP Address \[ip\_address\]|IP address of the DNS.|
    |Comments \[comments\]|Comments related to the CI.|

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The name of the load balancer pool.|
    |Object ID \[object\_id\]|Unique identifier, allocated by Amazon AWS Cloud for this resource.|
    |Comments \[comments\]|Comments related to the CI.|

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The name of the load balancer pool member \(known in AWS as a target\).|
    |Object ID \[object\_id\]|Unique identifier, allocated by Amazon AWS Cloud for this resource.|

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|Name of the load balancer service.|
    |Object ID \[object\_id\]|Unique identifier, allocated by Amazon AWS Cloud for this resource.|
    |Port \[port\]|The port on which the load balancer is listening.|
    |Service Port \[service\_port\]|The port on which the instance is listening.|
    |Server Protocol \[service\_protocol\]|The protocol to use for routing traffic to instances: HTTP, HTTPS, TCP, or SSL.|
    |Listener Protocol \[service\_protocol\]|The load balancer transport protocol to use for routing: HTTP, HTTPS, TCP, or SSL.|
    |Comments \[comments\]|Comments related to the CI.|

-   **Resources discovered using the Amazon AWS - LB Pool Member\(LP\) pattern**

<table id="table_ntq_x3y_p2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Target ID, depending on the target type. For example: Instance ID, IP address, Lambda ARN, or Application Load Balancer ARN.

</td></tr><tr><td>

Service port \[service\_port\]

</td><td>

The port on which the target is listening, if available.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

Possible values are:-   Target ID
-   Target ID and target port, if available, in the following format: `<target ID>#<target port>`.

For example: `i-0123456789abcdef0#8080`

</td></tr><tr><td>

Comments \[comments\]

</td><td>

Comments related to the CI.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the target. Possible values are Operational or Non-Operational.

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Installation status of the target. Possible values are Installed or Retired.

</td></tr><tr><td>

Pool \[pool\]

</td><td>

References the Load Balancer Pool \[cmdb\_ci\_lb\_pool\] table.

</td></tr></tbody>
</table>    **Note:** By default, the Amazon AWS - LB Pool Member\(LP\) pattern doesn't execute discovery. To enable the discovery of AWS Application Load Balancer targets, set the **sn\_itom\_pattern.discover\_aws\_app\_pool\_members** MID Server property to **true**. For more information, see [Enable AWS Application Load Balancer target discovery](../../service-mapping/task/enable-aws-app-lb-discovery.md).

-   **Resources discovered using the Amazon AWS - Customer Gateway \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|Name or ID if no Name is specified of the customer gateway.|
    |Object ID \[object\_id\]|ID of the customer gateway.|
    |Connection Type \[connection\_type\]|Type of VPN connection the customer gateway supports.|

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|Name or ID if no Name is specified of the customer gateway.|
    |Object ID \[object\_id\]|ID of the customer gateway.|

-   **Resources discovered using the Amazon AWS - discover Organization pattern**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The unique identifier \(ID\) of the management account of an organization.|
    |Object ID \[object\_id\]|The unique identifier \(ID\) of the management account of an organization.|
    |Root ID \[root\_id\]|The unique identifier \(ID\) of an organization.|
    |Master Email \[master\_email\]|The email address associated with the AWS account that is designated as the management account for the organization.|
    |Install Status \[install\_status\]|The install status of the Organization based on the AvailablePolicyTypes status.|
    |Operational status \[operational\_status\]|The operational status of the Organization based on the AvailablePolicyTypes status.|

-   **Resources discovered the using the Amazon AWS - Host \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|Name of this host.|
    |Object ID \[object\_id\]|Unique identifier, allocated by Amazon AWS Cloud for this resource.|
    |CPU Core Count \[cpu\_core\_count\]|The number of host cores.|
    |State \[state\]|The current state of the host.|
    |Host Type \[host\_type\]|The host type \(instanceFamily\).|
    |Cloud Vendor \[cloud\_vendor\]|The cloud vendor: AWS.|
    |Virtual \[virtual\]|Virtual host: False.|

-   **Resources discovered using the Amazon AWS - Internet Gateway \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|Name or ID if no Name is specified for the internet gateway.|
    |Object ID \[object\_id\]|ID of the internet gateway.|

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|Name or ID if no Name is specified for the internet gateway.|
    |Object ID \[object\_id\]|ID of the internet gateway.|

-   **Resources discovered using the Amazon AWS - IP Address \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The name or ID if no Name is specified for the Network Interface.|
    |IP Address \[ip\_address\]|If available, the address of the Elastic IP address bound to the network interface. If not available, the Private IP.|
    |Object ID \[object\_id\]|The ID of the Network Interface.|
    |Public DNS \[public\_dns\]|The public DNS name if available.|
    |Private IP Address \[private\_ip\]|The IPv4 address of the network interface within the subnet.|
    |Instance ID \[instance\_id\]|The ID of the instance.|

-   **Resources discovered the using the Amazon AWS - Key Pair \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The name of the key pair.|
    |Object ID \[object\_id\]|The ID of the key pair.|
    |Finger Print \[finger\_print\]|If you used [CreateKeyPair](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateKeyPair.html) to create the key pair, this value is the SHA-1 digest of the DER encoded private key. If you used ImportKeyPair to provide AWS the public key, this value is the MD5 public key fingerprint as specified in section 4 of RFC 4716.|

-   **Resources discovered using the Amazon AWS - LB Pool \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The name of the load balancer pool.|
    |Object ID \[object\_id\]|Unique identifier, allocated by Amazon AWS Cloud for this resource.|
    |Comments \[comments\]|Comments related to the CI.|

-   **Resources discovered using the Amazon AWS - LB Service \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|Name of the load balancer service.|
    |Object ID \[object\_id\]|Unique identifier, allocated by Amazon AWS Cloud for this resource.|
    |Port \[port\]|The port on which the load balancer is listening.|
    |Service Port \[service\_port\]|The port on which the instance is listening.|
    |Server Protocol \[service\_protocol\]|The protocol to use for routing traffic to instances: HTTP, HTTPS, TCP, or SSL.|
    |Listener Protocol \[service\_protocol\]|The load balancer transport protocol to use for routing: HTTP, HTTPS, TCP, or SSL.|
    |Comments \[comments\]|Comments related to the CI.|

-   **Resources discovered using the Amazon AWS - NAT Gateway \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|Name of the NAT gateway.|
    |Object ID \[object\_id\]|Unique identifier, allocated by Amazon AWS Cloud for this resource.|
    |Install Status \[install\_status\]|Provisioning status of the NAT gateway.|

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The name of the NAT endpoint.|
    |Object ID \[object\_id\]|Unique identifier, allocated by Amazon AWS Cloud for this resource.|

-   **Resources discovered using the Amazon AWS - Network \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|Name of the Virtual Private Cloud \(VPC\) network.|
    |Object ID \[object\_id\]|Unique identifier, allocated by Amazon AWS Cloud for this resource.|
    |State \[state\]|The current state of the VPC: pending or available.|
    |CIDR \[cidr\]|CIDR representation of the subnet. For example, 10.0.0.0/24.|
    |Install Status \[install\_status\]|Resource provisioning status.|

-   **Resources discovered using the Amazon AWS - NIC \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The Name or ID if no Name is specified for the Network Interface.|
    |Object ID \[object\_id\]|The ID of the network interface.|
    |State \[state\]|The status of the network interface. The valid values are as follows: available, associated, attaching, in-use, or detaching.|
    |Private IP \[private\_ip\]|The IPv4 address of the network interface within the subnet.|
    |IP Address \[ip\_address\]|If available, the address of the Elastic IP address bound to the network interface. If not available, the Private IP.|
    |Public IP \[public\_ip\]|The address of the Elastic IP address bound to the network interface.|

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|IP address of the Load Balancer.|
    |Object ID \[object\_id\]|If available, the address of the Elastic IP address bound to the network. If not available, the Private IP.|
    |IP Address \[ip\_address\]|If available, the address of the Elastic IP address bound to the network interface. If not available, the Private IP.|
    |Comments \[comments\]|Comments related to the CI.|

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The name of the virtual network machine interface \(VNIC\) endpoint.|
    |Object ID \[object\_id\]|Unique identifier, allocated by Amazon AWS Cloud for this resource.|
    |IP Address \[ip\_address\]|If available, the address of the Elastic IP address bound to the network interface. If not available, the Private IP.|
    |Host \[host\]|The ID of the instance.|

-   **Resources discovered using the Amazon AWS - Organizational Units \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The user-friendly name of the Organizational Unit \(OU\).|
    |Object ID \[object\_id\]|The unique identifier \(ID\) associated with this OU. The ID is unique to the organization.|
    |Organizational ID \[aws\_org\_id\]|The unique identifier \(ID\) associated with this OU. The ID is unique to the organization.|
    |Org Unit Parent ID \[org\_unit\_parent\_id\]|The ID of the root or the immediate parent OU.|

-   **Resources discovered using the Amazon AWS - Public IP Address \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The name or allocation ID, if no name is specified for the public IP address.|
    |Object ID \[object\_id\]|The ID representing the allocation of the address for the use with EC2-VPC.|
    |Public ID Address \[public\_ip\]|The elastic IP address.|

-   **Resources discovered using the Amazon AWS - Route Table \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The ID of the route table.|
    |State \[state\]|If the route table is discoverable, the value is available.|
    |Object ID \[object\_id\]|The name or ID, if no name is specified for the route table.|

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The name or ID, if no name is specified for the route table.|
    |Object ID \[object\_id\]|The ID of the route table.|

-   **Resources discovered using the Amazon AWS - Security Group \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The name of the security group.|
    |Object ID \[object\_id\]|The ID of the security group.|

-   **Resources discovered using the Amazon AWS - SSM Cloud Agents \(LP\) pattern**

    The Amazon AWS - SSM Cloud Agents \(LP\) pattern introduces the following CI class that extends an existing CMDB class.

    |CI class|Extends from|
    |--------|------------|
    |Cloud System Management Agent \[cmdb\_ci\_cloud\_system\_management\_agent\]|Virtual Machine Object \[cmdb\_ci\_vm\_object\]|

<table id="table_dnd_xpy_1fc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Cloud Agent Type \[cloud\_agent\_type\]

</td><td>

Type of cloud agent: AWS SSM.

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Install status of the AWS Systems Manager \(SSM\) agent:-   **Installed**: The agent is currently running.
-   **Absent**: The agent is not currently running.


</td></tr><tr><td>

IP Address \[ip\_address\]

</td><td>

Address of the VM instance.

</td></tr><tr><td>

Name \[name\]

</td><td>

Name of the VM instance that the SSM agent is running on.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

ID of the VM instance.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the agent service.Possible values are Operational or Non-Operational.

</td></tr><tr><td>

Operating System Platform \[operating\_system\_platform\]

</td><td>

Operating system type of the VM instance.

</td></tr><tr><td>

Resource Type \[resource\_type\]

</td><td>

Type of resource managed by SSM. Possible values are EC2Instance or ManagedInstance.

</td></tr><tr><td>

Version \[version\]

</td><td>

Version of the SSM agent.

</td></tr></tbody>
</table>-   **Resources discovered using the Amazon AWS - Storage \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |State \[state\]|The volume state. The following values are valid: creating, available, in-use, deleting, deleted, or error.|
    |Storage Type \[storage\_type\]|For example, hard-coded value: **block**.|
    |Volume ID \[volume\_id\]|The volume type. For example, gp2 for General Purpose SSD, io1 for Provisioned IOPS SSD, st1 for Throughput Optimized HDD, sc1 for Cold HDD, or standard for Magnetic volumes.|
    |Name \[name\]|The name or ID, if no name is specified for the volume.|
    |Size Bytes \[size\_bytes\]|The size of the volume, in bytes.|
    |Object ID \[object\_id\]|The ID of the volume.|

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The name or ID, if no name is specified for the volume.|
    |Object ID \[object\_id\]|The ID of the volume.|

-   **Resources discovered using the Amazon AWS - Sub Account \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Account ID \[account\_id\]|Unique identifier \(ID\) of the account.|
    |Object ID \[object\_id\]|Unique identifier \(ID\) of the account.|
    |Datacenter Type \[datacenter\_type\]|Hard-coded value: cmdb\_ci\_aws\_datacenter.|
    |Name \[name\]|User-friendly name of the account.|
    |Is Master Account \[is\_master\_account\]|Boolean attribute indicating if this account is the management account or not.|
    |Account Email \[account\_email\]|Email address of the AWS service account.|

-   **Resources discovered using the Amazon AWS - Subnet \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The name or ID, if no name is specified for the subnet.|
    |Object ID \[object\_id\]|The ID of the subnet.|
    |CIDR \[cidr\]|The IPv4 CIDR block assigned to the subnet.|
    |Available IP Count \[available\_ip\_count\]|The number of unused private IPv4 addresses in the subnet. The IPv4 addresses for any stopped instances are considered unavailable.|
    |State \[state\]|The current state of the subnet. The following values are valid: pending or available.|

-   **Resources discovered using the Amazon AWS - VPN Connections \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|Name of the project that is used for the discovery.|
    |Object ID \[object\_id\]|The name or ID, if no name is specified for the VPN connection.|
    |State \[state\]|The current state of the VPN connection. The following values are valid: pending, available, deleting, or deleted.|

-   **Resources discovered using the Amazon AWS - VPN Gateway \(LP\) pattern**

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The name or ID, if no name is specified for the VPN Gateway.|
    |Object ID \[object\_id\]|The ID of the virtual private gateway.|
    |Connection Type \[connection\_type\]|The type of VPN connection the virtual private gateway supports.|

    |Field|Description|
    |-----|-----------|
    |Name \[name\]|The name or ID, if no name is specified for the VPN Gateway.|
    |Object ID \[object\_id\]|The ID of the virtual private gateway.|
    |Connection Type \[connection\_type\]|The type of VPN connection the virtual private gateway supports.|

-   **Resources discovered using the Amazon AWS - Web ACL \(LP\) pattern**

    The Amazon AWS - Web ACL \(LP\) pattern introduces the following CI class that extends an existing CMDB class.

    |CI class|Extends from|
    |--------|------------|
    |Web ACL \[cmdb\_ci\_web\_acl\]|Virtual Machine Object \[cmdb\_ci\_vm\_object\]|

<table id="table_il1_nbb_y2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the web access control list \(web ACL\).

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

Unique ID for the web ACL from AWS.

</td></tr><tr><td>

Default Action \[defaul\_action\]

</td><td>

Default action when no rules in the web ACL match.Possible values are Allow or Deny.

</td></tr><tr><td>

Description \[short\_description\]

</td><td>

Description of web ACL provided by AWS.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Whether the web ACL is enabled or disabled.Possible values are Operational or Retired.

</td></tr></tbody>
</table>    **Note:** Security Operations users can leverage the integration with Discovery to import web ACL rules and load balancers with attached web ACLs. For more information on setting ACL rules and using the Mitigation Controls Monitoring app, see Configure the AWS WAF integration for mitigation controls monitoring.


## Events discovered by Discovery during horizontal discovery

Discovery uses patterns to find events created for Amazon AWS Cloud components. If there are events that indicate the change of state in one of the Amazon AWS Cloud components, it triggers discovery of Amazon AWS Cloud components using the patterns.

|Pattern|CI|
|-------|---|
|Amazon AWS Virtual Server Events|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|
|Amazon AWS Security Group Events|Compute Security Group \[cmdb\_ci\_compute\_security\_group\]|
|Amazon AWS Subnet Events|Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|
|Amazon AWS Storage Events|Storage Volume \[cmdb\_ci\_storage\_volume\]|
|Amazon AWS Network Events|Cloud Network \[cmdb\_ci\_network\]|
|Amazon AWS Classic LB Events|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|
|Amazon AWS Application and Network LBs Events|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|

![Dependency Views displaying the cloud load balancer and connected components.](../image/aws-cloud-load-balancer-components.png "Dependency Views displaying the cloud load balancer and connected components")

![Dependency Views displaying components connected to the cloud network in the AWS environment.](../image/aws-cloud-network-components.png "Dependency Views displaying components connected to the cloud network in the AWS environment")

![Dependency Views showing Virtual Machine and connected components in the AWS environment.](../image/aws-virtual-machine-components.png "Dependency Views showing Virtual Machine and connected components in the AWS environment")

## CI relationships

The AWS patterns create the following relationships and references to support AWS discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

-   **Relationships discovered using the Amazon AWS - ACL \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |Network \[cmdb\_ci\_network\]|Contains::Contained by|Network ACL \[cmdb\_ci\_network\_acl\]|
    |Network ACL \[cmdb\_ci\_network\_acl\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
    |Network ACL \[cmdb\_ci\_network\_acl\]|Implement End Point To::Implement End Point From|Network ACL \[cmdb\_ci\_endpoint\_acl\]|
    |Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|Use End Point To::Use End Point From|Network ACL \[cmdb\_ci\_endpoint\_acl\]|

-   **Relationships discovered using the Amazon AWS - Application and Network \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|Contains::Contained by|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|
    |Availability Zone \[cmdb\_ci\_availability\_zone\]|Contains::Contained by|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|
    |Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
    |Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Contains::Contained by|DNS Name \[cmdb\_ci\_dns\_name\]|
    |Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Contains::Contained by|Compute Security Group \[cmdb\_ci\_compute\_security\_group\]|

-   **Relationships discovered using the Amazon AWS - Availability Zone \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|Contains::Contained by|Availability Zone \[cmdb\_ci\_availability\_zone\]|

-   **Relationships discovered using the Amazon AWS - Classic LB \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |Load Balancer Service \[cmdb\_ci\_lb\_service\]|Hosted on::Hosts|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|
    |Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|Contains::Contained by|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|
    |Availability Zone \[cmdb\_ci\_availability\_zone\]|Contains::Contained by|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|
    |Load Balancer Pool \[cmdb\_ci\_lb\_pool\]|Hosted on::Hosts|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|
    |Load Balancer Pool \[cmdb\_ci\_lb\_pool\]|Owns::Owned by|Load Balancer Pool Member \[cmdb\_ci\_lb\_pool\_member\]|
    |Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Contains::Contained by|DNS Name \[cmdb\_ci\_dns\_name\]|
    |Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Owns::Owned by|Cloud LB IPAddress \[cmdb\_ci\_cloud\_lb\_ipaddress\]|
    |Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
    |Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Contains::Contained by|Compute Security Group \[cmdb\_ci\_compute\_security\_group\]|

-   **Relationships discovered using the Amazon AWS - LB Pool Member\(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |Load Balancer Pool \[cmdb\_ci\_lb\_pool\]|Owns::Owned by|Load Balancer Pool Member \[cmdb\_ci\_lb\_pool\_member\]|

    |CI|Field|Referenced CI|
    |---|-----|-------------|
    |Load Balancer Pool Member \[cmdb\_ci\_lb\_pool\_member\]|Pool \[pool\]|Load Balancer Pool \[cmdb\_ci\_lb\_pool\]|

    **Note:** By default, the Amazon AWS - LB Pool Member\(LP\) pattern doesn't execute discovery. To enable the discovery of AWS Application Load Balancer targets, set the **sn\_itom\_pattern.discover\_aws\_app\_pool\_members** MID Server property to **true**. For more information, see [Enable AWS Application Load Balancer target discovery](../../service-mapping/task/enable-aws-app-lb-discovery.md).

-   **Relationships discovered using the Amazon AWS - Customer Gateway \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |Customer Gateway \[cmdb\_ci\_customer\_gateway\]|Hosted on::Hosts|Virtual Machine Instance \[cmdb\_ci\_instance\]|
    |Customer Gateway \[cmdb\_ci\_customer\_gateway\]|Implement End Point To::Implement End Point From|Customer Gateway \[cmdb\_ci\_endpoint\_cust\_gateway\]|

-   **Relationships discovered using the Amazon AWS - Host \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |Host \[cmdb\_ci\_cloud\_host\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
    |Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Runs on::Runs|Host \[cmdb\_ci\_cloud\_host\]|

-   **Relationships discovered using the Amazon AWS - Internet Gateway \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |Internet Gateway \[cmdb\_ci\_internet\_gateway\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
    |Internet Gateway \[cmdb\_ci\_internet\_gateway\]|Implement End Point To::Implement End Point From|Internet Gateway EP \[cmdb\_ci\_endpoint\_intgateway\]|
    |Cloud Network \[cmdb\_ci\_network\]|Use End Point To::Use End Point From|Internet Gateway EP \[cmdb\_ci\_endpoint\_intgateway\]|

-   **Relationships discovered using the Amazon AWS - IP Address \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |Cloud Key Pair \[cmdb\_ci\_cloud\_key\_pair\]|Contains::Contained by|IP Address \[cmdb\_ci\_cloud\_ip\_address\]|

-   **Relationships discovered using the Amazon AWS - Key Pair \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |Servers \[cmdb\_ci\_server\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|

-   **Relationships discovered using the Amazon AWS - LB Pool \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |Load Balancer Pool \[cmdb\_ci\_lb\_pool\]|Hosted on::Hosts|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|

-   **Relationships discovered using the Amazon AWS - LB Service \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |Load Balancer Service \[cmdb\_ci\_lb\_service\]|Hosted on::Hosts|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|

-   **Relationships discovered using the Amazon AWS - NAT Gateway \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |NAT Gateway \[cmdb\_ci\_nat\_gateway\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
    |NAT Gateway \[cmdb\_ci\_nat\_gateway\]|Implement End Point To::Implement End Point From|NAT EP \[cmdb\_ci\_endpoint\_nat\]|
    |Network \[cmdb\_ci\_network\]|Use End Point To::Use End Point From|NAT EP \[cmdb\_ci\_endpoint\_nat\]|

-   **Relationships discovered using the Amazon AWS - Network \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |Network \[cmdb\_ci\_network\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|

-   **Relationships discovered using the Amazon AWS - NIC \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Owns::Owned by|Cloud LB IPAddress \[cmdb\_ci\_cloud\_lb\_ipaddress\]|
    |Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Use End Point To::Use End Point From|VNIC Endpoint \[cmdb\_ci\_endpoint\_vnic\]|
    |Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|Contains::Contained by|NIC \[cmdb\_ci\_nic\]|
    |VNIC Endpoint \[cmdb\_ci\_endpoint\_vnic\]|Implement End Point To::Implement End Point From|NIC \[cmdb\_ci\_nic\]|
    |NIC \[cmdb\_ci\_nic\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|

-   **Relationships discovered using the Amazon AWS - Organizational Units \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |Cloud Organization \[cmdb\_ci\_cloud\_org\]|Contains::Contained by|AWS Organizational Unit \[cmdb\_ci\_aws\_org\_unit\]|
    |AWS Organizational Unit \[cmdb\_ci\_aws\_org\_unit\]|Contains::Contained by|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|

    |CI|Field|Referenced CI|
    |---|-----|-------------|
    |Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|AWS Organizational Unit \[cmdb\_ci\_aws\_org\_unit\]|

-   **Relationships discovered using the Amazon AWS - Public IP Address \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |Cloud Public IP Address \[cmdb\_ci\_cloud\_public\_ipaddress\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|

-   **Relationships discovered using the Amazon AWS - Route Table \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |Network \[cmdb\_ci\_network\]|Contains::Contained by|Route Table \[cmdb\_ci\_route\_table\]|
    |Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|Use End Point To::Use End Point From|Route Table Endpoint \[cmdb\_ci\_endpoint\_route\_table\]|
    |Route Table \[cmdb\_ci\_route\_table\]|Implement End Point To::Implement End Point From|Route Table Endpoint \[cmdb\_ci\_endpoint\_route\_table\]|

-   **Relationships discovered using the Amazon AWS - Security Group \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |Network \[cmdb\_ci\_network\]|Contains::Contained by|Compute Security Group \[cmdb\_ci\_compute\_security\_group\]|
    |Compute Security Group \[cmdb\_ci\_compute\_security\_group\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|

-   **Relationships discovered using the Amazon AWS - SSM Cloud Agents \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |Cloud System Management Agent \[cmdb\_ci\_cloud\_system\_management\_agent\]|Runs on::Runs|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|

-   **Relationships discovered using the Amazon AWS - Storage \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |Virtual Machine Instance \[cmdb\_ci\_instance\]|Use End Point To::Use End Point From|Block Endpoint \[cmdb\_ci\_endpoint\_block\]|
    |Block Endpoint \[cmdb\_ci\_endpoint\_block\]|Implement End Point To::Implement End Point From|Storage Volume \[cmdb\_ci\_storage\_volume\]|
    |Availability Zone \[cmdb\_ci\_availability\_zone\]|Contains::Contained by|Storage Volume \[cmdb\_ci\_storage\_volume\]|
    |Storage Volume \[cmdb\_ci\_storage\_volume\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|

-   **Relationships discovered using the Amazon AWS - Subnet \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |Network \[cmdb\_ci\_network\]|Contains::Contained by|Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|
    |Availability Zone \[cmdb\_ci\_availability\_zone\]|Contains::Contained by|Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|

-   **Relationships discovered using the Amazon AWS - VPN Connections \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |Customer Gateway \[cmdb\_ci\_customer\_gateway\]|Contains::Contained by|VPN Connection \[cmdb\_ci\_vpn\_connection\]|
    |Virtual Private Gateway \[cmdb\_ci\_virtual\_pvt\_gateway\]|Contains::Contained by|VPN Connection \[cmdb\_ci\_vpn\_connection\]|
    |VPN Connection \[cmdb\_ci\_vpn\_connection\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|

-   **Relationships discovered using the Amazon AWS - VPN Gateway \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |Virtual Private Gateway \[cmdb\_ci\_virtual\_pvt\_gateway\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
    |Virtual Private Gateway \[cmdb\_ci\_virtual\_pvt\_gateway\]|Implement End Point To::Implement End Point From|Virtual Private Gateway Endpoint \[cmdb\_ci\_endpoint\_vpg\]|
    |Network \[cmdb\_ci\_network\]|Use End Point To::Use End Point From|Virtual Private Gateway Endpoint \[cmdb\_ci\_endpoint\_vpg\]|

-   **Relationships discovered using the Amazon AWS - Web ACL \(LP\) pattern**

    |CI|Relationship|CI|
    |---|------------|---|
    |Web ACL \[cmdb\_ci\_web\_acl\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|

    **Note:** Security Operations users can leverage the integration with Discovery to import web ACL rules and load balancers with attached web ACLs. For more information on setting ACL rules and using the Mitigation Controls Monitoring app, see Configure the AWS WAF integration for mitigation controls monitoring.


## Services discovered by patterns

Horizontal discovery finds EC2 and VPC services running on AWS resources.

|Service name|CI class|Pattern|
|------------|--------|-------|
|AWS::EC2::SecurityGroup|Compute Security Group \[cmdb\_ci\_compute\_security\_group\]|Amazon AWS Security Group Events|
|AWS::EC2::Subnet|Cloud Subnet \[cmdb\_ci\_cloud\_subnet\]|Amazon AWS Subnet Events|
|AWS::EC2::VPC|Cloud Network \[cmdb\_ci\_network\]|Amazon AWS Network Events|
|AWS::EC2::Instance|Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]|Amazon AWS Virtual Server Events|
|EQS::EC2::Volume|Storage Volume \[cmdb\_ci\_storage\_volume\]|Amazon AWS Elastic Block Storage|
|AWS::ElasticLoadBalancingV2::LoadBalancer|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Amazon AWS Application and Network LBs Events|
|AWS::ElasticLoadBalancing::LoadBalancer|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|Amazon AWS Classic LBs Events|

## Data collected by Service Mapping during tag-based discovery

Service Mapping uses tag-based discovery to create service instance maps including the Cloud components. The Service Mapping application comes with the following preconfigured CI relationships used for tag-based discovery. These CI relationships are available from the 1.0.68 release on the ServiceNow Store.

|CI|Relationship|CI|
|---|------------|---|
|Configuration Item \[cmdb\_ci\]|Hosted on::Hosts|Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]|
|Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|

-   **[Amazon API Gateway discovery with Patterns](../../service-mapping/concept/aws-api-gateway-discovery.md)**  
The ServiceNow Discovery and Service Mapping applications use the Amazon AWS API Gateway pattern to find Amazon API Gateways and connections to other entities. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Amazon API Gateway Domain Name pattern-based discovery](../../patterns/aws-api-gateway-domain-name.md)**  
Discovery and Service Mapping Patterns finds AWS services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Amazon DynamoDB Cluster pattern-based discovery](../../patterns/aws-dynamodb-cluster.md)**  
Discovery and Service Mapping Patterns finds AWS services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Amazon Elastic Compute Cloud \(EC2\) Amazon Elastic Block Store \(EBS\) Snapshot pattern-based discovery](../../patterns/aws-ec2-ebs-snapshot.md)**  
Discovery and Service Mapping Patterns finds AWS services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Amazon Elastic Compute Cloud \(EC2\) Reserved Instance pattern-based discovery](../../patterns/aws-ec2-reserved-instance.md)**  
Discovery and Service Mapping Patterns finds AWS services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Amazon Elastic Compute Cloud \(EC2\) virtual private cloud \(VPC\) Endpoint Service pattern-based discovery](../../patterns/aws-ec2-vpc-endpoint-service.md)**  
Discovery and Service Mapping Patterns finds AWS services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Amazon Elastic Compute Cloud \(EC2\) virtual private cloud \(VPC\) Peering Connection pattern-based discovery](../../patterns/aws-ec2-vpc-peering-connection.md)**  
Discovery and Service Mapping Patterns finds AWS services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Amazon Elastic File System \(Amazon EFS\) pattern-based discovery](../../patterns/aws-elastic-file-system.md)**  
Discovery and Service Mapping Patterns finds AWS services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Amazon ElastiCache Snapshot pattern-based discovery](../../patterns/aws-elasticache-snapshot.md)**  
Discovery and Service Mapping Patterns finds AWS services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Amazon Managed Workflows for Apache Airflow \(MWAA\) Environment pattern-based discovery](../../patterns/aws-mwaa-environment.md)**  
Discovery and Service Mapping Patterns finds AWS services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Amazon Relational Database Services \(RDS\) DB Snapshot pattern-based discovery](../../patterns/aws-rds-db-snapshot.md)**  
Discovery and Service Mapping Patterns finds AWS services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Amazon Redshift Serverless Namespace pattern-based discovery](../../patterns/aws-redshift-serverless-namespace.md)**  
Discovery and Service Mapping Patterns finds AWS services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Amazon Redshift Serverless Snapshot pattern-based discovery](../../patterns/aws-redshift-serverless-snapshot.md)**  
Discovery and Service Mapping Patterns finds AWS services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Amazon Redshift Serverless Workgroup pattern-based discovery](../../patterns/aws-redshift-serverless-workgroup.md)**  
Discovery and Service Mapping Patterns finds AWS services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Amazon Route 53 pattern-based discovery](../../service-mapping/reference/aws-route-53-pattern.md)**  
Discovery and Service Mapping Patterns finds Amazon Route 53 domain name systems \(DNS\) and aliases on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Amazon SageMaker Training Job pattern-based discovery](../../patterns/aws-sagemaker-training-job.md)**  
Discovery and Service Mapping Patterns finds AWS services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Amazon Timestream for InfluxDB Database Instance pattern-based discovery](../../patterns/aws-timestream-influxdb-db-instance.md)**  
Discovery and Service Mapping Patterns finds AWS services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[AWS Batch Compute Environment pattern-based discovery](../../patterns/aws-batch-compute-environment.md)**  
Discovery and Service Mapping Patterns finds AWS services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[AWS CloudHSM hardware security module \(HSM\) pattern-based discovery](../../patterns/aws-cloudhsm-hsm.md)**  
Discovery and Service Mapping Patterns finds AWS services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[AWS CloudTrail Trail pattern-based discovery](../../patterns/aws-cloudtrail-trail.md)**  
Discovery and Service Mapping Patterns finds AWS services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[AWS datacenter pattern-based discovery](../../service-mapping/reference/aws-datacenter-pattern.md)**  
Discovery and Service Mapping Patterns finds AWS Regions for your AWS account on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[AWS DataSync Task pattern-based discovery](../../patterns/aws-datasync-task.md)**  
Discovery and Service Mapping Patterns finds AWS services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[AWS Global Accelerator pattern-based discovery](../../patterns/aws-global-accelerator.md)**  
Discovery and Service Mapping Patterns finds AWS services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[AWS hardware type pattern-based discovery](../../service-mapping/reference/aws-hardware-type-pattern.md)**  
Discovery and Service Mapping Patterns finds Amazon EC2 instance types on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[AWS Network Firewall pattern-based discovery](../../patterns/aws-network-firewall.md)**  
Discovery and Service Mapping Patterns finds AWS services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[AWS Organizations pattern-based discovery](../../service-mapping/reference/aws-organizations-pattern.md)**  
Discovery and Service Mapping Patterns finds AWS Organizations accounts on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[AWS OS image pattern-based discovery](../../service-mapping/reference/aws-os-image-pattern.md)**  
Discovery and Service Mapping Patterns finds AWS OS images \(both owned and executable\) on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[AWS Serverless Database pattern-based discovery](../../service-mapping/reference/aws-serverless-database-pattern.md)**  
Discovery and Service Mapping Patterns finds Amazon Aurora Serverless databases on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[AWS Storage Gateway File Share pattern-based discovery](../../patterns/aws-storage-gateway-file-share.md)**  
Discovery and Service Mapping Patterns finds AWS services on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[AWS sub account pattern-based discovery](../../service-mapping/reference/aws-sub-account-pattern.md)**  
Discovery and Service Mapping Patterns finds member accounts and the primary account within an AWS Organization. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[AWS virtual server pattern-based discovery](../../service-mapping/reference/aws-virtual-server-pattern.md)**  
Discovery and Service Mapping Patterns finds AWS EC2 virtual machine instances on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   **[Limit AWS discovery to datacenters with resources](../../service-mapping/task/limit-aws-discovery-active-datacenter.md)**  
Optimize AWS discovery by limiting it to datacenters with resources.

**Parent Topic:**[Available cloud discovery patterns](../../service-mapping/concept/available-patterns-cloud.md)

**Related topics**  


[Kubernetes discovery using patterns](../../service-mapping/concept/kubernetes-discovery.md)

[AWS Certificate Manager discovery](../../service-mapping/reference/aws-certificate-manager-discovery-pattern.md)

[Amazon Bedrock pattern-based discovery](../../ai-agent-topology-mapping/reference/amazon-bedrock-pattern.md)

