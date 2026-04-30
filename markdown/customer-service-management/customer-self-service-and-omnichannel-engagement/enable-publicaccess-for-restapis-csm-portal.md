---
title: Enable public access on REST APIs
description: Configure Scripted REST APIs to enable public access.
locale: en-US
release: zurich
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Enable public access for a catalog item, Submit catalog item as a guest, Configure the Customer and Consumer Service Portals, Set up self-service, Configure, Customer Service Management]
---

# Enable public access on REST APIs

Configure Scripted REST APIs to enable public access.

## Before you begin

Role required: admin, catalog\_admin, web\_service\_admin

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **Scripted Web Services** &gt; **Scripted REST APIs**.

2.  Search and select for the type of API that you want to edit.

    You can search for the following types of REST APIs:

    -   Service Catalog API
    -   Submit a Record Producer
    -   Validate Variable Regex \(If the item consists of a variable which requires Regex Validation\)
    -   Checkout Order Guide
    -   Variable display value
    -   Check requested for delegation on item
3.  Select the**Resources** related list.

4.  Search and select `Buy Item` in Resources.

5.  Scroll down and clear the **Requires authentication** check box under Security.

6.  Select **Update**.


-   **[Apply rate limit on REST APIs](apply-ratelimit-for-restapis-csm-portal.md)**  
Apply rate limit to REST APIs to avoid excessive use or abuse of publicly available catalog items.

**Parent Topic:**[Enable public access for a catalog item](make-item-public-csm-portal.md)

