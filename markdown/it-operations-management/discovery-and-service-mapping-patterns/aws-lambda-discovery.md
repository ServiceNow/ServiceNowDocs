---
title: AWS Lambda discovery with Patterns
description: The ServiceNow Discovery and Service Mapping applications can find and map Lambda functions that run in your AWS cloud. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS Lambda discovery with Patterns

The ServiceNow Discovery and Service Mapping applications can find and map Lambda functions that run in your AWS cloud. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

Discovery and Service Mapping use the Amazon AWS Lambda pattern to run horizontal and top-down discovery. When you run cloud discovery, your instance queries your AWS service account using the necessary credentials, and then runs a query to obtain Lambda information. The pattern parses this information and then it is saved in the CMDB.

You can use this pattern on the ServiceNow platform using Jakarta Patch 10, Kingston Patch 8, or London Patch 1.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Update set**

    If your instance is on the Jakarta or Istanbul versions, import the update set provided in [KB0679927](https://support.servicenow.com/kb_view.do?sysparm_article=KB0679927): AWS Lambda top-down discovery update set. This update set is required for Service Mapping.

-   **User policy for AWS user**

    If you use Identity and Access Management \(IAM\) to manage users in Amazon Web Services \(AWS\) platform, ensure that you created a user policy for the AWS user. For more information, refer to [Control AWS access and permissions using policies](../../it-operations-management/task/aws-create-user-policy-cloud-mgt.md) in the ServiceNow Cloud Provisioning and Governance documentation.

-   **AWS service account with credentials**

    You must set up your service account with the appropriate AWS credentials. You run discovery from the service account form.

    Refer to Service accounts for Discovery and Service Mapping in product documentation.

-   **Service account**

    On the ServiceNow platform, create a service account. Set the Account ID to the Amazon account IT to which AWS Lambda belongs. Use the Account ID as it appears in the AWS Management Console. Ensure to place the MID Server on the virtual machine that is part of the service account that you are planning to discover.

-   **Discover logical datacenters using horizontal discovery**

    Click **Discover datacenters** under **Related Links** on the Cloud Service Account form.

-   **User permissions**

    Provide a user with permissions to run the ListFunctions API with the Resource: arn:aws:lambda:region:account-id: function:function-name. Provide a user with permissions to run the GetFunction API with the Resource: ‘\*’.

-   **Amazon Resource Name \(ARN\)**

    \(Optional for application services using ARN as an entry point\) Ensure that you know the ARN for the AWS Lambda you need to discover. ARNs serve as the resource identifiers for Amazon Web Services.

-   **Host**

    If your instance is on the Jakarta or Istanbul versions, use the following host: 127.0.0.1.

-   **Cloud Discovery**

    For Cloud Discovery, download the Discovery and Service Mapping Patterns from the ServiceNow Store.

-   **MID Server**

    When installing the MID Server, ensure that the host machine meets or exceeds the [MID Server system requirements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/r_MIDServerSystemRequirements.md) published on the ServiceNow documentation site.


## Verify the REST API Permissions

Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

**Note:** You can test the AWS REST APIs using Postman API platform. For more information, see the [How to test AWS REST API using POSTMAN \[KB0782183\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0782183) article in the Now Support Knowledge Base.

## Data collected by Discovery during horizontal discovery

Horizontal discovery populates this data in the CMDB:

|Table and field|Description|
|---------------|-----------|
|Cloud Function \[cmdb\_ci\_cloud\_function\]|
|Name \[name\]|The name of the function.|
|Object ID \[object\_id\]|The ID \(Amazon Resource Name\) of the AWS Lamdba function, for example: `arn:aws:lambda:{datacenter}1:751200741520:function:{function-name}`|
|Version \[version\]|The version of the function. For example, `$Latest` represents the most recent published version.|
|Language \[language\]|The runtime environment, or language and version, that the function is written in, for example: `Node.js6.10` for JavaScript version 6.10.|
|Code Location URL \[code\_location\_url\]|The URL of the function that you built from the API Gateway console.|
|CodeSha256 \[codesha256\]|The cryptographic hash signature for the function.|
|Code Size \[code\_size\]|The size of the function code in MB.|
|Function Last Modified \[function\_last\_modified\]|The date the function last changed in your AWS Lamdba environment.|

**Note:** To see all of these fields, you need to configure the form layout as described in product documentation.

## CI relationships

These relationships are created to support AWS Lambda discovery:

<table id="table_bhf_412_ycb"><thead><tr><th>

CI

</th><th>

Relationship

</th><th>

CI

</th></tr></thead><tbody><tr><td rowspan="3">

Cloud Function \[cmdb\_ci\_cloud\_function\]

</td><td>

Uses:Used by

</td><td>

Cloud DataBase\[cmdb\_ci\_cloud\_database\]

</td></tr><tr><td>

Hosted on:Hosts

</td><td>

AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]The AWS datacenter has relationships to other AWS CIs, such as availability zones, service accounts, and so on. Refer to AWS and Azure cloud discovery in product documentation.

</td></tr><tr><td>

Provides:Is provided by

</td><td>

Cloud Event Source \[cmdb\_ci\_cloud\_event\_source\]This CI could be any event source that triggers the cloud function or the API Gateway.

</td></tr></tbody>
</table>## Connections discovered by Service Mapping during the top-down discovery

Service Mapping performs the top-down discovery of the AWS Lambda in the context of application services. It discovers outgoing connections of the AWS Lambda:

-   AWS API Gateway
-   Amazon Relational Database Service \(RDS\)
-   Other instance of AWS Lambda inside or outside the current region using ARN

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

**Related topics**  


[Test patterns for discovering AWS API Gateway and AWS Lambda](../task/test-patterns-for-discovering-aws-api-and-aws-lambda.md)

[Define a Cloud REST Query for cloud computing devices](../task/cloud-rest-query-pattern.md)

