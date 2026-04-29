---
title: AWS SSM discovery
description: AWS Systems Manager \(SSM\) Agent discovery introduces a streamlined, agent-based approach to discovering Amazon Elastic Compute Cloud \(EC2\) using AWS SSM. This integration enhances Discovery by leveraging SSM agents to reduce dependency on traditional MID Server configurations, simplify credential management, and improve scalability across multi-region environments.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 5
breadcrumb: [Discovery for AWS, Discovery for cloud environment, Discovery, ITOM Visibility, IT Operations Management]
---

# AWS SSM discovery

AWS Systems Manager \(SSM\) Agent discovery introduces a streamlined, agent-based approach to discovering Amazon Elastic Compute Cloud \(EC2\) using AWS SSM. This integration enhances Discovery by leveraging SSM agents to reduce dependency on traditional MID Server configurations, simplify credential management, and improve scalability across multi-region environments.

## Workflow

![AWS SSM Agent discovery process](../image/aws-ssm-agent-discovery-process.svg "AWS SSM discovery workflow")

The overall process from a high level is as follows:

1.  The ServiceNow AI Platform® sends discovery commands to the MID Server.
2.  The MID interacts with AWS services \(SSM, Simple Storage Service \(S3\), Parameter Store\) to execute commands on target devices.
3.  The SSM agents run the commands and return results to S3.
4.  The MID retrieves and processes results.
5.  The MID sends the results back to the ServiceNow AI Platform® via the ECC queue, which updates the CMDB.

## Benefits and usage

The following examples highlight the primary advantages and practical uses of AWS SSM Agent discovery:

-   Execute discovery without needing additional credentials local to the operating system.
-   Simplify deployment without the need of Agent Client Collector \(ACC\) or Virtual Private Cloud \(VPC\) access.
-   Minimize the need for multiple MID Servers and direct network access to target devices.
-   Securely manage credentials and command execution using AWS services.

## Requirements

Confirm that you have the required versions of the following applications and plugins:

-   Discovery
-   Cloud Discovery Workspace version 1.7.1 or later.
-   CMDB CI Class Models version 1.74.0 or later.
-   Discovery and Service Mapping Patterns version 1.27.0 or later.

Install the MID Server. For more information, see [Install and configure the MID Servers](../../it-operations-management/task/mid-server-configuration-cloud.md).

Verify that you have an AWS user account with administrative access.

Verify that you have a ServiceNow AI Platform® user account with the discovery\_admin role.

## Unsupported features

Currently, the following features don’t support AWS SSM discovery:

-   File-based discovery
-   Certificate-based discovery
-   Top-down discovery
-   Enhanced ADM
-   Change/Unchange user step in patterns

**Note:** SSM supports only sudo for privileged command execution and defaults to the sh shell, with no support for alternate command or shell types.

## AWS environment configuration

-   **Create IAM roles and permissions**

    Define Identity and Access Management \(IAM\) roles to support AWS SSM operations, specifying the required permissions for executing Read, Write, and List commands. For more information, see [IAM Policies](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2150362#iampolicies)

-   **Configure EC2 roles and instances**

    Create EC2 roles and assign the necessary permissions for these roles to interact with SSM. For more information about setting up an EC2 instance, see [EC2 Instances](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2150362#ec2instances).

-   **Create S3 Buckets**

    Create S3 buckets to support large data transfers and configure appropriate bucket policies and life cycle rules. To overcome SSM's 24,000-character output limit, command output is redirected to S3, enabling full payload capture. Additionally, S3 facilitates file transfers to EC2 instances. For more information about creating S3 buckets, see [Setting up an S3 Bucket](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2150362#s3bucket).

-   **\(Optional\) Configure KMS keys**

    Create a custom AWS Key Management Service \(KMS\) key to encrypt sensitive credentials stored as SecureString parameters in the AWS Systems Manager Parameter Store. Using a dedicated key enhances security by verifying that credentials are encrypted and securely retrieved at runtime, without exposing them in plain text. For more information about creating KMS keys, see [Create a Customer Managed AWS KMS Key](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2150362#awskey).

    **Important:** If you’re using applicative credentials in Discovery, you must create a custom KMS key.

-   **Import custom SSM documents**

    SSM command execution depends on the availability of required documents. Before initiating SSM-based discovery, verify that all YAML files provided by ServiceNow have been successfully deployed to each AWS region where the discovery process will run. For more information on this process, see [Import Custom AWS Documents](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2150362#awsdocs). You can download the YAML files directly from this article.


For more information on AWS Management Console configuration, see the [Amazon SSM Discovery - AWS Environment Setup Instructions](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2150362) article in the Now Support Knowledge Base.

## ServiceNow AI Platform® instance configuration

-   **Configure System Properties**

    Enable the following Discovery system properties:

    -   **glide.discovery.enable\_ssm**
    -   **glide.discovery.ssm.enable\_windows**
    The AWS SSM Agent runs with root \(Linux\) or SYSTEM \(Windows\) privileges, meaning any command sent through it can execute with full system access. Due to this high level of access, SSM is turned off by default for security reasons. For more information, see [Enable AWS SSM-based discovery](enable-aws-ssm-based-discovery.md).

-   **Define root and non-root credentials**

    The MID Server property **mid.discovery.aws\_ssm.linux.fallback\_root\_user** enables EC2 instances to default to the root user. By default, this setting is **false**, but if you don’t want to set up alternate user credentials, you can enable it to run commands as root. If you leave this setting turned off, you must create a credential record in the AWS SSM Instance Users \[aws\_ssm\_instance\_user\_credentials\] table, where you simply provide the user name that should be used to run commands on the instance. For more information, [Enable root fallback](../task/enable-root-fallback.md) and [Configure custom user credentials](../task/configure-custom-user-credentials.md).

-   **Configure MID Server properties**

    After you set up KMS keys or S3 buckets in the AWS Management Console, configure the following MID Server system properties on the ServiceNow AI Platform®:

    -   **mid.discovery.aws\_ssm.kms\_key\_name**
    -   **mid.discovery.aws\_ssm.kms\_key\_region**
    -   **mid.discovery.aws\_ssm.s3\_bucket\_name**
    -   **mid.discovery.aws\_ssm.s3\_bucket\_region**
    For more information, see [Configure MID Server for AWS S3 access](../task/configure-mid-server-aws-s3-access.md) and [Configure MID Server for AWS KMS access](../task/config-mid-server-aws-kms-access.md).

-   **Enable MID Server capability**

    You must enable the new MID Server capability for AWS SSM so the MID Server can support running SSM discovery. By default, this capability is included if you're using the **ALL** capability. However, if you're using individual capabilities, you must manually add the new **AWS SSM** capability to your MID Servers. For information about adding a capability, see [Configure MID Server capabilities](https://www.servicenow.com/docs/access?context=t_ConfigureCapabilities&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).


## Cloud Discovery schedule configuration

-   **Create a Cloud Discovery schedule**

    SSM discovery can be deployed within an AWS-based Cloud Discovery schedule in the Discovery Admin Workspace. To do this, go to the Deep discovery step, enable the **Create an IP-based discovery schedule** toggle, and select **Discover servers though AWS Systems Manager \(SSM\) Agent** as the Discovery method. For more information, see [Create an AWS Discovery schedule in Discovery Admin Workspace](../task/create-AWS-schedule-DAW.md).


