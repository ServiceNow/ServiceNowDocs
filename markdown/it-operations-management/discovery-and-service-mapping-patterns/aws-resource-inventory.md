---
title: AWS Resource Inventory discovery with Patterns
description: The ServiceNow Discovery and Service Mapping applications can find and map the AWS resources available by AWS Config Service. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS Resource Inventory discovery with Patterns

The ServiceNow Discovery and Service Mapping applications can find and map the AWS resources available by AWS Config Service. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

Discovery uses the AWS Resource Inventory pattern to discover the resources available through AWS. Use this pattern for AWS resources which do not have a dedicated pattern, such as AWS Lambda or EC2. This pattern is limited to resources that are available from AWS Config Service, as described in the [AWS Config Developer Guide](https://docs.aws.amazon.com/config/latest/developerguide/resource-config-reference.html).

You can use this pattern on the ServiceNow platform using London \(Patch 8\), Madrid \(Patch 2\), or later releases.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   Create AWS credentials.
-   Create an AWS cloud service account.

    You can use only the AWS management service account for discovery, not its sub-accounts.

    **Note:** The Cloud Discovery user interface refers to member accounts as sub-accounts.

-   Discover AWS Datacenters \(LDC\)
-   Schedule a full AWS discovery or use a specific inventory pattern
-   Fine-tune AWS resource discovery using the Resource Inclusion List.

    If your deployment has custom patterns for AWS discovery, ensure that you do not discover AWS resources twice.

    1.  Ensure that the application scope is Discovery and Service Mapping Patterns:
        1.  Navigate to **Settings** &gt; **Developer**.
        2.  Select `Discovery and Service Mapping Patterns` from the **Application** list.
    2.  Navigate to **System Definitions** &gt; **Tables**.
    3.  Open the Cloud Inventory Resource Inclusion List \[sa\_cloud\_inventory\_resource\_whitelist\] table.
    4.  Under **Related Links**, click **Show List**.
    5.  Select resource types for which you have custom patterns, and select `Delete` from the **Actions on selected rows** list.
    The Cloud Inventory Resource Inclusion List is predefined with common services. You can expand the list with additional resource types that you want the pattern to discover. The names of these resource types must conform to the appropriate vendor naming conventions.

    **Note:** When you modify the out-of-the-box inclusion list, it is no longer updated automatically in application updates. You need to maintain the customized list on your own.

    1.  Open the Cloud Inventory Resource Inclusion List \[sa\_cloud\_inventory\_resource\_whitelist\] table.
    2.  Click **New**.
    3.  Fill in the form, and then click **Submit**.

        |Field|Description|
        |-----|-----------|
        |Cloud Vendor|The vendor of the resource type: AWS.|
        |Resource Type|The AWS resource type value. For example, AWS::CloudWatch::Alarm.|
        |Application|The application scope: Discovery and Service Mapping Patterns.|

    The changes are applied the next time you run the pattern.

-   To discover the resources that support the AWS Config service, the pattern uses API: `https://config.[AWS region].amazonaws.com`. It specifies the resource type in the API request using the following format: `{"resourceType":"AWS::[RESOURCE]::[TYPE]"}`​

    The POST method requires the following headers:

    -   X-Amz-Target - StarlingDoveService.ListDiscoveredResources​
    -   Accept - application/json​
    -   Content-Type - application/x-amz-json-1.1​
-   To discover the resource tags for resources that support tags, the pattern uses API: `https://tagging.[AWS region].amazonaws.com`. It specifies the resource type in the API request using the following format: `{"ResourceTypeFilters": [“[resource]:[type]"]}`

    The POST method requires the following headers:

    -   X-Amz-Target - ResourceGroupsTaggingAPI\_20170126.GetResources​
    -   Accept - application/json​
    -   Content-Type - application/x-amz-json-1.1​

## Data collected by Discovery during horizontal discovery

|Table and field|Description|
|---------------|-----------|
|Main CI \[cmdb\_ci\_cmp\_resource\]|
|object\_id|The ID of the item. This is typically the Amazon Resource Name \(ARN\).|
|name|Name of the resource.|
|resource\_type|The asset resource type, based on the contents of the JSON file.|
|description|Short description of how the CI is populated.|

## CI relationships

The AWS Resource Inventory pattern creates the following CI relationship:

|CI|Relationship|CI|
|---|------------|---|
|Cloud Resource \[cmdb\_ci\_cmp\_resource\]|Hosted on :: Hosts|Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]|

The following is a dependency view of the collected data flow.

![AWS Resource Inventory dependency view](../image/aws-resource-inventory.png "AWS Resource Inventory dependency view")

**Parent Topic:**[AWS discovery using patterns](../../discovery/reference/data-discovered-aws-patterns.md)

