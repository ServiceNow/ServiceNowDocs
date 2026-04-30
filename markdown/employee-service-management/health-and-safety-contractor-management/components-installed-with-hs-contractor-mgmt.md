---
title: Components installed with Health and Safety Contractor Management
description: Several types of components are installed with installation of the Health and Safety Contractor Management application, including tables, user roles, and scheduled jobs. The application also installs related store applications if they aren’t already installed.
locale: en-US
release: xanadu
product: Health and Safety Contractor Management
classification: health-and-safety-contractor-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, Health and Safety Contractor Management, Health and Safety, Employee Service Management]
---

# Components installed with Health and Safety Contractor Management

Several types of components are installed with installation of the Health and Safety Contractor Management application, including tables, user roles, and scheduled jobs. The application also installs related store applications if they aren’t already installed.

## Store applications installed

<table id="table_ulz_4tw_llba"><thead><tr><th>

Store application

</th><th>

Description

</th></tr></thead><tbody><tr><td>

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

<table id="table_vcd_4y1_zcc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Safety contractor coordinator

 \[sn\_hs\_crm.contractor\_coordinator\]

</td><td>

Coordinator for contractor companies and workers who can

-   View contractor companies and their related records in Health and Safety Workspace
-   Add, update, and delete these from Health and Safety Workspace
    -   Contractor companies for health and safety
    -   Contractor workers for health and safety profiles
-   Assign safety related tasks and actions to contractor workers
-   Collect safety related documents from contractor companies and workers
-   Grant site access to contractor workers

</td><td>

-   sn\_ohs\_im.hs\_profile\_writer
-   sn\_ohs\_im.workspace\_user
-   sn\_hs\_crm.reporter
-   sn\_ohs\_im.document\_admin
-   canvas\_user
-   sn\_ohs\_im.action\_writer
-   sn\_ohs\_im.action\_reader

</td></tr><tr><td>

Safety contractor reporter

 \[sn\_hs\_crm.reporter\]

</td><td>

View and create contractor companies for health and safety from Employee Center

</td><td>

-   sn\_ohs\_im.hs\_profile\_reader
-   sn\_hs\_crm.company\_writer
-   sn\_hs\_crm.company\_reader

</td></tr><tr><td>

Safety contractor company writer

 \[sn\_hs\_crm.company\_writer\]

</td><td>

Can write information into the contractor management company table and tables related to it

</td><td>

None

</td></tr><tr><td>

Safety contractor company reader

 \[sn\_hs\_crm.company\_reader\]

</td><td>

Can view information from the contractor management company table and tables related to it

</td><td>

None

</td></tr></tbody>
</table>## Tables installed

<table id="table_zcd_4y1_zcc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Contractor company

 \[sn\_hs\_crm\_company\]

</td><td>

Stores all contractor companies added for Health and Safety.

</td></tr><tr><td>

Site access

 \[sn\_hs\_crm\_location\_access\]

</td><td>

Stores all contractor workers who've been granted site access.

</td></tr><tr><td>

Document

 \[sn\_hs\_crm\_m2m\_company\_document\]

</td><td>

Stores all safety related documents collected from contractor companies and workers.

</td></tr></tbody>
</table>**Parent Topic:**[Health and Safety Contractor Management reference](../concept/hs-contractor-management-reference.md)

