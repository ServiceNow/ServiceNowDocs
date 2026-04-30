---
title: Service Graph Connector for AWS
description: Use the Service Graph Connector for AWS to securely bring in Amazon Web Services \(AWS\) data into your ServiceNow instance.
locale: en-US
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2026-03-01"
reading_time_minutes: 5
breadcrumb: [Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Graph Connector for AWS

Use the Service Graph Connector for AWS to securely bring in Amazon Web Services \(AWS\) data into your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

The integration uses AWS native technologies and AWS security best practices to enable cloud teams to connect the data within their ServiceNow workflow. For more information about the Service Graph Connector for AWS, see the [Service Graph Connector for AWS - Introduction](https://community.servicenow.com/community?id=community_article&sys_id=13aa801f1b1ec910c465ece6b04bcbec) article on the ServiceNow Community site.

## Supported ServiceNow versions

-   Yokohama
-   Zurich
-   Australia

## Use cases

The following are examples on how you can use the Service Graph Connector for different ServiceNow applications:

-   Visibility into cloud resources, relationships, and state.
-   Deep discovery of applications for ITAM or SAM outcomes.
-   Governance and compliance outcome.

## Important information for upgrading Service Graph Connector for AWS

Before you begin the upgrade process, complete the following tasks:

-   If there are any customizations, delete the records associated with the Service Graph Connector for AWS from the Customer Updates \[sys\_update\_xml\] table. See [Customer Updates table](https://www.servicenow.com/docs/access?context=r_CustomerUpdatesTable&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).
-   Upgrade any dependencies.

After you've installed the latest version of the Service Graph Connector for AWS:

-   Perform a full import of data from your AWS instance. Verify that the **Use last run datetime** field value is cleared for all the AWS data sources in the Data Source \[sys\_data\_source\] table.
-   Download and rerun the AWS scripts. See [Configure the AWS environment](../task/sgc-cmdb-aws-task-overview.md).

## Configuring a connection for the connector

You can configure a connection for the connector by using the SGC Central view in the Service Graph Workspace or CMDB Workspace. The view enables you to discover and install connectors, and then effectively manage the full life cycle of creating, editing, monitoring, and debugging connections. To configure the connector using SGC Central, see [Configure Service Graph Connector for AWS using SGC Central](../../sgc-central/task/sgcc-configure-aws-integ.md).

**Important:** Unless there are configuration issues, use the SGC Central view in the Service Graph Workspace or CMDB Workspace to configure the connection for the connector, as the guided setup method is planned for deprecated.

## CMDB integrations dashboard

The Integration Commons for CMDB store app provides a dashboard with a central view of the status, processing results, and processing errors of all installed integrations. You can see metrics for all integration runs. You can filter the view to a specific CMDB integration, a specific time duration, or a specific integration run. For more details about monitoring AWS integrations in the CMDB Integrations Dashboard, see [Using the CMDB Integrations Dashboard](integration-commons-for-cmdb.md#section_fxg_lh4_blb).

## BYOL support

Bringing your own licenses \(BYOL\) is the process of bringing previously purchased on-premises licenses to Amazon AWS Cloud. The connector supports the BYOL of the Image CIs for Oracle Database servers on Amazon AWS Cloud by populating the Key Value \[cmdb\_key\_value\] table with the licensing information. When the licensing information is found, the key is set to `Windows_OS_License_Type_automatic` and the key value is set to `BYOL` in the Key Value \[cmdb\_key\_value\] table.

To support BYOL, the **sn\_aws\_integ.load\_all\_images** system property is enabled during the initial pull to import the metadata of all Image CIs included in the SG-AWS-Image-Id data source. After the initial pull, the property is deactivated automatically. The SG-AWS-Image-Id data source then imports the metadata of the Image CIs without names only.

## Event-based discovery

The Service Graph Connector for AWS works with event-based discovery. Events that are pulled from AWS can create and update CIs that were brought by the Service Graph Connector for AWS.

## Managing retired CIs in EKS components

If the Amazon Elastic Kubernetes Services \(EKS\) CIs are deleted in EKS components such as pods, services, and volumes, the corresponding CI entries are automatically set to **Retired** in the following CMDB CI classes:

Kubernetes Cluster, Kubernetes Node, Kubernetes Pod, Kubernetes Service, Kubernetes DaemonSet Kubernetes Namespace, Kubernetes Deployment, Docker Container, Kubernetes Volume

## Shared VPC and subnets support

Import CI relationships established between virtual private clouds \(VPCs\), subnets, and network interfaces hosted in different AWS accounts. For example, a VPC in one AWS account can be connected to a subnet in the same account, which can then link to a network interface and a virtual machine in another AWS account.

## Additional resources

See the following articles on the ServiceNow Community site for any additional information on the AWS set up:

-   [Service Graph Connector for AWS - Introduction](https://www.servicenow.com/community/cmdb-articles/service-graph-connector-for-aws-introduction/ta-p/2300757)
-   [How do I configure the AWS Service Graph Connector?](https://www.servicenow.com/community/cmdb-articles/aws-service-graph-connector/ta-p/2958151)
-   [Service Graph Connector for AWS - Diagnostic Tool &amp; Troubleshooting Issues](https://community.servicenow.com/community?id=community_article&sys_id=668651e71bde4150c465ece6b04bcb23)
-   [Service Graph Connector for AWS - Functional Spec and CI](https://www.servicenow.com/community/cmdb-articles/service-graph-connector-for-aws-functional-spec-and-ci/ta-p/2301845)
-   [Cloud Discovery and SG-AWS](https://www.servicenow.com/community/cmdb-articles/cloud-discovery-and-sg-aws/ta-p/2300607)

## Related content

[Service Graph Connectors](cmdb-sgc-available.md)

[Data mapping for Service Graph Connector for AWS](../reference/cmdb-data-mapping-aws.md)

[CMDB classes targeted in Service Graph Connector for AWS](../reference/cmdb-aws-classes.md)

[Enable optimized deletion of retired CIs in AWS](../task/sgc-cmdb-aws-delete-cis.md)

[Enable optimized SG-AWS-SendCommand data source performance](../task/sgc-cmdb-aws-ssm-prop.md)

[Handling import failures for large AWS resources](sgc-cmdb-aws-large-data-vol.md)

[Handling memory utilization errors for Service Graph Connector for AWS](sgc-cmdb-aws-memory.md)

[Life cycle management of records in Service Graph Connector for AWS](sgc-cmdb-aws-lc.md)

[Record removal process in Service Graph Connector for AWS](sgc-cmdb-aws-removal.md)

[Service Graph Connector for AWS properties](../reference/cmdb-sgc-aws-props.md)

