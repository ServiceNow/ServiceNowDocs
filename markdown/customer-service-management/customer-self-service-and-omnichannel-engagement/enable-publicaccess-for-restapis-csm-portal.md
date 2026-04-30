---
title: Enable public access on REST APIs
description: Enable public access for the API resources to allow guest users to submit form.
locale: en-US
release: yokohama
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Enable public access for a catalog item, Enabling guest users to submit a catalog item on the Customer Service Portal, Configure the Customer and Consumer Service Portals, Set up self-service, Configuring Customer Service Management, Customer Service Management]
---

# Enable public access on REST APIs

Enable public access for the API resources to allow guest users to submit form.

## Before you begin

Role required: admin, catalog\_admin, web\_service\_admin

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **Scripted Web Services** &gt; **Scripted REST APIs**.

2.  Search and select `Service Catalog API` in the name field.

3.  Under Related Links, select **Resources**.

    ![showing resource tab on the service catalog api page](../image/service-catalog-api.png)

4.  Search and select the required items in Resources.

    You can search for the following types of REST APIs:

    -   Buy Item
    -   Submit a Record Producer
    -   Validate Variable Regex \(If the item consists of a variable which requires Regex Validation\)
    -   Checkout Order Guide
    -   Variable display value
    -   Check requested for delegation on item
5.  Scroll down and clear the **Requires authentication** check box under Security.

    ![showing requires authentication checkbox in the security tab](../image/requires-authentication-api.png)

6.  Select **Update**.


## Result

The REST APIs used to allow form submission for the guest users are made public.

