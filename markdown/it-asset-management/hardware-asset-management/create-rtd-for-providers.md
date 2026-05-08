---
title: Trigger the assignment of a remote task
description: As an asset provider, create remote task definitions that trigger the assignment of a remote task for your customer to communicate the details of Zero Touch Refresh requests.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Service Exchange configuration for Zero Touch Refresh, Manage refresh of assets using Zero Touch Refresh, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Trigger the assignment of a remote task

As an asset provider, create remote task definitions that trigger the assignment of a remote task for your customer to communicate the details of Zero Touch Refresh requests.

## Before you begin

As a provider, you must have created a provider record. For more details, see Set up a Service Exchange provider record.

Role required: admin

## About this task

You receive the details of a Zero Touch Refresh Fulfillment Request from your customer's ServiceNow instance through the inbound fields of the remote task definition. Any updates made to the Zero Touch Refresh Fulfillment Request are sent to your customer's ServiceNow instance through the outbound fields of the remote task definition.

## Procedure

1.  Navigate to **All** &gt; **Service Bridge** &gt; **Provider** &gt; **Remote Task Definitions**.

2.  Select **New**.

3.  On the form, fill in the fields.

    For the description of field values, see Remote task definition form.

4.  Set the **Provider table** and **Customer table** field values to the Zero Touch Refresh Fulfillment Request \[sn\_itam\_ztr\_fulfillment\_req\] table.

5.  Select **Submit**.

6.  Select this new remote task definition record.

7.  Create the inbound fields, which enable you to receive data from the customer's instance when a remote task is created or updated.

    1.  On the **Inbound fields** tab, select **New**.

    2.  For each field you create, fill in the fields and then select **Submit**.

        For the required details of the inbound fields that you must create, see [Remote task definition inbound and outbound fields](../reference/inbound-outbound-fields-for-rtd.md).

8.  Create the outbound fields, which enable you to send data to the customer's instance when a remote task is created or updated.

    1.  On the **Outbound fields** tab, select **New**.

    2.  For each field you create, fill in the fields and then select **Submit**.

        For the required details of the outbound fields that you must create, see [Remote task definition inbound and outbound fields](../reference/inbound-outbound-fields-for-rtd.md).

9.  Set customer criteria, which specify the customers who can use this remote task definition.

10. Select **Publish**.

    **Note:** If you later need to edit this remote task definition, access it and select **Edit**.


## Result

A remote task definition record is created on your instance and the **State** field of the record is set to Published. This record is also synchronized with your customer's instance and is pending activation on your customer's instance.

