---
title: Revision, operationalization, and decommission of a Configuration Item
description: Revision of Configuration Item \(CI\) enables you to update the network attributes of a Configuration Item, such as attributes, connection elements, and relations using the Telecommunications Network Inventory application. You can make a safe and efficient update to your network infrastructure by using the CI revision.
locale: en-US
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Explore, Telecommunications Network Inventory]
---

# Revision, operationalization, and decommission of a Configuration Item

Revision of Configuration Item \(CI\) enables you to update the network attributes of a Configuration Item, such as attributes, connection elements, and relations using the Telecommunications Network Inventory application. You can make a safe and efficient update to your network infrastructure by using the CI revision.

## CI revision overview

CI revisions enable you to modify network-configured attributes and connection elements of an operational Configuration Item. The CI revision is applicable only to logical connection and physical connection CIs. So, you can update all configuration items of a connection, as required with the help of revise CI and its subflows.

CI revisions enable you to modify network-configured attributes and connection elements of an operational Configuration Item. The CI revision is applicable only to logical connection and physical connection CIs. So, after a logical connection or a physical connection configuration Item is created, you can update it as required with the help of revise CI and its subflows.

## Operationalization and decommission flow

![image.agent-workflow]

The following process guides you through the flow for a Configuration Item \(CI\) record after a request is created.

1.  Initiate Revision Request: Once you create a revision request, the selected CI is automatically cloned. This cloned CI includes all its related tables such as, attributes, connection elements, and relations.
2.  Customize Cloning Process: You can customize the cloning process and specify which related tables are included. To learn more, see [../task/clone-and-revise-a-ci.md](../task/clone-and-revise-a-ci.md).
3.  Modify cloned CI: After successful cloning, you can perform changes on the cloned Configuration Item record, as required.
4.  Finalize and apply changes: Using operationalization process merge and finalize the changes. This process integrates the revisions into the original CI record. To learn more, see [Revise a configuration item using design and assign](revise-a-configuration-item.md).
5.  Decommission: After operationalization, the cloned CI record is automatically decommissioned, ensuring an efficient workflow. To learn more, see [Decommission an inventory record](../task/decommision-an-inventory-record.md).

.

## Use case

Let's say, for a logical connection having two ENETs, you want to add another ENET to increase the LAG capacity. So, in this scenario, for a safe LAG update, use the CI revision.

With the help of revise CI, the LAG and all of its connections are cloned. Then, in the cloned LAG Configuration Item, add the desired ENET member and merge it back into the original CI with the help of operationalize CI. After successful operationalization, all three ENETs are added to the original CI without disrupting the network. To learn more, see [Revise a configuration item using design and assign](revise-a-configuration-item.md), [Operationalize a configuration item](../task/operationalize-a-configuration-item.md). Here, the cloned CI is decommissioned automatically. To learn more, see [Decommission an inventory record](../task/decommision-an-inventory-record.md).

Let's say, you must update the IP address of a router in your network. This router is part of a complex network, and you aren’t sure how changing the IP address affects the rest of the network. So, in this scenario, for a safe update of the router's IP address, use the CI revision.

With the help of revise CI, you firstly, duplicate the router CI and all of its related data. Then, you change the IP address of the duplicated router and merge it back into the original CI with the help of operationalize CI. As a result, the changes are applied to the original router without disrupting the network. To learn more, see [Revise a configuration item using design and assign](revise-a-configuration-item.md) and [Operationalize a configuration item](../task/operationalize-a-configuration-item.md).

