---
title: Discovery for AWS
description: Amazon Web Services \(AWS\) cloud discovery enables visibility to your AWS cloud resources, to populate and update the Configuration Management Database \(CMDB\). Visibility into AWS supports business outcomes such as cloud transformation and optimizing efficiency for operations \(ITOM/ITSM/AIOps\).
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
keywords: [Patterns, Amazon Web Services \(AWS\), Cloud, Discovery, Visibility, CMDB, IAM]
breadcrumb: [Discovery for cloud environment, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery for AWS

Amazon Web Services \(AWS\) cloud discovery enables visibility to your AWS cloud resources, to populate and update the Configuration Management Database \(CMDB\). Visibility into AWS supports business outcomes such as cloud transformation and optimizing efficiency for operations \(ITOM/ITSM/AIOps\).

## What is AWS cloud discovery

AWS cloud discovery is an automated process that continuously identifies and maps AWS resources and populates the data in the Configuration Management Database \(CMDB\).

AWS discovery can be performed by a combination of approaches such as agent-based or agentless, cloud APIs for metadata discovery, or IPs for OS-level discovery. The visibility can be provided near real time \(using event-based discovery for example\) or by timed discovery schedules.

The Discovery and Service Mapping apps perform discovery by methods refereed to as horizontal discovery and top‑down mapping. Horizontal discovery identifies configuration items \(CIs\) without dependency mapping. Top‑down service mapping identifies application dependencies, connection paths, and service impact.

## Key outcomes and business value

AWS discovery facilitates several vital business outcomes by populating the CMDB with essential cloud data:

-   Regulatory compliance enabled by the data support. Visibility can promote alignment with compliance frameworks such as the Mutual Recognition Agreement \(MRA\) or Digital Operational Resilience Act \(DORA\).
-   Software asset management \(SAM\) enabled by visibility into cloud software deployments.
-   Financial operations\(FinOps\) enabled by comprehensive visibility into AWS resources and their usage,
-   Security operations\(SecOps\) enabled by continuous visibility into cloud resources and their configurations.
-   Certificate management enabled by the discovery of certificates, their expiry, and usage.
-   Artificial intelligence for IT operations \(AIOps\) enabled by Identifying and mapping all cloud resources, and their configurations.

## AWS discovery approaches

There are several approaches for discovering AWS environments.

1.  Cloud metadata discovery: Provides a high-level view of the AWS cloud infrastructure.
2.  Cloud OS-Level discovery: Provides a deeper level of discovery that indicates the state of the AWS cloud resources, such as installed software, active services, running processes, and system configurations.
3.  Event‑driven cloud discovery: Tracks changes in the life-cycle state or the configuration of AWS cloud resources. For more information, see [AWS events-driven discovery](../../it-operations-management/concept/aws-events-driven-discovery.md)
4.  Collecting data with Agent Client Collector \(ACC-VC\): Performs horizontal IP-based discovery for OS-related attributes such as system configurations, network interfaces, and running process. For more information, see [Agent Client Collector for Visibility - Content](../../agent-client-collector/concept/acc-visibility-landing-page.md).
5.  Collecting data with Service Graph Connectors: Imports and integrates AWS data into CMDB and non-CMDB tables. Specializes in collecting the data for AWS Organizations. For more information, see [AWS discovery solutions comparison](../../it-operations-management/reference/aws-discovery-methods.md) and [Service Graph Connector for AWS](https://www.servicenow.com/docs/access?context=cmdb-integration-aws-sg&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

For comparison of AWS cloud discovery methods and requirements, see [AWS cloud discovery methods and use cases](../../it-operations-management/reference/aws-discovery-methods-use-case.md)

## How to perform AWS cloud discovery

Multiple ITOM Visibility apps can collect \(or discover\) your data, visualize it, and help you monitor your AWS resources.

-   [Discovery Admin Workspace](discovery-admin-workspace.md)
-   [Discovery for Amazon Elastic Kubernetes Service \(EKS\)](../../service-mapping/concept/kubernetes-discovery.md)
-   [Service Mapping](../../service-mapping/concept/cloud-discovery-service-mapping.md)
-   [Discovery and Service Mapping Patterns](../reference/data-discovered-aws-patterns.md)
-   [Certificate Inventory and Management](../../service-mapping/reference/aws-certificate-manager-discovery-pattern.md)

Enabling Discovery or other Visibility solutions to access your AWS infrastructure depends on roles and permissions configured both in AWS and in ServiceNow AI Platform. The discovery process requires configuration within AWS, like setting up Identity and Access Management roles.

|AWS Users|Discovery permissions|
|---------|---------------------|
|AWS Organizations with master and member accounts|Access is based on the IAM roles defined for the master and member accounts.|
|AWS account root user|Has complete access to all AWS services and resources in the account.|
|IAM users/IAM user group|Has access to specific resources and services based on IAM roles or temporary access based on assumed roles.|

For more information, see [Access to cloud environments for ITOM products](../../it-operations-management/reference/accessing-cloud-itom.md)

In the ServiceNow AI Platform side, there are user configurations needed if you choose to use Discovery.

-   You must configure the discovery\_admin role for a user, to be able to run the discovery. For more information, see [Managing roles](https://www.servicenow.com/docs/access?context=ua-creating-roles&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)
-   Discovery runs commands and API queries to access and discover your AWS infrastructure. Before starting to configure Discovery roles and permissions, review the Cloud discovery spreadsheet and verify the REST API permissions.


## Verify the REST API Permissions

Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

