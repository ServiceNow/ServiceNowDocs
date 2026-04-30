---
title: Create a catalog request from another flow
description: You can create a catalog request to join the Service Catalog flow from a different flow. For example, from an incident flow, you can create a request, and associate the request with the incident. It helps you in tracking the requests associated with an incident and vice versa.
locale: en-US
release: zurich
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Service Catalog request fulfillment, Service Catalog configuration, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a catalog request from another flow

You can create a catalog request to join the Service Catalog flow from a different flow. For example, from an incident flow, you can create a request, and associate the request with the incident. It helps you in tracking the requests associated with an incident and vice versa.

## Before you begin

Role required: itil

-   To associate a request with any parent table record, the corresponding mapping configuration should be available in the **Catalog Administration** &gt; **Request Parent Mapping** submodule.
-   To associate a record producer request with the parent table record, retrieve the **sysparm\_parent\_sys\_id** and **sysparm\_parent\_table** parameters from the URL using the RP.getParameterValue\(\) method in the **Script** field of the record producer.

**Note:** If you set the **Use the sc\_layout driven cart macros \(default true\)** \(**glide.sc.use\_cart\_layouts**\) property to **false** and create a request from a parent table record, the request is not associated with the parent table record.

## Procedure

1.  Navigate to the required table and select a parent record.

2.  Click the additional actions menu icon ![Additional actions menu icon.](../image/AdditinalActions.png) and select **Create Request**.

    The Catalogs home page is displayed with all active catalogs that you can access.

    **Note:** If there is only one active catalog, then that catalog page is displayed with available categories.

3.  Select the required catalog and navigate through its categories and items.

4.  Check out the required catalog item, order guide, or record producer.

    For information on checkout models, see [.](../concept/c_EnableATwoStepCheckout.md#)

    For a catalog item or order guide, a request is created and displayed under the **Requests** tab of the parent table record. For a record producer, the corresponding task is created and displayed under the **Problems** tab of the parent table record, for example, an incident.

    **Note:**

    -   The associated incident is specified in the annotation message throughout the request process.
    -   Both for the one-step and two-step checkout, the caller of the incident is automatically set as the **Requested For** user for the request. If the two-step checkout is enabled, the fulfiller can change the **Requested For**.

        **Note:** For delegated request experience, the caller of the incident is populated in the Requested For variable. For information on delegated request experience, see [Delegated request experience](../concept/delegated-request-exp.md).

    -   You cannot add items to the wish list, or save a record producer in this flow.

**Parent Topic:**[Service Catalog request fulfillment](../concept/request-fulfillment.md)

