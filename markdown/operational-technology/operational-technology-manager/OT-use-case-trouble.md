---
title: Operational Technology FAQ
description: You might have questions while implementing the CSDM framework.
locale: en-US
release: xanadu
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Applying CSDM guidelines to Operational Technology, Configure, Operational Technology Manager, Operational Technology]
---

# Operational Technology FAQ

You might have questions while implementing the CSDM framework.

-   **What is the difference between a production process and an equipment model entity?**

    Equipment model entities are the service records used to describe how an industrial operation is organized to produce an output or product. The production process describes the relationships between equipment model entities as material flows from raw input to a finished product.

-   **What is a site?**

    A site is a parent equipment model entity record that itself has no parent. A site is a special equipment model entity record because it is used to assign read or write level access to the OT devices assigned to the site.

-   **Why does an OT device have both a site assignment and automates::automated by relationships?**

    The site assignment is needed for role-based security \(RBAC\) of the OT devices. This is implemented as a choice list reference field on the OT Device Details \(cmdb\_ot\_entity\) table portion of the OT device record because an OT device can belong to one site only.

    The **automates::automated by** relationship describes how the OT device is related to the production process, which could include more than one equipment model entity.

-   **What is the difference between a Windows server found on an OT network and one found on an IT network?**

    In both types of network, the Windows server is represented in the cmdb\_ci\_win\_server server. Additionally, the Windows server in the OT network has a reference in the cmdb\_ci\_win\_server.cmdb\_ot\_entity field pointing to a record in the cmdb\_ot\_entity table that describes its function in OT and other OT characteristics like Purdue Level, site, and so on.


**Parent Topic:**[Applying CSDM guidelines to Operational Technology](ot-use-case-product-view.md)

