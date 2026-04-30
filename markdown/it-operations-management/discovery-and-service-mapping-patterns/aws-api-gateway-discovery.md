---
title: Amazon API Gateway discovery with Patterns
description: The ServiceNow Discovery and Service Mapping applications use the Amazon AWS API Gateway pattern to find Amazon API Gateways and connections to other entities. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: xanadu
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Amazon API Gateway discovery with Patterns

The ServiceNow Discovery and Service Mapping applications use the Amazon AWS API Gateway pattern to find Amazon API Gateways and connections to other entities. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

Starting with Discovery and Service Mapping Patterns version 1.29.0, the Amazon AWS API Gateway pattern data model has changed.

![Amazon AWS API Gateway pattern new data model relationships](../image/aws-api-gateway-new-model.png "New Amazon AWS API Gateway pattern data model")

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Verify the AWS prerequisites**

    For more information, see the prerequisite section in [Amazon AWS Cloud components discovery using patterns](../../discovery/reference/data-discovered-aws-patterns.md).

-   **Retire legacy data model CIs to avoid duplicates**

    To avoid duplicate CIs, activate a schedule job to mark legacy data model CIs as retired. For more information, see [Retire legacy AWS API Gateway data model CIs](../task/retire-legacy-aws-api-gateway-cis.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Amazon AWS API Gateway pattern.

<table id="table_axv_trw_chc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Concatenate of "aws-gateway-" + account ID + region.For example: **aws-gateway-000000000000-us-east-1**.

</td></tr><tr><td>

ID \[id\]

</td><td>

Concatenate of "aws-gateway-" + account ID + region.For example: **aws-gateway-000000000000-us-east-1**.

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Install status of the AWS gateway. Default value is Installed.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the AWS gateway. Default value is Operational.

</td></tr></tbody>
</table><table id="table_brf_rtw_chc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ID \[id\]

</td><td>

Concatenate of "https://" + API ID + ".execute-api." + region + ".amazonaws.com". For example: **https://a1b2c3d4e5.execute-api.us-east-1.amazonaws.com**.

</td></tr><tr><td>

Name \[name\]

</td><td>

Name of the API.

</td></tr><tr><td>

Description \[short\_description\]

</td><td>

Description of API.

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Install status of the API. Default value is Installed.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the API. Default value is Operational.

</td></tr><tr><td>

Type \[type\]

</td><td>

Type of API: REST.

</td></tr><tr><td>

Version \[version\]

</td><td>

Version of API.

</td></tr><tr><td>

Fully qualified domain name \[fqdn\]

</td><td>

Concatenate of API ID + ".execute-api." + region + ".amazonaws.com".For example: **a1b2c3d4e5.execute-api.us-east-1.amazonaws.com**.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Name \[name\]|Unique name or IP address of the DNS host.|
|IP Address \[ip\_address\]|IP address of the DNS host.|

![aWS API gateway CIs and connections on a Dependency Views map](../image/aws-api-gateway-dependency-view.png "Amazon API gateway dependency view")

## Relationships

Discovery creates these relationships to support Amazon API Gateway discovery.

|CI|Relationship|CI|
|---|------------|---|
|AWS API Gateway \[cmdb\_ci\_aws\_api\_gateway\]|Provides::Provided by|Managed API \[cmdb\_ci\_managed\_api\]|
|Managed API \[cmdb\_ci\_managed\_api\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Managed API \[cmdb\_ci\_managed\_api\]|Uses::Used by|DNS Name \[cmdb\_ci\_dns\_name\]|
|DNS Name \[cmdb\_ci\_dns\_name\]|Hosted on::Hosts|AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]|
|Key Value \[cmdb\_key\_value\]|References|Managed API \[cmdb\_ci\_managed\_api\]|

## Tag discovery

The Amazon AWS API Gateway pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Managed API \[cmdb\_ci\_managed\_api\] table.|

## Connections discovered by Service Mapping during the top-down discovery

Service Mapping performs the top-down discovery of the AWS API Gateways in the context of application services. It discovers outgoing connections of the AWS API Gateways:

-   AWS Lambda
-   VPC Link for Virtual Private Cloud
-   HTTP endpoint defined as the configured URL on the API Gateway

-   **[Test patterns for discovering AWS API Gateway and AWS Lambda](../task/test-patterns-for-discovering-aws-api-and-aws-lambda.md)**  
Run the horizontal and top-down discovery using Amazon AWS API Gateway \[cmdb\_ci\_cloud\_gateway\] and Amazon AWS Lambda \[cmdb\_ci\_cloud\_function\] patterns. Verify that the result is as expected.
-   **[Retire legacy AWS API Gateway data model CIs](../task/retire-legacy-aws-api-gateway-cis.md)**  
Avoid duplicate AWS API Gateway configuration items \(CIs\) by retiring legacy data model CIs through a scheduled job.

**Parent Topic:**[Available discovery patterns](available-patterns.md)

