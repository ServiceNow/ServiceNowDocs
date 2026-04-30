---
title: Configure catalog items for a service definition
description: After creating a service definition, you can associate one or more catalog items with the definition.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring service definitions, Service definitions, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Configure catalog items for a service definition

After creating a service definition, you can associate one or more catalog items with the definition.

## Before you begin

Role required: sn\_csm\_case\_types.service\_definition\_manager, sn\_csm\_case\_types.service\_definition\_admin, or admin

## About this task

A catalog item is a product or service that is available within a service catalog. A record producer is a specific type of catalog item that enables users to create task-based records.

From the Customer and Consumer Portals, end users can select available services from the [Services portal widget](../concept/csm-service-definitions.md#section_krm_zkv_cwb). Selecting a service displays the record producer associated with the service definition. Submitting the record producer creates a case of the correct case type.

A variable set for service definitions is available with the Customer Service Case Types plugin \(com.snc.csm\_case\_types\). This variable set populates the service definition based on the product and/or service selected on the record producer.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Service Definitions**.

2.  Select a service definition.

3.  In the Catalog Service Relationships related list, select **New**.

    The system displays a new Catalog Service Relationship record. The **Service definition** field is auto-filled with the name of the selected service definition.

4.  Select a catalog item in the **Catalog Item** field.

5.  Select **Submit**.

    The catalog item is added to the to the Catalog Service Relationships related list.


**Related topics**  


[Service Catalog items](https://www.servicenow.com/docs/access?context=c_IntroductionToCatalogItems&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)

[Create or edit a catalog item](https://www.servicenow.com/docs/access?context=t_DefineACatalogItem&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)

