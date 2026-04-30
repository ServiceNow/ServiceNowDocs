---
title: Usage criteria for publisher packs
description: Description of usage criteria that indicates whether a publisher pack is being utilized or not in your instance.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Value builder, Success portal view in Software Asset Workspace, Software Asset Workspace, Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Usage criteria for publisher packs

Description of usage criteria that indicates whether a publisher pack is being utilized or not in your instance.

This table describes the criteria used for the **Usage found** entity for each publisher pack to be identified as fully utilized. The criteria differ for each publisher pack.

<table id="table_h3v_l1c_kvb"><thead><tr><th>

Publisher Pack

</th><th>

Usage criteria

</th><th>

Source tables

</th></tr></thead><tbody><tr><td>

Red Hat Enterprise Linux

</td><td>

Software installations

</td><td>

cmdb\_sam\_sw\_install

</td></tr><tr><td>

Adobe

</td><td>

-   Software installations
-   Subscriptions

</td><td>

-   cmdb\_sam\_sw\_install
-   samp\_sw\_subscription

</td></tr><tr><td>

Citrix

</td><td>

-   Software installations
-   Client access

</td><td>

-   cmdb\_sam\_sw\_install
-   samp\_sw\_client\_access

</td></tr><tr><td>

Microsoft

</td><td>

-   Software installations
-   Subscriptions

</td><td>

-   cmdb\_sam\_sw\_install
-   samp\_sw\_subscription

</td></tr><tr><td>

IBM

</td><td>

Software installations

</td><td>

cmdb\_sam\_sw\_install

</td></tr><tr><td>

Oracle

</td><td>

Software installations

</td><td>

cmdb\_sam\_sw\_install

</td></tr><tr><td>

SAP

</td><td>

-   SAP user
-   Client access

</td><td>

-   samp\_sap\_system\_user
-   samp\_sap\_sw\_client\_access

</td></tr><tr><td>

VMware

</td><td>

Software installations

</td><td>

cmdb\_sam\_sw\_install

</td></tr></tbody>
</table>