---
title: Amazon Simple Storage Service \(Amazon S3\) discovery with Patterns
description: The ServiceNow Discovery application uses the Amazon AWS S3 pattern to find public and non-public storage buckets of Amazon Simple Storage Service. The pattern uses a set of REST API calls to find these resources. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Amazon Simple Storage Service \(Amazon S3\) discovery with Patterns

The ServiceNow Discovery application uses the Amazon AWS S3 pattern to find public and non-public storage buckets of Amazon Simple Storage Service. The pattern uses a set of REST API calls to find these resources. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

In addition to the discovery schedule, the ServiceNow instance triggers the Amazon AWS S3 pattern when AWS Config sends an event to the ServiceNow instance. Config is a service that continuously monitors AWS resources and sends events to the ServiceNow every time it senses that a resource configuration has changed.

Amazon AWS S3 pattern can also discover AWS S3 buckets located in the AWS GovCloud \(US\) region. For AWS S3 located in the AWS GovCloud \(SU\), the pattern cannot discover AWS S3 outgoing connections to other cloud resources like Lambda function. Discovery of outgoing connections for AWS S3 will be supported in future releases.

You can use this pattern on the ServiceNow platform using Jakarta Patch 10, Kingston Patch 8, or London Patch 1.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   If you use Identity and Access Management \(IAM\) to manage users in Amazon Web Services \(AWS\) platform, ensure that you created a user policy for the AWS user. For more information, refer to Create an IAM user policy for Cloud Provisioning and Governance in the ServiceNow Cloud Provisioning and Governance documentation.
-   Configure the AWS service account.
-   Configure AWS credentials, using a secret key and an access key.
-   AmazonS3ReadOnlyAccess policy user permissions.
-   Discover Logical Datacenters hosting S3 buckets as described in Run Discovery on an AWS cloud service account in the ServiceNow Cloud Provisioning and Governance documentation.
-   Create a schedule for the relevant AWS service account as described in Schedule Discovery on a service account in the ServiceNow Cloud Provisioning and Governance documentation.
-   To enable alert-based discovery, configure the AWS event service as described in Set up AWS event processing for Discovery and Service Mapping in the ServiceNow Cloud Provisioning and Governance documentation.
-   For Cloud Discovery, download the Discovery and Service Mapping Patterns from the ServiceNow Store.
-   When installing the MID Server, ensure that the host machine meets or exceeds the [MID Server system requirements](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) published on the ServiceNow documentation site.

## Verify the REST API Permissions

Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

**Note:** You can test the AWS REST APIs using Postman API platform. For more information, see the [How to test AWS REST API using POSTMAN \[KB0782183\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0782183) article in the Now Support Knowledge Base.

## Data collected by Discovery during horizontal discovery

<table id="table_td3_psz_42b"><thead><tr><th>

Table and field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Cloud Object Storage \[cmdb\_ci\_cloud\_object\_storage\]

</td></tr><tr><td>

Bucket name \[bucket\_name\]

</td><td>

The name of the AWS S3 bucket. You can discover all buckets hosted on a Logical Datacenter during one discovery process.

</td></tr><tr><td>

Creation date \[creation date\]

</td><td>

Creation date of the AWS S3 bucket.

</td></tr><tr><td>

Cloud provider \[cloud\_provider\]

</td><td>

Amazon AWS

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

The Amazon Resource Name \(ARN\), expressed in this format: **arn:aws:s3:::&lt;bucket name&gt;**

</td></tr><tr><td>

Service name \[service\_name\]

</td><td>

Set to **S3** by default.

</td></tr><tr><td>

Owner \[owner\]

</td><td>

Account ID in which the bucket exists.

</td></tr><tr><td>

Encryption type \[encryption\_type\]

</td><td>

Type of encryption for this bucket. The choices are:-   None
-   AES-256
-   AWS-KMS

</td></tr><tr><td>

ACL access type \[acl\_access\_type\]

</td><td>

The choices for access control types are:-   Public
-   Not Public

</td></tr><tr><td>

Policy access type \[policy\_access\_type\]

</td><td>

The choices for policy access types are:-   Public
-   Not Public

</td></tr><tr><td>

Replication destination \[replication\_destination\]

</td><td>

Bucket ARN of the Replication Destination bucket.

</td></tr></tbody>
</table>**Note:** In Discovery and Service Mapping Patterns versions before 1.30.2, the Owner field displays the bucket owner's name.

On the Dependency Views map you can see all discovered S3 buckets in your organization, including S3 buckets that you configured as replicas. In this example, Cloud Object Storage 1, Cloud Object Storage 2, and Cloud Object Storage 3 replicate Cloud Object Storage 2. In its turn, Cloud Object Storage 2 replicates Cloud Object Storage 1.

![Result of horizontal discovery of AWS S3 as appears in Dependency Views](../image/AWS-S3-dependency-views.png "Dependency Views showing AWS S3 components")

## CI relationships

These relationships are created to support AWS S3 discovery:

|CI|Relationship|CI|
|---|------------|---|
|cmdb\_ci\_cloud\_object\_storage|Replicates to::Replicated By|cmdb\_ci\_cloud\_object\_storage|
|cmdb\_ci\_cloud\_object\_storage|Hosted on::Hosts|cmdb\_ci\_logical\_datacenter|

## Data discovered by Service Mapping during top-down discovery

Service Mapping can discover AWS S3 outgoing connections to cloud resources, for example Lambda function.

![Service Mapping map showing a service with discovered S3 buckets.](../image/AWS-S3-top-down-map.png "Application service map showing an S3 bucket CI")

## Troubleshooting

If the mapping process does not proceed as you expected, follow the following suggestions.

<table id="table_ggn_ypj_yhb"><thead><tr><th>

Symptom

</th><th>

Cause

</th><th>

Solution

</th></tr></thead><tbody><tr><td>

Discovery fails. The discovery message contains the information about an error caused by the REST timeout.

</td><td>

There are many CIs sending the REST call response in the deployment. The MID Server cannot process the REST call response without exceeding the time limit controlled by the **mid.sa.cloud.request\_timeout** parameter.

</td><td>

By default, the **mid.sa.cloud.request\_timeout** parameter is set to 30000 milliseconds. Increase the value of this parameter on the relevant MID Server and run discovery again.

**Note:** If the **Configuration Parameters** related list for the relevant MID Server does not show this parameter, you may need to add it.

</td></tr><tr><td>

Pattern Designer fails during a debug session. The Pattern Designer message contains information about an error caused by a timeout.

</td><td>

The Pattern Designer fails because of a timeout during pattern debugging \(and not during discovery\).

</td><td>

By default, the **sa.debugger.max\_timeout**parameter is set to 240 seconds.Increase the value of this parameter on the relevant MID Server.

</td></tr></tbody>
</table>**Parent Topic:**[AWS discovery using patterns](../../discovery/reference/data-discovered-aws-patterns.md)

