---
title: Amazon DynamoDB discovery using Patterns
description: The ServiceNow Discovery and Service Mapping applications use the Amazon AWS DynamoDB pattern to find components of DynamoDB. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: xanadu
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Amazon DynamoDB discovery using Patterns

The ServiceNow Discovery and Service Mapping applications use the Amazon AWS DynamoDB pattern to find components of DynamoDB. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

The Amazon AWS DynamoDB pattern deploys REST APIs for fetching information about DynamoDB. You can also configure Service Mapping and Discovery to discover AWS DynamoDB components using AWS events.

The ServiceNow AI Platform supports Amazon Commercial Cloud Services \(C2S\) for discovery and cloud governance. C2S is the government program that brings AWS into the Intelligence Community.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **User access**

    On the AWS Console, provide a user with the following permissions: AmazonDynamoDBReadOnly Access and AWSLambdaInvocation-DynamoDB.

-   **Cloud Service Account**

    On the ServiceNow AI Platform®, set up the service account with these properties:

    -   An **Account ID**, which is the Amazon account ID to which DynamoDB belongs. Use the Account ID as it appears in the AWS Management Console.
    -   The appropriate AWS credentials required for the account ID to reach the AWS cloud.
-   **AWS Credentials**

    On the ServiceNow AI Platform®, configure AWS credentials, using a secret key and an access key.

-   **Entry point for service containing DynamoDB**

    Use **AWS Resource Name Endpoint** as the Entry Point Type when creating a service containing DynamoDB. Provide the Amazon Resource Name \(ARN\) and host for the entry point.

-   **\(For top-down discovery by Service Mapping\) Run horizontal discovery of the Logical Datacenters**

    Discover Logical Datacenters hosting DynamoDBs as described in Run Discovery on an AWS cloud service account in the ServiceNow Cloud Provisioning and Governance documentation.

-   **Cloud Discovery**

    For Cloud Discovery, download the Discovery and Service Mapping pattern from the ServiceNow Store.

-   **MID Server**

    When installing the MID Server, ensure that the host machine meets or exceeds the [MID Server system requirements](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

-   **Discovery schedule**

    Create a schedule for the relevant AWS service account as described in Schedule Discovery on a service account in the ServiceNow Cloud Provisioning and Governance documentation.

-   **Configure AWS event service**

    To enable alert-based discovery, configure the AWS event service as described in Set up AWS event processing for Discovery and Service Mapping in the ServiceNow Cloud Provisioning and Governance documentation.


## Verify the REST API Permissions

Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

**Note:** You can test the AWS REST APIs using Postman API platform. For more information, see the [How to test AWS REST API using POSTMAN \[KB0782183\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0782183) article in the Now Support Knowledge Base.

## Data collected by Discovery during horizontal discovery

<table id="table_td3_psz_42b"><thead><tr><th>

Table and field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

DynamoDB Global Table \[cmdb\_ci\_dynamodb\_global\_table\]

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

The Amazon Resource Name \(ARN\), expressed in this format: **arn:aws:dynamodb::xxxxxxxxxxxx:table:&lt;table name&gt;**

</td></tr><tr><td colspan="2">

DynamoDB Table \[cmdb\_ci\_dynamodb\_table\]

</td></tr><tr><td>

Name \[name\]

</td><td>

Table name.

</td></tr><tr><td>

Creation date \[creation date\]

</td><td>

Creation date of DynamoDB according to the time zone of the MID Server that discovers this DynamoDB.

</td></tr><tr><td>

Cloud provider \[cloud\_provider\]

</td><td>

Amazon AWS

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

The Amazon Resource Name \(ARN\), expressed in this format: **arn:aws:dynamodb:&lt;region&gt;:xxxxxxxxxxxx:table:&lt;table name&gt;**

</td></tr><tr><td>

Global ARN \[global\_arn\]

</td><td>

The global ARN of the table for the global DynamoDB table. This field is empty if the DynamoDB is not global.

</td></tr><tr><td>

Stream ARN \[stream\_arn\]

</td><td>

The choices are:-   Stream ARN
-   Disabled

</td></tr><tr><td>

Service name \[service\_name\]

</td><td>

Set to **DynamoDB** by default.

</td></tr><tr><td>

Encryption \[encryption\]

</td><td>

Encryption configuration on DynamoDB. The choices are:-   Enabled
-   Disabled

</td></tr><tr><td>

Replication group \[replication\_group\]

</td><td>

Table ARN of the connected global DynamoDB tables.

</td></tr><tr><td>

Read Autoscaling \[read\_autoscaling\]

</td><td>

The choices are:-   Enabled
-   Disabled

</td></tr><tr><td>

Read Units \[read\_units\]

</td><td>

The number of read units on the DynamoDB table.

</td></tr><tr><td>

Read Max Units \[read\_max\_units\]

</td><td>

The maximum allowed number of read units on the DynamoDB table.

</td></tr><tr id="store-12-2018"><td>

Read Min Units \[read\_min\_units\]

</td><td>

The minimum allowed number of read units on the DynamoDB table.

</td></tr><tr><td>

Write Units \[write\_units\]

</td><td>

The number of write units on the DynamoDB table.

</td></tr><tr><td>

Write Max Units \[write\_max\_units\]

</td><td>

The maximum allowed number of write units on the DynamoDB table.

</td></tr><tr><td>

Write Min Units \[write\_min\_units\]

</td><td>

The minimum allowed number of write units on the DynamoDB table.

</td></tr><tr><td>

Table Size \[table\_size\]

</td><td>

The currently provisioned size of the DynamoDB table in bytes.

</td></tr><tr><td>

Write Autoscaling \[write\_autoscaling\]

</td><td>

The choices are:-   Enabled
-   Disabled

</td></tr><tr><td>

Point-in-Time \[point\_in\_time\]

</td><td>

The choices are:-   Enabled
-   Disabled

</td></tr></tbody>
</table>The graphic illustrates CIs that are part of DynamoDB discovery.

![DynamoDB components](../image/DynamoDB-components.png "Dependency Views showing DynamoDB components")

## CI relationships

The Amazon AWS DynamoDB pattern creates the following CI relationships:

|CI|Relationship|CI|
|---|------------|---|
|DynamoDB Global Table \[cmdb\_ci\_dynamodb\_global\_table\]|Cluster of::Cluster|DynamoDB Table \[cmdb\_ci\_dynamodb\_table\]|

## Data collected by Service Mapping during top-down discovery

The Amazon AWS DynamoDB pattern identifies connections from the DynamoDB to AWS Lambda functions.

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
</table>-   **[Define a Cloud REST Query for cloud computing devices](../task/cloud-rest-query-pattern.md)**  
As part of creating or modifying a discovery pattern, you can use the **Cloud REST Query** operation to extract information from configuration items \(CIs\) of the PaaS \(Platform as a Service\) type, such as Microsoft Azure or Amazon Web Services.

**Parent Topic:**[Available discovery patterns](available-patterns.md)

**Related topics**  


[Define a Cloud REST Query for cloud computing devices](../task/cloud-rest-query-pattern.md)

