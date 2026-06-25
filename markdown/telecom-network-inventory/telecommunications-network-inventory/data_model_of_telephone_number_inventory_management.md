---
title: Telephone number inventory management data model
description: Created topic as per STRY54971605 - DOC1067550By using the telephone number inventory management data model, you can understand how the tables of a telephone block, telephone number allocation, and telephone number relate to each other.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/data\_model\_of\_telephone\_number\_inventory\_management.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Telecommunications Network Inventory]
---

# Telephone number inventory management data model

By using the telephone number inventory management data model, you can understand how the tables of a telephone block, telephone number allocation, and telephone number relate to each other.

## Data model

The following diagram shows the telephone number inventory management data model.\[Omitted image "telephone\_datamodel.png"\] Alt text: Data model that explains how the tables of a telephone number block, telephone number allocation, and telephone number are related.

The data model provides an overview of telephone number usage and availability. With this data model, you can store the telephone block, allocation, and telephone number.

**Note:** You can also allocate or deallocate a telephone number for a customer service. You must create a telephone block for the telephone number block table.

A telephone number is assigned this way:

1.  A telephone number inventory manager creates a telephone number block to store all the different types of telephone numbers. The numbers can be categorized based on the area, country, port-in type, or port-out type. Each record of the block is stored in the table of the telephone number block.
2.  A telephone number inventory manager then creates a telephone allocation to assign a service to a series or to a set of numbers. A telephone block can have a group as its child. These allocations are created in the telephone number allocation table.
3.  The telephone number allocation table relates the telephone numbers that are ready to use to a record in the telephone number table.

**Parent Topic:**[Telecommunications Network Inventory reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/telecommunications-network-inventory-reference.md)

**Related topics**  


[Create a telephone infrastructure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/telephone_block_telephone_number_and_telephone_number.md)

