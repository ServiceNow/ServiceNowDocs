---
title: Amazon Relational Database Service \(Amazon RDS\) discovery with Patterns
description: Discovery and Service Mapping Patterns uses the Amazon AWS Relational Database Service pattern to find Amazon RDS components in your environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
keywords: [Relational Database Service, RDS, Amazon RDS]
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Amazon Relational Database Service \(Amazon RDS\) discovery with Patterns

Discovery and Service Mapping Patterns uses the Amazon AWS Relational Database Service pattern to find Amazon RDS components in your environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

Amazon RDS is a managed relational database service by Amazon Web Services \(AWS\). Amazon RDS enables you to create and manage relational database instances in the cloud.

The ServiceNow AI Platform supports Amazon Commercial Cloud Services \(C2S\) for discovery and cloud governance. C2S is the government program that brings AWS into the Intelligence Community.

## Prerequisites

-   Install the Discovery and Service Mapping Patterns application from the ServiceNow Store.
-   On the ServiceNow AI Platform, configure AWS credentials, using a secret key and an access key.
-   [Create a service account](../../cloud-management-v2-setup/task/aws-first-cld-and-srvc-accts.md). Set the **Account ID** to the Amazon account ID to which RDS belongs. Use the Account ID as it appears in the AWS Management Console.
-   Set read-only permissions for these REST APIs:
    -   https://rds.&lt;REGION&gt;.amazonaws.com/?Action=DescribeDBInstances
    -   https://rds.&lt;REGION&gt;.amazonaws.com/?Action=DescribeDBInstances&amp;DBInstanceIdentifier=&lt;input\_object\_id&gt; for events discovery
    -   https://tagging.&lt;REGION&gt;.amazonaws.com/ for tags discovery
-   Ensure to place the MID Server inside the Amazon cloud.
-   For Cloud Discovery, download the Discovery and Service Mapping pattern from the ServiceNow Store.
-   When installing the MID Server, ensure that the host machine meets or exceeds the [MID Server system requirements](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) published on the ServiceNow documentation site.

## Verify the REST API Permissions

Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

**Note:** You can test the AWS REST APIs using Postman API platform. For more information, see the [How to test AWS REST API using POSTMAN \[KB0782183\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0782183) article in the Now Support Knowledge Base.

## Support for AWS services in the China region

The latest version of Discovery and Service Mapping Patterns supports discovering AWS services in the China region. You can discover these services on the ServiceNow AI Platform, starting from Xanadu Patch 3 and Washington DC Patch 9 instances.

Discovering AWS services in the China region requires using a datacenter URL when setting up an AWS service account. For example: `https://organizations.cn-northwest-1.amazonaws.com.cn`.

-   To learn more about AWS master account and sub-account support in the China region, see [KB1704526](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1704526).
-   To identify AWS patterns supported in the China region, refer to the Cloud Discovery patterns spreadsheet. The **AWS China Region Support** column has a Yes value for supported patterns.

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Amazon AWS Relational Database Service pattern.

<table id="table_cloud_database"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object ID \[object\_id\]

</td><td>

Unique identifier for the RDS database instance, assigned by AWS.

</td></tr><tr><td>

Name \[name\]

</td><td>

Name of the database. If no database name is provided, the value is the same as the Object ID.

</td></tr><tr><td>

Fully qualified domain name \[fqdn\]

</td><td>

Fully qualified domain name \(FQDN\) endpoint used to connect to the database instance.

</td></tr><tr><td>

TCP port\(s\) \[tcp\_port\]

</td><td>

Port number on which the database instance accepts connections.

</td></tr><tr><td>

Type \[type\]

</td><td>

Database engine type. For example: mysql, postgres, or aurora.

</td></tr><tr><td>

Version \[version\]

</td><td>

Database engine version number.

</td></tr><tr><td>

Category \[category\]

</td><td>

DB instance class that specifies the compute and memory capacity. For example: db.t3.micro or db.m5.large.

</td></tr><tr><td>

IP Address \[ip\_address\]

</td><td>

IP address resolved from the FQDN.

</td></tr><tr><td>

State \[state\]

</td><td>

State of the database instance. For example: Available or Terminated.

</td></tr><tr><td>

Automated Backups \[automated\_backup\]

</td><td>

Indicates whether automated backups are enabled and the retention period. Possible values are either **Disabled** or **Enabled \(X Days\)**, where X represents the backup retention period in days.

</td></tr><tr><td>

Deletion Protection Enabled \[deletion\_protection\_enabled\]

</td><td>

Indicates whether deletion protection is enabled for the database instance. Possible values are **true** or **false**. -   **true**: Deletion protection is enabled and the database can't be deleted
-   **false**: Deletion protection is disabled

</td></tr><tr><td>

IAM Authentication Enabled \[iam\_authentication\_enabled\]

</td><td>

Indicates whether AWS Identity and Access Management \(IAM\) database authentication is enabled. Possible values are **true** or **false**. -   **true**: IAM authentication is enabled and you can use IAM credentials to authenticate to the database
-   **false**: IAM authentication is disabled

</td></tr><tr><td>

Storage Encrypted \[storage\_encrypted\]

</td><td>

Indicates whether the database storage is encrypted.

</td></tr><tr><td>

Multiple Availability Zones \[multi\_az\]

</td><td>

Indicates whether the database instance is deployed across multiple Availability Zones for high availability.

</td></tr><tr><td>

Publicly Enabled \[publicly\_enabled\]

</td><td>

Indicates whether the database instance is publicly accessible from the internet.

</td></tr><tr><td>

Vendor \[vendor\]

</td><td>

Database vendor. Value is set to **Amazon**.

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Install status of the database instance. Default value is Installed.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the database instance. Default value is Operational.

</td></tr></tbody>
</table><table id="table_ip_address"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

IP Address \[ip\_address\]

</td><td>

IP address resolved from the database instance FQDN.

</td></tr><tr><td>

Netmask \[netmask\]

</td><td>

Network mask for the IP address. Value is set to 0.0.0.0.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|Availability Zone identifier.|
|Name \[name\]|Availability Zone name.|

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|Virtual Private Cloud \(VPC\) identifier for the network containing the database instance.|

## CI relationships

The Amazon AWS Relational Database Service pattern creates these relationships to support Amazon RDS discovery.

|CI|Relationship|CI|
|---|------------|---|
|Availability Zone \[cmdb\_ci\_availability\_zone\]|Contains::Contained by|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|
|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|Contains::Contained by|Availability Zone \[cmdb\_ci\_availability\_zone\]|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|Uses::Used by|Cloud Network \[cmdb\_ci\_network\]|
|Cloud Network \[cmdb\_ci\_network\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Key Value \[cmdb\_key\_value\]|References|Cloud DataBase \[cmdb\_ci\_cloud\_database\]|

## AWS Tag discovery

The Amazon AWS Relational Database Service pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Cloud DataBase \[cmdb\_ci\_cloud\_database\] table.|

**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)

