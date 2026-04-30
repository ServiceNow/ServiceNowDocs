---
title: Configure Universal Request for legal services
description: Review the base system configurations for integration of legal requests with universal requests and configure as per your business needs.
locale: en-US
release: xanadu
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Universal Request for Legal Service Delivery, Integration of Legal Service Delivery with ServiceNow applications, Legal Service Delivery, Employee Service Management]
---

# Configure Universal Request for legal services

Review the base system configurations for integration of legal requests with universal requests and configure as per your business needs.

## Before you begin

Ensure that you've the following plugins activated and apps installed:

-   Universal Request plugin \(com.snc.universal\_request\)
-   Legal Request Management version 6.1

You can also install Employee Center to provide employees to submit requests.

Role required: admin

## About this task

Legal Request Management version 6.1 installs the service set, service set assignment group, transfer configuration, and state mappings required for the legal requests to work with the universal requests.

## Procedure

1.  Navigate to **All** &gt; **Universal Request** &gt; **Administration**.

2.  Review and configure the following settings as per your business needs.

<table id="choicetable_bnc_s4k_c5b"><thead><tr><th align="left" id="d514710e105">

Setting

</th><th align="left" id="d514710e108">

Description

</th></tr></thead><tbody><tr><td id="d514710e114">

**Service set**

</td><td>

A service set represents a department in your organization. The service set configured in Universal Request enables you to use the UR capabilities for a department.**Legal** is the base system service set available for the Legal department.

 For more information, see [Create a service set](../../universal-request/task/ur-create-service-set.md).

</td></tr><tr><td id="d514710e144">

**Service for Universal Request**

</td><td>

Register your service name for your service specific table and associate it with a service set \(department\) to use the Universal Request capabilities for a specific service in your organization.For more information, see [Create your service for Universal Request](../../universal-request/task/ur-register-service.md)

</td></tr><tr><td id="d514710e169">

**Mapping configuration**

</td><td>

The mapping configuration enables you to configure a target table from the service set \(department\) and then map fields from the target table and Universal Request table to create and transfer department-level tickets.For more information, see [Configure mappings](../../universal-request/task/ur-transfer-map-config.md).

 You can update the `LegalUniversalRequest` script include to map additional legal request and universal request fields in addition to the default mapped fields.

</td></tr><tr><td id="d514710e194">

**Service set assignment group**

</td><td>

A service set must be assigned an assignment group for automatically routing universal requests to the appropriate agents \(assignment group\) within a certain department \(service set\).**Legal Routing Group** is the base system assignment group assigned to the Legal service set.

 For more information, see [Assign assignment group to your service](../../universal-request/task/assign-group-to-service.md).

</td></tr><tr><td id="d514710e219">

**State mapping**

</td><td>

The state mapping enables you to map the states of the legal request and the universal request so that the changes in the state of the legal request are reflected in the state of the universal request.For example, say the legal request's states— New, Assigned to, and Work in Progress—are mapped to the In Progress state of the universal request. So, when a legal request is in any of these states, the universal request's state shows as In Progress.

 For more information, see [Universal Request state mapping](../../universal-request/task/ur-state-mapping.md).

</td></tr><tr><td id="d514710e241">

**Transfer Configuration**

</td><td>

The transfer configuration helps you to set the mandatory field updates, transfer, and closure information when transferring a legal request to another department or back to the universal request.For more information, see [Transfer configuration](../../universal-request/task/configure-route-state.md).

</td></tr></tbody>
</table>3.  Add users to the **Legal Routing Group** service set assignment group.

    **Legal Routing Group** is the base system assignment group with the required roles added. Users in the assignment group will act as the routing agent, triaging the universal request and creating of legal requests to get support from the Legal department.

4.  Select the **Enable Legal Request creation From Universal Request** option from the **Options** field of an intake form in a practice area.

    For more information, see [Add an intake form to a practice area](associate-categories-practice-area.md).


**Parent Topic:**[Universal Request for Legal Service Delivery](../concept/universal-requests-legal.md)

