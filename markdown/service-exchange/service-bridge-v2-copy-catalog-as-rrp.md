---
title: Publish catalog items as remote record producers
description: As a provider, you can copy your local catalog items to Service Exchange as remote record producers \(RRP\) enabling you to avoid manual re-creation of catalog items as RRPs.
locale: en-US
release: australia
product: Service Exchange
classification: service-exchange
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure for providers, Service Exchange for Providers, Service Exchange]
---

# Publish catalog items as remote record producers

As a provider, you can copy your local catalog items to Service Exchange as remote record producers \(RRP\) enabling you to avoid manual re-creation of catalog items as RRPs.

## Before you begin

Make sure that the catalog items you want to copy meet the following requirements:

-   Must be in the published state
-   Must not have been already copied to Service Exchange

Role required: admin

## About this task

By default, you can copy hardware, software, record producers, and general catalog items to RRPs, either individually or in bulk. You can copy other catalog items as well by creating a property file to include all the catalog item type you want to copy.

**Tip:** If you create a system property, make sure to select the application scope as Service Exchange provider.

After you copy, you can edit and publish these RRPs.

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

    Each RRP must have a flow. Choose one of the default Service Exchange flows provided or create your own flow if required.

8.  Add a consumer criteria.

9.  Select **Publish**.


