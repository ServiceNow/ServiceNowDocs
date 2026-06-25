---
title: Create up to ten copies of Service Catalog request
description: Clone a request to create up to ten copies \(clones\) of the same Service Catalog request, for different users, without having to enter the same information multiple times. For example, you can request a new piece of equipment for several specified people, generating multiple individual requests quickly from a single initial request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-catalog/t\_EnablingBulkRequests.html
release: australia
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service Catalog customization, Types of catalog items, Explore, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create up to ten copies of Service Catalog request

Clone a request to create up to ten copies \(clones\) of the same Service Catalog request, for different users, without having to enter the same information multiple times. For example, you can request a new piece of equipment for several specified people, generating multiple individual requests quickly from a single initial request.

## Before you begin

Role required: admin or catalog\_admin

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **Maintain Cart Layouts**

2.  Under the **Target type: Browser Screen** section, select **Order Status Screen**.

3.  In the **Components** tab, select the **Clone Checkout** check box.

4.  Navigate to **Service Catalog** &gt; **Catalog Administration** &gt; **Properties**.

5.  In the **Cart** category, perform the following:

    -   Enable the **Enable cloning requests during checkout** property.
    -   For the **List of roles \(comma-separated\) that can use bulk ordering functionality** property, enter the roles for which you want to enable bulk request capability for all users with these roles, or leave the field blank to enable the capability for all users.
6.  Click **Save**.


**Parent Topic:**[Service Catalog customization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/p_ServiceCatalogCustomization.md)

**Related topics**  


[Clone a request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/t_UsingBulkRequests.md)

[Request a catalog item from Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/request-cat-item-portal.md)

[Request an order guide from Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/request-order-guide-portal.md)

[Delegated request experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/delegated-request-exp.md)

