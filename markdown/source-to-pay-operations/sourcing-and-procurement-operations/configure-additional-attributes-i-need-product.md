---
title: Configure additional attributes for I need a product or service
description: You can configure additional attributes on the intake for variable sets configured on the I need a product and I need a service record producers. Any new fields that are added to the variable set must be mapped in the record producer script to ensure that the information is saved in the backend.
locale: en-US
release: yokohama
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Request for products or services that you don't see on ShoppingHub, Using Shopping Hub, Using Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Configure additional attributes for I need a product or service

You can configure additional attributes on the intake for variable sets configured on the **I need a product** and **I need a service** record producers. Any new fields that are added to the variable set must be mapped in the record producer script to ensure that the information is saved in the backend.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to the **I need a product** or **I need a service** record producer, as required.

2.  Go to the script section of the record producer and ensure that the intake details fields are mapped to the payload appropriately.

    **Note:** If any of the fields aren’t mapped, then mapping logic must be added.

3.  Go to the script include: NonCataloglntakeService, function: createSourcingRequest.

    This function creates and appends the information passed from the record producer to the sourcing request record. Ensure that the sourcing request has the appropriate field in its table.

4.  To save the information on the purchase request line, go to the script include: NonCataloglntakeService.

    This creates an import set record in the non-catalog import set table, sn\_shop\_non\_catalog\_intake.

5.  Go to the Table Transform Map: Non catalog intake, and check if the field mapping between the source and target is correct.


**Parent Topic:**[Requesting for products or services that you don't see on ShoppingHub](../concept/request-prod-serv-dont-see-sh.md)

