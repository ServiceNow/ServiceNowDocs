---
title: Software Asset Management licensing
description: Software Asset Management \(SAM\) licensing is based on five categories of managed IT resources: Server, End User Computing Device, SaaS Subscription User, PaaS Resources, and IaaS Storage. Each category is counted toward your subscription at a different ratio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-asset-management/software-asset-management/managed-it-resource-types.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Subscriptions for Software Asset Management, Software Asset Management, IT Asset Management, Asset Management]
---

# Software Asset Management licensing

Software Asset Management \(SAM\) licensing is based on five categories of managed IT resources: Server, End User Computing Device, SaaS Subscription User, PaaS Resources, and IaaS Storage. Each category is counted toward your subscription at a different ratio.

Each managed IT resource category is represented as a configuration item \(CI\) or table record in Software Asset Management. The subscription ratio differs by category, since the management effort required varies by resource type.

## Managed IT resource categories

<table><thead><tr><th>

Resource type

</th><th>

Description

</th><th>

Ratio

</th><th>

CMDB classes

</th></tr></thead><tbody><tr><td>

Server

</td><td>

Physical or virtual server that is represented as a configuration item \(CI\) in the CMDB tables listed in the following license resource categories and managed by Software Asset Management.

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

 **Note:** Any CMDB classes derived from the above listed classes or cmdb\_ci\_hardware and not defined as another Managed IT Resource type.

</td></tr><tr><td>

End User Computing Device

</td><td>

Physical or virtual non-server CI in the CMDB tables listed in the following license resource categories and managed by Software Asset Management.

</td><td>

1:4

</td><td>

-   cmdb\_ci\_computer
-   cmdb\_ci\_handheld\_computing
-   cmdb\_ci\_pc\_hardware

 Any CMDB classes derived from cmdb\_ci\_pc\_hardware.

</td></tr><tr><td>

SaaS Subscription User

</td><td>

Unique User Principal name in the SaaS Subscription User table listed in the following license resource categories and managed by Software Asset Management.

</td><td>

1:15

</td><td>

samp\_sw\_subscription

</td></tr><tr><td>

PaaS Resources

</td><td>

Cloud-based platform services that are represented as a CI in the CMDB tables listed in the following license resource categories and managed by Software Asset Management.

</td><td>

1:3

</td><td>

-   cmdb\_ci\_database
-   cmdb\_ci\_cloud\_database

 Any child classes of the above listed classes.

</td></tr><tr><td>

IaaS Storage

</td><td>

Cloud-based infrastructure service represented as a CI in a CMDB table listed in the following license resource categories and managed by Software Asset Management.

</td><td>

1:3

</td><td>

cmdb\_ci\_storage\_volumeAny child classes of the above listed classes.

</td></tr></tbody>
</table>**Important:**

Software Asset Management manages servers and end user computing devices only when their installed software on the Managed IT Resources is represented in the Software Installation \[cmdb\_sam\_sw\_install\] table.

**Parent Topic:**[Subscriptions for Software Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/sam-subscription.md)

