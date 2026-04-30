---
title: Components installed with Contractor Service Center
description: Several types of components are installed with activation of the Contractor Service Center plugin, including tables, user roles, and scheduled jobs. The application also installs related store applications if they aren't already installed.
locale: en-US
release: zurich
product: Contractor Service Center
classification: contractor-service-center
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Contractor Service Center, Health and Safety, Employee Service Management]
---

# Components installed with Contractor Service Center

Several types of components are installed with activation of the Contractor Service Center plugin, including tables, user roles, and scheduled jobs. The application also installs related store applications if they aren't already installed.

## Store applications installed

<table id="table_klx_qvr_yfc"><thead><tr><th>

Store Application

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Health and Safety Contractor Management

 \[sn\_hs\_crm\]

</td><td>

Installs contractor pre-qualification capabilities enabling contractors to prequalify contractor companies and their workers and monitor them in the Health and Safety application.

 For more information on components installed with Health and Safety Contractor Management, see [Components installed with Health and Safety Contractor Management](../../hs-contractor-management/reference/components-installed-with-hs-contractor-mgmt.md).

</td></tr><tr><td>

Health and Safety Core

</td><td>

Installs core data model for Health and Safety. This data model includes common components such as Health and Safety user profile and actions that are used in the Health and Safety applications.

 For more information on store applications, roles, and tables installed with Health and Safety Core, see [Components installed with Health and Safety Core](../../hs-core/reference/components-installed-hs-core.md).

</td></tr><tr><td>

Workplace Core \[sn\_wsd\_core\]

</td><td>

Enables workplace locations for Health and Safety applications.**Important:** The application installation doesn’t install the location demo data for the Workplace Core location model. As a workaround, repair the Workplace Core plugin with the **Load demo data** option.

</td></tr></tbody>
</table>## Roles installed

<table id="table_ilx_qvr_yfc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Contractor

 \[sn\_hs\_csc.contractor\]

</td><td>

Can access self-service capabilities in the Contractor service center to raise safety requests, permits, complete tasks, and upload documents.

</td><td>

-   sn\_ohs\_im.observation\_reporter
-   sn\_hs\_rm.safety\_register\_reader
-   snc\_external
-   sn\_wsd\_core.workplace\_user
-   sn\_ohs\_im.incident\_reporter
-   sn\_hs\_rm.permit\_requestor
-   sn\_hs\_rm.jsa\_reporter

</td></tr></tbody>
</table>## Tables installed

<table id="table_mlx_qvr_yfc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Contractor service portal menu

 \[sn\_hs\_csc\_menu\]

</td><td>

Used to configure the menu for the service center portal.

</td></tr><tr><td>

Contractor service portal menu item

 \[sn\_hs\_csc\_menu\_item\]

</td><td>

Used to configure the menu items for the service center portal.

</td></tr></tbody>
</table>**Parent Topic:**[Contractor Service Center reference](../concept/hs-contractor-service-center-reference.md)

