---
title: AWS tag discovery
description: The ServiceNow Discovery and Service Mapping applications can use patterns to discover the tags for AWS resources and configuration item \(CI\) types, and then populate the CMDB with these discoveries. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS tag discovery

The ServiceNow Discovery and Service Mapping applications can use patterns to discover the tags for AWS resources and configuration item \(CI\) types, and then populate the CMDB with these discoveries. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

This tag-specific discovery pattern is in addition to the other AWS patterns available on the ServiceNow Store.This pattern extends the ones used for discovering the respective AWS resources.

Discovery populates the CMDB with tags for the following AWS patterns and CI types:

-   Amazon AWS - ACL \(LP\) \[cmdb\_ci\_network\_acl\]
-   Amazon AWS API Gateway \[cmdb\_ci\_cloud\_gateway\]
-   Amazon AWS - Application and Network LB \(LP\) \[cmdb\_ci\_cloud\_load\_balancer\]
-   Amazon AWS Application and Network LBs Events
-   Amazon AWS - Classic LB \(LP\) \[cmdb\_ci\_cloud\_load\_balancer\]
-   Amazon AWS Classic LB Events
-   Amazon AWS Cognito \[cmdb\_ci\_cloud\_authentication\]
-   Amazon AWS - Customer Gateway \(LP\) \[cmdb\_ci\_customer\_gateway\]
-   Amazon AWS DB Cluster
-   Amazon AWS DynamoDB \[cmdb\_ci\_dynamodb\_table\]
-   Amazon AWS ElastiCache
-   Amazon AWS - ECS \[cmdb\_ci\_cloud\_service\_account\]
-   Amazon AWS - Executable Template \(LP\) \[cmdb\_ci\_os\_template\]
-   Amazon AWS - Host \(LP\)
-   Amazon AWS - Internet Gateway \(LP\)
-   Amazon AWS keyspace
-   Amazon AWS - Key Pair \(LP\)
-   Amazon AWS Lambda \[cmdb\_ci\_cloud\_function\]
-   Amazon AWS - LB Pool \(LP\)
-   Amazon AWS - NAT Gateway \(LP\)
-   Amazon AWS - Network \(LP\)
-   Amazon AWS Network Events
-   Amazon AWS - NIC \(LP\)
-   Amazon AWS - Owned Template \(LP\)
-   Amazon AWS - Public IP Address \(LP\)
-   Amazon AWS Redshift
-   Amazon AWS Relational Database Service \[cmdb\_ci\_cloud\_database\]
-   Amazon AWS Resource Inventory
-   Amazon AWS - Route Table \(LP\)
-   Amazon AWS S3 \[cmdb\_ci\_cloud\_object\_storage\]
-   Amazon AWS - Security Group \(LP\)
-   Amazon AWS Security Group Events
-   Amazon AWS Serverless Database
-   Amazon AWS - Storage \(LP\)
-   Amazon AWS Storage Events
-   Amazon AWS sub account discovery
-   Amazon AWS - Subnet \(LP\)
-   Amazon AWS - Virtual Server \(LP\)
-   Amazon AWS Virtual Server Events
-   Amazon AWS - VPN Connections \(LP\)
-   Amazon AWS - VPN Gateway \(LP\)

**Note:** For more information about the tags and patterns for each of these resources, see the documentation for the specific AWS resource.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **AWS Credentials**
    -   On the ServiceNow AI Platform, configure AWS credentials, using a secret key and an access key.
    -   Have an Amazon **Account ID**. Use the Account ID as it appears in the AWS Management Console. You can run Discovery from the service account form.
    -   Set read-only permissions for the following URL: `https//tagging.<region>.amazonaws.com.`
-   **Discovery schedule**

    Create a schedule for the relevant AWS service account. For more information, see [Create a discovery schedule in Cloud Discovery Workspace](../../discovery/task/cloud-operations-disco-create-schedule.md).


## Pattern tasks

When discovering AWS tags, the pattern completes the following high-level tasks:

-   Sets the Resource Type filter: Filters the tags to only those tags related to the pattern CI type.
-   Initiates the Cloud API call: The API call to the cloud environment that collects the tags and parses their attributes in the Tags table.
-   Parses the resource name from the Amazon Resource Name \(ARN\). Each Amazon resource is assigned a name and a unique identifier.

    **Note:** Parsing the resource name is needed only for patterns where the main identification section does not work with the ARN of the AWS resource. When that is the case, a relation attribute has to be parsed from the AWS ARN.

-   Includes references to cloud resource type. Establishes the relationship between the tag and the cloud resource type.

## Cloud Rest Call

The pattern includes an API called "Cloud Rest Call” Post Call used to collect the following data:

-   API URL used to retrieve the data — "https://tagging." + $ldc\[1\].object\_id + ".amazonaws.com/“
-   API Body — "\{\\"ResourceTypeFilters\\":\[\\"" + $resource\_type + "\\"\]\}“
-   Headers — "Content-Type:application/x-amz-json-1.1,X-Amz-Target:ResourceGroupsTaggingAPI\_20170126.GetResources"

This data displays as shown in the following window.

![Data from Cloud Rest Call](../image/aws-tagging-pattern-api.png "Data from Cloud Rest Call")

## Data collected by Discovery during horizontal discovery

The pattern collects the following data during horizontal discovery:

<table id="table_olk_1pq_f56b"><thead><tr><th>

Table and field

</th><th>

Additional information

</th></tr></thead><tbody><tr><td colspan="2">

CI type \[cmdb\_key\_value\]

</td></tr><tr><td>

Key

</td><td>

Tag key

</td></tr><tr><td>

Value

</td><td>

Tag value

</td></tr><tr><td>

Object\_id

</td><td>

Unique resource ID that identifies the resource in the AWS console.

</td></tr><tr><td colspan="2">

Class model \[cmdb\_key\_value\]

</td></tr><tr><td>

Extends table

</td><td>

Not applicable

</td></tr><tr><td>

Identifier – Object\_id

</td><td>

Related entries to cloud resources

</td></tr><tr><td>

Metadata rules

</td><td>

Not applicable

</td></tr></tbody>
</table>This data is displayed as shown in the following window:

![Data collected during horizontal discovery](../image/aws-tagging-key-value.png "Data collected during horizontal discovery")

AWS discovery pattern uses the following EVAL:

```
var rtrn;
var name = ${cmdb_key_value[].object_id}
name = name.substring(name.lastIndexOf("restapis/")+9,name.lastIndex);
name = name.substring(0,name.indexOf("/"));
rtrn = name;

```

Similar EVALS are available for patterns where the main identification section does not include ARN information in the main CI type table. When this information is not available, the Tag Extension section must parse a unique ARN used to establish the relationship to the related cloud resource.

**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)

