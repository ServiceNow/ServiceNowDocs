---
title: Modeling a 5G xNF in Telecommunications Network Inventory
description: You can model your 5G network and manage all your xNFs \(any type of network functions\) by using the Telecommunications Network Inventory application. By using the model, you can create, review, update, and delete your networks.Created topic as per STRY55389656 - DOC1072742
locale: en-US
release: xanadu
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Exploring Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# Modeling a 5G xNF in Telecommunications Network Inventory

You can model your 5G network and manage all your xNFs \(any type of network functions\) by using the Telecommunications Network Inventory application. By using the model, you can create, review, update, and delete your networks.

## 5G network model

You must create a business application, an application service, and network interfaces to model your 5G network as show in the following diagram.

![5G network model that shows the business application, the application service, and network interfaces.](../image/MMASSET0020496-5g-network-model.png)

-   Business Application: The business application table stores all xNFs. The business application records the labels of all classes proposed by 3GPPTM\* as a type of managed network function. To learn more, see [Create an xNF](../task/create_business_applications.md).
-   Application Service: The application service stores the instance of the corresponding network function, which is associated with the business applications to indicate its type, such as DU or CU-CP and so on. Each instance of a function has a record in the application service. You can create a relationship with a business application and network interface. To learn more, see [Create or add an xNF instance](../task/create_application_services.md).
-   Network Interface: The network interface stores all the logical IP interfaces that are assigned to the managed network. The logical interfaces represent a peer-to-peer relationship. If there’s a connection between a distributed unit \(DU\) and centralized unit \(CU\) control plane or user plane \(UP\) functions, a logical connection is created between the logical interfaces. By using the relationship editor, you can create a relationship with an application service. To learn more, see [Define the network interface details](../task/define-tni-interfaces.md) and [CI relationship editor](https://servicenow.com/docs/bundle/utah-servicenow-platform/page/product/configuration-management/concept/c_RelationshipEditor.html) to create or edit a relationship.

\*The 3GPPTM TS28.541 V18.2.2 inspired attributes are provided as the pack tables. To learn more, see [Pack tables](../reference/pack_tables.md). To learn more about attribute packs, see [Attribute packs](telecommunication-network-inventory-pack.md).

\*3GPP is a trademark of ETSI.

**Related topics**  


[Create xNF and xNF instances](services.md)

