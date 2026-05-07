---
title: Create a consumer criteria
description: Using consumer criteria associated with record producers and other configurations, Service Exchange automatically generates the entitlement records that are replicated to eligible consumer instances.
locale: en-US
release: australia
product: Service Exchange
classification: service-exchange
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create remote catalogs, Configure for providers, Service Exchange for Providers, Service Exchange]
---

# Create a consumer criteria

Using consumer criteria associated with record producers and other configurations, Service Exchange automatically generates the entitlement records that are replicated to eligible consumer instances.

## Before you begin

Role required: admin

## Procedure

1.  In the Consumer Criteria related table, select **New**.

2.  In the **Condition** field, select the Lookup using list icon, and then either select an existing condition or create a new condition![Lookup using list icon](../../../common/image/List_SearchIcon.png).

<table id="choicetable_yhh_n4d_5fc"><thead><tr><th align="left" id="d22226e75">

Option

</th><th align="left" id="d22226e78">

Action

</th></tr></thead><tbody><tr><td id="d22226e84">

**Select existing condition**

</td><td>

From the list, select an existing condition.

</td></tr><tr><td id="d22226e93">

**Create a new condition**

</td><td>

1.  In the Entity Criteria popup, select **New**.
2.  On the Consumer criteria new record form, fill in the fields.

For a description of the field values, see [Consumer criteria new record form](../reference/service-bridge-v2-consumer-criteria-new-record-form.md).

3.  Select **Submit.**
4.  From the criteria list, select your criteria.


</td></tr></tbody>
</table>
## Consumer criteria

The following examples show how consumer criteria can be configured.

This consumer criteria can be used to entitle content to Service Exchange customers that have an active sold product where product name contains **Laptop – DaaS**.

![Consumer criteria configuration example 1](../image/service-bridge-v2-consum-crit-ex1.jpg)

This consumer criteria entitles content to the Boxeo Service Exchange consumer. It is used to query the Service Exchange Connection table and is filtered with Boxeo as the consumer.

![Consumer criteria configuration example 2](../image/service-bridge-v2-consum-crit-ex2.jpg)

This consumer criteria entitles content to Service Exchange consumers that have an active contract where the Contract model is Print Solution and the Contract Type is Service Contract.

![Consumer criteria configuration example 3](../image/service-bridge-v2-consum-crit-ex3.jpg)

