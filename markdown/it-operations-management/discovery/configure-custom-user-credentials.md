---
title: Configure custom user credentials
description: Define a non-root user for AWS SSM discovery by creating a credential record that specifies a user name with sufficient privileges to execute discovery commands on Linux targets.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-05-08"
reading_time_minutes: 1
breadcrumb: [AWS SSM discovery, Discovery for AWS, Discovery for cloud environment, Discovery, ITOM Visibility, IT Operations Management]
---

# Configure custom user credentials

Define a non-root user for AWS SSM discovery by creating a credential record that specifies a user name with sufficient privileges to execute discovery commands on Linux targets.

## Before you begin

Confirm the following:

-   The system property **glide.discovery.enable\_ssm** is turned on. For more information, see [Enable AWS SSM-based discovery](../concept/enable-aws-ssm-based-discovery.md).
-   The user you're assigning as the non-root user has access to run all the necessary commands on the target server. This user requires the same access as credentials used for regular Linux discovery, including the necessary root-level access for privileged commands. For more information, see [Credentials required for host discovery](../../service-mapping/reference/r_Credentials4HostDiscovery.md) and SSH credentials

Role required: discovery\_admin

## About this task

Instead of relying on root, you can define a custom user with sufficient privileges to execute the required Discovery commands. Only a user name is needed—no password or key—provided that the user has the same level of access as traditional Linux Discovery credentials. This approach promotes restricted access and better alignment with enterprise security policies.

**Note:** Currently, SSM supports only sudo for privileged command execution and defaults to the sh shell, with no support for alternate command or shell types.

## Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Credentials**.

2.  Select **New**.

3.  Select **AWS SSM instance User**.

4.  Enter a unique name for the user.

5.  Enter the user name from the alternate user credential that you created on your EC2 instance in the AWS Management Console.

    For more information, see the [Amazon SSM Discovery - AWS Environment Setup Instructions](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2150362) article in the Now Support Knowledge Base.

6.  Select **Submit**.


## Result

A new record is added to the AWS SSM Instance Users \[aws\_ssm\_instance\_user\_credentials\] table.

