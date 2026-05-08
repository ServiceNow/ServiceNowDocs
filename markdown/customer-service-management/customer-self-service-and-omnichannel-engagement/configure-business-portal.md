---
title: Configure Business and Consumer Portal
description: Configure the business and consumer portal to provide information and support for your customers.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up self-service, Configure, Customer Service Management]
---

# Configure Business and Consumer Portal

Configure the business and consumer portal to provide information and support for your customers.

## Before you begin

Role required: sp\_admin

## About this task

The Business and Consumer Portals are self-service web portals based on the ServiceNow Service Portal application.

The Business Portal supports your business-to-business \(B2B\) customers and the Consumer Portal supports your business-to-consumer \(B2C\) customers.

Configure Business and Consumer Portal 

Use the portals to provide information and support for your customers. The portals provides ready to use features that require minimal setup. These include:

-   Header and footer with links for different customer activities.
-   Home page provides a summary of essential items to the logged-in user.
-   Hierarchical menu to systematically navigate to different portal pages.
-   Unified browse experience for knowledge and catalog through taxonomy topics.
-   List pages to browse, search, and filter through records of cases, products, orders, and others.
-   Record view pages to view key information, related actions, related lists, and quick links of a record.

You can add additional self-service capabilities such as order management by installing the respective plugin.

**Note:**

-   The Business Portal Store app is automatically installed when you install the Customer Service Portal store app \(from version 24.0.0 and above\).
-   The Consumer Portal Store app is automatically installed when you install the Consumer Service Portal store app \(from version 24.0.0 and above\).

For details, see [Activate the Consumer and Customer Service Portals](activate-consumer-portal.md).

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Portals**.

2.  On the Service Portals page, in the Title column, enter `*business portal` or `*consumer portal`.

3.  Select **Business Portal** or **Consumer Portal**.

    A page opens in your instance where you can configure the Business or Consumer Portal.

4.  Clear **Inactive** check box.

    **Note:** The Business Portal and Consumer Portal is inactive by default.

5.  Select **Update**.

    You can access the Business Portal using the URL, &lt;servicenow instance URL&gt;/business\_portal and Consumer Portal using the URL, &lt;servicenow instance URL&gt;/consumer\_portal.


**Related topics**  


[bundle-platux.c_ServicePortal]

