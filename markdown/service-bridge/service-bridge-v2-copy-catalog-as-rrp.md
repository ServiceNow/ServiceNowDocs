---
title: Publish catalog items as remote record producers
description: As a provider, you can copy your local catalog items to Service Exchange as remote record producers \(RRP\) to avoid having to manually re-create catalog items as RRPs.
locale: en-US
release: yokohama
product: Service Bridge
classification: service-bridge
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Use Service Exchange for providers, Service Exchange for Providers, Service Exchange]
---

# Publish catalog items as remote record producers

As a provider, you can copy your local catalog items to Service Exchange as remote record producers \(RRP\) to avoid having to manually re-create catalog items as RRPs.

## Before you begin

Make sure that the catalog items you want to copy meet the following requirements:

-   Must be in the published state
-   Must be of a supported class: sc\_cat\_item, sc\_cat\_item\_producer, pc\_hardware\_cat\_item, or pc\_software\_cat\_item
-   Must not have been already copied to Service Exchange

Role required: admin

## About this task

You can copy hardware, software, record producers, and general catalog items to RRPs, either individually or in bulk. After you copy, you can edit and publish these RRPs.

## Procedure

1.  Navigate to **All** and type `sc_cat_item.list` in the navigation filter.

2.  Select the catalog item.

    You can select more than one.

    By default, you can copy 20 catalog items as RRPs at a time. If you want to change the limit, you need to add the **sn\_sb\_pro.max\_batch\_size\_covertable\_catalog\_items** system property, which is of type Integer.

3.  From the action menu, select **Publish to Service Exchange**.

    A message is displayed stating the publishing status.

    -   If the publishing to Service Exchange is successful, a success message is displayed.
    -   If the publishing isn’t successful, a failed message is displayed.

        Resolve the failed process by reviewing the logs to identify the issues, fixing the issues, and trying to publish to Service Exchange again.

4.  View copied RRPs by selecting **Click here** in the success message.

5.  Review the copied RRPs for accuracy.

6.  Add a variable to each RRP if not already available.

    Each RRP must have at least one variable. You can add more than one variable. For more details, see [Create variables for remote record producers in Service Exchange for Providers](service-bridge-v2-assign-variables-ser-defn.md).

7.  Add a flow to the RRP using **Flow** field.

    Each RRP must have a flow. Choose one of the default Service Exchange flows provided or create your own flow if needed.

8.  Determine which customers can use the RRP by adding consumer criteria to the RRP.

    1.  Open the RRP.

    2.  In the **Consumer criteria** related tab, select **New**.

    3.  In the **Consumer condition** field, provide the customer company or account that can access this remote task definition.

        For more details on consumer criteria, see [Creating entitlements in Service Exchange for Providers](../concept/service-bridge-v2-entitlements.md).

9.  Select **Publish**.


## Result

Remote record producer records are created on your instance. These records are also synchronized with your customer's instance and are pending activation on your consumer's instance.

