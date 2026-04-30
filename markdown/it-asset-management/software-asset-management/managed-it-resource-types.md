---
title: Managed IT Resource types
description: There are five IT Resource categories in ServiceNow Software Asset Management - Server, End User Computing Device, SaaS Subscription User, PaaS Resources, and IaaS Storage.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Subscriptions for Software Asset Management, Software Asset Management, IT Asset Management]
---

# Managed IT Resource types

There are five IT Resource categories in ServiceNow Software Asset Management - Server, End User Computing Device, SaaS Subscription User, PaaS Resources, and IaaS Storage.

-   Server is any physical or virtual server that is represented as a configuration item \(CI\) in the CMDB tables listed in the following license resource categories and managed by the Software Asset Management application.
-   End User Computing Device is any physical or virtual non-server CI in the CMDB tables listed in the following license resource categories and managed by the Software Asset Management application.
-   SaaS Subscription User is any unique User Principal name in the SaaS Subscription User table listed in the following license resource categories and managed by the Software Asset Management application.
-   PaaS Resources are cloud-based platform services that are represented as a CI in the CMDB tables listed in the following license resource categories and managed by the Software Asset Management application.
-   IaaS Storage is any cloud-based infrastructure service represented as a CI in a CMDB table listed in the following license resource categories and managed by the Software Asset Management application.

Servers and End User Computing Devices are managed by the Software Asset Management application when the installed software on the Managed IT Resources is represented in the Software Installation \[cmdb\_sam\_sw\_install\] table.

<table id="table_qfg_twd_4qb"><thead><tr><th>

Resource category

</th><th>

Subscription unit ratio

</th><th>

Model category

</th></tr></thead><tbody><tr><td>

Server

</td><td>

1:1

</td><td>

-   cmdb\_ci\_server
-   cmdb\_ci\_win\_server
-   cmdb\_ci\_linux\_server
-   cmdb\_ci\_aix\_server
-   cmdb\_ci\_esx\_server
-   cmdb\_ci\_solaris\_server
-   cmdb\_ci\_hyper\_v\_server
-   cmdb\_ci\_hpux\_server

 Any CMDB classes derived from the above listed classes or cmdb\_ci\_hardware and not defined as another Managed IT Resource type.

</td></tr><tr><td>

End user computing device

</td><td>

1:4

</td><td>

-   cmdb\_ci\_computer
-   cmdb\_ci\_handheld\_computing
-   cmdb\_ci\_pc\_hardware

 Any CMDB classes derived from cmdb\_ci\_pc\_hardware.

</td></tr><tr><td>

SaaS subscription user

</td><td>

1:15

</td><td>

samp\_sw\_subscription

</td></tr><tr><td>

PaaS resources

</td><td>

1:3

</td><td>

-   cmdb\_ci\_database
-   cmdb\_ci\_cloud\_database

 Any child classes of the above listed classes.

</td></tr><tr><td>

IaaS storage

</td><td>

1:3

</td><td>

cmdb\_ci\_storage\_volumeAny child classes of the above listed classes.

</td></tr></tbody>
</table>**Parent Topic:**[Subscriptions for Software Asset Management](sam-subscription.md)

