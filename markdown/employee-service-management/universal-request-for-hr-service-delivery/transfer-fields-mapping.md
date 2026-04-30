---
title: Map UR fields with target table fields
description: Define the fields that you want to map between the universal request and the target table fields that you already configured. This configuration enables you to copy the values of mapped fields from the universal request to the new ticket, and vice versa.
locale: en-US
release: xanadu
product: Universal Request for HR Service Delivery
classification: universal-request-for-hr-service-delivery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure mappings, Configure service to use Universal Request, Setting up and configuring Universal Request, Universal Request, Employee Service Management]
---

# Map UR fields with target table fields

Define the fields that you want to map between the universal request and the target table fields that you already configured. This configuration enables you to copy the values of mapped fields from the universal request to the new ticket, and vice versa.

## Before you begin

Role required: ur\_admin

To map automatically the fields, select **Map fields automatically** related link. This action maps all fields that are common between UR and the service ticket and vice versa.

**Note:** Field mappings will take precedence over transfer template configuration, if you’ve already defined them.

## Procedure

1.  Navigate to **All** &gt; **Universal Request** &gt; **Administration** &gt; **Mapping Configuration**.

2.  Open the configuration for which you want to map the fields.

<table id="choicetable_mmq_lyn_mtb"><thead><tr><th align="left" id="d145844e83">

Mapping type

</th><th align="left" id="d145844e86">

Description and action

</th></tr></thead><tbody><tr><td id="d145844e92">

**Direct transfer mappings**

</td><td>

Map the fields to create service level tickets when a ticket is transferred from one department to another.On the **Transfer Mappings** tab,

1.  Select **New**.
2.  Select the **Source field** of the universal request.
3.  Select the **Target field** that you want to map with the service ticket.
4.  Select **Submit**.


</td></tr><tr><td id="d145844e133">

**Associated ticket mappings**

</td><td>

Map the fields to create an associated ticket for universal request.On the **Associated ticket Mappings** tab,

1.  Select **New**.
2.  Select the **Source field** of the universal request.
3.  Select the **Target field** that you want to map with the service ticket.
4.  Select **Submit**.


</td></tr><tr><td id="d145844e174">

**Create UR mappings**

</td><td>

Map the fields to create automatically a universal request when a request is raised from any of the available channels.

**Note:** Before you perform this step, ensure that you’ve created a new Before insert business rule to call the respective API. For more information, see [Create a business rule to automatically create universal request](ur-create-brule-omnichannel.md).

 On the **Create UR Mappings** tab,

1.  Select **New**.
2.  Select the **Source field** of the service table.
3.  Select the **Target field** that you want to map with the universal request.
4.  Select **Submit**.


</td></tr></tbody>
</table>    **Note:** The **Type** field indicates the type field mapping selected, such as Transfer, Associated Ticket, or Create UR.

3.  Select **Update**.


**Parent Topic:**[Configure mappings](ur-transfer-map-config.md)

