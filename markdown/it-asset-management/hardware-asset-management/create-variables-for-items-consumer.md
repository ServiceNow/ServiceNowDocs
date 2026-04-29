---
title: Create variables for the catalog item associated with the Zero Touch request flow
description: Create variables for your catalog item so that your provider can fulfill the requests for that item based on the variable details.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage Service Catalog items for the Zero Touch request flow, Zero Touch request flow, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Create variables for the catalog item associated with the Zero Touch request flow

Create variables for your catalog item so that your provider can fulfill the requests for that item based on the variable details.

## Before you begin

Role required: catalog\_admin

## About this task

To enable your provider to fulfill the catalog requests accurately, you must create variables similar to the variables associated with your provider's remote record producer. For example, if the remote record producer has size and color variables, then you must create the same set of variables for the catalog item. For details, see [View the variables of a remote record producer](view-remote-record-producer-variables.md).

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **Maintain Items**.

2.  Select the catalog item.

3.  On the catalog form, select the **Variables** tab.

4.  Select **New**.

5.  On the form, fill in the fields.

    For details on the form fields, see [Service Catalog variable form fields](../reference/service-catalog-var-form-fields.md).

    **Important:** If your provider supports multiple quantities of an asset in a single request, hide the equivalent quantity variable for the catalog item by selecting the **Hidden** check box. This approach avoids multiple quantity fields on the catalog request.

6.  Select **Submit**.


## Result

The variables are displayed on the Service Catalog request for that catalog item.

## What to do next

[Associate a catalog item with a remote record producer](associate-catalog-item-with-record-producer.md).

