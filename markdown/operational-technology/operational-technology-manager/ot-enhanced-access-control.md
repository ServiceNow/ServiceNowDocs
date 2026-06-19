---
title: Enhanced Access Control for Operational Technology
description: Enhanced Access Control for Operational Technology \(Operational Technology\) implements data filters, deny unless access control rules \(ACLs\), and ACL query rules to help promote system security.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/operational-technology-manager/ot-enhanced-access-control.html
release: australia
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Explore, Operational Technology Manager, Operational Technology]
---

# Enhanced Access Control for Operational Technology

Enhanced Access Control for Operational Technology \(Operational Technology\) implements data filters, deny unless access control rules \(ACLs\), and ACL query rules to help promote system security.

## Enhanced Access Control overview

Enhanced Access Control provides the following components to provide access control configurations for your data to help avoid misconfiguration and security issues.

-   **Data filers**

    Ability to control access at the query level.

-   **Deny Unless ACLs**

    Ability to deny access to data unless the specific conditions are met.

-   **ACL Query Rules**

    Exact query and range query ACL operations to control query privileges.


## Enhanced Access Control for OT

Deny Unless ACLs help enforce IT and OT separation and site-based access.

**IT and OT separation**

Non-OT users can't view OT devices in Configuration Management Database \(CMDB\) tables. If a device is classified as an OT CI, only users assigned the **cmdb\_ot\_viewer** role or the **cmdb\_ot\_editor** role can access it. The following table describes each role.

<table id="table_lgz_3w2_fgc"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

OT Viewer \[cmdb\_ot\_viewer\]

</td><td>

Read-only access to OT device records.

</td></tr><tr><td>

OT Editor \[cmdb\_ot\_editor\]

</td><td>

Create, read, update, and delete access for Operation Technology \(OT\) extension classes.**Note:** Users assigned the **cmdb\_ot\_editor** role can edit and delete only OT configuration items \(CIs\), and can't edit IT CIs.

</td></tr></tbody>
</table>There are also restrictions on OT users who can edit or delete IT configuration items \(CIs\). Users assigned the **cmdb\_ot\_editor** role or the **cmdb\_ot\_admin** role can’t edit or delete IT CIs in the following related lists:

-   IP Address
-   Network Adapter
-   Storage Device
-   File System
-   Memory Module
-   Patch = CI Field
-   Package = CI Field
-   Managed Network

**Site-based access**

Site-based access specifies which users can view, edit, and delete OT devices for a designated site. You can assign site-based access to users by using Can Read or Can Edit user criteria. For more information about assigned Can Read access, see [Assign the user criteria for Can Read access to a site](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/industrial-process-manager/assign-user-criteria-for-can-read-access.md). For more information about assigning Can Edit access, see [Assign the user criteria for Can Edit access to a site](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/industrial-process-manager/assign-user-criteria-for-can-edit-access.md).

The following table describes the site-based access for users assigned the **cmdb\_ot\_viewer** role or the **cmdb\_ot\_editor** role.

<table id="table_td2_jy2_fgc"><thead><tr><th>

Role

</th><th>

Site-based permission

</th></tr></thead><tbody><tr><td>

cmdb\_ot\_viewer

</td><td>

With Can Read access, users assigned the **cmdb\_ot\_viewer** role can only view OT devices for a designated site.For example, if you're assigned the **cmdb\_ot\_viewer** role and have Can Read access to the Atlanta site, then you can only view the site's OT devices. You can't edit or delete the OT devices associated with Atlanta.

</td></tr><tr><td>

cmdb\_ot\_editor

</td><td>

To edit OT devices, users with the **cmdb\_ot\_editor** role should be assigned Can Edit access for the site, or sites they belong to.For example, if you're assigned the **cmdb\_ot\_editor** role but only have Can Read access to the Atlanta site, you can only view the devices associated with Atlanta. If you're assigned the **cmdb\_ot\_editor** role and have Can Edit access to the San Diego site, you can edit or delete the devices associated with San Diego.

</td></tr></tbody>
</table>## Enhanced Access Control for OT CMDB CI related record tables

Non-OT users can't view OT devices in the following related record OT-related CMDB CI related record tables:

-   IP Address \[cmdb\_ci\_ip\_address\]
-   Network Adapter \[cmdb\_ci\_network\_adapter\]
-   Serial Number \[cmdb\_serial\_number\]

If a related record is an OT device, only users assigned the **cmdb\_ot\_viewer** role or the **cmdb\_ot\_editor** can view or edit the OT device respectively.

Related records also adhere to site-based access restrictions. With Can Read access, users assigned the **cmdb\_ot\_viewer** role can only view the OT-related CMDB CI records for a designated site. Users with the **cmdb\_ot\_editor** role must be assigned Can Edit access for a site to edit or delete the OT-related CMDB CI records of the designated site.

**Parent Topic:**[Exploring the Operational Technology Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/operational-technology-manager/exploring-operational-technology-manager.md)

