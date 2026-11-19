---
title: AWS Marketplace pattern-based discovery
description: Discovery and Service Mapping Patterns finds active AWS Marketplace subscriptions on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery-and-service-mapping-patterns/aws-marketplace-pattern.html
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-07-23"
reading_time_minutes: 2
keywords: [AWS Marketplace, marketplace subscriptions, deployed marketplace product, AWS discovery, AWS patterns]
breadcrumb: [AWS discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# AWS Marketplace pattern-based discovery

Discovery and Service Mapping Patterns finds active AWS Marketplace subscriptions on your cloud environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

The Amazon AWS - Marketplace \(LP\) pattern discovers the following AWS Marketplace products:

-   Amazon Machine Images \(AMI\)
-   SaaS

\[Omitted image "aws-marketplace-data-model.png"\] Alt text: Amazon AWS - Marketplace \(LP\) pattern data model.

## Pattern-based discovery and mapping requirements

-   **Verify the AWS discovery prerequisites**

    For more information, see the prerequisites section in [AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md).

-   **Verify that the us-east-1 region is activated on your instance**

    The pattern connects to the AWS Marketplace APIs through us-east-1, regardless of your account's configured region.


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Amazon AWS - Marketplace \(LP\) pattern.

<table id="table_mkf_2hc_dgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the marketplace product.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

Unique identifier of the marketplace product in the format **\{productId\}/Marketplace**.

</td></tr><tr><td>

Resource Type \[resource\_type\]

</td><td>

Type of the marketplace product. For example: AmiProduct or SaaSProduct.

</td></tr><tr><td>

Plan Name \[plan\_name\]

</td><td>

Pricing plan for the marketplace subscription. Discovery maps AWS Marketplace pricing terms to the **Plan Name** values. For example:

-   UsageBasedPricingTerm: Pay As You Go
-   ByolPricingTerm: BYOL
-   RecurringPaymentTerm: Recurring

</td></tr><tr><td>

Short Description \[short\_description\]

</td><td>

Brief description of the marketplace product.

</td></tr><tr><td>

Organization Id \[organization\_id\]

</td><td>

Unique identifier of the AWS organization associated with the subscription.

</td></tr><tr><td>

Market \[market\]

</td><td>

Geographic market where the product is sold. Discovery maps AWS Marketplace currency codes to the **Market** values.For example:

-   USD: US
-   EUR: Europe
-   JPY: Japan

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Install status of the resource. Default value is Installed.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the resource. Default value is Operational.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Product Code \[product\_code\]|Unique product identifier from AWS Marketplace.|
|Publisher Name \[publisher\_name\]|Name of the organization or individual that publishes the marketplace product.|
|Version \[version\]|Version of the marketplace product. The value is set to **None**.|

\[Omitted image "aws-marketplace-dependency-view.png"\] Alt text: AWS Marketplace CIs and connections on a Dependency Views map

## CI relationships and references

The Amazon AWS - Marketplace \(LP\) pattern creates the following relationships and references to support AWS Marketplace discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Deployed Marketplace Product \[cmdb\_ci\_deployed\_marketplace\_product\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|Marketplace Product Details \[marketplace\_product\_details\]|Deployed On \[deployed\_on\]|Deployed Marketplace Product \[cmdb\_ci\_deployed\_marketplace\_product\]|

**Parent Topic:**[AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md)

