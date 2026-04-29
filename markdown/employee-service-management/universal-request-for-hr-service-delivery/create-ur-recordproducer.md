---
title: Configure a catalog item or record producer to create a universal request
description: Create a universal request along with a requested item or task-based record to provide unified ticketing experience.
locale: en-US
release: australia
product: Universal Request for HR Service Delivery
classification: universal-request-for-hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Unified ticket experience setting, Configure service to use Universal Request, Setting up and configuring Universal Request, Universal Request, Employee Service Management]
---

# Configure a catalog item or record producer to create a universal request

Create a universal request along with a requested item or task-based record to provide unified ticketing experience.

## Before you begin

Role required: admin

## About this task

Only when the Universal Request plugin \(com.snc.universal\_request\) is activated, the **Universal Request Config** section is added to a catalog item or record producer form.

A universal request is not created for the following scenarios:

-   Cart with multiple catalog items is checked out
-   Order guide is submitted

For information on creating a catalog item, see [Create or edit a catalog item](https://www.servicenow.com/docs/access?context=t_DefineACatalogItem&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

For information on creating a record producer, see [Create a record producer](https://www.servicenow.com/docs/access?context=t_DefRecProdInSCat&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **Maintain Items**.

2.  Select the required catalog item or record producer.

3.  In the Catalog Item or Record Producer form, configure these fields in the **Universal Request Config** section.

<table id="table_lz2_ydm_jpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

UR certified/enabled item

</td><td>

Option to specify that a universal request should also be created along with a requested item or task-based record. In the universal request, a reference is created to the associated requested item or task-based record, which becomes the primary task of the universal request.

</td></tr><tr><td>

Requires Additional Review

</td><td>

Option to automatically select the **Needs resolution review** check box on the corresponding universal request. For information about the universal request fields, see [Universal Request form](../../universal-request/reference/new-ur-record-form.md).The **Requires Additional Review** field appears only when the **UR certified/enabled item** check box is selected.

</td></tr></tbody>
</table>4.  Click **Update**.


**Parent Topic:**[Unified ticket experience setting](../../universal-request/concept/unified-ticket-experience.md)

**Related topics**  


[Create universal request automatically for department tickets via other channels](../../universal-request/task/autocreate-ur-from-interactionrecord-WS.md)

[Email notification preferences for your service](../../universal-request/concept/ur-customize-email-notifcations.md)

[Automatically create universal request from an inbound email](../../universal-request/concept/create-ur-from-inbound-email.md)

[Service Catalog configuration for Universal Request](https://www.servicenow.com/docs/access?context=ur-catalog-config&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

