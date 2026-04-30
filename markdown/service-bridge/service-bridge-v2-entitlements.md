---
title: Creating entitlements in Service Exchange for Providers
description: Using consumer criteria associated with record producers and other configurations, Service Exchange automatically generates the entitlement records that are replicated to eligible consumer instances.
locale: en-US
release: xanadu
product: Service Bridge
classification: service-bridge
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Remote record producers in Service Exchange, Create remote catalogs in Service Exchange for providers, Installing and configuring Service Exchange for Providers, Service Exchange for Providers, Service Exchange]
---

# Creating entitlements in Service Exchange for Providers

Using consumer criteria associated with record producers and other configurations, Service Exchange automatically generates the entitlement records that are replicated to eligible consumer instances.

Consumer Criteria records are used to entitle Service Exchange content, such as Remote Record Producers and Remote Task Definitions, to Service Exchange consumers. Consumer criteria enables you to ensure that a consumer has access only to the appropriate Service Exchange content. Using consumer criteria, you can entitle content explicitly to a single customer or to multiple customers.

A few examples of how you configure the consumer criteria are given below. For example, you can entitle content:

-   To a specific consumer.
-   To all consumers that have an active sold product of a specific model.
-   To all consumers that have an active service contract.

The Service Exchange entitlement process runs as a scheduled job each night. During the entitlement process, filters defined in the condition builder of the consumer criteria record are applied to the selected table to find records that match the condition. If a matching record is found, the associated Service Exchange content is entitled to the consumer. For example, when a consumer with an active sold product creates an order, the appropriate Service Exchange content is automatically entitled to the consumer. Entitlements are updated daily, reflecting changes if the data in the tables being queried has changed.

## Benefits

Your consumers can see and request the content entitled to them. A scheduled job runs nightly and updates the entitlements, based on any changes made to the tables or records that are queried by the consumer criteria. Additionally, entitlements are checked immediately when updates are made.

You can update Service Exchange entitlements in the following ways:

-   Define the consumer criteria in the Remote Record Producer.
-   Register a new consumer in Service Exchange.
-   Click the **Refresh Entitlements** related link in the Consumer Connections record or the Provider record.

## Define a consumer criteria

1.  1. Navigate to **All** &gt; **Service Exchange Provider** &gt; **Remote Catalog Items** or **All** &gt; **Service Exchange Provider** &gt; **Remote Task Definitions**.
2.  Select a remote record producer or a remote task definition for which you want to define the consumer criteria.
3.  Navigate to the Consumer Criterias tab on the related list and click **New**.
4.  You can associate an existing consumer criteria or create a new one.
5.  Fill in the fields on the form.

<table id="table_u2k_mpp_b1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the consumer condition.

</td></tr><tr><td>

Active

</td><td>

Select this check box to enable the consumer condition.

</td></tr><tr><td>

Condition for

</td><td>

Allows you to specify the Company or Account can be used to match the records on the table being queried. Select the corresponding option based on which field \(Company or Account\) is available on the table being queried. For example, this field can be used on the Sold Product table as the Account field is used to query the table.

</td></tr><tr><td>

Condition on

</td><td>

Field indicates which table is to be queried to find matching records.**Note:** Tables where Customer Field cannot be selected should not be used.

</td></tr><tr><td>

Customer field

</td><td>

Select the field on the table being queried that matches the Company or Account defined on the Service Exchange connection. If the consumer connected through Service Exchange is an Account, you can use either a Company or Account field to match against it. If the consumer connected is only a Company, you will be restricted to Company.

</td></tr><tr><td>

Condition

</td><td>

Details of the filter. For example, Active is True.

</td></tr></tbody>
</table>
The following examples show how consumer criteria can be configured.

This consumer criteria can be used to entitle content to Service Exchange customers that have an active sold product where product name contains **Laptop – DaaS**.

![Consumer criteria configuration example 1](../image/service-bridge-v2-consum-crit-ex1.jpg)

This consumer criteria entitles content to the Boxeo Service Exchange consumer. It is used to query the Service Exchange Connection table and is filtered with Boxeo as the consumer.

![Consumer criteria configuration example 2](../image/service-bridge-v2-consum-crit-ex2.jpg)

This consumer criteria entitles content to Service Exchange consumers that have an active contract where the Contract model is Print Solution and the Contract Type is Service Contract.

![Consumer criteria configuration example 3](../image/service-bridge-v2-consum-crit-ex3.jpg)

