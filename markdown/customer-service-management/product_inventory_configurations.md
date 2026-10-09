---
title: Product inventory configurations
description: You can select one or more product inventory records to update their configurations and perform the Modify,Suspend, Resume, and Disconnect operations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/product\_inventory\_configurations.html
release: brazil
topic_type: concept
last_updated: "2026-10-09"
reading_time_minutes: 3
breadcrumb: [Customer Life Cycle Management Workflows, Product data, Set up your environment, Configure, Customer Service Management]
---

# Product inventory configurations

You can select one or more product inventory records to update their configurations and perform the **Modify**,**Suspend**, **Resume**, and **Disconnect** operations.

Create orders or quotes from product inventory records on the CRM Workspace.

|Action|Description|
|------|-----------|
|[Modify product inventory records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/modify_product_inventory_records.md)|Perform the **Modify** operation on a single product inventory record that results in the creation of an order.|
|[Modify product inventory records to create a quote](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/modify_product_inventory_records_to_create_a_quote.md)|Perform the **Modify** operation on a single product inventory record that results in the creation of a quote.|
|[Resume product inventory records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/resume_product_inventory_records.md)|Perform the **Resume** operation on single or multiple product inventory records that result in the creation of resume orders.|
|[Suspend product inventory records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/suspend_product_inventory_records.md)|Perform the **Suspend** operation on single or multiple product inventory records that result in the creation of suspend orders.|
|[Disconnect product inventory records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/disconnect_product_inventory_records.md)|Perform the **Disconnect** operation on single or multiple product inventory records that result in the creation of disconnect orders.|

## Product inventory records on a service organization

When a service organization is the buyer, you can view its product inventory records in a related list on the service organization record. Users with the Admin role see every record in the list, with no access restrictions applied.

Users with the Admin role can also use the **Modify** action on any product inventory record in this related list.

## Access to product inventory records by role

Access to product inventory records, install base items, and entitlements depends on your role and is based on the **Buyer Service Organization** field. The following table describes the access for each role.

|Role|Access|
|----|------|
|Admin|View and manage records across all buying and service organizations, with no access restrictions applied.|
|Buyer Org Manager|View and manage all install base items, product inventory records, and entitlements across the buyer or service organization that you manage, including records that belong to its members.|
|Buyer Org Member|View only the install base items, entitlements, and products that are assigned to you as a primary or secondary member.|

## Modify and disconnect actions on a service organization record

Users with a buyer or seller location role can use the **Modify** and **Disconnect** actions in the product inventory related list on the service organization record. When you select **Modify**, the system creates an order or a quote for the requested modification. When you select **Disconnect**, the system creates an order for the requested disconnect.

