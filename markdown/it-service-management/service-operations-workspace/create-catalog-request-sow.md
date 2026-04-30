---
title: Create a catalog request in Service Operations Workspace
description: Create a catalog request in Service Operations Workspace to initiate a catalog request flow from a different IT Service Management flow. For example, from an incident flow, you can create a request and associate the request with the incident to help track requests associated with an incident and vice versa.
locale: en-US
release: zurich
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Request Management in Service Operations Workspace, Operate, Service Operations Workspace for ITSM, IT Service Management]
---

# Create a catalog request in Service Operations Workspace

Create a catalog request in Service Operations Workspace to initiate a catalog request flow from a different IT Service Management flow. For example, from an incident flow, you can create a request and associate the request with the incident to help track requests associated with an incident and vice versa.

## Before you begin

Role required: itil or sn\_request\_write

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  Initiate a catalog request from an incident or from an interaction record.

<table id="choicetable_khj_fll_zdb"><thead><tr><th align="left" id="d345045e74">

Option

</th><th align="left" id="d345045e77">

Steps

</th></tr></thead><tbody><tr><td id="d345045e83">

**From an incident using the Create request UI action**

</td><td>

1.  Navigate to **Lists &gt; Incidents &gt; All**.
2.  Open the incident for which you want to create a request.
3.  Select **Create request** from the drop-down menu next to **Create change request**.
4.  On the Service Catalog categories page, navigate to the catalog item, order guide, or record producer that you want to order.

**Note:** You can order items only from catalogs that you have access rights to.

</td></tr><tr><td id="d345045e121">

**From an incident using Agent Assist**

</td><td>

1.  Navigate to **Lists &gt; Incidents &gt; All**.
2.  Open the incident for which you want to create a request.
3.  Select **Agent Assist** in the contextual sidebar.
4.  Search for the catalog item, order guide, or record producer that you want to request.


</td></tr><tr><td id="d345045e154">

**From an interaction record**

</td><td>

1.  Select **Add** &gt; **New Interaction**.
2.  Enter the interaction details and select **Save**.
3.  Select **Create request** from the drop-down menu next to **Create incident**.
4.  On the Service Catalog categories page, navigate to the catalog item or order guide that you want to order.

**Note:** You can order items only from the catalogs that you have access rights to.

</td></tr></tbody>
</table>3.  Select **Order Now**.

    The value in the **Request for** field is set by default depending on where the request is created:

    -   If the request is created from an incident, the value is set to the person who called in the incident.
    -   If the request was started from an interaction, the value is set to the person with whom the interaction is happening.
4.  On the Order Confirmation page, specify the shipping address in the **Delivery Information** field.

5.  On the Order Confirmation page, provide any additional information in the **Special Instructions** field.

6.  Select **Checkout**.

    The request is created and associated with the parent incident.

7.  Select **Close**.

8.  View the created request by selecting **View Details**.


**Parent Topic:**[Request Management in Service Operations Workspace](../concept/request-sow.md)

